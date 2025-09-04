[← Volver al índice](README.md)

# ¿Qué es `None` en Python?

`None` es un valor especial en Python que representa la **ausencia de valor** o "nada".

> **Nota:** No significa `0`, ni `False`, ni una cadena vacía (`""`).

## Características principales

- Es de tipo `NoneType`, un tipo de dato único en Python
- Se usa mucho cuando una función no devuelve nada
- Sirve para indicar que una variable todavía no tiene un valor asignado

---

## Ejemplo 1: Variable sin valor

```python
x = None
print(x)        # Muestra: None
print(type(x))  # Muestra: <class 'NoneType'>
```

---

## Ejemplo 2: Función sin `return`

```python
def saludar(nombre):
    print("Hola,", nombre)

resultado = saludar("Ana")  # La función solo imprime
print(resultado)            # Muestra: None
```

> **💡 Tip:** Como la función no tiene `return`, Python devuelve automáticamente `None`.

---

## Ejemplo 3: Uso para indicar "sin valor"

```python
def buscar_usuario(id):
    if id == 1:
        return "Usuario encontrado"
    return None  # Si no hay resultado

print(buscar_usuario(1))  # Usuario encontrado
print(buscar_usuario(5))  # None
```

> **⚠️ Importante:** Aquí `None` sirve para dejar claro que no se encontró nada.