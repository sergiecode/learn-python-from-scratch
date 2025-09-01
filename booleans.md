# Booleanos en Python

Un booleano es un tipo de dato que solo puede tener dos valores:

- **True** (verdadero)
- **False** (falso)

Se usan mucho para decidir si algo es verdadero o falso en el código.

## 1. Valores booleanos con comparaciones

Cuando comparamos valores, Python devuelve `True` o `False`:

```python
print(10 > 9)   # True
print(10 == 9)  # False
print(10 < 9)   # False
```

En un `if`, Python evalúa la condición y ejecuta el bloque correspondiente:

```python
a = 200
b = 33

if b > a:
    print("b es mayor que a")
else:
    print("b no es mayor que a")
```

## 2. Evaluar cualquier valor con bool()

La función `bool()` convierte un valor en `True` o `False`:

```python
print(bool("Hola"))  # True
print(bool(15))      # True

x = "Hola"
y = 15
print(bool(x))  # True
print(bool(y))  # True
```

## 3. Valores que son True

Casi cualquier valor con contenido se evalúa como `True`:

- Cualquier string no vacío → `"abc"`
- Cualquier número distinto de 0 → `123`
- Listas, tuplas, conjuntos y diccionarios no vacíos → `["manzana"]`, `(1,2)`, `{1}`, `{"clave": "valor"}`

```python
bool("abc")                   # True
bool(123)                     # True
bool(["manzana", "banana"])   # True
```

## 4. Valores que son False

Los valores vacíos o especiales se evalúan como `False`:

- `False`
- `None`
- `0`
- Strings vacíos → `""`
- Listas, tuplas, conjuntos y diccionarios vacíos → `[]`, `()`, `{}`, `set()`

```python
bool(False)   # False
bool(None)    # False
bool(0)       # False
bool("")      # False
bool([])      # False
bool({})      # False
```

También un objeto con longitud 0 puede ser `False`:

```python
class MiClase():
    def __len__(self):
        return 0

obj = MiClase()
print(bool(obj))  # False
```

## 5. Funciones que devuelven booleanos

Podemos crear funciones que devuelvan `True` o `False`:

```python
def miFuncion():
    return True

print(miFuncion())  # True
```

Y ejecutar código según el valor devuelto:

```python
if miFuncion():
    print("¡SÍ!")
else:
    print("¡NO!")
```

## 6. Funciones integradas que devuelven booleanos

Python tiene funciones que retornan booleanos, como `isinstance()`, que verifica el tipo de un objeto:

```python
x = 200
print(isinstance(x, int))  # True
```

# Lógica con Booleanos en Python

Los booleanos (`True`/`False`) se pueden combinar con operadores lógicos:

- **and** → verdadero si ambos son `True`
- **or** → verdadero si al menos uno es `True`
- **not** → invierte el valor

## Tablas de verdad

### AND (a and b)

| a     | b     | a and b |
|-------|-------|---------|
| True  | True  | True    |
| True  | False | False   |
| False | True  | False   |
| False | False | False   |

### OR (a or b)

| a     | b     | a or b |
|-------|-------|--------|
| True  | True  | True   |
| True  | False | True   |
| False | True  | True   |
| False | False | False  |

### NOT (not a)

| a     | not a |
|-------|-------|
| True  | False |
| False | True  |

```python
x = True
y = False

print(x and y)  # False
print(x or y)   # True
print(not x)    # False
```

## Ejemplo práctico

**Proposición:** "Si tengo dinero y estoy de vacaciones, entonces iré a la playa"

Definimos las variables:
- `dinero = True` si tengo dinero, `False` si no
- `vacaciones = True` si estoy de vacaciones, `False` si no
- `playa = dinero and vacaciones` → solo voy a la playa si ambas condiciones se cumplen

### Tabla de verdad

| dinero | vacaciones | playa |
|--------|------------|-------|
| True   | True       | True  |
| True   | False      | False |
| False  | True       | False |
| False  | False      | False |

### Ejemplo en Python

```python
dinero = True
vacaciones = False

playa = dinero and vacaciones
print(playa)  # False
```