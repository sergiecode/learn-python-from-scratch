[← Back to Index](README.md)

# Comentarios en Python

## 📌 ¿Qué son los comentarios?

Los comentarios sirven para explicar el código, hacerlo más fácil de leer o desactivar una línea mientras probamos.

Python ignora todo lo que esté después del símbolo `#`.

## ✅ Ejemplos de comentarios de una línea

### Comentario en línea separada
```python
# Esto es un comentario
print("Hola Mundo")
```

### Comentario al final de la línea
```python
print("Hola Mundo")  # Comentario al final de la línea
```

### Desactivar código temporalmente
```python
# print("Esto no se ejecuta")
print("Este sí se ejecuta")
```

## 📌 Comentarios en varias líneas

Python no tiene una sintaxis especial para comentarios largos. Se suelen escribir varios `#` uno debajo del otro:

### Método 1: Múltiples líneas con #
```python
# Este es un comentario
# en más de una línea
# para explicar el código
print("Hola Mundo")
```

### Método 2: Usando comillas triples
También se pueden usar comillas triples (`"""` o `'''`) como si fueran comentarios, aunque en realidad son cadenas de texto que Python ignora si no se guardan en una variable:

```python
"""
Esto parece un comentario
de varias líneas
y Python lo ignora
"""
print("Hola Mundo")
```
