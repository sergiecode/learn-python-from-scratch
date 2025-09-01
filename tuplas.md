[← Back to Index](README.md)

# Tuplas en Python

## ¿Qué es una tupla?

Una tupla es una colección de elementos que:

- **Está ordenada**: los elementos tienen un orden fijo
- **Es inmutable**: no se puede cambiar, agregar ni eliminar elementos después de creada
- **Permite duplicados**: los mismos valores pueden repetirse

Se escribe usando paréntesis:

```python
frutas = ("manzana", "banana", "cereza")
print(frutas)
```

## Características principales

### Elementos ordenados
Cada elemento tiene un índice, empezando en 0.

### Inmutables
No puedes cambiar sus valores directamente.

### Permiten duplicados
Puedes tener el mismo valor varias veces:

```python
frutas = ("manzana", "banana", "cereza", "manzana", "cereza")
print(frutas)
```

## Longitud de una tupla

Para saber cuántos elementos tiene una tupla, usamos `len()`:

```python
frutas = ("manzana", "banana", "cereza")
print(len(frutas))  # Resultado: 3
```

## Tuplas con un solo elemento

Para crear una tupla de un solo elemento, debes poner una coma después del valor:

```python
fruta = ("manzana",)
print(type(fruta))  # <class 'tuple'>

no_tupla = ("manzana")
print(type(no_tupla))  # <class 'str'>
```

## Tipos de datos en tuplas

Una tupla puede contener cualquier tipo de dato:

```python
tuple1 = ("abc", 34, True, 40, "masculino")
```

## Constructor tuple()

También puedes crear tuplas usando `tuple()`:

```python
frutas = tuple(("manzana", "banana", "cereza"))
print(frutas)
```

## Acceder a los elementos

### Usando índices

```python
frutas = ("manzana", "banana", "cereza")
print(frutas[1])  # banana
```

### Índices negativos

Empieza desde el final:

```python
print(frutas[-1])  # cereza
```

### Rango de elementos

```python
frutas = ("manzana", "banana", "cereza", "naranja", "kiwi")
print(frutas[2:5])   # ('cereza', 'naranja', 'kiwi')
print(frutas[:4])    # desde el inicio hasta el índice 3
print(frutas[2:])    # desde el índice 2 hasta el final
print(frutas[-4:-1]) # desde el -4 hasta el -2
```

### Verificar si un elemento existe

```python
frutas = ("manzana", "banana", "cereza")
if "manzana" in frutas:
    print("Sí, 'manzana' está en la tupla")
```

## Modificar tuplas (workarounds)

Aunque las tuplas son inmutables, puedes:

### Convertir a lista, modificar y volver a tupla

```python
x = ("manzana", "banana", "cereza")
y = list(x)
y[1] = "kiwi"
x = tuple(y)
print(x)
```

### Agregar elementos

```python
y = list(x)
y.append("naranja")
x = tuple(y)

# O unir tuplas
x += ("naranja",)
```

### Eliminar elementos

No se puede eliminar directamente, pero se puede convertir a lista y luego eliminar, o eliminar la tupla completa:

```python
del x
```

## Desempaquetado de tuplas

Puedes asignar los elementos a variables:

```python
frutas = ("manzana", "banana", "cereza")
(a, b, c) = frutas
print(a, b, c)
```

### Usando asterisco `*`

Si hay más elementos que variables:

```python
frutas = ("manzana", "banana", "cereza", "frutilla", "frambuesa")
(a, b, *resto) = frutas
print(a, b, resto)  # ['cereza', 'frutilla', 'frambuesa']
```

## Recorrer tuplas

### Con for

```python
for f in frutas:
    print(f)
```

### Con índices

```python
for i in range(len(frutas)):
    print(frutas[i])
```

### Con while

```python
i = 0
while i < len(frutas):
    print(frutas[i])
    i += 1
```

## Unir y multiplicar tuplas

### Unir tuplas

```python
t1 = ("a", "b", "c")
t2 = (1, 2, 3)
t3 = t1 + t2
print(t3)  # ('a', 'b', 'c', 1, 2, 3)
```

### Multiplicar tupla

```python
frutas = ("manzana", "banana", "cereza")
print(frutas * 2)  # ('manzana', 'banana', 'cereza', 'manzana', 'banana', 'cereza')
```