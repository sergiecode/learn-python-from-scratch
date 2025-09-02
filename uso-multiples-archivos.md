[← Volver al índice](README.md)

# Uso de Múltiples Archivos en Python (Módulos)

En Python, un archivo con extensión `.py` no es solamente un script: también puede funcionar como un **módulo**. Esto significa que podemos importar el código de un archivo en otro, evitando repetir funciones o clases y organizando mejor el proyecto.

## Ejemplo Básico

### Archivo: `saludos.py`

```python
def decir_hola():
    print("Hola desde el módulo saludos!")

def decir_adios():
    print("Chau, nos vemos!")
```

### Archivo: `main.py`

```python
# Importamos la función desde el módulo saludos
from saludos import decir_hola, decir_adios

decir_hola()
decir_adios()
```

**Resultado:** Cuando ejecutamos `main.py`, se muestran los mensajes. El archivo `saludos.py` funciona como una biblioteca personalizada que reutilizamos.

## Explicación de la Sintaxis de Importación

### Sintaxis: `from menu import mostrar_menu`

- **`menu`** → es el nombre del archivo (`menu.py`), sin la extensión `.py`
- **`import`** → es la instrucción que le dice a Python que queremos usar algo de ese archivo
- **`mostrar_menu`** → es el nombre de la función dentro de `menu.py` que estamos trayendo

De esta forma, podemos usar `mostrar_menu()` en el archivo actual sin necesidad de escribir `menu.mostrar_menu()`.

> **Es como decirle a Python:** "Traeme del archivo `menu.py` solamente la función `mostrar_menu` para usarla directamente acá."

### Variante Alternativa

```python
import menu

menu.mostrar_menu()
```

En este caso importamos todo el archivo completo, y para llamar la función necesitamos escribir `menu.mostrar_menu()`. Ambas formas son correctas, depende de si queremos importar una parte específica o todo.

## Explicación de `if __name__ == "__main__"`

Este es un bloque muy usado en Python, y su función principal es controlar si un archivo se ejecuta directamente o si se está importando en otro lado.

### Paso a Paso

1. En cada archivo `.py`, Python define una variable especial llamada `__name__`
2. Si el archivo se está ejecutando directamente (por ejemplo, `python main.py`), entonces `__name__` toma el valor `"__main__"`
3. Si el archivo se está importando en otro archivo (como hicimos con `from saludos import decir_hola`), entonces `__name__` vale el nombre del archivo (`"saludos"` en ese caso)

### Ejemplo Práctico

**Archivo: `ejemplo.py`**

```python
def saludar():
    print("Hola!")

print("Este mensaje aparece siempre")

if __name__ == "__main__":
    print("Este archivo se ejecutó directamente")
    saludar()
```

### Casos de Uso

**Si ejecutamos directamente `python ejemplo.py`:**

```
Este mensaje aparece siempre
Este archivo se ejecutó directamente
Hola!
```

**Si lo importamos en otro archivo (`import ejemplo`):**

```
Este mensaje aparece siempre
```

> **Nota:** La parte dentro de `if __name__ == "__main__":` no se ejecuta al importar, porque el archivo no fue abierto directamente, solo cargado como módulo.