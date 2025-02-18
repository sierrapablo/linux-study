# Conceptos básicos de navegación

En Linux, la navegación entre directorios y archivos es una función fundamental pero esencial que te permite aprovechar al máximo la potencia de la interfaz de línea de comandos (CLI). Dominar los comandos básicos de navegación en Linux, como `cd`, `pwd`,`ls` y `tree`, te permitirá moverte sin problemas dentro del sistema de archivos, mostrar la lista de archivos y directorios, y comprender tu posición en relación con otros componentes del sistema.

## Uso de comandos de navegación en Linux

Dominar los comandos básicos de navegación en Linux te permite moverte de manera eficiente dentro del sistema de archivos. A continuación, te explico cómo usar los comandos esenciales:

- **Cambiar de directorio (`cd`):**
  
  Permite desplazarte entre directorios.
  
  ```bash
  cd /ruta/al/directorio
  ```

- **Mostrar el directorio actual (`pwd`):**
  
  Muestra la ruta absoluta del directorio en el que te encuentras.
  
  ```bash
  pwd
  ```

- **Listar el contenido de un directorio (`ls`):**
  
  Muestra los archivos y subdirectorios dentro del directorio actual o uno específico.
  
  ```bash
  ls
  ls -l  # Muestra detalles adicionales como permisos y tamaño
  ls -a  # Muestra archivos ocultos
  ```

- **Mostrar la estructura de directorios en forma de árbol (`tree`):**
  
  Proporciona una vista jerárquica del contenido de un directorio. 
  
  ```bash
  tree
  tree /ruta/al/directorio
  ```

    _Nota: `tree`no siempre está instalado por defecto._

### Uso de `zoxide (z)` para una navegación más eficiente

Si navegas constantemente entre directorios, `zoxide` es una herramienta avanzada que mejora `cd`, permitiéndote saltar rápidamente a directorios que has visitado anteriormente. Funciona registrando los directorios a los que accedes con `cd` y permitiéndote volver a ellos de manera inteligente.

#### Instalación de `zoxide`

Para instalarlo en Arch Linux:

```bash
sudo pacman -S zoxide
```

#### Uso básico de `zoxide`

- Para registrar directorios de forma automática, añade esto a tu `~/.zshrc` o `~/.bashrc`:
  
  ```bash
  eval "$(zoxide init zsh)"  # Si usas Zsh
  eval "$(zoxide init bash)" # Si usas Bash
  ```

- En lugar de `cd`, usa `z` para saltar rápidamente a cualquier directorio que hayas visitado antes:
  
  ```bash
  z nombre_del_directorio
  ```

- Para listar los directorios más visitados:
  
  ```bash
  zoxide query -l
  ```

- Para borrar directorios obsoletos de la base de datos:
  
  ```bash
  zoxide remove /ruta/al/directorio
  ```

Con `zoxide`, puedes moverte por el sistema de archivos mucho más rápido sin necesidad de recordar rutas largas.
