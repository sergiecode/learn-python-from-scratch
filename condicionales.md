[← Back to Index](README.md)

# Condicionales en Python: if, elif, else

`elif` significa "else if" y se usa para probar otra condición si la primera no se cumple:

```python
a = 33
b = 33

if b > a:
    print("b es mayor que a")
elif a == b:
    print("a y b son iguales")
```

Como `a` y `b` son iguales, la primera condición no se cumple, pero la segunda sí. Resultado:
```
a y b son iguales
```
En Python, los condicionales nos permiten ejecutar código solo si se cumple cierta condición. Las condiciones usan operadores lógicos que ya conocés de matemáticas:

- **Igual a**: `a == b`
- **Distinto de**: `a != b`
- **Menor que**: `a < b`
- **Menor o igual que**: `a <= b`
- **Mayor que**: `a > b`
- **Mayor o igual que**: `a >= b`

## 1. if – si

El condicional `if` se usa para decir: "Si se cumple esta condición, ejecuta esto".

```python
a = 33
b = 200

if b > a:
    print("b es mayor que a")
```

Como `b` es 200 y `a` es 33, la condición es verdadera, así que se imprime:
```
b es mayor que a
```

> ⚠️ **Importante**: Python usa indentación (espacios al inicio de la línea) para definir qué código pertenece al `if`. Sin indentación, dará error.

2. elif – si no, entonces

elif significa “else if” y se usa para probar otra condición si la primera no se cumple:

a = 33
b = 33

if b > a:
    print("b es mayor que a")
elif a == b:
    print("a y b son iguales")


Como a y b son iguales, la primera condición no se cumple, pero la segunda sí. Resultado:
a y b son iguales

## 3. else – si ninguna condición se cumple

`else` captura todo lo que no cumpla las condiciones anteriores:

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

Aquí ninguna de las condiciones `if` o `elif` se cumple, así que se ejecuta el `else`.

También se puede usar solo `if ... else` si no necesitamos `elif`:

```python
if b > a:
    print("b es mayor que a")
else:
    print("b no es mayor que a")
```

## 4. Forma corta: if en una línea

Si tenés solo una instrucción, podés ponerla en la misma línea:

```python
if a > b: print("a es mayor que b")
```

Y con `if ... else`:

```python
a = 2
b = 330
print("A") if a > b else print("B")
```

Esto se llama **operador ternario** o **expresión condicional**.

Incluso podés anidar varias condiciones en una sola línea:

```python
a = 330
b = 330
print("A") if a > b else print("=") if a == b else print("B")
```

## 5. Operadores lógicos

- **`and`** → y (todas las condiciones deben ser verdaderas)
- **`or`** → o (al menos una condición debe ser verdadera)  
- **`not`** → no (invierte el valor de la condición)

```python
a = 200
b = 33
c = 500

if a > b and c > a:
    print("Ambas condiciones son verdaderas")

if a > b or a > c:
    print("Al menos una condición es verdadera")

if not a > b:
    print("a NO es mayor que b")
```

## 6. if anidado (nested if)

Podés poner un `if` dentro de otro:

```python
x = 41

if x > 10:
    print("Mayor que 10")
    if x > 20:
        print("Y también mayor que 20")
    else:
        print("Pero no mayor que 20")
```

## 7. pass – para dejar un if vacío

Si querés dejar un `if` sin instrucciones por ahora, usá `pass` para evitar errores:

```python
a = 33
b = 200

if b > a:
    pass  # aquí no hacemos nada
```