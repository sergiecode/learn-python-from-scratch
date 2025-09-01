# Condicionales en Python: if, elif y else

En Python, las condicionales se usan para tomar decisiones en tu código según ciertas condiciones.

## Operadores de Comparación

Las condiciones más comunes son:

- **Igual a:** `a == b`
- **Distinto de:** `a != b`
- **Menor que:** `a < b`
- **Menor o igual que:** `a <= b`
- **Mayor que:** `a > b`
- **Mayor o igual que:** `a >= b`

Estas condiciones se usan principalmente con **if statements** (sentencias if) y bucles.

## 1. if

La sentencia `if` ejecuta un bloque de código solo si la condición es verdadera.

```python
a = 33
b = 200

if b > a:
    print("b es mayor que a")
```

**Explicación:**
Como `b` es 200 y `a` es 33, la condición `b > a` es verdadera, entonces Python imprime:

```
b es mayor que a
```

> **Importante:** Python usa indentación (espacios al inicio de la línea) para definir qué código pertenece al `if`. Sin la indentación, se produce un error.

## 2. elif

`elif` significa "else if" y se usa para probar otra condición si la anterior no fue verdadera.

```python
a = 33
b = 33

if b > a:
    print("b es mayor que a")
elif a == b:
    print("a y b son iguales")
```

Aquí, la primera condición `b > a` es falsa, pero `a == b` es verdadera, así que imprime:

```
a y b son iguales
```

## 3. else

`else` captura todo lo que no cumple las condiciones anteriores.

```python
a = 200
b = 33

if b > a:
    print("b es mayor que a")
elif a == b:
    print("a y b son iguales")
else:
    print("a es mayor que b")
```

Como ninguna de las condiciones anteriores es verdadera, se ejecuta `else` y Python imprime:

```
a es mayor que b
```

También puedes usar `else` sin `elif`:

```python
if b > a:
    print("b es mayor que a")
else:
    print("b no es mayor que a")
```

## 4. Forma corta de if y if ... else

Si solo hay una línea de código, puedes escribirlo en la misma línea:

```python
if a > b: print("a es mayor que b")
```

Para un `if ... else` en una sola línea:

```python
a = 2
b = 330

print("A") if a > b else print("B")
```

También se pueden encadenar varias condiciones:

```python
a = 330
b = 330

print("A") if a > b else print("=") if a == b else print("B")
```

## 5. Operadores lógicos: and, or, not

### and
Todas las condiciones deben ser verdaderas:

```python
a = 200
b = 33
c = 500

if a > b and c > a:
    print("Ambas condiciones son verdaderas")
```

### or
Basta que una condición sea verdadera:

```python
if a > b or a > c:
    print("Al menos una condición es verdadera")
```

### not
Invierte la condición:

```python
a = 33
b = 200

if not a > b:
    print("a NO es mayor que b")
```

## 6. if anidados

Puedes poner un `if` dentro de otro `if`:

```python
x = 41

if x > 10:
    print("Mayor que diez,")
    if x > 20:
        print("y también mayor que 20!")
    else:
        print("pero no mayor que 20.")
```

## 7. pass

Si necesitas un `if` vacío, puedes usar `pass` para evitar errores:

```python
a = 33
b = 200

if b > a:
    pass
```

`pass` no hace nada, pero permite que tu código siga funcionando.