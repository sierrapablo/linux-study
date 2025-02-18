# Redirección

La **redirección** es una característica poderosa en Linux que permite manipular los flujos de entrada y salida de un comando o programa. Linux, siendo un sistema operativo multiusuario y multitarea, maneja tres flujos principales de datos para cada proceso:

1. **Entrada estándar (stdin)**: Es de donde el proceso lee su entrada. Por defecto, la entrada proviene del teclado.
2. **Salida estándar (stdout)**: Es donde el proceso escribe su salida. Por defecto, la salida va a la terminal.
3. **Error estándar (stderr)**: Es donde el proceso escribe los mensajes de error. También se dirige a la terminal por defecto.

La redirección en Linux permite cambiar el destino de estos flujos, lo que proporciona una gran flexibilidad para ejecutar comandos y programas. Puedes redirigir estos flujos a archivos o incluso a otros dispositivos en lugar de utilizar los dispositivos predeterminados (teclado para entrada y terminal para salida).

---

## Redirección de Salida: `>` y `>>`

**Redirección de salida**: Si deseas que la salida de un comando no se imprima en la terminal, sino que se almacene en un archivo, puedes usar el operador `>`.

**Ejemplo:**

```bash
ls -al > file_list.txt
```

Este comando ejecuta `ls -al` y guarda su salida en el archivo `file_list.txt`. Si el archivo no existe, será creado. Si ya existe, se **sobreescribirá** con el nuevo contenido.

Si prefieres **añadir** la salida de un comando a un archivo en lugar de sobrescribirlo, puedes usar el operador `>>`.

**Ejemplo:**

```bash
ls -al >> file_list.txt
```

Este comando agrega la salida del `ls -al` al final de `file_list.txt` sin borrar su contenido anterior.

## Redirección de error: `2>` y `2>>`

De manera similar a la redirección de salida estándar, también puedes redirigir los errores estándar (stderr) a un archivo usando el operador `2>`. Aquí, el `2` se refiere al número de descriptor de archivo de **stderr**.

**Ejemplo:**

```bash
ls nonexistentfile 2> error_log.txt
```

Este comando intenta listar un archivo inexistente, y en lugar de mostrar el error en la terminal, redirige el mensaje de error a `error_log.txt`.

Si deseas agregar errores al final de un archivo sin sobrescribirlo, puedes usar `2>>`.

**Ejemplo:**

```bash
ls nonexistentfile 2>> error_log.txt
```

## Redirección de Entrada: `<`

La redirección de entrada permite que un comando reciba datos desde un archivo en lugar del teclado. Esto se realiza con el operador `<`.

**Ejemplo:**

```bash
sort < input_file.txt
```

Este comando toma los datos de `input_file.txt` y los pasa al comando `sort` como si fueran ingresados desde el teclado.

## Redirigir tando la salida como los errores `&>`

Si deseas redirigir tanto la salida estándar (stdout) como el error estándar (stderr) a un archivo, puedes usar el operador `&>`.

**Ejemplo:**

```bash
ls -al &> output_and_error.txt
```

Este comando redirige tanto la salida como los errores al archivo `output_and_error.txt`.

---

## Resumen

- **`>`**: Redirige la salida estándar a un archivo, sobrescribiéndolo.
- **`>>`**: Redirige la salida estándar a un archivo, añadiendo contenido sin sobrescribir.
- **`2>`**: Redirige los errores estándar a un archivo, sobrescribiéndolo.
- **`2>>`**: Redirige los errores estándar a un archivo, añadiendo contenido sin sobrescribir.
- **`<`**: Redirige la entrada de un comando desde un archivo.
- **`&>`**: Redirige tanto la salida estándar como los errores a un archivo.

Estas herramientas de redirección hacen que el trabajo con la terminal de Linux sea mucho más eficiente, permitiéndote gestionar la salida y los errores de manera flexible y personalizada.

---

[Linux Command Line Mastery: Logical Operators, Redirection, and Pipelines | LabEx](https://labex.io/tutorials/linux-logical-commands-and-redirection-387332)
