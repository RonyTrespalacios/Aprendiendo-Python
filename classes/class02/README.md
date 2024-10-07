# Operadores y Expresiones

En Python, los operadores son símbolos que se utilizan para realizar operaciones sobre valores y variables. Las expresiones son combinaciones de valores, variables y operadores que se evalúan para obtener un resultado.

## Operadores Aritméticos

Los operadores aritméticos se utilizan para realizar operaciones matemáticas básicas.

```python
# Suma
resultado = 5 + 3  # resultado es 8

# Resta
resultado = 10 - 2  # resultado es 8

# Multiplicación
resultado = 4 * 2  # resultado es 8

# División
resultado = 16 / 2  # resultado es 8.0 (la división siempre produce un flotante)

# Módulo (resto de la división)
resultado = 10 % 3  # resultado es 1

# Exponenciación (potencia)
resultado = 2 ** 3  # resultado es 8
```

## Operadores de Comparación

Los operadores de comparación se utilizan para comparar dos valores. El resultado de una expresión con un operador de comparación es un valor booleano (`True` o `False`).

```python
# Igualdad
resultado = (5 == 5)  # True

# Desigualdad
resultado = (5 != 3)  # True

# Mayor que
resultado = (7 > 5)  # True

# Menor que
resultado = (3 < 5)  # True

# Mayor o igual que
resultado = (7 >= 7)  # True

# Menor o igual que
resultado = (3 <= 5)  # True
```

## Operadores Lógicos

Los operadores lógicos se utilizan para combinar expresiones booleanas.

```python
# AND lógico
resultado = (5 > 3) and (8 > 6)  # True, ambas condiciones son verdaderas

# OR lógico
resultado = (5 > 3) or (8 < 6)  # True, al menos una de las condiciones es verdadera

# NOT lógico
resultado = not (5 > 3)  # False, invierte el valor de verdad
```

## Operadores de Asignación

Los operadores de asignación se utilizan para asignar valores a las variables. El operador de asignación más común es `=`, pero hay otros que combinan operaciones aritméticas con la asignación.

```python
# Asignación simple
x = 5  # x es 5

# Asignación con suma
x += 3  # Equivale a x = x + 3, ahora x es 8

# Asignación con resta
x -= 2  # Equivale a x = x - 2, ahora x es 6

# Asignación con multiplicación
x *= 2  # Equivale a x = x * 2, ahora x es 12

# Asignación con división
x /= 3  # Equivale a x = x / 3, ahora x es 4.0

# Asignación con módulo
x %= 3  # Equivale a x = x % 3, ahora x es 1.0

# Asignación con exponenciación
x **= 2  # Equivale a x = x ** 2, ahora x es 1.0
```

Con esta sección, ahora entiendes cómo usar operadores y expresiones en Python para realizar cálculos, comparaciones y combinaciones lógicas. Estas herramientas son fundamentales para escribir código que pueda tomar decisiones y realizar operaciones complejas.

## Ejercicios Propuestos

### **Ejercicio 1**:

Calcula la diferencia entre el cuadrado de 10 y el producto de 5 por 4. Luego, verifica si el resultado es mayor que 50.

<details> <summary>Ver solución</summary>
```python
print(f"((10 ** 2) - 5*4) = {((10 ** 2) - 5*4)}, por lo tanto, la afirmacion 'la diferencia entre el cuadrado de 10 y el producto de 5 por 4' es: {((10 ** 2) - 5*4) > 50}")
```
</details>

### **Ejercicio 2**:

Crea una expresión que verifique si un número es par. Un número es par si el resto de su división por 2 es cero.

<details> <summary>Ver solución</summary>
```python
num = int(input("Digite su numero: "))
print("El numero es par: ", num % 2 == 0)
```
</details>

### **Ejercicio 3**:

Utiliza operadores lógicos para determinar si un número es mayor que 10 y, al mismo tiempo, menor que 20.

<details> <summary>Ver solución</summary>
```python
num = int(input("Digite un numero: "))
print("El numero esta entre 10 y 20:",num > 10 and num < 20)
```
</details>

<div class="navigation-buttons">
    <a href="./#/class01" class="prev-button">← Clase Anterior</a>
    <a href="./#/class03" class="next-button">Clase Siguiente →</a>
</div>