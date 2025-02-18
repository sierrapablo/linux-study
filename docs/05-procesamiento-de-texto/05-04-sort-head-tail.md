# **Comandos `sort`, `head` y `tail` en Linux**

Estos tres comandos son fundamentales para el procesamiento y manipulación de archivos de texto en Linux.

---

## **1️⃣ Comando `sort`**
El comando `sort` se usa para ordenar líneas dentro de un archivo o una salida de texto.

### **Sintaxis:**
```bash
sort [OPCIONES] archivo.txt
```

### **Ejemplos de Uso:**

📌 **Ordenar un archivo en orden alfabético (por defecto)**
```bash
sort archivo.txt
```

📌 **Ordenar en orden inverso (`-r`)**
```bash
sort -r archivo.txt
```

📌 **Ordenar numéricamente (`-n`)**
```bash
sort -n numeros.txt
```
Si `numeros.txt` contiene:
```
10
2
30
1
```
Salida:
```
1
2
10
30
```

📌 **Ordenar por columna específica (`-k`)**
```bash
sort -k2 archivo.txt
```
Si `archivo.txt` tiene:
```
manzana 5
pera 3
banana 7
```
Se ordena por la segunda columna (números):
```
pera 3
manzana 5
banana 7
```

📌 **Ordenar eliminando duplicados (`-u`)**
```bash
sort -u archivo.txt
```

📌 **Guardar la salida en un nuevo archivo**
```bash
sort archivo.txt > archivo_ordenado.txt
```

---

## **2️⃣ Comando `head`**
Muestra las primeras líneas de un archivo.

### **Sintaxis:**
```bash
head [OPCIONES] archivo.txt
```

### **Ejemplos de Uso:**

📌 **Mostrar las primeras 10 líneas (por defecto)**
```bash
head archivo.txt
```

📌 **Mostrar las primeras 5 líneas (`-n`)**
```bash
head -n 5 archivo.txt
```

📌 **Mostrar los primeros 20 caracteres (`-c`)**
```bash
head -c 20 archivo.txt
```

---

## **3️⃣ Comando `tail`**
Muestra las últimas líneas de un archivo.

### **Sintaxis:**
```bash
tail [OPCIONES] archivo.txt
```

### **Ejemplos de Uso:**

📌 **Mostrar las últimas 10 líneas (por defecto)**
```bash
tail archivo.txt
```

📌 **Mostrar las últimas 5 líneas (`-n`)**
```bash
tail -n 5 archivo.txt
```

📌 **Mostrar las últimas líneas en tiempo real (`-f`), útil para logs**
```bash
tail -f /var/log/syslog
```

📌 **Mostrar los últimos 50 caracteres (`-c`)**
```bash
tail -c 50 archivo.txt
```

---

### **Conclusión**
Estos comandos son herramientas esenciales para manipular archivos de texto, especialmente en combinación con `grep`, `awk`, `cut`, `sed`, y `paste`. Son muy usados en administración de sistemas y análisis de datos.

---

[Linux sort Command: Text Sorting](https://labex.io/tutorials/linux-linux-sort-command-text-sorting-219196)
[Linux head Command: File Beginning Display](https://labex.io/tutorials/linux-linux-head-command-file-beginning-display-214302)
[Linux tail Command: File Ending Display](https://labex.io/tutorials/linux-linux-tail-command-file-end-display-214303)

```
