# Variables de entorno

En Linux, las **variables de entorno** son valores dinámicos con nombre que pueden afectar el comportamiento de los procesos que se ejecutan en una shell. Estas variables existen en cada sesión de la shell y contienen configuraciones del sistema, como el directorio home del usuario, la ruta de búsqueda de comandos, el tipo de terminal y las preferencias de los programas.

Las **variables de entorno** contribuyen a la flexibilidad y personalización que caracterizan a los sistemas Unix. Proporcionan una manera sencilla de compartir configuraciones entre múltiples aplicaciones y procesos en Linux.

---

## ¿Qué Son las Variables de Entorno?

Las variables de entorno permiten que la configuración y las preferencias del sistema sean fácilmente accesibles y modificables. A través de estas, el sistema y los programas pueden adaptarse según el entorno de la shell en la que se están ejecutando.

Algunos ejemplos comunes de variables de entorno incluyen:

- **$HOME**: El directorio home del usuario actual.
- **$PATH**: La ruta de búsqueda de los comandos ejecutables.
- **$USER**: El nombre del usuario actual.
- **$SHELL**: La shell que está en uso (por ejemplo, `/bin/bash`).
- **$EDITOR**: El editor de texto preferido.

## Comandos para Ver y Usar las Variables de Entorno

- **Listar todas las variables de entorno:**
  
  El comando `env` muestra todas las variables de entorno activas en una sesión de shell.
  
  ```bash
  $ env
  ```
  
  Esto devolverá una lista completa de las variables de entorno disponibles.

- **Mostrar una variable en particular:**
  
  Si deseas ver el valor de una variable específica, como `$PATH`, puedes usar el comando `echo` seguido del nombre de la variable precedido por un signo de dólar (`$`).
  
  ```bash
  $ echo $PATH
  ```
  
  Este comando devolverá la lista de directorios donde la shell buscará los ejecutables para los comandos.

## Modificar Variables de Entorno

Puedes establecer o modificar variables de entorno dentro de una sesión de shell con el comando `export`. Esto cambia el valor de la variable para el resto de la sesión actual.

Por ejemplo, para agregar un directorio a la variable `$PATH`, usarías:

```bash
$ export PATH=$PATH:/nuevo/directorio
```

Este comando agrega `/nuevo/directorio` al final de la variable `$PATH`, permitiendo que el sistema busque ejecutables en ese directorio adicional.

## Persistencia de Variables de Entorno

Si deseas que una variable de entorno persista entre sesiones, puedes agregar el comando `export` en el archivo de configuración de tu shell, como `~/.bashrc` o `~/.zshrc`, dependiendo de la shell que uses.

---

## Conclusión

Las **variables de entorno** son esenciales para personalizar y controlar el comportamiento de los procesos y comandos en una sesión de shell en Linux. Ofrecen flexibilidad para adaptar el sistema según las necesidades del usuario y la aplicación.

Al comprender y manipular estas variables, puedes mejorar la eficiencia y personalización en el uso de la terminal de Linux. 🌟

---

[Environment Variables in Linux](https://labex.io/tutorials/linux-environment-variables-in-linux-385274)
