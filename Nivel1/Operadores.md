# Operadores en Python

## Introducción

Los **operadores** son símbolos que permiten realizar operaciones sobre valores o variables.  
Python incluye operadores aritméticos, de comparación, lógicos, de asignación y más.

---

## 1. Operadores aritméticos

Se utilizan para realizar cálculos matemáticos.

| Operador | Descripción | Ejemplo | Resultado |
|-----------|--------------|----------|------------|
| `+` | Suma | `5 + 3` | `8` |
| `-` | Resta | `10 - 4` | `6` |
| `*` | Multiplicación | `2 * 3` | `6` |
| `/` | División (decimal) | `10 / 4` | `2.5` |
| `//` | División entera | `10 // 4` | `2` |
| `%` | Módulo (resto) | `10 % 4` | `2` |
| `**` | Potencia | `2 ** 3` | `8` |

Ejemplo:

```python
a = 10
b = 3

print(a + b)   # 13
print(a - b)   # 7
print(a * b)   # 30
print(a / b)   # 3.333...
print(a // b)  # 3
print(a % b)   # 1
print(a ** b)  # 1000
```

## Operadores Lógicos, de Asignación, de Identidad y de Pertenencia

---

### 1. Operadores Lógicos

Se utilizan para combinar condiciones lógicas.  
El resultado siempre es un valor booleano (`True` o `False`).

| Operador | Descripción | Ejemplo | Resultado |
|-----------|--------------|----------|------------|
| `and` | Devuelve `True` si **ambas condiciones** son verdaderas | `(5 > 2 and 8 > 6)` | `True` |
| `or` | Devuelve `True` si **al menos una** condición es verdadera | `(5 > 2 or 8 < 6)` | `True` |
| `not` | Invierte el valor lógico | `not(5 > 2)` | `False` |

Ejemplo:

```python
x = 10
y = 5

print(x > 0 and y > 0)  # True
print(x > 0 or y < 0)   # True
print(not(x < y))       # True
```

### Operadores de Asignación en Python

Los operadores de asignación se utilizan para **dar valor a una variable** o **actualizar su contenido** sin necesidad de escribir expresiones largas.

---

#### Asignación simple

El operador `=` asigna el valor de la derecha a la variable de la izquierda.

```python
x = 10
nombre = "Python"
activo = True
```

### Operadores de Pertenencia en Python

Los operadores de pertenencia permiten **verificar si un valor se encuentra dentro** de una secuencia o estructura de datos como listas, cadenas, tuplas, conjuntos o diccionarios.

Devuelven un valor booleano (`True` o `False`).

---

## Tipos de operadores de pertenencia

| Operador | Descripción | Ejemplo | Resultado |
|-----------|--------------|----------|------------|
| `in` | Devuelve `True` si el elemento está en la secuencia | `'a' in 'python'` | `False` |
| `not in` | Devuelve `True` si el elemento **no** está en la secuencia | `'z' not in 'python'` | `True` |

---

#### Ejemplos con distintos tipos de datos

##### 1. Cadenas de texto

```python
texto = "Python"

print("P" in texto)       # True
print("p" in texto)       # False (mayúsculas y minúsculas importan)
print("th" in texto)      # True (subcadena)
print("z" not in texto)   # True
```

##### 2. Tuplas

```python
tupla = ("rojo", "verde", "azul")

print("verde" in tupla)      # True
print("amarillo" not in tupla)  # True
```

##### 3. Filas

```python
numeros = [10, 20, 30, 40]

print(20 in numeros)       # True
print(50 not in numeros)   # True
print(10 in numeros)       # True
```

##### 4. Conjuntos

```python
colores = {"rojo", "verde", "azul"}

print("rojo" in colores)   # True
print("negro" not in colores)  # True
```

##### 5. Diccionarios

```python
persona = {"nombre": "Ian", "edad": 18}

print("nombre" in persona)       # True (verifica claves)
print("Ian" in persona)          # False (no busca valores)
print("edad" not in persona)     # False
print("Ian" in persona.values()) # True (verifica valores)
```

### Operadores de Identidad en Python

Los operadores de identidad se utilizan para **comparar si dos variables hacen referencia al mismo objeto en memoria**, no si tienen el mismo valor.

Estos operadores devuelven un valor booleano (`True` o `False`).

---

#### Tipos de operadores de identidad

| Operador | Descripción | Ejemplo | Resultado |
|-----------|--------------|----------|------------|
| `is` | Devuelve `True` si ambas variables apuntan al mismo objeto en memoria | `a is b` | Depende |
| `is not` | Devuelve `True` si las variables apuntan a objetos distintos | `a is not b` | Depende |

---

#### Ejemplo básico

```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

print(a is b)      # True  (ambas referencias apuntan al mismo objeto)
print(a is c)      # False (contenido igual, pero distinto objeto)
print(a == c)      # True  (contenido igual)
```

#### Ejemplo con objetos Inmutables

En Python, los objetos inmutables (como **int**, **float**, **str**, **tuple**) pueden compartir la misma referencia por optimización interna.

```python
x = 5
y = 5
print(x is y)   # True  (por optimización)

a = "hola"
b = "hola"
print(a is b)   # True  (las cadenas cortas pueden compartir referencia)
```

Sin embargo, esto no debe asumirse siempre. Por ejemplo:

```python
x = 1000
y = 1000
print(x is y)   # Puede ser False, depende del intérprete
```

#### Ejemplo con **none**

Una práctica común es usar **is** o **is not** para comparar con **None**.

```python
x = None

if x is None:
    print("La variable no tiene valor asignado.")
```
