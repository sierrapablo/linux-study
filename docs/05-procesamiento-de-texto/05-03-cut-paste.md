# Los comandos `cut` y `paste`
---

## **El Comando `cut` en Linux**

El comando `cut` es una herramienta de procesamiento de texto en Linux que permite extraer secciones específicas de cada línea de un archivo o flujo de entrada. Se usa comúnmente en scripts y tuberías (`|`) para manipulación de texto, especialmente en archivos estructurados como logs o CSV.

---

### **Sintaxis Básica**
```bash
cut [OPCIÓN]... [ARCHIVO]...
```

Donde las opciones más utilizadas son:

- **`-d [DELIMITADOR]`** → Especifica un delimitador para dividir los campos.
- **`-f [CAMPOS]`** → Indica qué campos extraer (usado junto con `-d`).
- **`-c [CARACTERES]`** → Extrae caracteres específicos de cada línea.

---

### **Ejemplos Prácticos**

1️⃣ **Extraer el segundo campo de un CSV delimitado por comas:**
```bash
echo "uno,dos,tres,cuatro" | cut -d "," -f 2
```
**Salida:**  
```
dos
```
Aquí, `-d ","` especifica la coma como delimitador y `-f 2` selecciona el segundo campo.

---

2️⃣ **Extraer los primeros 5 caracteres de cada línea en un archivo:**
```bash
cut -c 1-5 archivo.txt
```
Esto mostrará solo los primeros 5 caracteres de cada línea en `archivo.txt`.

---

3️⃣ **Extraer múltiples campos de un archivo CSV:**
```bash
cut -d ";" -f 1,3 nombres.csv
```
Si `nombres.csv` tiene este contenido:
```
Juan;25;Ingeniero
María;30;Doctora
Carlos;28;Abogado
```
La salida será:
```
Juan;Ingeniero
María;Doctora
Carlos;Abogado
```
Porque hemos seleccionado el primer y tercer campo (`-f 1,3`) usando `";"` como delimitador (`-d ";"`).

---

## **El Comando `paste` en Linux**

El comando `paste` en Linux es una herramienta de procesamiento de texto utilizada para combinar líneas de múltiples archivos. A diferencia de `cat`, que concatena archivos línea por línea, `paste` une los archivos por columnas, facilitando la manipulación de datos estructurados.

---

### **Sintaxis Básica**
```bash
paste [OPCIONES] archivo1 archivo2 ...
```
Las opciones más comunes incluyen:

- **`-d [DELIMITADOR]`** → Especifica un delimitador personalizado en lugar del tabulador por defecto.
- **`-s`** → Combina todas las líneas de un archivo en una sola fila, en lugar de unir por columnas.

---

### **Ejemplos de Uso**

1️⃣ **Unir dos archivos línea por línea**
```bash
paste archivo1.txt archivo2.txt
```
Si `archivo1.txt` contiene:
```
A
B
C
```
Y `archivo2.txt` contiene:
```
1
2
3
```
La salida será:
```
A	1
B	2
C	3
```
(Se usa tabulación como separador por defecto).

---

2️⃣ **Usar un delimitador personalizado (`-d`)**
```bash
paste -d "," archivo1.txt archivo2.txt
```
Salida:
```
A,1
B,2
C,3
```
Aquí, `-d ","` usa la coma como separador en lugar del tabulador.

---

3️⃣ **Fusionar todas las líneas en una sola fila (`-s`)**
```bash
paste -s archivo1.txt
```
Si `archivo1.txt` contiene:
```
A
B
C
```
Salida:
```
A	B	C
```
El `-s` evita la combinación por columnas y en su lugar coloca todo en una sola fila.

---

### **Conclusión**
El comando `cut` es muy útil para extraer información estructurada de archivos de texto sin necesidad de herramientas más complejas como `awk` o `sed`. Se recomienda cuando necesitas trabajar con columnas específicas de archivos CSV, logs del sistema o salidas de comandos estructurados.

El comando `paste` es una excelente opción cuando se necesita combinar archivos por columnas o reformatear datos de texto. Es útil en combinación con `cut`, `awk` y `sort` para manipular archivos estructurados como CSV o logs del sistema.

---

[Linux cut Command: Text Cutting](https://labex.io/tutorials/linux-linux-cut-command-text-cutting-219187)
