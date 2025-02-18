# Permisos

En los sistemas Linux, los derechos y privilegios se asignan a archivos y directorios mediante permisos. Estos permisos indican quién puede leer, escribir o ejecutar (ejecutar) los archivos. En Linux, existen tres tipos de usuarios: el propietario, el grupo y los demás, cada uno de los cuales puede tener un conjunto diferente de permisos.

Los permisos en el sistema tienen un propósito importante: evitar que los usuarios no privilegiados realicen cambios en el sistema que puedan afectar a otros usuarios. Con permisos inadecuados, los usuarios sin privilegios podrían realizar cambios que resulten ser dañinos o innecesarios para el sistema Linux.

---

## Estructura de permisos

Veamos un ejemplo de los permisos de un archivo:

```
-rwxr--r-- 1 root root 4096 Jan 1 12:00 filename
```

En este ejemplo:

1. **El primer carácter** (`-`) indica el tipo de archivo. Si es un archivo regular, será un guion (`-`), si es un directorio, se mostrará una `d`.

2. **Los siguientes tres caracteres** (`rwx`) indican los permisos del propietario del archivo. En este caso:
   
   - `r` (read): El propietario puede leer el archivo.
   - `w` (write): El propietario puede modificar el archivo.
   - `x` (execute): El propietario puede ejecutar el archivo.

3. **Los siguientes tres caracteres** (`r--`) representan los permisos del grupo:
   
   - `r` (read): Los miembros del grupo pueden leer el archivo.
   - `--` (sin permisos de escritura ni ejecución): El grupo no tiene permisos para modificar ni ejecutar el archivo.

4. **Los últimos tres caracteres** (`r--`) representan los permisos de otros usuarios:
   
   - `r` (read): Otros usuarios pueden leer el archivo.
   - `--` (sin permisos de escritura ni ejecución): Otros usuarios no tienen permisos de modificación ni ejecución.

## Tipos de permisos

- **Lectura (r)**: Permite leer el contenido del archivo o directorio.
- **Escritura (w)**: Permite modificar el contenido de un archivo o agregar/eliminar archivos dentro de un directorio.
- **Ejecución (x)**: Permite ejecutar un archivo como un programa o script. En el caso de los directorios, significa que puedes acceder a su contenido.

## Comandos para modificar permisos

- **chmod**: Cambia los permisos de un archivo o directorio.
  
  Ejemplo de uso:
  
  ```bash
  chmod u+x archivo.txt
  ```
  
  Este comando añade permisos de ejecución (`x`) al propietario del archivo (`u`).
  
  Otro ejemplo:
  
  ```bash
  chmod 755 archivo.txt
  ```
  
  Este comando asigna permisos `rwx` (lectura, escritura y ejecución) al propietario y permisos `rx` (lectura y ejecución) al grupo y otros usuarios.

- **chown**: Cambia el propietario de un archivo o directorio.
  
  Ejemplo de uso:
  
  ```bash
  chown usuario:grupo archivo.txt
  ```
  
  Este comando cambia el propietario y el grupo del archivo a `usuario` y `grupo`.

- **chgrp**: Cambia el grupo de un archivo o directorio.
  
  Ejemplo de uso:
  
  ```bash
  chgrp grupo archivo.txt
  ```
  
  Este comando cambia el grupo asociado al archivo `archivo.txt` a `grupo`.

### Ejemplo práctico

Supongamos que quieres dar permisos completos al propietario, solo lectura y ejecución al grupo, y ninguno a los demás. Usarías el siguiente comando:

```bash
chmod 750 archivo.txt
```

Esto da permisos `rwx` al propietario, `rx` al grupo y ninguno al resto de los usuarios.

### Importancia de los permisos en Linux

Los permisos son fundamentales para la seguridad en Linux, ya que permiten controlar quién puede acceder, modificar y ejecutar archivos. Esto ayuda a prevenir que usuarios no autorizados realicen cambios críticos en el sistema, garantizando que solo las personas adecuadas puedan gestionar archivos importantes o sistemas sensibles.

---

## Conclusión

Entender y gestionar correctamente los permisos en Linux es crucial para la administración de sistemas y la seguridad. Los comandos `chmod`, `chown` y `chgrp` te permiten modificar los permisos de archivos y directorios para asegurar que tu sistema permanezca organizado y seguro.

---

[Linux File Permissions and Ownership Explained with Examples](https://linuxhandbook.com/linux-file-permissions/)

[Managing File Permissions in Linux | LabEx](https://labex.io/tutorials/linux-permissions-of-files-270252)

[Linux File Permissions in 5 Minutes | MUST Know! - YouTube](https://www.youtube.com/watch?v=LnKoncbQBsM)
