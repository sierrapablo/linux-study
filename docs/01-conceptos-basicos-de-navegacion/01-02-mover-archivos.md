# Mover archivos en Linux

En Linux, mover archivos es una tarea esencial que realizarás con frecuencia. El comando `mv` (abreviatura de *move*) se usa para trasladar archivos y directorios de una ubicación a otra. Además, también se puede utilizar para renombrar archivos en Linux.

 **Sintaxis general del comando `mv`**

```bash
mv [opciones] origen destino
```

Donde:

- **`origen`**: es el archivo o directorio que deseas mover.
- **`destino`**: es la ubicación donde quieres mover el archivo o directorio de origen.

El comando `mv` es ampliamente utilizado debido a su simplicidad y versatilidad. Ya sea para organizar archivos moviéndolos a diferentes directorios o renombrar varios archivos, `mv` es una herramienta fundamental en Linux.

---

## Uso básico del comando `mv`

1. **Mover un archivo a otra ubicación:**
   
   ```bash
   mv archivo.txt /ruta/destino/
   ```
   
   Esto trasladará `archivo.txt` al directorio `/ruta/destino/`.

2. **Renombrar un archivo:**
   
   ```bash
   mv archivo_viejo.txt archivo_nuevo.txt
   ```
   
   Este comando cambiará el nombre de `archivo_viejo.txt` a `archivo_nuevo.txt`.

3. **Mover varios archivos a un directorio:**
   
   ```bash
   mv archivo1.txt archivo2.txt /ruta/destino/
   ```
   
   Esto moverá `archivo1.txt` y `archivo2.txt` al directorio `/ruta/destino/`.

4. **Mover un directorio completo:**
   
   ```bash
   mv directorio1 /ruta/destino/
   ```
   
   Esto trasladará `directorio1` dentro de `/ruta/destino/`.

5. **Sobreescribir archivos sin confirmación:**
   
   Cuando `mv` encuentra un archivo con el mismo nombre en el destino, lo sobrescribe sin advertencia. Para evitar esto, usa `-i` (interactivo), que preguntará antes de sobrescribir:
   
   ```bash
   mv -i archivo.txt /ruta/destino/
   ```
   
   Para sobrescribir sin confirmación, usa `-f`:
   
   ```bash
   mv -f archivo.txt /ruta/destino/
   ```

---

## Opciones útiles del comando `mv`

| Opción | Descripción                                                               |
| ------ | ------------------------------------------------------------------------- |
| `-i`   | Modo interactivo: solicita confirmación antes de sobrescribir un archivo. |
| `-f`   | Fuerza el movimiento y sobrescribe archivos sin confirmación.             |
| `-n`   | Evita sobrescribir archivos existentes.                                   |
| `-v`   | Muestra en pantalla los movimientos realizados (*verbose*).               |

Ejemplo con `-v` para ver lo que está haciendo el comando:

```bash
mv -v archivo.txt /ruta/destino/
```

---

## Trucos y mejores prácticas

- **Mover archivos coincidentes con un patrón:**
  
  ```bash
  mv *.txt /ruta/destino/
  ```
  
  Esto moverá todos los archivos `.txt` al directorio `/ruta/destino/`.

- **Usar `find` con `mv` para mover archivos específicos:**
  
  ```bash
  find /ruta/origen -name "*.log" -exec mv {} /ruta/destino/ \;
  ```
  
  Esto moverá todos los archivos `.log` dentro de `/ruta/origen/` a `/ruta/destino/`.

- **Evitar perder archivos accidentalmente con `mv -n`**
  
  ```bash
  mv -n archivo.txt /ruta/destino/
  ```
  
  Si `archivo.txt` ya existe en `/ruta/destino/`, no lo sobrescribirá.

---

## **Conclusión**

El comando `mv` es una herramienta esencial en Linux, tanto para la gestión de archivos como para su organización. Su versatilidad lo convierte en una opción eficiente para tareas cotidianas como mover archivos, renombrarlos y reorganizar directorios. Conociendo sus opciones y combinándolo con otras herramientas como `find`, puedes optimizar aún más la administración de tu sistema de archivos.

---

[Linux mv Command: File Moving and Renaming](https://labex.io/tutorials/linux-linux-mv-command-file-moving-and-renaming-209743)
