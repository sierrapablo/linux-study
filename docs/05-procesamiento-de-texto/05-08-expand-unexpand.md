## **Comandos `expand` y `unexpand` en Linux** 🛠️

Los comandos `expand` y `unexpand` permiten convertir **tabulaciones en espacios** y viceversa en archivos de texto, asegurando una **formateo consistente** y mejorando la legibilidad del código o documentos.

---

## **📌 `expand`: Convertir Tabulaciones en Espacios**
El comando `expand` **sustituye tabulaciones (`\t`) por espacios**. Esto es útil cuando se necesita una **indentación uniforme**, ya que algunos editores o sistemas muestran tabulaciones con diferentes anchos.

### **🔹 Uso básico**
```bash
expand archivo.txt
```
🔹 **Explicación:**
- Muestra el contenido de `archivo.txt` con **las tabulaciones convertidas en espacios**.
- **No modifica el archivo original**, solo imprime el resultado en pantalla.

### **🔹 Especificar el número de espacios por tabulación**
```bash
expand -t 4 archivo.txt
```
🔹 **Explicación:**
- `-t 4` convierte cada tabulación en **4 espacios** en lugar del valor predeterminado (8).

### **🔹 Guardar el resultado en un archivo nuevo**
```bash
expand -t 2 codigo_fuente.py > codigo_sin_tabs.py
```
🔹 **Explicación:**
- Convierte las tabulaciones en **2 espacios** y guarda el resultado en `codigo_sin_tabs.py`.

---

## **📌 `unexpand`: Convertir Espacios en Tabulaciones**
El comando `unexpand` **convierte espacios en tabulaciones (`\t`)**, útil para reducir el tamaño de archivos y mejorar la alineación en editores configurados para usar tabulaciones.

### **🔹 Uso básico**
```bash
unexpand archivo.txt
```
🔹 **Explicación:**
- Sustituye **múltiples espacios consecutivos** por tabulaciones **donde sea posible**.

### **🔹 Convertir cada 4 espacios en un tab**
```bash
unexpand -t 4 archivo.txt
```
🔹 **Explicación:**
- `-t 4` reemplaza cada **grupo de 4 espacios** con una tabulación.

### **🔹 Convertir solo los espacios al inicio de las líneas**
```bash
unexpand -a archivo.txt
```
🔹 **Explicación:**
- `-a` convierte **todos** los espacios posibles en tabulaciones (por defecto solo los espacios iniciales de cada línea).

---

## **🚀 Combinaciones Útiles**
### **1️⃣ Convertir tabulaciones en espacios y contar líneas**
```bash
expand -t 4 script.sh | wc -l
```
🔹 **Convierte tabulaciones en 4 espacios y cuenta las líneas del archivo**.

### **2️⃣ Convertir espacios en tabs y guardar en un nuevo archivo**
```bash
unexpand -t 2 texto_formateado.txt > texto_tabs.txt
```
🔹 **Reemplaza cada 2 espacios por una tabulación y guarda el resultado**.

---

## **🎯 Conclusión**
Los comandos `expand` y `unexpand` garantizan **formatos de texto uniformes** en entornos donde el uso de espacios o tabulaciones es inconsistente. Son herramientas esenciales en la limpieza y estandarización de archivos de código y documentos de texto en Linux. 🚀


