# Tipos de Datos en Python

## Introducción

Los **tipos de datos** determinan el tipo de valor que puede almacenar una variable y las operaciones que pueden realizarse sobre él.  
Python detecta el tipo de dato automáticamente cuando asignamos un valor (esto se llama **tipado dinámico**).

Ejemplo:

```python
x = 10          # entero (int)
y = 3.14        # número decimal (float)
nombre = "Ian"  # cadena de texto (str)
es_mayor = True # valor booleano (bool)
```

## Basicos

### 1. Números enteros (int)

Representan números sin parte decimal.
```python
a = 7
b = -15
```

Podés hacer operaciones aritméticas:

```python
suma = a + b
resta = a - b
producto = a * b
division = a / b
```

### 2. Números decimales (float)

Se usan para representar valores con parte decimal.

```python
pi = 3.1416
temperatura = -2.5
```

También se pueden operar igual que los enteros:

```python
resultado = pi * 2
```

### 3. Cadenas de texto (str)

Las cadenas se encierran entre comillas simples ' o dobles ".

```python
mensaje = "Hola, Python"
nombre = 'Ian'
```

Podés combinar textos con el operador + o multiplicarlos:

```python
saludo = "Hola " + nombre
eco = "Hey! " * 3
```

También se pueden usar f-strings (formateo de texto):

```python
edad = 18
print(f"Me llamo {nombre} y tengo {edad} años.")
```

### 4. Booleanos (bool)

Solo pueden tener dos valores:

```python
verdadero = True
falso = False
```

Se utilizan en condiciones o comparaciones:

```python
x = 5
y = 10
print(x < y)   # True
print(x == y)  # False
```

### 5. Tipo NoneType

Representa la ausencia de valor (similar a “nulo” en otros lenguajes).

```python
variable = None
print(variable)  # Muestra: None
```

### 6.Función type()

Podés comprobar el tipo de dato de cualquier valor o variable con:

```python
x = 3.5
print(type(x))
```

### Conversión de tipos (casting)

Python permite convertir valores de un tipo a otro.

```python
# int a float
x = float(5)

# float a int (pierde decimales)
y = int(3.7)

# número a cadena
texto = str(100)

# cadena a número (si es posible)
num = int("25")
```
