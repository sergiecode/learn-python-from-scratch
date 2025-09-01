# Tipos de Datos en Python

## 1. str (string) – Texto

Se utiliza para representar texto o cadenas de caracteres. Puedes usar comillas simples, dobles o triples:

```python
comillasSimples = 'Este es un texto'
comillasDobles = "Este es un texto"
comillasTriples = """Este es un texto"""
comillasTriplesSimples = '''Este es un texto'''
```

## 2. int (integer) – Números enteros

Son números sin decimales.

```python
numero_entero = 1
```

## 3. float – Números decimales

Se usan para representar números con parte decimal.

```python
numero_decimal = 3.14
```

## 4. complex – Números complejos

Tienen una parte real y una parte imaginaria.

```python
numero_complejo = 5 + 2j
```

## 5. list – Lista

Colección ordenada y mutable de elementos. Cada elemento tiene un índice (posición).

```python
lista = [0, 1, 2, 3, 4, 5]
```

## 6. tuple – Tupla

Colección ordenada pero inmutable de elementos. También tiene índices.

```python
tupla = ("a", "b", "c")
```

## 7. range – Rango de números

Genera una secuencia de números dentro de un rango definido.

```python
rango = range(1, 10)  # Números del 1 al 9
```

## 8. dict (dictionary) – Diccionario

Colección desordenada de pares clave-valor y mutable.

```python
diccionario = {"nombre": "Sergie Code"}
```

## 9. set – Conjunto

Colección desordenada, mutable y con elementos únicos.

```python
conjunto = {1, 1, 2, 2, 3}  # Resultado: {1, 2, 3}
```

## 10. frozenset – Conjunto inmutable

Colección desordenada, inmutable y con elementos únicos.

```python
conjunto_inmutable = frozenset([1, 2, 3, 3, 3])  # Resultado: frozenset({1, 2, 3})
```

## 11. bool – Booleanos

Representa valores de verdad: `True` (verdadero) o `False` (falso).

```python
booleanoVerdadero = True
booleanoFalso = False
```