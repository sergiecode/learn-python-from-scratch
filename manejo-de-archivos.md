[← Back to Index](README.md)

# Manejo de Archivos en Python para Principiantes

El manejo de archivos es una parte fundamental de cualquier aplicación en Python. Nos permite crear, leer, actualizar y eliminar archivos de manera sencilla.

## 1. Abrir Archivos

La función principal para trabajar con archivos en Python es `open()`. Esta función necesita dos parámetros:

```python
open(nombre_archivo, modo)
```

### Modos de apertura

| Modo | Descripción |
|------|-------------|
| `"r"` | Leer (por defecto). Error si el archivo no existe. |
| `"a"` | Añadir contenido al final. Crea el archivo si no existe. |
| `"w"` | Escribir. Sobrescribe el archivo si existe, o lo crea si no. |
| `"x"` | Crear un archivo nuevo. Error si ya existe. |

También se puede especificar si el archivo es texto (`t`) o binario (`b`). Por defecto, es `"t"`.

```python
# Abrir un archivo para lectura de texto
f = open("demofile.txt")  # equivalente a open("demofile.txt", "rt")
```

> **Nota:** Siempre verifica que el archivo exista para evitar errores.

## 2. Leer Archivos

### Leer todo el contenido

```python
with open("demofile.txt") as f:
    print(f.read())
```

### Leer líneas específicas

```python
with open("demofile.txt") as f:
    print(f.readline())  # primera línea
    print(f.readline())  # segunda línea
```

### Leer línea por línea con un bucle

```python
with open("demofile.txt") as f:
    for linea in f:
        print(linea)
```

### Leer solo cierta cantidad de caracteres

```python
with open("demofile.txt") as f:
    print(f.read(5))  # devuelve los primeros 5 caracteres
```

> **💡 Tip:** Usar `with` es recomendable porque cierra automáticamente el archivo.

Si no usas `with`, deberías cerrar el archivo manualmente:

```python
f = open("demofile.txt")
print(f.readline())
f.close()
```

## 3. Escribir Archivos

### Añadir contenido

```python
with open("demofile.txt", "a") as f:
    f.write("Ahora el archivo tiene más contenido!")
```

### Sobrescribir contenido

```python
with open("demofile.txt", "w") as f:
    f.write("¡Ups! He borrado el contenido anterior.")
```

### Crear un archivo nuevo

```python
f = open("myfile.txt", "x")  # crea un archivo vacío
```

> **Nota:** `"w"` y `"a"` también pueden crear archivos si no existen, pero `"x"` dará error si ya existe.

## 4. Eliminar Archivos y Carpetas

Para eliminar archivos o carpetas, se usa el módulo `os`:

### Eliminar un archivo

```python
import os

if os.path.exists("demofile.txt"):
    os.remove("demofile.txt")
else:
    print("El archivo no existe")
```

### Eliminar una carpeta vacía

```python
import os
os.rmdir("mi_carpeta")
```

> **⚠️ Importante:** Solo se pueden eliminar carpetas vacías con `os.rmdir()`.