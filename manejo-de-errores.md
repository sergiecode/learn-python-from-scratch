[← Back to Index](README.md)

# Manejo de Errores en Python

## 1. Try y Except

- `try`: sirve para "probar" un bloque de código que podría generar un error
- `except`: sirve para manejar el error si ocurre

### Ejemplo básico:

```python
try:
    print(x)  # x no está definido
except:
    print("Ocurrió un error")
```

Como `x` no está definido, el bloque `try` genera un error, y Python ejecuta el bloque `except`.

Si no usamos `try`, el programa se detendría y mostraría un error:

```python
print(x)  # Esto causará un error
```Python

En Python, los errores se llaman **excepciones**. Cuando ocurre una excepción, normalmente el programa se detiene y muestra un mensaje de error. Para evitar que nuestro programa se caiga, podemos manejar estas excepciones usando `try` y `except`.

1. Try y Except

try: sirve para “probar” un bloque de código que podría generar un error.

except: sirve para manejar el error si ocurre.

Ejemplo básico:

try:
    print(x)  # x no está definido
except:
    print("Ocurrió un error")


Como x no está definido, el bloque try genera un error, y Python ejecuta el bloque except.

Si no usamos try, el programa se detendría y mostraría un error:

print(x)  # Esto causará un error

## 2. Diferentes tipos de excepciones

Podemos definir varios bloques `except` para distintos tipos de errores:

```python
try:
    print(x)
except NameError:
    print("La variable x no está definida")
except:
    print("Ocurrió otro tipo de error")
```

## 3. Else

El bloque `else` se ejecuta cuando no hay errores en el `try`:

```python
try:
    print("Hola")
except:
    print("Ocurrió un error")
else:
    print("Todo salió bien")
```

## 4. Finally

El bloque `finally` se ejecuta siempre, haya ocurrido un error o no. Es útil para cerrar recursos, como archivos o conexiones:

```python
try:
    print(x)
except:
    print("Ocurrió un error")
finally:
    print("El bloque try-except terminó")
```

### Ejemplo con archivo:

```python
try:
    f = open("demofile.txt")
    try:
        f.write("Hola")
    except:
        print("Error al escribir en el archivo")
    finally:
        f.close()  # Se asegura de cerrar el archivo
except:
    print("Error al abrir el archivo")
```

## 5. Lanza tus propias excepciones

Puedes lanzar (`raise`) excepciones cuando ocurra una condición que quieras controlar:

```python
x = -1
if x < 0:
    raise Exception("No se permiten números negativos")
```

También podemos especificar el tipo de error:

```python
x = "hola"
if not type(x) is int:
    raise TypeError("Solo se permiten números enteros")
```

> **💡 Nota:** Este enfoque permite que nuestros programas sean más robustos y controlados, evitando que se detengan inesperadamente.