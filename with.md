[← Volver al índice](README.md)

# ¿Qué es `with` en Python?

La sentencia `with` es una **herramienta especial** que se usa para manejar recursos (como archivos, conexiones, etc.) de forma automática y segura.

> **Ventaja principal:** Python se encarga automáticamente de liberar el recurso cuando se termina el bloque, evitando errores y haciendo el código más limpio.

## ¿Qué es un Context Manager?

A lo que se ejecuta dentro de `with` se lo llama **context manager** - un objeto que define qué hacer al entrar y salir del bloque de código.

---

## Ejemplo 1: Abrir y cerrar un archivo

### ❌ Sin `with` (manual y propenso a errores):

```python
archivo = open("ejemplo.txt", "w")
archivo.write("Hola mundo")
archivo.close()  # Hay que cerrarlo a mano
```

### ✅ Con `with` (automático y seguro):

```python
with open("ejemplo.txt", "w") as archivo:
    archivo.write("Hola mundo")
# El archivo se cierra solo al salir del bloque
```

> **🔒 Seguridad:** Más seguro y más claro - no hay riesgo de olvidar cerrar el archivo.

---

## Ejemplo 2: Leer un archivo línea por línea

```python
with open("ejemplo.txt", "r") as archivo:
    for linea in archivo:
        print(linea.strip())
```

> **💡 Ventaja:** No hace falta preocuparse por cerrar el archivo - se hace automáticamente.

---

## Ejemplo 3: Usando múltiples contextos

```python
with open("entrada.txt", "r") as entrada, open("salida.txt", "w") as salida:
    for linea in entrada:
        salida.write(linea.upper())
```

> **🚀 Eficiencia:** Abre dos archivos a la vez y se encarga de cerrarlos al terminar.

---

## ¿Cuándo usar `with`?

### ✅ **Recomendado para:**
- **Archivos** - Lectura y escritura
- **Sockets** - Conexiones de red
- **Bases de datos** - Conexiones y transacciones
- **Cualquier recurso** que necesita cerrarse/liberarse

### 🎯 **Beneficios:**
- Hace el código **más seguro**
- **Fácil de mantener**
- **Previene memory leaks**
- **Código más limpio** y legible