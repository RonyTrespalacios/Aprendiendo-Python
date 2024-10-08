# Estructuras de Control de Flujo I

## Condicionales (if, else, elif)

### Uso Básico de `if`

La declaración `if` evalúa una condición: si la condición es `True`, ejecuta el bloque de código indentado bajo ella. Si es `False`, pasa al siguiente bloque de código.

```python
edad = 20
if edad >= 18:
    print("Eres mayor de edad")
```

### Uso de `else`
El bloque `else` se ejecuta si la condición en el `if` es `False`.

```python
edad = 16
if edad >= 18:
    print("Eres mayor de edad")
else:
    print("Eres menor de edad")
```

### Uso de `elif`
La palabra clave `elif` (abreviatura de "else if") te permite verificar múltiples condiciones. Si la primera condición `if` es `False`, se evalúan las condiciones `elif` en orden. Si todas las condiciones son `False`, se ejecuta el bloque `else` al final.

```python
nota = 85
if nota >= 90:
    print("Excelente")
elif nota >= 80:
    print("Muy bien")
elif nota >= 70:
    print("Bien")
else:
    print("Necesitas mejorar")
```

### Condiciones Anidadas
Puedes anidar condicionales dentro de otros condicionales para manejar situaciones más complejas.

```python
edad = 20
tiene_identificacion = True

if edad >= 18:
    if tiene_identificacion:
        print("Puedes entrar al club")
    else:
        print("No puedes entrar sin identificación")
else:
    print("No puedes entrar, eres menor de edad")
```

### Ejercicios Propuestos

#### **Ejercicio 1**:

Escribe un programa que determine si un número ingresado por el usuario es positivo, negativo o cero.

```python
numero = int(input("Ingresa un número: "))
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
numero = int(input("Ingresa un número: "))
if numero > 0:
  print('El numero es positivo.')
elif numero < 0:
  print('El numero es negativo.')
else:
  print('El numero es igual a 0.')
```
</details>

#### **Ejercicio 2**:

Supón que estás desarrollando un sistema de calificaciones para una escuela. Escribe un programa que asigne una letra de calificación (A, B, C, D, F) basada en la nota numérica ingresada.

```python
nota = int(input("Ingresa tu nota: "))
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
nota = float(input("Ingresa tu nota: "))

if nota > 0 and nota <= 5:
  print("Su calificacion es: ",end="")
  # ---------------
  if nota < 2:
    print("F")
  elif nota < 3:
    print("E")
  elif nota < 4:
    print("C")
  elif nota <  4.5:
    print("B")
  else:
    print("A")
  # ---------------
elif nota > 5:
  print("Error, digite un valor entre 0 y 5")
else:
  print("Error, digite un numero positivo entre 0 y 5")
```
</details>

#### **Ejercicio 3**:

Imagina que estás desarrollando un sistema de control de acceso. El sistema debe permitir el acceso solo si la persona tiene más de 18 años y presenta una identificación válida. Escribe un programa que realice esta verificación.

```python
edad = int(input("Ingresa tu edad: "))
tiene_identificacion = input("¿Tienes identificación válida? (si/no): ").lower() == "si"
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
edad = int(input("Ingresa tu edad: "))
tiene_identificacion = input("¿Tienes identificación válida? (si/no): ").lower() == "si"
if edad > 18 and tiene_identificacion:
  print("Acceso valido.")
else:
  print("Acceso denegado.")
```
</details>

## Bucles `for`

Los bucles `for` en Python se utilizan para iterar sobre una secuencia (como una lista, tupla, diccionario, conjunto o cadena) y ejecutar un bloque de código por cada elemento de la secuencia.

### Iteración sobre Listas
El uso más común de un bucle `for` es iterar sobre los elementos de una lista.

```python
frutas = ["manzana", "banana", "cereza"]
for fruta in frutas:
    print(fruta)
```

### Iteración sobre Cadenas
También puedes usar un bucle `for` para iterar sobre los caracteres de una cadena de texto.

```python
palabra = "Python"
for letra in palabra:
    print(letra)
```

### Iteración con `range()`
La función `range()` se utiliza para generar una secuencia de números, lo que es útil cuando necesitas repetir una acción un número específico de veces.

```python
for i in range(5):
    print(i)
```

### Iteración sobre Diccionarios
Cuando iteras sobre un diccionario, puedes recorrer tanto las claves como los valores.

```python
estudiante = {"nombre": "Ana", "edad": 21, "carrera": "Ingeniería"}
for clave, valor in estudiante.items():
    print(f"{clave}: {valor}")
```

### Comprensión de Listas (List Comprehensions)
Una comprensión de listas es una manera concisa de crear listas utilizando bucles `for` y opcionalmente condicionales.

```python
numeros = [1, 2, 3, 4, 5]
cuadrados = [x ** 2 for x in numeros]
print(cuadrados)  # Imprime [1, 4, 9, 16, 25]
```

### Ejercicios Propuestos

#### **Ejercicio 1**:

Dada una lista de números `[1, 2, 3, 4, 5]`, escribe un bucle `for` que imprima el cuadrado de cada número.

```python
numeros = [1, 2, 3, 4, 5]
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
numeros = [1, 2, 3, 4, 5]
print([x ** 2 for x in numeros])
```
</details>

#### **Ejercicio 2**:

Tienes un diccionario con los nombres y edades de tres personas:

```python
personas = {"Juan": 25, "Ana": 30, "Luis": 20}
```

Escribe un bucle `for` que recorra el diccionario y muestre un mensaje con el nombre y la edad de cada persona.

<details> <summary>Ver solución</summary>
```python
personas = {"Juan": 25, "Ana": 30, "Luis": 20}
for clave, valor in personas.items():
  print(f"{clave.capitalize()} tiene {valor} años.")
```
</details>

#### **Ejercicio 3**:

Utiliza un bucle `for` con `range()` para imprimir los números del 1 al 10.

```python
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
print(", ".join([str(x+1) for x in range(10)]), end=".")
```
</details>

## Bucles `for` Avanzados

En situaciones más complejas, a menudo es necesario utilizar bucles `for` anidados, es decir, un bucle `for` dentro de otro. Esto es útil cuando trabajas con estructuras de datos que contienen otras estructuras, como listas de listas o diccionarios de diccionarios.

### Bucles `for` Anidados
Un bucle `for` anidado es simplemente un bucle `for` dentro de otro bucle `for`. Cada iteración del bucle externo ejecuta completamente el bucle interno.

```python
matriz = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

for fila in matriz:
    for elemento in fila:
        print(elemento)
```

En este ejemplo, el bucle externo itera sobre cada fila de la matriz, mientras que el bucle interno itera sobre cada elemento de esa fila.

### Aplicaciones Comunes

1. **Recorrido de Matrices**: Los bucles anidados son ideales para trabajar con matrices (listas de listas) o tablas de datos, donde necesitas acceder a cada elemento individualmente.
  
2. **Generación de Combinaciones**: Otro uso común de los bucles anidados es generar todas las combinaciones posibles de elementos entre dos o más listas.

### Ejercicios Propuestos

#### **Ejercicio 1**:

Dada una lista de listas que representa una tabla de multiplicar, escribe un programa que utilice bucles `for` anidados para imprimir cada elemento de la tabla.

```python
tabla_multiplicar = [
    [1, 2, 3],
    [2, 4, 6],
    [3, 6, 9]
]
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
tabla_multiplicar = [
    [1, 2, 3],
    [2, 4, 6],
    [3, 6, 9]
]
print(", ".join(str(elemento) for fila in tabla_multiplicar for elemento in fila), end='.')
```
</details>

#### **Ejercicio 2**:

Imagina que tienes dos listas: una con nombres y otra con apellidos. Escribe un programa que genere y muestre todas las combinaciones posibles de nombres y apellidos.

```python
nombres = ["Juan", "Ana", "Luis"]
apellidos = ["Pérez", "García", "Rodríguez"]
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
nombres = ["Juan", "Ana", "Luis"]
apellidos = ["Pérez", "García", "Rodríguez"]
print(", ".join( f"{i} {j}" for j in apellidos for i in nombres ))
```
</details>

#### **Ejercicio 3**:

Tienes un diccionario que contiene listas como valores. Escribe un programa que utilice bucles `for` anidados para imprimir cada clave junto con cada uno de sus valores.

```python
diccionario = {
    "frutas": ["manzana", "banana", "cereza"],
    "verduras": ["zanahoria", "brocoli", "espinaca"]
}
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
diccionario = {
    "frutas": ["manzana", "banana", "cereza"],
    "verduras": ["zanahoria", "brocoli", "espinaca"]
}

print("\n".join(f"{clave} : {', '.join(valor)}" for clave, valor in diccionario.items()))
```
</details>

#### **Ejercicio 4**:

En una escuela, te han pedido que calcules la calificación promedio de cada estudiante y muestres esos promedios en una sola línea. Cada alumno tiene sus calificaciones almacenadas en un diccionario anidado. La tarea consiste en obtener los promedios de cada alumno y mostrarlos separados por comas, todo en una sola línea de código.

```python
alumnos_calificaciones = {
    "Juan": {"Matemáticas": 85, "Ciencias": 90, "Historia": 88},
    "Maria": {"Matemáticas": 78, "Ciencias": 85, "Historia": 92},
    "Pedro": {"Matemáticas": 90, "Ciencias": 88, "Historia": 84}
}
```

<details> <summary>Ver solución</summary>
```python
alumnos_calificaciones = {
    "Juan": {"Matemáticas": 85, "Ciencias": 90, "Historia": 88},
    "Maria": {"Matemáticas": 78, "Ciencias": 85, "Historia": 92},
    "Pedro": {"Matemáticas": 90, "Ciencias": 88, "Historia": 84}
}

print("NOTAS >>>> \n\t"+"\n\t".join( f"{nombre}: {', '.join([str(nota) for materia, nota in valor.items()])}" for nombre, valor in alumnos_calificaciones.items()))

def mean(a):
  return sum(a) / len(a)

print("PROMEDIOS >>>> \n\t"+"\n\t".join( f"{nombre}: {mean([nota for materia, nota in valor.items()])}" for nombre, valor in alumnos_calificaciones.items()))

### Solucion optima:
print("PROMEDIOS >>>> \n\t" + "\n\t".join(f"{nombre}: {sum(notas.values()) / len(notas)}" for nombre, notas in alumnos_calificaciones.items()))
```
</details>

#### **Ejercicio 5**:

Tienes una lista de precios desordenada de productos en varias categorías, y necesitas aplicar un descuento del 10% a todos los precios, mostrando los precios finales en una sola línea, separados por comas. El reto es que debes calcular el precio con descuento y mostrar el resultado en una sola línea de código.

```python
lista_precios = [
    [12.99, 8.50, 5.75],
    [19.99, 9.50],
    [3.99, 4.25, 7.80]
]
```

<details> <summary>Ver solución</summary>
```python
lista_precios = [
    [12.99, 8.50, 5.75],
    [19.99, 9.50],
    [3.99, 4.25, 7.80]
]
print("PRECIO >>> \n\t",", ".join(f"{elemento}" for fila in lista_precios for elemento in fila))
print("10% DCTO >>> \n\t",", ".join(f"{elemento*0.9}" for fila in lista_precios for elemento in fila))
```
</details>

#### **Ejercicio 6**:

En una tienda, tienes un registro de ventas mensuales donde cada mes está representado por un diccionario de productos y sus ventas. Debes calcular el total de ventas de cada producto a lo largo de todos los meses y mostrar el total de ventas de cada producto en una sola línea, separado por comas. El desafío es hacerlo en una sola línea de código.

```python
ventas_mensuales = {
    "Enero": {"Producto A": 150, "Producto B": 230},
    "Febrero": {"Producto A": 180, "Producto B": 220},
    "Marzo": {"Producto A": 210, "Producto B": 190}
}
```

<details> 
  <summary>Ver solución</summary>
    ```python
    ventas_mensuales = {
        "Enero": {"Producto A": 150, "Producto B": 230},
        "Febrero": {"Producto A": 180, "Producto B": 220},
        "Marzo": {"Producto A": 210, "Producto B": 190}
    }

    print("Ventas >>> \n\t" + "\n\t".join( f"{mes} : {', '.join([f'{p}: {v}' for p, v in value.items()])}" for mes, value in ventas_mensuales.items()))
    print("Ventas Mensuales >>> \n\t" + "\n\t".join( f"{mes} : {sum(value.values())}" for mes, value in ventas_mensuales.items()))
    print("Ventas por producto >>> \n\t" + "\n\t".join([f"{p}: {sum(mes.get(p, 0) for mes in ventas_mensuales.values())}" for p in {p for v in ventas_mensuales.values() for p in v}]))
    ```
</details>
