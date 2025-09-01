[← Back to Index](README.md)

# Sintaxis Básica de Python

## 📌 ¿Qué es sintaxis?

La sintaxis es el conjunto de reglas que indican cómo escribir correctamente el código en un lenguaje de programación. En Python, si no respetás la sintaxis, el programa no corre.

## 📌 ¿Qué es indentación?

La indentación es el espacio (generalmente 4 espacios o una tabulación) que se pone al inicio de una línea de código para indicar que pertenece a un bloque, por ejemplo dentro de un `if` o de un `for`. En Python, la indentación no es opcional: si no está bien, el programa da error.

## ✅ Ejemplos correctos

### Ejemplo 1
```python
if 5 > 3:
    print("Esto funciona")
```

### Ejemplo 2 con un if dentro de otro
```python
if 5 > 3:
    if 4 > 3:
        print("Ambas condiciones son verdaderas")
```

## ❌ Ejemplos incorrectos

### Error: falta indentación en el print
```python
if 5 > 3:
print("Esto da error")
```

### Error: indentación incorrecta
```python
if 5 > 3:
  if 4 > 3:
    print("Correcto")
      print("Este renglón está mal indentado")
```

## Diferencias con otros lenguajes

En muchos lenguajes de programación como C, Java o JavaScript, los bloques de código se delimitan con llaves `{ }` o con paréntesis adicionales, mientras que en Python no se usan llaves: se define la estructura del programa únicamente con la **indentación**. Esto hace que el código en Python sea más limpio y fácil de leer, pero también obliga a respetar estrictamente los espacios.
