# Strings en Python

Un string es una secuencia de caracteres, es decir, texto. En Python se pueden definir con comillas simples `'...'` o comillas dobles `"..."`:

```python
print("Hola")
print('Hola')
```

## Comillas dentro de un string

Puedes usar comillas dentro del texto, siempre que no sean iguales a las que rodean el string:

```python
print("It's alright")
print("Se llama 'Johnny'")
print('Se llama "Johnny"')
```

## Asignar strings a variables

```python
a = "Hola"
print(a)
```

## Strings multilínea

Puedes crear strings que ocupen varias líneas usando tres comillas:

```python
a = """Esto es un
texto que ocupa
varias líneas"""
print(a)
```

O con tres comillas simples:

```python
a = '''Esto es otro
texto multilínea'''
print(a)
```

## Strings como arrays

Los strings son arrays de caracteres, cada letra tiene un índice comenzando en 0:

```python
a = "Hola, Mundo!"
print(a[1])  # "o"
```

Se puede recorrer cada carácter con un `for`:

```python
for letra in "banana":
    print(letra)
```

## Longitud de un string

Para obtener la longitud se usa `len()`:

```python
a = "Hola, Mundo!"
print(len(a))  # 12
```

## Comprobar contenido

Usamos `in` para saber si un texto está en el string:

```python
txt = "Las mejores cosas de la vida son gratis!"
print("gratis" in txt)  # True

if "gratis" in txt:
    print("Sí, 'gratis' está presente")
```

Para verificar que NO esté, usamos `not in`:

```python
if "caro" not in txt:
    print("No, 'caro' NO está presente")
```

## Slicing (substrings)

Podemos obtener partes del string usando índices:

```python
b = "Hola, Mundo!"
print(b[2:5])   # "la,"
print(b[:5])    # "Hola,"
print(b[2:])    # "la, Mundo!"
print(b[-5:-2]) # "Mun"
```

## Modificar strings

Algunos métodos útiles:

```python
a = " Hola, Mundo! "
print(a.upper())           # MAYÚSCULAS
print(a.lower())           # minúsculas
print(a.strip())           # elimina espacios al inicio y fin
print(a.replace("H", "J")) # reemplaza H por J
print(a.split(","))        # divide en lista por ","
```

## Concatenar strings

Se puede unir texto con `+`:

```python
a = "Hola"
b = "Mundo"
c = a + " " + b
print(c)  # "Hola Mundo"
```

## Formatear strings

Para combinar texto con números se usan f-strings o `format()`:

```python
edad = 36
txt = f"Mi nombre es Juan, tengo {edad} años"
print(txt)

precio = 59
txt = f"El precio es {precio:.2f} dólares"  # con 2 decimales
print(txt)

txt = f"El precio es {20 * 59} dólares"  # operaciones dentro
print(txt)
```

## Caracteres especiales (escape characters)

Se usan `\` para caracteres especiales:

```python
txt = "Somos los llamados \"Vikingos\" del norte"
print(txt)
```

### Otros escapes comunes:
- `\'` - comilla simple
- `\\` - barra invertida  
- `\n` - nueva línea
- `\t` - tabulación