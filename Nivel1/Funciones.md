# Funciones básicas en Python

## ¿Qué es una función?

Una **función** es un bloque de código que **realiza una tarea específica** y puede ser reutilizado en diferentes partes del programa.  
Permiten **organizar**, **reutilizar** y **mantener** el código de manera más sencilla.

---

## Definición de una función

En Python, una función se define con la palabra clave `def`.

### Sintaxis

```python
def nombre_funcion(parámetros):
    # bloque de código
    return valor
```

## Con Parametros

Los parámetros permiten enviar datos a una función para que trabaje con ellos.

```
def saludar(nombre):
    print("Hola,", nombre)
```

## Con Retorno

Las funciones pueden devolver valores usando la palabra clave **return**.

```python
def sumar(a, b):
    resultado = a + b
    return resultado

total = sumar(5, 3)
print("La suma es:", total)
```

## Scoope

Las variables definidas dentro de una función tienen un ámbito local, y solo existen dentro de esa función.

```python
def mostrar_variable():
    mensaje = "Hola desde la función"
    print(mensaje)

mostrar_variable()
# print(mensaje)  # Error: la variable no existe fuera de la función
```

## Lambda

Las funciones lambda son funciones pequeñas de una sola línea.
No tienen nombre y se usan para tareas simples.

```python
lambda parámetros: expresión
```
