[← Volver al índice](README.md)

# ¿Qué es el operador walrus (`:=`)?

El **operador walrus** se introdujo en Python 3.8 y recibe su nombre porque `:=` parece la carita de una morsa 🦭.

> **Función principal:** Permite asignar un valor a una variable dentro de una expresión (por ejemplo, dentro de un `if`, `while` o una comprensión de listas).

## Características principales

- **Asigna y evalúa** al mismo tiempo
- **Ahorra código repetido** y hace el código más compacto
- **Mejora la legibilidad** cuando se usa correctamente

---

## Ejemplo 1: Uso básico

```python
if (n := 5) > 3:
    print("El número es", n)
```

> **💡 Explicación:** Aquí se asigna `5` a `n` y al mismo tiempo se evalúa si es mayor que `3`.

---

## Ejemplo 2: En un bucle `while`

```python
# Leer input hasta que el usuario escriba "salir"
while (texto := input("Escribí algo: ")) != "salir":
    print("Ingresaste:", texto)
```

> **🔄 Ventaja:** El operador walrus permite leer y comprobar en la misma línea.

---

## Ejemplo 3: Evitando repetir código

### ❌ Sin walrus (código repetitivo):

```python
datos = input("Ingresá tu nombre: ")
if len(datos) > 3:
    print("Nombre válido:", datos)
```

### ✅ Con walrus (más eficiente):

```python
if (datos := input("Ingresá tu nombre: ")) and len(datos) > 3:
    print("Nombre válido:", datos)
```

---

## ¿Cuándo usarlo?

### ✅ **Recomendado cuando:**
- Querés evitar escribir dos veces la misma expresión
- Necesitás hacer el código más compacto sin perder claridad

### ⚠️ **Usar con moderación:**
- Puede confundir a desarrolladores principiantes
- No abuses de él para mantener la legibilidad del código