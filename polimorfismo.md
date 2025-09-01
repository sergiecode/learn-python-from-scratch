[← Volver al índice](README.md)

# Polimorfismo en Python

La palabra **polimorfismo** significa "muchas formas". En programación, se refiere a métodos, funciones u operadores con el mismo nombre que pueden actuar sobre distintos objetos o clases.imorfismo en Python

La palabra polimorfismo significa “muchas formas”. En programación, se refiere a métodos, funciones u operadores con el mismo nombre que pueden actuar sobre distintos objetos o clases.

## 1. Polimorfismo con funciones

Algunas funciones de Python pueden trabajar con distintos tipos de datos. Por ejemplo, la función `len()`:

### Con cadenas de texto (string):

```python
x = "Hola Mundo"
print(len(x))  # Devuelve 10, la cantidad de caracteres
```

### Con tuplas:

```python
mi_tupla = ("manzana", "banana", "cereza")
print(len(mi_tupla))  # Devuelve 3, la cantidad de elementos
```

### Con diccionarios:

```python
mi_diccionario = {"marca": "Ford", "modelo": "Mustang", "año": 1964}
print(len(mi_diccionario))  # Devuelve 3, la cantidad de pares clave-valor
```

Como ves, `len()` se comporta distinto según el tipo de objeto, pero siempre usamos el mismo nombre de función.

## 2. Polimorfismo con clases

El polimorfismo también se usa mucho con métodos de clases. Podemos tener varias clases con un método del mismo nombre que se comporta distinto en cada clase.

### Ejemplo: diferentes vehículos con un método mover()

```python
class Auto:
    def mover(self):
        print("¡Conducir!")

class Barco:
    def mover(self):
        print("¡Navegar!")

class Avion:
    def mover(self):
        print("¡Volar!")

vehiculos = [Auto(), Barco(), Avion()]

for v in vehiculos:
    v.mover()
```

**Salida:**
```
¡Conducir!
¡Navegar!
¡Volar!
```

Aunque usamos el mismo método `mover()`, cada clase lo ejecuta de manera diferente.

## 3. Polimorfismo con herencia

Si tenemos clases que heredan de otra clase, también podemos aplicar polimorfismo. Por ejemplo:

```python
class Vehiculo:
    def __init__(self, marca, modelo):
        self.marca = marca
        self.modelo = modelo

    def mover(self):
        print("¡Mover!")

class Auto(Vehiculo):
    pass

class Barco(Vehiculo):
    def mover(self):
        print("¡Navegar!")

class Avion(Vehiculo):
    def mover(self):
        print("¡Volar!")

vehiculos = [Auto("Ford", "Mustang"), Barco("Ibiza", "Touring 20"), Avion("Boeing", "747")]

for v in vehiculos:
    print(v.marca, v.modelo)
    v.mover()
```

**Salida:**
```
Ford Mustang
¡Mover!
Ibiza Touring 20
¡Navegar!
Boeing 747
¡Volar!
```

La clase `Auto` no redefinió el método `mover()`, así que usa el de la clase padre `Vehiculo`. Las clases `Barco` y `Avion` sobrescriben el método, demostrando polimorfismo.