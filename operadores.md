[← Volver al índice](README.md)

# Operadores en Python

En Python, los operadores se usan para realizar operaciones con variables y valores. Por ejemplo:

```python
print(10 + 5)  # Suma dos números
```

Python divide los operadores en varios grupos:

- **Aritméticos**
- **De asignación**
- **De comparación**
- **Lógicos**
- **De identidad**
- **De pertenencia**
- **Bit a bit (Bitwise)**

## 1. Operadores aritméticos

Se usan para hacer operaciones matemáticas básicas con números:

| Operador | Nombre          | Ejemplo |
|----------|-----------------|---------|
| `+`      | Suma            | `x + y` |
| `-`      | Resta           | `x - y` |
| `*`      | Multiplicación  | `x * y` |
| `/`      | División        | `x / y` |
| `%`      | Módulo          | `x % y` |
| `**`     | Potencia        | `x ** y`|
| `//`     | División entera | `x // y`|

## 2. Operadores de asignación

Se usan para asignar valores a las variables:

| Operador | Ejemplo         | Significado     |
|----------|-----------------|-----------------|
| `=`      | `x = 5`         | Asigna 5 a x    |
| `+=`     | `x += 3`        | `x = x + 3`     |
| `-=`     | `x -= 3`        | `x = x - 3`     |
| `*=`     | `x *= 3`        | `x = x * 3`     |
| `/=`     | `x /= 3`        | `x = x / 3`     |
| `%=`     | `x %= 3`        | `x = x % 3`     |
| `//=`    | `x //= 3`       | `x = x // 3`    |
| `**=`    | `x **= 3`       | `x = x ** 3`    |
| `:=`     | `print(x := 3)` | Asigna 3 a x y lo imprime |
## 3. Operadores de comparación

Se usan para comparar valores:

| Operador | Significado     | Ejemplo  |
|----------|-----------------|----------|
| `==`     | Igual           | `x == y` |
| `!=`     | Distinto        | `x != y` |
| `>`      | Mayor que       | `x > y`  |
| `<`      | Menor que       | `x < y`  |
| `>=`     | Mayor o igual   | `x >= y` |
| `<=`     | Menor o igual   | `x <= y` |

## 4. Operadores lógicos

Se usan para combinar condiciones:

| Operador | Significado                                   | Ejemplo              |
|----------|-----------------------------------------------|----------------------|
| `and`    | Devuelve `True` si ambas condiciones son `True` | `x < 5 and x < 10`   |
| `or`     | Devuelve `True` si alguna condición es `True`   | `x < 5 or x < 4`     |
| `not`    | Invierte el resultado                         | `not(x < 5)`         |

## 5. Operadores de identidad

Se usan para comprobar si dos variables son el mismo objeto en memoria:

| Operador | Significado                           | Ejemplo      |
|----------|---------------------------------------|--------------|
| `is`     | `True` si son el mismo objeto         | `x is y`     |
| `is not` | `True` si NO son el mismo objeto      | `x is not y` |

## 6. Operadores de pertenencia

Se usan para verificar si un valor está en una secuencia:

| Operador | Significado                    | Ejemplo      |
|----------|--------------------------------|--------------|
| `in`     | `True` si está presente        | `x in y`     |
| `not in` | `True` si NO está presente     | `x not in y` |
## 7. Operadores bit a bit (Bitwise)

Se usan para trabajar con los bits de los números:

| Operador | Nombre             | Descripción                           |
|----------|--------------------|---------------------------------------|
| `&`      | AND                | Cada bit es 1 si ambos bits son 1    |
| `\|`     | OR                 | Cada bit es 1 si algún bit es 1      |
| `^`      | XOR                | Cada bit es 1 si solo uno de los bits es 1 |
| `~`      | NOT                | Invierte todos los bits               |
| `<<`     | Desplazamiento izq | Desplaza bits a la izquierda         |
| `>>`     | Desplazamiento der | Desplaza bits a la derecha           |

## Precedencia de operadores

Al combinar operadores, Python sigue un orden:

1. **Paréntesis** `()`
2. **Exponente** `**`
3. **Multiplicación, división** `*` `/` `//` `%`
4. **Suma y resta** `+` `-`
5. **Comparaciones, identidad, pertenencia** `==` `!=` `>` `<` `>=` `<=` `is` `in` `not in`
6. **Lógicos** `not`, `and`, `or`

> **Nota:** Si dos operadores tienen la misma precedencia, se evalúan de izquierda a derecha.

### Ejemplos:

```python
print(5 + 4 - 7 + 3)  # Se evalúa de izquierda a derecha
print(100 + 5 * 3)    # Multiplicación antes que suma
```