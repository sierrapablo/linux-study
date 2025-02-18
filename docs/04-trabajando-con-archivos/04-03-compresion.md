# Archivos comprimidos

En Linux, la creación de archivos de archivo (archivos comprimidos) es una práctica esencial para gestionar datos, hacer copias de seguridad y facilitar la distribución de archivos. Linux ofrece herramientas potentes como `tar`, `gzip` y `bzip2` para crear y manejar estos archivos de archivo.

- **`tar`**: Originalmente utilizado para la creación de archivos en cintas (tape archiving), es una herramienta versátil para combinar varios archivos y directorios en un solo archivo.
- **`gzip`** y **`bzip2`**: Son herramientas para la compresión de archivos, lo que reduce el tamaño de los archivos y facilita su transmisión.

---

## Comandos comunes para archivar y comprimir

### Crear un archivo tar (sin compresión)

Para crear un archivo tar que combine múltiples archivos o directorios en uno solo, usamos:

```bash
tar cvf archive_name.tar directory_to_archive/
```

- `c` (create): Crea un nuevo archivo de archivo.
- `v` (verbose): Muestra los archivos que están siendo archivados.
- `f` (file): Especifica el nombre del archivo de salida.
- `archive_name.tar`: Nombre del archivo de archivo a crear.
- `directory_to_archive/`: El directorio o archivos que se van a archivar.

### Extraer un archivo tar

Para extraer el contenido de un archivo tar, usamos el siguiente comando:

```bash
tar xvf archive_name.tar
```

- `x` (extract): Extrae los archivos del archivo tar.
- `v` (verbose): Muestra los archivos que se están extrayendo.
- `f` (file): Especifica el nombre del archivo de archivo del que se extraerán los datos.

### Crear un archivo tar comprimido con gzip

Si deseas crear un archivo tar y, además, comprimirlo usando `gzip` para reducir el tamaño del archivo, usas:

```bash
tar cvzf archive_name.tar.gz directory_to_archive/
```

- `z` (gzip): Comprime el archivo usando `gzip`.
- `archive_name.tar.gz`: Nombre del archivo de archivo comprimido con extensión `.tar.gz`.

### Crear un archivo tar comprimido con bzip2

Si prefieres utilizar `bzip2` para una mayor compresión, usa:

```bash
tar cvjf archive_name.tar.bz2 directory_to_archive/
```

- `j` (bzip2): Comprime el archivo usando `bzip2`.
- `archive_name.tar.bz2`: Nombre del archivo de archivo comprimido con extensión `.tar.bz2`.

## Descomprimir

- **Extraer un archivo `.tar.gz`:**
  
  ```bash
  tar xvzf archive_name.tar.gz
  ```

- **Extraer un archivo `.tar.bz2`:**
  
  ```bash
  tar xvjf archive_name.tar.bz2
  ```

## Diferencias entre archivar y comprimir

- **Archivar** (con `tar`) agrupa varios archivos en un solo archivo para facilitar su manejo.
- **Comprimir** (con `gzip` o `bzip2`) reduce el tamaño de los archivos para ahorrar espacio y facilitar la transmisión.

Aunque estos dos procesos (archivar y comprimir) son comúnmente utilizados juntos, también pueden usarse por separado. Por ejemplo, puedes archivar archivos con `tar` y luego comprimir ese archivo usando `gzip` o `bzip2`.

## Resumen de comandos

| **Acción**                       | **Comando**                                           | **Descripción**                            |
| -------------------------------- | ----------------------------------------------------- | ------------------------------------------ |
| Crear archivo tar sin compresión | `tar cvf archive_name.tar directory_to_archive/`      | Archiva archivos sin compresión.           |
| Extraer archivo tar              | `tar xvf archive_name.tar`                            | Extrae el contenido de un archivo tar.     |
| Crear archivo tar con gzip       | `tar cvzf archive_name.tar.gz directory_to_archive/`  | Archiva y comprime con gzip.               |
| Crear archivo tar con bzip2      | `tar cvjf archive_name.tar.bz2 directory_to_archive/` | Archiva y comprime con bzip2.              |
| Extraer archivo tar con gzip     | `tar xvzf archive_name.tar.gz`                        | Extrae el contenido de un archivo tar.gz.  |
| Extraer archivo tar con bzip2    | `tar xvjf archive_name.tar.bz2`                       | Extrae el contenido de un archivo tar.bz2. |

---

## Conclusión

El uso de herramientas como `tar`, `gzip` y `bzip2` en Linux es fundamental para la gestión de archivos grandes, la creación de copias de seguridad, y la distribución eficiente de datos. Comprender cómo archivar y comprimir archivos puede hacer que la administración de sistemas y la transferencia de datos sea mucho más fácil.

---

[Linux File Packaging and Compression](https://labex.io/tutorials/linux-file-packaging-and-compression-385413)
