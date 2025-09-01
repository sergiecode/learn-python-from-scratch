# Clases y Objetos en Python

Python es un lenguaje orientado a objetos. Esto significa que casi todo en Python es un **objeto** con sus **propiedades** (variables) y **métodos** (funciones).

Una **clase** es como un molde o un plano para crear objetos.

## Crear una clase

Para crear una clase, usamos la palabra clave `class`:

```python
class MiClase:
    x = 5
```

Aquí creamos una clase llamada `MiClase` con una propiedad `x`.

## Crear un objeto

Para usar la clase y crear un objeto:

```python
p1 = MiClase()
print(p1.x)  # Imprime 5
```

`p1` es un **objeto** de la clase `MiClase`.

## El método __init__()

El ejemplo anterior es muy básico. En la vida real, necesitamos inicializar valores cuando se crea un objeto. Para eso usamos el método especial `__init__()`.

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

p1 = Persona("Juan", 36)
print(p1.nombre)  # Juan
print(p1.edad)    # 36
```

`__init__()` se llama automáticamente al crear un objeto. Sirve para asignar propiedades iniciales.

## El método __str__()

El método `__str__()` controla cómo se muestra un objeto como texto:

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
    
    def __str__(self):
        return f"{self.nombre} ({self.edad})"

p1 = Persona("Juan", 36)
print(p1)  # Juan (36)
```

Si no se define `__str__()`, Python muestra algo como `<__main__.Persona object at 0x...>`.

## Crear métodos

Los **métodos** son funciones dentro de una clase que actúan sobre los objetos:

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
    
    def saludar(self):
        print("Hola, mi nombre es " + self.nombre)

p1 = Persona("Juan", 36)
p1.saludar()  # Hola, mi nombre es Juan
```

## El parámetro self

`self` hace referencia al propio objeto.

Siempre debe ser el primer parámetro de los métodos, aunque puede llamarse de otra forma:

```python
class Persona:
    def __init__(miobj, nombre, edad):
        miobj.nombre = nombre
        miobj.edad = edad

    def saludar(x):
        print("Hola, mi nombre es " + x.nombre)

p1 = Persona("Juan", 36)
p1.saludar()
```

## Modificar propiedades

```python
p1.edad = 40  # Cambiar edad
```

## Eliminar propiedades y objetos

```python
del p1.edad   # Eliminar propiedad
del p1        # Eliminar objeto completo
```

## La instrucción pass

Si una clase no tiene contenido, usamos `pass` para evitar errores:

```python
class Persona:
    pass
```