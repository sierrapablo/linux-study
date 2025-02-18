# Copiando y renombrando archivos

En Linux, las operaciones de copiar, mover y renombrar archivos son comunes en la administración de archivos, tanto para usuarios comunes como para administradores del sistema o desarrolladores. Las herramientas principales que usamos para estas operaciones son `cp` para copiar archivos y `mv` para mover o renombrar archivos.

---

## Copiar archivos con `cp`

El comando `cp` se utiliza para copiar archivos o directorios de una ubicación a otra. Los dos principales argumentos de este comando son:

1. **Origen**: La ubicación del archivo o directorio que quieres copiar.
2. **Destino**: La ubicación donde deseas copiar el archivo.

Ejemplo básico:

```bash
cp /ruta/al/archivo/original /ruta/al/archivo/copied
```

**Ejemplo 1**: Para copiar un archivo llamado `documento.txt` de tu directorio actual a otro directorio llamado `/backup`, puedes usar el siguiente comando:

```bash
cp documento.txt /backup/
```

Esto copiará `documento.txt` en el directorio `/backup`.

**Ejemplo 2**: Para copiar un directorio completo, puedes usar el argumento `-r` (recursivo) si deseas copiar subdirectorios y archivos dentro de ellos:

```bash
cp -r /ruta/al/directorio_origen /ruta/al/directorio_destino
```

Este comando copiaría el directorio y su contenido al destino especificado.

## Renombrar y mover archivos con `mv`

El comando `mv` se utiliza tanto para mover archivos de una ubicación a otra como para renombrarlos. Similar al comando `cp`, toma dos argumentos:

1. **Origen**: El archivo o directorio que deseas mover o renombrar.
2. **Destino**: La nueva ubicación o el nuevo nombre del archivo o directorio.

### Renombrar un archivo:

Para cambiar el nombre de un archivo, simplemente usas el comando `mv` con el archivo original como origen y el nuevo nombre como destino:

```bash
mv /ruta/al/archivo/antiguo /ruta/al/archivo/nuevo
```

Ejemplo: Para renombrar `documento.txt` a `documento_nuevo.txt`, usarías:

```bash
mv documento.txt documento_nuevo.txt
```

### Mover un archivo a otro directorio

Si deseas mover el archivo o directorio a otro directorio (sin cambiar su nombre), puedes hacer lo siguiente:

```bash
mv archivo.txt /ruta/al/nuevo/directorio/
```

**Ejemplo**: Para mover `documento.txt` al directorio `/backup`, puedes hacer:

```bash
mv documento.txt /backup/
```

Esto mueve el archivo al directorio de destino.

## Consideraciones importantes

- **Sensibilidad a mayúsculas y minúsculas**: Los comandos en Linux son **sensibles a las mayúsculas y minúsculas**. Esto significa que `documento.txt` y `Documento.txt` son considerados archivos diferentes.

- **Sobrescribir archivos**: Si usas `cp` o `mv` y el archivo de destino ya existe, el archivo se sobrescribirá sin advertencia (a menos que uses la opción `-i` para pedir confirmación antes de sobrescribir).

- **Opción `-i` para confirmación**: Si quieres asegurarte de que no se sobrescriban archivos accidentalmente, puedes usar la opción `-i` (interactivo), que te pedirá confirmación antes de sobrescribir un archivo:

## Resumen de comandos

| **Operación**        | **Comando**                                  | **Descripción**                                        |
| -------------------- | -------------------------------------------- | ------------------------------------------------------ |
| Copiar un archivo    | `cp archivo_origen archivo_destino`          | Copia el archivo o directorio a una nueva ubicación.   |
| Copiar un directorio | `cp -r directorio_origen directorio_destino` | Copia un directorio y su contenido de forma recursiva. |
| Renombrar un archivo | `mv archivo_origen archivo_nuevo`            | Renombra un archivo.                                   |
| Mover un archivo     | `mv archivo_origen directorio_destino`       | Mueve un archivo o directorio a otro directorio.       |

---

## Conclusión

Las herramientas `cp` y `mv` son esenciales para la gestión de archivos en Linux. Dominar estas herramientas es crucial para organizar, mover, copiar y renombrar archivos de manera eficiente en el sistema.

---

[Linux cp Command: File Copying](https://labex.io/tutorials/linux-linux-cp-command-file-copying-209744)

[Linux mv Command Tutorial: Moving and Renaming Files | LabEx](https://labex.io/tutorials/linux-linux-mv-command-file-moving-and-renaming-209743)


