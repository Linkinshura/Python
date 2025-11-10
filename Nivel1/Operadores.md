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
