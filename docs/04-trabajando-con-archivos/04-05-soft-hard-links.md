# Soft y Hard Links

En sistemas operativos Unix-like como Linux, los **enlaces** (links) son referencias a archivos existentes, que permiten crear accesos directos o duplicaciones dentro del sistema de archivos. Existen dos tipos de enlaces: **enlaces duros (hard links)** y **enlaces simbólicos (soft links)**.

---

## Hard Links

Un **enlace duro** es una referencia directa a los **datos** de un archivo, no al archivo en sí. Tanto el archivo original como el enlace duro comparten el mismo **número de inode** (identificador único del archivo en el sistema de archivos). Los enlaces duros son idénticos en cuanto al contenido del archivo, ya que ambos apuntan al mismo bloque de datos. Si el archivo original se elimina, el enlace duro sigue funcionando, ya que los datos no se eliminan hasta que todos los enlaces que apuntan a ellos sean eliminados.

**Ejemplo de un enlace duro**

```bash
ln archivo_original.txt enlace_duro.txt
```

En este caso, **archivo_original.txt** es el archivo original y **enlace_duro.txt** es el enlace duro creado. Ambos archivos ahora apuntan a los mismos datos en el sistema de archivos.

**Características de los Enlaces Duros:**

- Ambos archivos comparten el mismo número de inode.
- Si se elimina el archivo original, el enlace duro todavía es válido y apunta a los mismos datos.
- No se pueden crear enlaces duros para directorios (excepto para el directorio raíz o mediante permisos de superusuario).

## Soft Links

Un **enlace simbólico** (o soft link) es más parecido a un **acceso directo**. Este tipo de enlace contiene una ruta que apunta al archivo original, pero tiene su propio número de inode y no comparte los mismos datos. Si el archivo original se elimina, el enlace simbólico **rompe** y deja de funcionar, ya que el enlace depende de la existencia del archivo original.

**Ejemplo de un Enlace Simbólico:**

```bash
ln -s archivo_original.txt enlace_simbolico.txt
```

En este caso, **enlace_simbolico.txt** es el enlace simbólico que apunta a **archivo_original.txt**. Si el archivo original es eliminado, el enlace simbólico se quedará "roto", es decir, no podrá acceder al archivo original.

**Características de los Enlaces Simbólicos:**

- El enlace simbólico tiene su propio número de inode.
- Si el archivo original se elimina, el enlace simbólico se "rompe" y no apunta a ningún archivo válido.
- Puede apuntar a directorios, lo que no es posible con los enlaces duros.

## Diferencias entre enlaces duros y simbólicos

| **Característica**                   | **Enlace Duro**                                                                      | **Enlace Simbólico**                                                                                        |
| ------------------------------------ | ------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------- |
| **Número de Inode**                  | Comparte el mismo número de inode.                                                   | Tiene un inode diferente al del archivo original.                                                           |
| **Dependencia del Archivo Original** | El archivo original no necesita existir para que el enlace siga funcionando.         | Depende de que el archivo original exista. Si se elimina el archivo original, el enlace simbólico se rompe. |
| **Permite directorios**              | No permite crear enlaces a directorios (excepto el directorio raíz).                 | Permite crear enlaces a directorios.                                                                        |
| **Uso de espacio en disco**          | No utiliza espacio adicional significativo en el disco.                              | Utiliza espacio adicional para almacenar la ruta al archivo original.                                       |
| **Riesgo de enlaces rotos**          | No hay riesgo de enlaces rotos mientras haya al menos un enlace al archivo original. | El enlace simbólico puede romperse si se elimina el archivo original.                                       |

## Comandos y ejemplos

### Crear un enlace duro

```bash
ln archivo_original.txt enlace_duro.txt
```

Este comando crea un enlace duro llamado **enlace_duro.txt** que apunta a los mismos datos que **archivo_original.txt**.

### Crear un enlace simbólico

```bash
ln -s archivo_original.txt enlace_simbolico.txt
```

Este comando crea un enlace simbólico llamado **enlace_simbolico.txt** que apunta a **archivo_original.txt**. Si **archivo_original.txt** se elimina, **enlace_simbolico.txt** dejará de funcionar.

---

## Conclusión

Los enlaces duros y simbólicos son herramientas poderosas en Linux para gestionar archivos. Los enlaces duros permiten duplicar archivos sin ocupar espacio adicional significativo y garantizan que los datos sigan siendo accesibles incluso si el archivo original se elimina. Los enlaces simbólicos, por otro lado, son útiles para crear accesos directos o referencias a archivos y directorios, pero dependen de la existencia del archivo original.

---

[How to understand the difference between hard and symbolic links in Linux | LabEx](https://labex.io/tutorials/linux-how-to-understand-the-difference-between-hard-and-symbolic-links-in-linux-409929)
