# Comprendiendo la jerarquía de directorios en Linux

En Linux, entender la jerarquía de directorios es esencial para una navegación eficiente y una gestión organizada de archivos. La estructura de directorios sigue el **Filesystem Hierarchy Standard (FHS)**, un estándar que define una organización lógica de los archivos en un esquema de árbol, evitando que se dispersen sin orden dentro del sistema.

---

## Estructura principal del sistema de archivos

| Directorio | Descripción                                                                                              |
| ---------- | -------------------------------------------------------------------------------------------------------- |
| `/`        | Directorio raíz (*root*), el nivel más alto del sistema de archivos.                                     |
| `/home`    | Contiene los directorios personales de los usuarios del sistema.                                         |
| `/bin`     | Ejecutables esenciales del sistema accesibles para todos los usuarios.                                   |
| `/sbin`    | Ejecutables para administración del sistema, generalmente accesibles solo para el superusuario (`root`). |
| `/etc`     | Archivos de configuración del sistema y aplicaciones instaladas.                                         |
| `/var`     | Contiene datos variables como registros (*logs*), archivos de correo, caché y colas de impresión.        |
| `/usr`     | Contiene programas, bibliotecas y documentación para usuarios.                                           |
| `/lib`     | Bibliotecas compartidas esenciales utilizadas por los programas en `/bin` y `/sbin`.                     |
| `/tmp`     | Archivos temporales creados por usuarios y aplicaciones. Se borra en cada reinicio.                      |

## Estructura detallada de algunos directorios

### 📁 `/home` – Directorios Personales de los Usuarios

Cada usuario tiene su propia carpeta dentro de `/home`, donde se almacenan documentos, configuraciones personales y otros archivos.

Ejemplo:

```bash
/home/usuario  # Carpeta personal del usuario "usuario"
```

### 📁 `/etc` – Configuraciones del Sistema

Contiene archivos de configuración esenciales. Algunos ejemplos:

- `/etc/passwd` → Lista de usuarios del sistema.
- `/etc/fstab` → Configuración de particiones y puntos de montaje.
- `/etc/hosts` → Tabla de nombres de host locales.

### 📁 `/var` – Datos Variables del Sistema

Contiene archivos que cambian constantemente, como registros del sistema y colas de impresión.

Ejemplo de registros del sistema:

```bash
/var/log/syslog
/var/log/auth.log
```

### 📁 `/usr` – Aplicaciones y Recursos de Usuario

Este directorio contiene la mayoría de los programas instalados y bibliotecas de usuario. Algunos subdirectorios importantes incluyen:

- `/usr/bin` → Programas para todos los usuarios.
- `/usr/sbin` → Programas administrativos.
- `/usr/share` → Documentación, iconos y otros archivos compartidos.

### 📁 `/tmp` – Archivos Temporales

Aquí se almacenan archivos temporales utilizados por programas. Se vacía al reiniciar el sistema.

---

## Conclusión

La jerarquía de directorios en Linux sigue una estructura bien definida que facilita la organización y administración de archivos. Comprender cómo están organizados los directorios principales ayuda a navegar mejor en el sistema, solucionar problemas y administrar archivos de manera más eficiente.

---

[Overview of File System Hierarchy Standard (FHS)](https://access.redhat.com/documentation/ru-ru/red_hat_enterprise_linux/4/html/reference_guide/s1-filesystem-fhs#s3-filesystem-usr)


