# Introducción a los fundamentos de Linux - ¿Qué es Linux?
---
**Autor:** Hillary Nyakundi
**Profesión:** Curriculum Developer @ freeCodeCamp | Technical Writer
**Fecha de publicación:** 14/02/2024
**Fuente original:** [LinkedIn](https://www.linkedin.com/pulse/intro-linux-fundamentals-what-hillary-nyakundi-4u7af/)
---
El núcleo de Linux ha encontrado su camino en muchos sistemas diversos. Hoy en día, se puede encontrar en todo, desde automóviles hasta cohetes, relojes hasta televisores, y desde netbooks hasta los superordenadores más rápidos. Linux solo representa un porcentaje relativamente pequeño de los sistemas operativos utilizados en computadoras de escritorio, pero ha ganado un uso generalizado en servidores, dispositivos del Internet de las Cosas (IoT), equipos de red, teléfonos inteligentes y muchos otros dispositivos.

Nuestro enfoque principal en este artículo será su aplicación en el mundo de la computación en la nube, ya que forma parte del recorrido por la computación en la nube. Sigue leyendo mientras nos sumergimos en el mundo de los fundamentos de Linux, sus componentes y su impacto en el mundo de la tecnología. ¡Comencemos!

## ¿Qué es Linux?
Linux es un núcleo de sistema operativo de código abierto que sirve como base para una amplia variedad de sistemas operativos. Fue desarrollado por Linus Torvalds en 1991 y, desde entonces, ha evolucionado hasta convertirse en uno de los sistemas operativos más potentes disponibles. Al decir que es de código abierto, significa que los usuarios pueden ver, modificar y distribuir libremente el código fuente, algo que no ocurre con otros sistemas operativos comunes como Windows y macOS.

El modelo de Linux se basa en la colaboración, lo que facilita que desarrolladores de todo el mundo contribuyan a su mejora. Aunque es posible que no hayas interactuado directamente con el sistema operativo, probablemente sí con dispositivos que funcionan con Linux; un buen ejemplo de ello son los dispositivos Android.

### Características de Linux
 - **Código abierto:** su naturaleza de código abierto permite que cualquier persona acceda al código fuente para contribuir, modificar y compartirlo.
 - **Fiabilidad:** su estabilidad y confiabilidad lo convierten en la opción ideal para sistemas críticos y servidores.
 - **Multitarea y multiusuario:** admite múltiples usuarios, lo que facilita el uso compartido de recursos y la ejecución de múltiples procesos simultáneamente.
 - **Seguridad:** cuenta con una amplia gama de funciones de seguridad, como la gestión de privilegios de usuario, permisos del sistema de archivos y controles de acceso obligatorios.
 - **Portabilidad:** su capacidad de adaptación ha permitido su adopción en una gran variedad de entornos, desde sistemas embebidos y teléfonos inteligentes hasta servidores y superordenadores.
 - **Interfaz de línea de comandos (CLI):** ofrece una potente CLI que proporciona a los usuarios un control extenso sobre las funciones del sistema.

### El kernel de Linux
![El kernel de Linux](../../assets/images/00-01-linux-kernel.png)
El núcleo (kernel) actúa como el componente central del sistema operativo Linux. Funciona como un puente entre el hardware y el software. Algunas de sus principales funciones incluyen la gestión de la ejecución de múltiples aplicaciones, el reparto de recursos entre varios usuarios, el control de la interfaz de los dispositivos de entrada/salida (I/O) conectados a la computadora y la administración de archivos y directorios. Otras funciones incluyen:

 - **Gestión de procesos:** inicia, programa y finaliza procesos.
 - **Gestión de memoria:** asigna y libera espacio de memoria para los procesos, además de implementar memoria virtual.
 - Facilita la comunicación entre los componentes de hardware y el sistema operativo.
 - Administra los permisos de archivos y el control de acceso.

Comprender correctamente el núcleo permite obtener una visión más profunda sobre cómo se ejecutan las distintas operaciones dentro del sistema operativo.

### Estructura del sistema de archivos en Linux
Comprender la estructura del sistema de archivos en Linux es muy útil para la navegación y organización del sistema.

 - **Directorio raíz (/):** es el directorio de nivel superior que contiene todos los demás directorios y archivos.
 - **/bin y /sbin:** contienen ejecutables binarios importantes. /bin almacena programas esenciales para todos los usuarios del sistema, mientras que /sbin está reservado para binarios del sistema, utilizados principalmente por administradores.
 - **/home:** directorio donde se encuentran los archivos y configuraciones personales de los usuarios regulares.
 - **/etc:** contiene archivos de configuración del sistema.
 - **/var:** almacena archivos variables, como registros (logs), archivos de spool y archivos temporales.
 - **/usr:** contiene programas y datos relacionados con los usuarios.
 - **/tmp:** almacena archivos temporales generados por el sistema y las aplicaciones.

## Distribuciones de Linux
Como se mencionó anteriormente, Linux es un sistema operativo de código abierto que permite a las personas hacer copias y distribuirlo. Estas distribuciones se conocen comúnmente como "distros". Una distribución de Linux es un conjunto completo de paquetes que incluye el núcleo (kernel), utilidades del sistema, bibliotecas y aplicaciones adicionales, proporcionando a los usuarios un sistema operativo listo para usar. Algunas de las distribuciones más populares son:

 - **Ubuntu:** una excelente opción para principiantes debido a su interfaz fácil de usar.
 - **Fedora:** ideal para quienes buscan las últimas novedades, ya que está a la vanguardia en la adopción de nuevas características. Se enfoca en la seguridad, lo que lo hace perfecto para desarrolladores y usuarios preocupados por la seguridad.
 - **Debian:** recomendado para servidores y sistemas críticos. Su sistema de gestión de paquetes facilita la instalación de software.
 - **Arch Linux:** conocido por su alto nivel de personalización, permitiendo a los usuarios construir su sistema desde cero. Proporciona actualizaciones continuas sin necesidad de reinstalar aplicaciones.
