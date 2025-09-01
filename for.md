# Bucle for en Python

El bucle `for` se utiliza para recorrer una secuencia, como una lista, una tupla, un conjunto, un diccionario o incluso una cadena de texto.

A diferencia de otros lenguajes, en Python funciona más como un **iterador**, es decir, toma cada elemento de la secuencia uno por uno y ejecuta un bloque de código.

## Ejemplo básico

```python
frutas = ["manzana", "banana", "cereza"]
for fruta in frutas:
    print(fruta)
```

**Cómo funciona:**

- `fruta` toma el valor de cada elemento de la lista `frutas` en cada vuelta del bucle
- No necesitamos definir un índice como en otros lenguajes

## Recorrer una cadena

Incluso un string se puede recorrer, ya que cada letra es un elemento de la secuencia:

```python
for letra in "banana":
    print(letra)
```

## Sentencia break

Detiene el bucle inmediatamente, aunque queden elementos por recorrer.

```python
frutas = ["manzana", "banana", "cereza"]
for fruta in frutas:
    print(fruta)
    if fruta == "banana":
        break
```

## Sentencia continue

Saltea la iteración actual y pasa a la siguiente.

```python
frutas = ["manzana", "banana", "cereza"]
for fruta in frutas:
    if fruta == "banana":
        continue
    print(fruta)
```

## La función range()

Se usa para generar secuencias de números, útil cuando queremos repetir algo un número específico de veces.

### Ejemplo básico:

```python
for i in range(6):
    print(i)
```

Esto imprime del 0 al 5 (el último número no se incluye).

### Especificar inicio:

```python
for i in range(2, 6):
    print(i)
```

Imprime del 2 al 5.

### Especificar incremento:

```python
for i in range(2, 30, 3):
    print(i)
```

Imprime 2, 5, 8, 11… hasta 29, saltando de 3 en 3.

## else en for

El bloque `else` se ejecuta cuando el bucle termina normalmente, pero no si se interrumpe con `break`.

```python
for i in range(6):
    print(i)
else:
    print("¡Bucle terminado!")
```

## Bucles anidados

Un bucle dentro de otro:

```python
adjetivos = ["rojo", "grande", "rico"]
frutas = ["manzana", "banana", "cereza"]

for adj in adjetivos:
    for fruta in frutas:
        print(adj, fruta)
```

Por cada adjetivo, se recorre toda la lista de frutas.

## Sentencia pass

Si por alguna razón necesitamos un `for` vacío, usamos `pass` para que Python no dé error.

```python
for i in [0, 1, 2]:
    pass
```