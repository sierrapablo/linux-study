## **Comandos `tee`, `nl` y `wc` en Linux** 🛠️

Linux ofrece una variedad de herramientas para el procesamiento de texto. Entre ellas, `tee`, `nl` y `wc` permiten manipular, numerar y analizar archivos de texto de manera eficiente.

---

## **📌 `tee`: Redirigir y Guardar Salida**
El comando `tee` **divide la salida de un comando en dos destinos**: la pantalla y un archivo. Su nombre proviene de la forma en "T" de los tubos de plomería, que dividen el flujo en dos direcciones.

### **🔹 Uso básico**
```bash
ls -l | tee listado.txt
```
🔹 **Explicación:**
- `ls -l` genera un listado detallado de archivos.
- `tee listado.txt` muestra la salida en la terminal **y** la guarda en `listado.txt`.

### **🔹 `tee` con `sudo` para escribir en archivos protegidos**
```bash
echo "127.0.0.1 mywebsite.com" | sudo tee -a /etc/hosts
```
🔹 **Explicación:**
- `-a` agrega (`append`) la línea al archivo `/etc/hosts`.

---

## **📌 `nl`: Numerar Líneas de un Archivo**
El comando `nl` **agrega números a las líneas de un archivo**. Por defecto, **ignora líneas vacías**, pero puedes modificar este comportamiento.

### **🔹 Uso básico**
```bash
nl archivo.txt
```
🔹 **Explicación:**
- Numerará solo las líneas con contenido.

### **🔹 Numerar todas las líneas (incluyendo vacías)**
```bash
nl -ba archivo.txt
```
🔹 **Explicación:**
- `-ba` fuerza la numeración de **todas** las líneas.

---

## **📌 `wc`: Contar Palabras, Líneas y Caracteres**
El comando `wc` (**word count**) cuenta **líneas, palabras y caracteres** en un archivo.

### **🔹 Uso básico**
```bash
wc archivo.txt
```
🔹 **Salida:**
```bash
10 50 250 archivo.txt
```
🔹 **Significado:**
- `10` → Número de líneas.
- `50` → Número de palabras.
- `250` → Número de caracteres.

### **🔹 Contar líneas, palabras o caracteres por separado**
```bash
wc -l archivo.txt  # Número de líneas
wc -w archivo.txt  # Número de palabras
wc -m archivo.txt  # Número de caracteres
```

---

## **🚀 Combinaciones Útiles**
### **1️⃣ Guardar y contar líneas en un paso**
```bash
ls -l | tee listado.txt | wc -l
```
🔹 Muestra el listado de archivos, lo guarda y cuenta cuántos hay.

### **2️⃣ Numerar y guardar en un nuevo archivo**
```bash
nl documento.txt | tee numerado.txt
```
🔹 Añade números a cada línea y guarda el resultado en `numerado.txt`.

### **3️⃣ Contar palabras en un archivo y guardar el resultado**
```bash
wc -w texto.txt | tee wordcount.txt
```
🔹 Cuenta las palabras en `texto.txt` y guarda el resultado en `wordcount.txt`.

---

## **🎯 Conclusión**
Estos comandos son herramientas esenciales para **gestionar y analizar archivos de texto en Linux**. Al combinarlos con `grep`, `cut`, `awk` y `sed`, se pueden construir flujos de trabajo eficientes y automatizados. 🚀

---

[Linux nl Command: Line Numbering](https://labex.io/tutorials/linux-linux-nl-command-line-numbering-210988)

[Linux wc Command: Word Count](https://labex.io/tutorials/linux-linux-wc-command-text-counting-219200)
