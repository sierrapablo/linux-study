# **STDOUT y STDERR en Linux**

En Linux, cuando se ejecuta un programa o un comando, se abren tres canales de comunicación principales:

- **STDIN** (Standard Input): Es el canal de entrada estándar, por donde el programa recibe los datos de entrada. Por lo general, este canal está vinculado al teclado.
- **STDOUT** (Standard Output): Es el canal de salida estándar, por donde el programa envía su salida normal, que normalmente se muestra en la pantalla.
- **STDERR** (Standard Error): Es el canal de salida estándar para los errores. Los mensajes de error generados por el programa se envían a través de este canal.

## **Diferencias entre STDOUT y STDERR**
- **STDOUT** se utiliza para enviar la salida normal de un comando, que generalmente se muestra en el terminal o consola.
- **STDERR** se utiliza específicamente para mensajes de error. Los mensajes de error no se mezclan con la salida estándar, lo que permite un manejo más efectivo de errores en los scripts y programas.

## **Redirección de STDOUT y STDERR**

Puedes redirigir tanto la salida estándar (STDOUT) como los errores estándar (STDERR) a archivos separados, utilizando operadores de redirección.

### Ejemplo:
```bash
$ command > stdout.txt 2>stderr.txt
```

- **`>`**: Este operador redirige la salida estándar (STDOUT) al archivo **`stdout.txt`**.
- **`2>`**: Este operador redirige la salida de error estándar (STDERR) al archivo **`stderr.txt`**.

## **Explicación del Ejemplo:**
En este ejemplo, si el comando genera una salida normal, esta se almacenará en el archivo **`stdout.txt`**, mientras que si el comando produce algún error, el mensaje de error se almacenará en el archivo **`stderr.txt`**.

Esto permite separar y gestionar la salida normal de los errores de manera distinta. Esta es una técnica muy útil cuando estamos ejecutando scripts y necesitamos procesar o analizar los resultados y los errores por separado.

## **Más ejemplos de redirección:**

1. **Redirigir solo STDOUT a un archivo**:
    ```bash
    $ command > output.txt
    ```

2. **Redirigir solo STDERR a un archivo**:
    ```bash
    $ command 2> error.txt
    ```

3. **Redirigir ambos STDOUT y STDERR al mismo archivo**:
    ```bash
    $ command > all_output.txt 2>&1
    ```

En este último ejemplo, **`2>&1`** significa que se redirige STDERR (canal 2) al mismo destino que STDOUT (canal 1), es decir, ambos se envían al archivo **`all_output.txt`**.

---

## **Conclusión:**

La capacidad de separar y redirigir **STDOUT** y **STDERR** es extremadamente útil en Linux, especialmente cuando se trabajan con scripts o automatización de tareas. Permite manejar la salida de manera más organizada, asegurando que los errores sean tratados de forma independiente y no mezclados con la salida normal.

---


