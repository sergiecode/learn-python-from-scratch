[← Volver al índice](README.md)

# Formateo de texto en Python

En Python, muchas veces necesitamos combinar texto con variables, por ejemplo mostrar un precio o un nombre dentro de un mensaje. Existen varias formas de hacerlo, pero la más moderna y recomendada es usando **f-strings** (a partir de Python 3.6).

## 1. F-strings

Una **f-string** nos permite insertar valores directamente dentro de un texto. Para crearla, simplemente ponemos una `f` antes de las comillas del texto:

```python
txt = f"El precio es 49 dólares"
print(txt)
```

Aquí el texto se muestra tal cual, sin variables aún.

## 2. Placeholders (espacios para variables)

Para mostrar variables dentro del texto, usamos llaves `{}`:

```python
precio = 59
txt = f"El precio es {precio} dólares"
print(txt)
```

Dentro de las llaves puede ir:

- Una variable (`precio`)
- Una operación (`precio * 1.25`)
- Una función (`nombre.upper()`)

## 3. Modificadores (dar formato a los valores)

Si queremos mostrar números con decimales, usamos `:.2f`:

```python
precio = 59
txt = f"El precio es {precio:.2f} dólares"
print(txt)
```

Esto muestra el número con 2 decimales.

También podemos poner directamente un valor:

```python
txt = f"El precio es {95:.2f} dólares"
print(txt)
```

## 4. Operaciones dentro de f-strings

Podemos hacer cálculos directamente:

```python
txt = f"El precio con impuesto es {59 + (59 * 0.25)} dólares"
print(txt)
```

Incluso podemos usar condicionales:

```python
precio = 49
txt = f"Es {'Caro' if precio > 50 else 'Barato'}"
print(txt)
```

## 5. Ejecutar funciones

Podemos llamar funciones dentro de las llaves:

```python
fruta = "manzanas"
txt = f"Me gustan {fruta.upper()}"
print(txt)
```

O nuestras propias funciones:

```python
def convertir_a_metros(pies):
    return pies * 0.3048

txt = f"El avión vuela a {convertir_a_metros(30000)} metros de altura"
print(txt)
```

## 6. Más modificadores

Algunos ejemplos útiles:

```python
precio = 59000
txt = f"El precio es {precio:,} dólares"  # separador de miles
print(txt)
```

Otros formatos incluyen alineación, porcentaje, hexadecimal, etc. (`:<`, `:>`, `:%`, `:x`, etc.)

## 7. Método format() (forma antigua)

Antes de Python 3.6 se usaba `format()`:

```python
precio = 49
txt = "El precio es {} dólares"
print(txt.format(precio))
```

### Se pueden usar múltiples valores:

```python
cantidad = 3
articulo = 567
precio = 49
pedido = "Quiero {} unidades del artículo {} por {:.2f} dólares."
print(pedido.format(cantidad, articulo, precio))
```

### O índices para repetir valores:

```python
edad = 36
nombre = "Juan"
txt = "Su nombre es {1}. {1} tiene {0} años."
print(txt.format(edad, nombre))
```

### O nombres para mayor claridad:

```python
pedido = "Tengo un {auto}, es un {modelo}."
print(pedido.format(auto="Ford", modelo="Mustang"))
```