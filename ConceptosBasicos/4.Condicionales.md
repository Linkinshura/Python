# Condicionales en Python

Los condicionales permiten **tomar decisiones** dentro de un programa.  
Sirven para ejecutar diferentes bloques de código dependiendo de si una condición se cumple o no.

---

## Estructura básica: `if`

La sentencia `if` evalúa una **condición booleana**.  
Si la condición es verdadera (`True`), se ejecuta el bloque indentado; si es falsa (`False`), se salta.

```python
edad = 18

if edad >= 18:
    print("Sos mayor de edad.")
```

## **if else**

Permite ejecutar un bloque alternativo si la condición no se cumple.

```python
edad = 16

if edad >= 18:
    print("Sos mayor de edad.")
else:
    print("Sos menor de edad.")
```

## **if - elif - else**

Cuando hay más de una condición a evaluar, se usa **elif** (abreviatura de **else if**).

```python
nota = 7

if nota >= 9:
    print("Excelente")
elif nota >= 6:
    print("Aprobado")
else:
    print("Desaprobado")
```

## Anidados

Se pueden colocar condicionales dentro de otros para verificar condiciones más específicas.

```python
edad = 20
tiene_licencia = True

if edad >= 18:
    if tiene_licencia:
        print("Podés conducir.")
    else:
        print("Necesitás una licencia.")
else:
    print("Sos menor de edad.")
```

## Ternarios

Permiten escribir una condición en una sola línea.

```python
edad = 22
mensaje = "Mayor de edad" if edad >= 18 else "Menor de edad"
print(mensaje)
```

## Con Operadores Logicos

Se pueden combinar condiciones con **and**, **or** y **not**.

```python
x = 10
y = 5

if x > 0 and y > 0:
    print("Ambos números son positivos.")

if x > 0 or y < 0:
    print("Al menos una condición se cumple.")

if not (x < y):
    print("x no es menor que y.")
```
