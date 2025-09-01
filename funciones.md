# Funciones en Python

Una **función** es un bloque de código que solo se ejecuta cuando la llamamos. Las funciones nos permiten organizar mejor el código, reutilizarlo y trabajar con datos de manera más flexible.

## Crear una función

En Python, se define una función usando la palabra clave `def`:

```python
def mi_funcion():
    print("Hola desde una función")
```

Para ejecutar la función, la llamamos por su nombre seguido de paréntesis:

```python
mi_funcion()
```

**Salida:**
```
Hola desde una función
```

## Argumentos y parámetros

Podemos enviar información a una función usando **argumentos** (a veces llamados args). Los **parámetros** son las variables que definimos en la función para recibir esos argumentos.

```python
def saludar(nombre):
    print(nombre + " Refsnes")

saludar("Emil")
saludar("Tobias")
```

**Salida:**
```
Emil Refsnes
Tobias Refsnes
```

## Número de argumentos

Si la función espera cierta cantidad de argumentos, debemos dárselos exactamente:

```python
def nombre_completo(nombre, apellido):
    print(nombre + " " + apellido)

nombre_completo("Emil", "Refsnes")  # Correcto
```

> **⚠️ Importante:** Si faltan o sobran argumentos, Python dará un error.

## Argumentos arbitrarios (*args)

Si no sabemos cuántos argumentos vamos a recibir, usamos un `*` antes del nombre del parámetro. Esto crea una tupla con todos los argumentos:

```python
def hijos(*nombres):
    print("El hijo más joven es " + nombres[2])

hijos("Emil", "Tobias", "Linus")
```

## Argumentos con palabras clave (Keyword Arguments)

Podemos pasar los argumentos usando `nombre=valor`, sin importar el orden:

```python
def hijos(child3, child2, child1):
    print("El hijo más joven es " + child3)

hijos(child1="Emil", child2="Tobias", child3="Linus")
```

Si no sabemos cuántos argumentos con palabras clave tendremos, usamos `**` (esto crea un diccionario):

```python
def apellido(**datos):
    print("Su apellido es " + datos["apellido"])

apellido(nombre="Tobias", apellido="Refsnes")
```

## Valores por defecto

Podemos asignar valores por defecto a los parámetros, que se usan si no se pasa ningún argumento:

```python
def pais_origen(pais="Noruega"):
    print("Soy de " + pais)

pais_origen("Suecia")
pais_origen()
```

## Pasar listas

Podemos pasar listas u otros tipos de datos a funciones:

```python
def imprimir_lista(lista):
    for item in lista:
        print(item)

frutas = ["manzana", "banana", "cereza"]
imprimir_lista(frutas)
```

## Retornar valores

Si queremos que una función devuelva un resultado, usamos `return`:

```python
def multiplicar(x):
    return 5 * x

print(multiplicar(3))
print(multiplicar(5))
```

## Funciones vacías

Si queremos definir una función pero aún no escribir su contenido, usamos `pass` para evitar errores:

```python
def funcion_vacia():
    pass
```

## Argumentos solo posicionales y solo con palabra clave

### Posicionales

El argumento debe pasarse en orden:

```python
def suma(x, /):
    print(x)

suma(3)  # Correcto
```

### Solo palabra clave

El argumento debe pasarse con `nombre=valor`:

```python
def suma(*, x):
    print(x)

suma(x=3)  # Correcto
```

### Combinando ambos tipos

También se pueden combinar los dos tipos:

```python
def combinada(a, b, /, *, c, d):
    print(a + b + c + d)

combinada(5, 6, c=7, d=8)
```

## Recursión

Python permite que una función se llame a sí misma, esto se llama **recursión**:

```python
def suma_recursiva(k):
    if k > 0:
        resultado = k + suma_recursiva(k - 1)
        print(resultado)
    else:
        resultado = 0
    return resultado

print("Resultado recursivo:")
suma_recursiva(6)
```

> **💡 Nota:** La recursión permite resolver problemas matemáticos y de programación de forma elegante, pero hay que usarla con cuidado para no generar bucles infinitos.