[← Volver al índice](README.md)

# Diccionarios en Python

## ¿Qué es un diccionario?```

> **Nota:** Las listas devueltas son "vistas", es decir, si cambias el diccionario, estas listas se actualizan automáticamente.Un diccionario es una colección de elementos que almacena pares **clave:valor**.

- Cada valor se accede mediante su clave, no mediante un índice
- Está **ordenado** (a partir de Python 3.7)
- Es **mutable**, es decir, se puede cambiar, agregar o eliminar elementos
- **No permite claves duplicadas**; si hay duplicados, la última clave sobrescribe la anterior

Se escribe con llaves `{}`:

```python
auto = {
  "marca": "Ford",
  "modelo": "Mustang",
  "año": 1964
}
print(auto)
```

## Acceder a los valores

Puedes acceder a los valores usando la clave:

```python
print(auto["marca"])  # Ford
```

También se puede usar `get()`:

```python
print(auto.get("modelo"))  # Mustang
```

## Obtener claves, valores o ítems

### Claves: `keys()`

```python
print(auto.keys())
```

### Valores: `values()`

```python
print(auto.values())
```

### Pares clave:valor: `items()`

```python
print(auto.items())
```  


Las listas devueltas son “vistas”, es decir, si cambias el diccionario, estas listas se actualizan automáticamente.

## Verificar si una clave existe

```python
if "modelo" in auto:
    print("Sí, 'modelo' es una clave del diccionario")
```

## Modificar valores

```python
auto["año"] = 2020  # Cambia el año
auto.update({"modelo": "Fiesta"})  # También se puede usar update()
```

## Agregar elementos

```python
auto["color"] = "rojo"  
auto.update({"puertas": 4})  # También con update()
```

## Eliminar elementos

- **`pop(clave)`**: elimina un elemento por su clave
- **`popitem()`**: elimina el último elemento agregado
- **`del diccionario["clave"]`**: elimina un elemento por clave
- **`clear()`**: vacía el diccionario
- **`del diccionario`**: elimina el diccionario completo

```python
auto.pop("modelo")
auto.popitem()
del auto["año"]
auto.clear()
del auto
```

## Recorrer un diccionario

### Solo claves

```python
for k in auto:
    print(k)
```

### Solo valores

```python
for v in auto.values():
    print(v)
```

### Claves y valores

```python
for k, v in auto.items():
    print(k, v)
```

## Copiar diccionarios

### Usando `copy()`

```python
nuevo_auto = auto.copy()
```

### Usando `dict()`

```python
nuevo_auto = dict(auto)
```

## Diccionarios anidados

Un diccionario puede contener otros diccionarios:

```python
familia = {
  "hijo1": {"nombre": "Emil", "año": 2004},
  "hijo2": {"nombre": "Tobias", "año": 2007},
  "hijo3": {"nombre": "Linus", "año": 2011}
}

print(familia["hijo2"]["nombre"])  # Tobias
```

## Recorrer diccionarios anidados

```python
for clave, subdict in familia.items():
    print(clave)
    for k, v in subdict.items():
        print(k + ':', v)
```