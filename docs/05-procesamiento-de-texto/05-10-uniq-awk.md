# **📝 Comando `uniq` en Linux**  

El comando `uniq` se usa en Linux para **eliminar líneas duplicadas consecutivas** en archivos de texto. Sin embargo, **solo funciona con líneas adyacentes repetidas**, por lo que es común combinarlo con `sort` para eliminar duplicados en toda la lista.  

📌 **Características clave:**  
✅ Filtra líneas duplicadas consecutivas.  
✅ Puede contar cuántas veces aparece cada línea.  
✅ Funciona mejor cuando se combina con `sort`.  

---

### **📌 Uso Básico de `uniq`**
### 🔹 Eliminar líneas duplicadas consecutivas  
```bash
uniq nombres.txt
```
🔹 **Explicación:**  
- Elimina **líneas repetidas consecutivas** en `nombres.txt`.  

### 🔹 Ordenar antes de eliminar duplicados  
```bash
sort nombres.txt | uniq
```
🔹 **Explicación:**  
- `sort` ordena el archivo, asegurando que las líneas duplicadas sean consecutivas.  
- `uniq` elimina las repeticiones.  

### 🔹 Contar repeticiones de cada línea  
```bash
uniq -c nombres.txt
```
🔹 **Explicación:**  
- `-c` muestra cuántas veces aparece cada línea.  
- Útil para **contar elementos únicos** en una lista.  

Ejemplo de salida:
```
  3 Juan
  2 Pedro
  5 María
```

---

## **📝 Comando `awk` en Linux**  

El comando `awk` es un lenguaje de programación orientado a **procesamiento de texto**. Es extremadamente potente para analizar archivos y extraer información estructurada.  

📌 **Características clave:**  
✅ Extrae y manipula columnas de archivos de texto.  
✅ Soporta **expresiones regulares** y lógica condicional.  
✅ Útil para **generar reportes y analizar datos**.  

---

### **📌 Uso Básico de `awk`**
### 🔹 Mostrar la primera columna de un archivo  
```bash
awk '{print $1}' archivo.txt
```
🔹 **Explicación:**  
- `$1` representa la **primera columna** de cada línea.  

Ejemplo:  
Si `archivo.txt` contiene:
```
Juan 25
Pedro 30
María 27
```
El resultado será:
```
Juan
Pedro
María
```

### 🔹 Mostrar las dos primeras columnas  
```bash
awk '{print $1, $2}' archivo.txt
```
🔹 **Explicación:**  
- `$1` = primera columna, `$2` = segunda columna.  

Salida:
```
Juan 25
Pedro 30
María 27
```

### 🔹 Filtrar líneas que contienen un valor específico  
```bash
awk '$2 > 28 {print $1, $2}' archivo.txt
```
🔹 **Explicación:**  
- Filtra y muestra las líneas donde la segunda columna (`$2`) es mayor a `28`.  

Ejemplo de salida:
```
Pedro 30
```

### 🔹 Cambiar el delimitador de columnas  
Si un archivo usa `:` en lugar de espacios para separar columnas:  
```bash
awk -F ':' '{print $1, $3}' archivo.txt
```
🔹 **Explicación:**  
- `-F ':'` indica que el **delimitador** es `:`.  

---

## **🎯 Conclusión**  
✅ `uniq` se usa para **eliminar duplicados** en archivos de texto, pero funciona mejor con `sort`.  
✅ `awk` es una **herramienta avanzada** para extraer y procesar información en archivos estructurados.  
✅ Ambos comandos son **fundamentales** para el análisis y manipulación de datos en Linux. 🚀

---

[Linux uniq Command: Duplicate Filtering](https://labex.io/tutorials/linux-linux-uniq-command-duplicate-filtering-219199)

[IBM.com: Awk by Example](https://developer.ibm.com/tutorials/l-awk1/)
[Linux Handbook: Awk](https://linuxhandbook.com/awk-command-tutorial/)
[Linux Awk Command: Text Processing](https://labex.io/tutorials/linux-linux-awk-command-text-processing-388493)
[Learning Awk is Essential for Linux Users](https://www.youtube.com/watch?v=9YOZmI-zWok)

[Explore top posts about Bash](https://app.daily.dev/tags/bash?ref=roadmapsh)
