[← Back to Index](README.md)

# Python Lambda

Una función `lambda` es una función pequeña y anónima.

Una función `lambda` puede tomar cualquier número de argumentos, pero solo puede tener una expresión.

## Sintaxis

```python
lambda argumentos : expresión
```

La expresión se ejecuta y el resultado se devuelve.

## Ejemplos básicos

### Ejemplo 1: Sumar 10 a un argumento

```python
x = lambda a : a + 10
print(x(5))
```

### Ejemplo 2: Múltiples argumentos

Las funciones lambda pueden tomar cualquier número de argumentos:

```python
x = lambda a, b : a * b
print(x(5, 6))
```

### Ejemplo 3: Tres argumentos

```python
x = lambda a, b, c : a + b + c
print(x(5, 6, 2))
```

## ¿Por qué usar funciones Lambda?

El poder de `lambda` se muestra mejor cuando las usamos como función anónima dentro de otra función.

Imaginemos que tenemos una función que toma un argumento, y ese argumento será multiplicado por un número desconocido:

```python
def mifuncion(n):
    return lambda a : a * n
```

Podemos usar esa definición de función para crear una función que siempre duplique el número que enviamos:

### Ejemplo: Duplicar números

```python
def mifuncion(n):
    return lambda a : a * n

duplicador = mifuncion(2)

print(duplicador(11))
```

### Ejemplo: Triplicar números

O usar la misma definición de función para crear una función que siempre triplique el número:

```python
def mifuncion(n):
    return lambda a : a * n

triplicador = mifuncion(3)

print(triplicador(11))
```

### Ejemplo: Ambas funciones en el mismo programa

```python
def mifuncion(n):
    return lambda a : a * n

duplicador = mifuncion(2)
triplicador = mifuncion(3)

print(duplicador(11))
print(triplicador(11))
```
