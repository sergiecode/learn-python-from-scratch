[← Volver al índice](README.md)

# Condicional match en Python

El `match` es una nueva característica de Python (desde la versión 3.10).

## 3. Valor por defecto

Si que (incompleto)

## 4. Combinar valores en un case

Podés usar el símbolo `|` para decir "o" y agrupar varios valores en un solo bloque:

```python
day = 4

match day:
    case 1 | 2 | 3 | 4 | 5:
        print("Hoy es un día laboral")
    case 6 | 7:
        print("Me encantan los fines de semana")
```

Aquí, cualquier día de semana (1 a 5) ejecuta el primer bloque.que se ejecute cuando ningún `case` coincida, se usa el guion bajo `_`:

```python
day = 4

match day:
    case 6:
        print("Hoy es sábado")
    case 7:
        print("Hoy es domingo")
    case _:
        print("Esperando el fin de semana")
```

> **Nota:** `_` siempre coincide, así que debe ir al final para funcionar como "default".utar diferentes bloques de código según el valor de una expresión, sin tener que escribir muchos `if ... elif ... else`.

Se parece al `switch` de otros lenguajes.

## 1. Sintaxis básica

```python
match expresión:
    case valor1:
        # código si expresión == valor1
    case valor2:
        # código si expresión == valor2
    case valor3:
        # código si expresión == valor3
```

**Cómo funciona:**

- Se evalúa la expresión una sola vez
- Se compara con cada `case`
- Si encuentra coincidencia, ejecuta el bloque de código correspondiente

## 2. Ejemplo práctico: días de la semana

```python
day = 4

match day:
    case 1:
        print("Lunes")
    case 2:
        print("Martes")
    case 3:
        print("Miércoles")
    case 4:
        print("Jueves")
    case 5:
        print("Viernes")
    case 6:
        print("Sábado")
    case 7:
        print("Domingo")
```

Como `day` es `4`, se imprime: **Jueves**.

3. Valor por defecto

Si querés un bloque que se ejecute cuando ningún case coincida, se usa el guion bajo _:

day = 4

match day:
    case 6:
        print("Hoy es sábado")
    case 7:
        print("Hoy es domingo")
    case _:
        print("Esperando el fin de semana")


_ siempre coincide, así que debe ir al final para funcionar como “default”.

4. Combinar valores en un case

Podés usar el símbolo | para decir “o” y agrupar varios valores en un solo bloque:

day = 4

match day:
    case 1 | 2 | 3 | 4 | 5:
        print("Hoy es un día laboral")
    case 6 | 7:
        print("Me encantan los fines de semana")


Aquí, cualquier día de semana (1 a 5) ejecuta el primer bloque.

## 5. Condiciones adicionales (guards)

Podés agregar `if` dentro de un `case` para hacer un chequeo extra:

```python
month = 5
day = 4

match day:
    case 1 | 2 | 3 | 4 | 5 if month == 4:
        print("Un día laboral de abril")
    case 1 | 2 | 3 | 4 | 5 if month == 5:
        print("Un día laboral de mayo")
    case _:
        print("No coincide")
```

Esto permite condicionar el bloque no solo al valor de `day`, sino también a otra variable (`month`).