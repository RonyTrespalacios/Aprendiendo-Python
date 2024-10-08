# Manejo de Errores y Excepciones

En Python, el manejo de errores y excepciones es fundamental para escribir código robusto que pueda manejar situaciones inesperadas sin fallar. Una excepción es un evento que ocurre durante la ejecución de un programa y que interrumpe su flujo normal. Python proporciona un mecanismo para manejar estas excepciones de manera controlada.

## Bloques `try` y `except`
El manejo de excepciones se realiza con los bloques `try` y `except`. El código que puede generar una excepción se coloca dentro del bloque `try`, y el código que maneja la excepción se coloca en el bloque `except`.

```python
try:
    numero = int(input("Ingresa un número: "))
    resultado = 10 / numero
    print(f"El resultado es {resultado}")
except ZeroDivisionError:
    print("Error: No se puede dividir entre cero.")
except ValueError:
    print("Error: Entrada inválida, por favor ingresa un número.")
```

## Bloque `else`
El bloque `else` opcional se ejecuta si no se genera ninguna excepción en el bloque `try`.

```python
try:
    numero = int(input("Ingresa un número: "))
    resultado = 10 / numero
except ZeroDivisionError:
    print("Error: No se puede dividir entre cero.")
except ValueError:
    print("Error: Entrada inválida, por favor ingresa un número.")
else:
    print(f"El resultado es {resultado}")
```

## Bloque `finally`
El bloque `finally` se ejecuta independientemente de si se genera una excepción o no. Es útil para limpiar recursos o realizar tareas de cierre.

```python
try:
    archivo = open("datos.txt", "r")
    contenido = archivo.read()
except FileNotFoundError:
    print("Error: El archivo no existe.")
finally:
    archivo.close()
```

## Lanzar Excepciones Personalizadas
Puedes lanzar (o generar) excepciones personalizadas usando la palabra clave `raise`. Esto es útil cuando quieres verificar condiciones específicas en tu código y generar una excepción si no se cumplen.

```python
def dividir(a, b):
    if b == 0:
        raise ValueError("El divisor no puede ser cero.")
    return a / b

try:
    resultado = dividir(10, 0)
except ValueError as e:
    print(e)
```

## Ejercicios Propuestos

### **Ejercicio 1**:

Escribe un programa que solicite al usuario que ingrese un número y maneje las posibles excepciones que puedan ocurrir, como `ValueError` si la entrada no es un número y `ZeroDivisionError` si el número ingresado es cero.

```python
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>

### **Ejercicio 2**:

Desarrolla una función llamada `abrir_archivo` que intente abrir un archivo de texto cuyo nombre es proporcionado por el usuario. Maneja la excepción `FileNotFoundError` si el archivo no existe y muestra un mensaje apropiado. Usa el bloque `finally` para asegurarte de que el archivo se cierra si se pudo abrir.

```python
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>

### **Ejercicio 3**:

Imagina que estás desarrollando una función que calcula la raíz cuadrada de un número. Si el número es negativo, lanza una excepción personalizada `ValueError` con un mensaje indicando que no se puede calcular la raíz cuadrada de un número negativo.

```python
# Escribe tu función y código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>

