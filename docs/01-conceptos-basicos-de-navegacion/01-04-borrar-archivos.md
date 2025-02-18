# Eliminar archivos en Linux

Eliminar archivos en Linux significa deshacerse de archivos no deseados o innecesarios en tu sistema. Para esto, se utiliza el comando `rm`, el cual elimina archivos de forma permanente, por lo que se debe usar con precaución.

---

## Uso del comando `rm`

1. **Eliminar un archivo específico:**
   
   ```bash
   rm archivo.txt
   ```
   
   Esto eliminará `archivo.txt`de manera permanente.

2. **Eliminar varios archivos a la vez:**
   
   ```bash
   rm archivo1.txt archivo2.txt archivo3.txt
   ```

3. **Solicitar confirmación antes de eliminar (`-i`):**
   
   Para evitar borrar archivos por accidente, usa la opción `-i`, que pedirá confirmación antes de cada eliminación:
   
   ```bash
   rm -i archivo.txt
   ```

4. **Eliminar un directorio vacío (`rmdir`):**
   
   ```bash
   rmdir directorio
   ```
   
   La opción `-r` (*recursive*) permite eliminar el directorio y todos sus archivos y subdirectorios.

5. **Forzar la eliminación sin confirmación (`rm -rf`):**
   
   ```bash
   rm -rf directorio
   ```
   
   ⚠ **Precaución:** `rm -rf` elimina todo sin preguntar. No hay forma de recuperar los archivos eliminados.

---

## Opciones útiles de `rm`

| Opción | Descripción                                               |
| ------ | --------------------------------------------------------- |
| `-i`   | Pide confirmación antes de eliminar.                      |
| `-f`   | Fuerza la eliminación sin advertencias.                   |
| `-r`   | Elimina directorios de forma recursiva.                   |
| `-v`   | Muestra en pantalla qué archivos están siendo eliminados. |

Ejemplo con `-v`:

```bash
rm -rv directorio
```

Esto mostrará cada archivo que está siendo eliminado dentro del directorio.

---

## Evitar errores al eliminar archivos

- **Usar `rm -i` si tienes dudas**: Evita perder archivos por error.

- **No ejecutar `rm -rf /`**: Esto eliminaría todo el sistema, dejándolo inutilizable.

- **Verificar qué vas a eliminar antes con `ls`**:
  
  ```bash
  ls archivo.txt  # Asegura que el archivo existe antes de eliminarlo
  ```

- **Mover archivos a la papelera en lugar de eliminarlos directamente:**
  
  ```bash
  mv archivo.txt ~/.local/share/Trash/files/
  ```
  
  _Nota: Algunas distribuciones permiten recuperar archivos desde la papelera con `gio trash`._

---

## Conclusión

El comando `rm` es una herramienta poderosa y peligrosa si no se usa con cuidado. Si necesitas eliminar archivos o directorios en Linux, asegúrate de verificar antes de ejecutar el comando, especialmente si usas opciones como `-rf`. Siempre es recomendable usar `rm -i` para evitar pérdidas accidentales de datos.

---

[Linux rm Command: File Removing](https://labex.io/tutorials/linux-linux-rm-command-file-removing-209741)
