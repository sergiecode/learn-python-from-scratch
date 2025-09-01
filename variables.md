# Variables en Python

## 🔹 ¿Qué es una variable?

Una variable es como una caja donde guardamos un valor para poder usarlo después en el programa.

```python
x = 5
y = "Juan"
print(x)
print(y)
```

## 🔹 Crear variables

En Python no hace falta declararlas antes: se crean cuando les damos un valor.

Una variable puede cambiar de tipo:

```python
x = 4       # x es un número entero (int)
x = "Hola"  # ahora x es un texto (str)
print(x)
```

## 🔹 Tipos de datos y conversión (casting)

Podemos indicar el tipo de una variable usando funciones como `str()`, `int()` o `float()`.

```python
x = str(3)    # '3' (texto)
y = int(3)    # 3  (entero)
z = float(3)  # 3.0 (decimal)
```

## 🔹 Saber el tipo de una variable

Con la función `type()` podemos comprobar de qué tipo es:

```python
x = 5
y = "Juan"
print(type(x))  # int
print(type(y))  # str
```

## 🔹 Comillas simples o dobles

Para textos (strings) se pueden usar comillas simples o dobles, ambas funcionan igual:

```python
x = "Juan"
y = 'Pedro'
```

## 🔹 Variables sensibles a mayúsculas

Python distingue entre mayúsculas y minúsculas:

```python
a = 4
A = "Sally"
print(a)  # 4
print(A)  # Sally
```

## 🔹 Reglas para nombres de variables

### ✅ Nombres válidos:

```python
myvar = "Juan"
my_var = "Juan"
_my_var = "Juan"
myVar = "Juan"
MYVAR = "Juan"
myvar2 = "Juan"
```

### ❌ Nombres inválidos:

```python
2myvar = "Juan"    # No puede empezar con número
my-var = "Juan"    # No puede tener guiones
my var = "Juan"    # No puede tener espacios
```

## 🔹 Estilos para nombres largos

- **camelCase**: `myVariableName`
- **PascalCase**: `MyVariableName`
- **snake_case**: `my_variable_name` (el más usado en Python ✅)

## 🔹 Asignación múltiple

### Varios valores en varias variables

Podemos asignar varios valores en una sola línea:

```python
x, y, z = "Naranja", "Banana", "Cereza"
print(x, y, z)
```

### Un valor en varias variables

```python
x = y = z = "Naranja"
print(x, y, z)
```

### Desempaquetar colecciones (unpacking)

Si tenemos una lista, podemos asignar cada valor a una variable:

```python
frutas = ["Manzana", "Banana", "Cereza"]
x, y, z = frutas
print(x, y, z)
```

## 🔹 Mostrar variables con print()

### Concatenar strings
```python
x = "Python"
y = "es"
z = "genial"

print(x, y, z)        # Python es genial
print(x + " " + y)    # Python es
```

### Operaciones con números
Con números, el `+` funciona como suma:

```python
a = 5
b = 10
print(a + b)   # 15
```

## 🔹 Variables globales y locales

Una **variable global** se crea fuera de una función y se puede usar en cualquier parte.

Una **variable local** se crea dentro de una función y solo existe ahí.

### Ejemplo básico
```python
x = "genial"  # global

def mi_funcion():
    x = "fantástico"  # local
    print("Python es " + x)

mi_funcion()
print("Python es " + x)
```

### Modificar variable global dentro de una función
Para modificar una variable global dentro de una función se usa la palabra `global`:

```python
def mi_funcion():
    global x
    x = "fantástico"

mi_funcion()
print("Python es " + x)
```