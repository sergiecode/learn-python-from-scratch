[← Back to Index](README.md)

# Conjuntos en Python

## ¿Qué es un conjunto?

Un conjunto o set es una colección de elementos que:

- **No tiene orden** (no se puede acceder a los elementos por índice)
- **Es inmutable en sus elementos** (no puedes cambiar los elementos existentes, pero sí agregar o eliminar)
- **No permite valores duplicados**

Se escribe usando llaves `{}`:

```python
frutas = {"manzana", "banana", "cereza"}
print(frutas)
```

> **Nota:** Los elementos pueden aparecer en cualquier orden cada vez que los imprimas.

## Características principales

### No ordenados
No puedes usar índices para acceder a los elementos.

### Inmutables (parcialmente)
No se pueden cambiar los elementos existentes, pero puedes agregar o eliminar elementos.

### Sin duplicados
Si agregas un elemento que ya existe, Python lo ignorará.

```python
frutas = {"manzana", "banana", "cereza", "manzana"}
print(frutas)  # {'banana', 'cereza', 'manzana'}
```

## Longitud de un conjunto

Usamos `len()` para saber cuántos elementos tiene:

```python
frutas = {"manzana", "banana", "cereza"}
print(len(frutas))  # 3
```

## Tipos de datos

Los conjuntos pueden contener cualquier tipo de dato:

```python
set1 = {"abc", 34, True, 40, "masculino"}
```

## Constructor set()

También se puede crear un conjunto con `set()`:

```python
frutas = set(("manzana", "banana", "cereza"))
print(frutas)
```

## Acceder a elementos

No puedes usar índices, pero puedes:

### Recorrer el conjunto con un for

```python
frutas = {"manzana", "banana", "cereza"}
for f in frutas:
    print(f)
```

### Verificar si un elemento existe con in

```python
print("banana" in frutas)    # True
print("pera" not in frutas)  # True
```

## Modificar conjuntos

### Agregar elementos

#### Un elemento: `add()`

```python
frutas.add("naranja")
```

#### Varios elementos: `update()`

```python
tropical = {"piña", "mango"}
frutas.update(tropical)
```

> **Nota:** `update()` también acepta listas, tuplas o diccionarios.

### Eliminar elementos

- **`remove()`**: elimina el elemento, genera error si no existe
- **`discard()`**: elimina el elemento, no genera error si no existe
- **`pop()`**: elimina un elemento aleatorio y lo devuelve
- **`clear()`**: vacía el conjunto
- **`del`**: elimina el conjunto completo

```python
frutas.remove("banana")
frutas.discard("pera")
x = frutas.pop()
frutas.clear()
del frutas
```

## Operaciones entre conjuntos

### Unión

Todos los elementos de ambos conjuntos:

```python
set1 = {"a", "b"}
set2 = {1, 2}
set3 = set1.union(set2)
# o set3 = set1 | set2
```

### Intersección

Solo los elementos que están en ambos:

```python
set1 = {"manzana", "banana"}
set2 = {"banana", "pera"}
set3 = set1.intersection(set2)
# o set3 = set1 & set2
```

### Diferencia

Elementos que están en el primero pero no en el segundo:

```python
set3 = set1.difference(set2)
# o set3 = set1 - set2
```

### Diferencia simétrica

Elementos que no están en ambos:

```python
set3 = set1.symmetric_difference(set2)
# o set3 = set1 ^ set2
```

> **Nota:** Las versiones `_update()` (como `intersection_update()`) modifican el conjunto original en lugar de crear uno nuevo.