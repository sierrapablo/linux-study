# **Comandos `tr`, `join` y `split` en Linux**

Estos tres comandos son esenciales en el procesamiento de texto en Linux, cada uno con una función específica para manipular y transformar archivos de texto.

---

## **1️⃣ Comando `tr` (Translate)**
El comando `tr` se usa para traducir, reemplazar o eliminar caracteres de un flujo de texto.

### **Sintaxis:**
```bash
tr [OPCIONES] SET1 [SET2]
```

### **Ejemplos de Uso:**

📌 **Convertir minúsculas a mayúsculas**
```bash
echo 'linux' | tr 'a-z' 'A-Z'
```
Salida:
```
LINUX
```

📌 **Eliminar caracteres específicos**
```bash
echo 'hello 123' | tr -d '0-9'
```
Salida:
```
hello 
```

📌 **Reemplazar espacios por guiones**
```bash
echo "hello world" | tr ' ' '-'
```
Salida:
```
hello-world
```

📌 **Eliminar caracteres repetidos (`-s` para squeeze)**
```bash
echo "aaabbbccc" | tr -s 'a-c'
```
Salida:
```
abc
```

---

## **2️⃣ Comando `join`**
El comando `join` combina líneas de dos archivos en función de una clave común, similar a una operación `JOIN` en SQL.

### **Sintaxis:**
```bash
join [OPCIONES] archivo1 archivo2
```

### **Ejemplo de Uso:**

Supongamos que tenemos dos archivos:

📁 **nombres.txt**
```
1 Ana
2 Luis
3 Juan
```
📁 **edades.txt**
```
1 25
2 30
3 22
```

📌 **Unir los archivos por el primer campo (deben estar ordenados)**
```bash
join nombres.txt edades.txt
```
Salida:
```
1 Ana 25
2 Luis 30
3 Juan 22
```

📌 **Ordenar antes de unir (si no están ordenados)**
```bash
sort nombres.txt -o nombres.txt
sort edades.txt -o edades.txt
join nombres.txt edades.txt
```
Especificar
📌 **Especificar delimitador en archivos CSV (`-t`)**
```bash
join -t ',' file1.csv file2.csv
```

---

## **3️⃣ Comando `split`**
El comando `split` divide un archivo grande en múltiples partes más pequeñas.

### **Sintaxis:**
```bash
split [OPCIONES] [ARCHIVO] [PREFIX]
```

### **Ejemplos de Uso:**

📌 **Dividir un archivo en partes de 500 líneas**
```bash
split -l 500 bigfile.txt
```
Esto generará archivos `xaa`, `xab`, `xac`, etc.

📌 **Especificar un prefijo para los archivos de salida**
```bash
split -l 500 bigfile.txt parte_
```
Generará:
```
parte_aa
parte_ab
parte_ac
...
```

📌 **Dividir un archivo por tamaño en bytes (ejemplo: 1MB por archivo)**
```bash
split -b 1M bigfile.txt chunk_
```

📌 **Dividir un archivo en exactamente 4 partes iguales**
```bash
split -n 4 bigfile.txt
```

---

### **Conclusión**
Estos comandos permiten realizar transformaciones avanzadas de texto, combinaciones de archivos y divisiones eficientes de grandes volúmenes de datos. Son herramientas clave para el procesamiento de datos en Linux. 🚀

---

[Linux tr Command: Character Translating](https://labex.io/tutorials/linux-linux-tr-command-character-translating-388064)
[Linux join Command: File Joining](https://labex.io/tutorials/linux-linux-join-command-file-joining-219193)

