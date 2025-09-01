[← Volver al índice](README.md)

# Bucles en Python

Python tiene dos tipos básicos de bucles:

- **while loops**
- **for loops**

Aquí nos vamos a enfocar en `while`.

## El bucle while

El bucle `while` ejecuta un conjunto de instrucciones mientras una condición sea verdadera.

### Ejemplo básico

```python
i = 1
while i < 6:
    print(i)
    i += 1
```

**Cómo funciona:**

1. Primero, definimos la variable `i = 1`
2. La condición `i < 6` se evalúa. Mientras sea verdadera, el bloque dentro del `while` se ejecuta
3. `i += 1` incrementa `i` para que el bucle eventualmente termine

> **⚠️ Importante:** Si olvidamos incrementar `i`, el bucle se ejecutaría para siempre (bucle infinito).

## La sentencia break

Con `break` podemos detener el bucle inmediatamente, aunque la condición siga siendo verdadera.

### Ejemplo

```python
i = 1
while i < 6:
    print(i)
    if i == 3:
        break
    i += 1
```

**Qué sucede:**

El bucle se detiene cuando `i` llega a `3`.

## La sentencia continue

Con `continue` podemos saltarnos la iteración actual y pasar a la siguiente.

### Ejemplo

```python
i = 0
while i < 6:
    i += 1
    if i == 3:
        continue
    print(i)
```

**Qué sucede:**

Cuando `i` es `3`, `continue` hace que no se ejecute `print(i)` y pase a la siguiente iteración.

## La cláusula else

Podemos usar `else` para ejecutar un bloque una sola vez cuando la condición del `while` deja de ser verdadera.

### Ejemplo

```python
i = 1
while i < 6:
    print(i)
    i += 1
else:
    print("i ya no es menor que 6")
```

**Qué sucede:**

1. Se imprime cada valor de `i` hasta que la condición deja de cumplirse
2. Después, se ejecuta el bloque dentro del `else`