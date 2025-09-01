[← Volver al índice](README.md)

# Listas en Python

## ¿Qué es una lista?

Una lista en Python es una colección de elementos que se guardan en una sola variable.

**Ejemplo:**

```python
mylist = ["manzana", "banana", "cereza"]
print(mylist)
```

Las listas son **ordenadas**, **modificables** y **permiten valores duplicados**.

Python tiene otras colecciones: tuplas, conjuntos y diccionarios, cada una con características distintas.

## Características de las listas

### Ordenadas
Los elementos tienen un orden definido, y ese orden no cambia automáticamente.

- Se pueden agregar elementos al final
- Algunas funciones pueden cambiar el orden, pero en general se mantiene

### Modificables
Puedes cambiar, agregar o eliminar elementos después de crear la lista.

### Permiten duplicados
Una lista puede contener elementos repetidos.

```python
thislist = ["manzana", "banana", "cereza", "manzana", "cereza"]
print(thislist)
```

### Longitud de la lista
Para saber cuántos elementos tiene una lista, usamos `len()`:

```python
thislist = ["manzana", "banana", "cereza"]
print(len(thislist))  # Salida: 3
```

### Tipos de datos
Una lista puede contener cualquier tipo de dato y combinarlos:

```python
list1 = ["abc", 34, True, 40, "masculino"]
```

### Constructor de listas
También se puede crear una lista usando `list()`:

```python
thislist = list(("manzana", "banana", "cereza"))
print(thislist)
```

## Acceder a los elementos

### Por índice (comienza en 0)

```python
thislist = ["manzana", "banana", "cereza"]
print(thislist[1])  # Salida: banana
```

### Índices negativos (empezando desde el final)

```python
print(thislist[-1])  # Salida: cereza
```

### Rangos de índices

```python
thislist = ["manzana", "banana", "cereza", "naranja", "kiwi"]
print(thislist[2:4])  # Salida: ['cereza', 'naranja']
print(thislist[:3])   # Desde el inicio hasta el índice 2
print(thislist[2:])   # Desde el índice 2 hasta el final
```

### Verificar si un elemento existe

```python
if "manzana" in thislist:
    print("Sí, 'manzana' está en la lista")
```

## Modificar listas

### Cambiar un elemento

```python
thislist[1] = "grosella"
```

### Cambiar un rango de elementos

```python
thislist[1:3] = ["grosella", "sandía"]
```

### Insertar un elemento sin reemplazar

```python
thislist.insert(2, "sandía")  # Inserta en la posición 2
```

### Agregar al final

```python
thislist.append("naranja")
```

### Agregar elementos de otra lista

```python
tropical = ["mango", "piña"]
thislist.extend(tropical)
```

## Eliminar elementos

### Por valor

```python
thislist.remove("banana")
```

### Por índice

```python
thislist.pop(1)  # Elimina el elemento en el índice 1
del thislist[0]  # Elimina el primer elemento
```

### Vaciar la lista

```python
thislist.clear()
```

### Eliminar la lista completa

```python
del thislist
```

## Recorrer listas

### For loop

```python
for x in thislist:
    print(x)
```

### Por índice

```python
for i in range(len(thislist)):
    print(thislist[i])
```

### While loop

```python
i = 0
while i < len(thislist):
    print(thislist[i])
    i += 1
```

### List comprehension (forma corta)

```python
[print(x) for x in thislist]
```

## List comprehension avanzada

### Crear una nueva lista filtrando elementos

```python
frutas = ["manzana", "banana", "cereza", "kiwi", "mango"]
nuevalista = [x for x in frutas if "a" in x]
print(nuevalista)
```

### Sintaxis general

```python
nuevalista = [expresion for item in iterable if condicion]
```

### Se puede manipular el resultado

```python
nuevalista = [x.upper() for x in frutas]
```

## Ordenar listas

### Ascendente

```python
thislist.sort()
```

### Descendente

```python
thislist.sort(reverse=True)
```

### Orden personalizado

```python
def cerca_de_50(n):
    return abs(n - 50)

numeros = [100, 50, 65, 82, 23]
numeros.sort(key=cerca_de_50)
```

### Invertir lista

```python
thislist.reverse()
```

## Copiar listas

```python
mylist = thislist.copy()
mylist = list(thislist)
mylist = thislist[:]
```

## Unir listas

### Con `+`

```python
lista3 = lista1 + lista2
```

### Con append en bucle

```python
for x in lista2:
    lista1.append(x)
```

### Con extend

```python
lista1.extend(lista2)
```