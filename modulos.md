# Módulos en Python

## ¿Qué es un módulo?

Un **módulo** en Python es como una biblioteca de código.
Es un archivo que contiene un conjunto de funciones, variables u objetos que queremos usar en nuestro programa.

## Crear un módulo

Para crear un módulo solo necesitamos guardar nuestro código en un archivo con extensión `.py`.

### Ejemplo:

Creamos un archivo llamado `mimodulo.py`:

```python
def saludo(nombre):
    print("Hola, " + nombre)
```

## Usar un módulo

Para usar el módulo que creamos, utilizamos la palabra clave `import`.

### Ejemplo:

```python
import mimodulo

mimodulo.saludo("Jonathan")
```

Cuando usamos una función de un módulo, la sintaxis es:
```
nombre_modulo.nombre_función
```

## Variables en un módulo

Un módulo no solo puede contener funciones, también puede tener variables de cualquier tipo: listas, diccionarios, objetos, etc.

### Ejemplo en `mimodulo.py`:

```python
persona1 = {
    "nombre": "Juan",
    "edad": 36,
    "pais": "Noruega"
}
```

### Ejemplo de uso:

```python
import mimodulo

edad = mimodulo.persona1["edad"]
print(edad)
```

## Nombres de módulos

Puedes nombrar tu módulo como quieras, siempre que tenga la extensión `.py`.

También puedes crear un **alias** usando `as` para llamarlo de forma más corta.

### Ejemplo:

```python
import mimodulo as mm

edad = mm.persona1["edad"]
print(edad)
```

## Módulos incorporados (built-in)

Python ya trae varios módulos listos para usar. Por ejemplo, el módulo `platform` nos permite conocer información del sistema operativo:

```python
import platform

sistema = platform.system()
print(sistema)
```

## Usar dir() para explorar un módulo

La función `dir()` nos permite listar todas las funciones y variables de un módulo:

```python
import platform

print(dir(platform))
```

Esto sirve para cualquier módulo, incluso los que tú crees.

## Importar solo parte de un módulo

Si no necesitamos todo el módulo, podemos importar solo lo que necesitamos usando `from ... import ...`.

### Ejemplo en `mimodulo.py`:

```python
def saludo(nombre):
    print("Hola, " + nombre)

persona1 = {
    "nombre": "Juan",
    "edad": 36,
    "pais": "Noruega"
}
```

### Importando solo la variable `persona1`:

```python
from mimodulo import persona1

print(persona1["edad"])
```