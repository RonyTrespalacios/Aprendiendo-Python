# Funciones y Modularidad

Las funciones son bloques de código reutilizables que realizan una tarea específica. Las funciones te permiten organizar tu código, hacerlo más legible y evitar la repetición de código.

## Definición de Funciones
Una función en Python se define utilizando la palabra clave `def`, seguida del nombre de la función, paréntesis `()` y dos puntos `:`. Dentro del cuerpo de la función, que se indenta, puedes escribir el código que quieres que se ejecute cada vez que se llame a la función.

```python
def saludar():
    print("Hola, bienvenido a Python")

# Llamar a la función
saludar()
```

## Parámetros y Argumentos
Las funciones pueden aceptar parámetros, que son variables que se utilizan dentro de la función. Los valores reales que se pasan a la función cuando se llama se llaman argumentos.

```python
def saludar(nombre):
    print(f"Hola, {nombre}, bienvenido a Python")

# Llamar a la función con un argumento
saludar("Juan")
```

## Valor de Retorno
Las funciones pueden devolver un valor utilizando la palabra clave `return`. Esto permite que la función envíe datos de vuelta al lugar donde fue llamada.

```python
def sumar(a, b):
    return a + b

resultado = sumar(5, 3)
print(f"El resultado es {resultado}")
```

## Funciones Anidadas y Alcance
Puedes definir funciones dentro de otras funciones. Además, las variables definidas dentro de una función no son accesibles fuera de esa función, lo que se conoce como alcance local.

```python
def funcion_externa():
    def funcion_interna():
        print("Soy la función interna")
    funcion_interna()

funcion_externa()
```

## Modularidad
La modularidad es el concepto de dividir un programa grande en partes más pequeñas y manejables (módulos). En Python, puedes organizar tu código en funciones y módulos (archivos `.py`) que pueden ser importados y reutilizados en diferentes programas.

### Importar Módulos
Puedes importar un módulo en otro archivo Python usando la palabra clave `import`.

```python
# archivo math_utils.py
def sumar(a, b):
    return a + b
```

```python
# archivo principal.py
import math_utils

resultado = math_utils.sumar(5, 3)
print(f"El resultado es {resultado}")
```

## Ejercicios Propuestos

### **Ejercicio 1**:

Crea una función llamada `es_par` que tome un número como parámetro y devuelva `True` si el número es par, y `False` si es impar. Luego, utiliza esta función en un bucle para imprimir si los números del 1 al 10 son pares o impares.

```python
# Escribe tu función y código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>

### **Ejercicio 2**:

Desarrolla una función llamada `calcular_area_circulo` que tome el radio de un círculo como parámetro y devuelva el área del círculo. Usa la fórmula `area = π * radio^2`. Luego, solicita al usuario que ingrese un radio y muestra el área correspondiente utilizando la función que creaste.

```python
# Escribe tu función y código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>

### **Ejercicio 3**:

Imagina que estás desarrollando un programa para una tienda en línea. Crea un módulo llamado `inventario.py` que contenga una función `agregar_producto(nombre, cantidad)` que agregue productos a un diccionario de inventario. Luego, en otro archivo, importa el módulo `inventario` y utiliza la función para agregar varios productos y mostrar el inventario final.

```python
# Escribe tu módulo y código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>