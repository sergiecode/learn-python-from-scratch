# Números en Python

En Python existen tres tipos de números principales:

- **int** – Números enteros
- **float** – Números decimales  
- **complex** – Números complejos

Cuando asignamos un valor a una variable, automáticamente se crea del tipo correspondiente:

```python
x = 1      # int
y = 2.8    # float
z = 1j     # complex
```

Podemos verificar el tipo de cualquier variable con la función `type()`:

```python
print(type(x))  # <class 'int'>
print(type(y))  # <class 'float'>
print(type(z))  # <class 'complex'>
```

## 1. int (enteros)

Son números enteros, positivos o negativos, sin decimales y de tamaño ilimitado.

```python
x = 1
y = 35656222554887711
z = -3255522

print(type(x))
print(type(y))
print(type(z))
```

## 2. float (decimales)

Son números con decimales, positivos o negativos.

```python
x = 1.10
y = 1.0
z = -35.59

print(type(x))
print(type(y))
print(type(z))
```

### Notación científica

También se pueden escribir en notación científica usando `e` (10 elevado a...):

```python
x = 35e3   # 35 × 10^3 = 35000.0
y = 12E4   # 12 × 10^4 = 120000.0
z = -87.7e100

print(type(x))
print(type(y))
print(type(z))
```

## 3. complex (complejos)

Tienen una parte real y una parte imaginaria, donde la parte imaginaria se escribe con `j`.

```python
x = 3 + 5j
y = 5j
z = -5j

print(type(x))
print(type(y))
print(type(z))
```

## Conversión de tipos

Se puede convertir un número de un tipo a otro usando `int()`, `float()` o `complex()`.

```python
x = 1    # int
y = 2.8  # float
z = 1j   # complex

# int a float
a = float(x)

# float a int
b = int(y)

# int a complex
c = complex(x)

print(a, type(a))  # 1.0 <class 'float'>
print(b, type(b))  # 2 <class 'int'>
print(c, type(c))  # (1+0j) <class 'complex'>
```

> **Nota:** no se pueden convertir números complejos a otros tipos directamente.

## Números aleatorios

Python no tiene una función `random()` por defecto, pero podemos usar el módulo `random` para generar números aleatorios:

```python
import random

print(random.randrange(1, 10))  # Un número aleatorio entre 1 y 9
```