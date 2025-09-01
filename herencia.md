[← Back to Index](README.md)

# Herencia en Python

La **herencia** nos permite crear una clase que hereda propiedades y métodos de otra clase.

- **Clase padre** (Parent/Base Class): la clase de la que se hereda
- **Clase hija** (Child/Derived Class): la clase que hereda de otra

## Crear una clase padre

Ejemplo de una clase `Persona` con propiedades y un método:

```python
class Persona:
    def __init__(self, nombre, apellido):
        self.nombre = nombre
        self.apellido = apellido

    def mostrar_nombre(self):
        print(self.nombre, self.apellido)

# Crear un objeto de la clase Persona
p = Persona("Juan", "Pérez")
p.mostrar_nombre()  # Juan Pérez
```

## Crear una clase hija

Para que una clase herede de otra, escribimos el nombre de la clase padre entre paréntesis:

```python
class Estudiante(Persona):
    pass  # No añadimos nada nuevo todavía

e = Estudiante("Ana", "Gómez")
e.mostrar_nombre()  # Ana Gómez
```

La clase `Estudiante` ahora tiene todas las propiedades y métodos de `Persona`.

## Agregar el método __init__() a la clase hija

Si queremos inicializar propiedades adicionales, podemos sobrescribir el `__init__()`:

```python
class Estudiante(Persona):
    def __init__(self, nombre, apellido, anio):
        Persona.__init__(self, nombre, apellido)  # Llamamos al init de la clase padre
        self.anio_graduacion = anio

e = Estudiante("Ana", "Gómez", 2025)
print(e.nombre, e.apellido, e.anio_graduacion)
```

## Usar super() para heredar métodos y propiedades

En lugar de llamar directamente al `__init__()` del padre, podemos usar `super()`:

```python
class Estudiante(Persona):
    def __init__(self, nombre, apellido, anio):
        super().__init__(nombre, apellido)
        self.anio_graduacion = anio
```

## Agregar métodos a la clase hija

Podemos añadir métodos propios a la clase hija:

```python
class Estudiante(Persona):
    def __init__(self, nombre, apellido, anio):
        super().__init__(nombre, apellido)
        self.anio_graduacion = anio

    def bienvenida(self):
        print("Bienvenido", self.nombre, self.apellido, "a la clase del", self.anio_graduacion)

e = Estudiante("Ana", "Gómez", 2025)
e.bienvenida()  # Bienvenido Ana Gómez a la clase del 2025
```