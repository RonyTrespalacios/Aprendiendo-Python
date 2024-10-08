# Estructuras de Control de Flujo II

## Uso de Condicionales `if` y Bucles `for` en Una Sola Línea

Python permite escribir condicionales `if` y bucles `for` en una sola línea de código. Esto puede hacer que el código sea más conciso y fácil de leer, aunque es importante usar esta técnica con moderación para no sacrificar la claridad del código.

### Condicionales `if` en Una Sola Línea

Puedes escribir una declaración `if` sencilla en una sola línea utilizando el operador ternario en Python. La sintaxis general es:

```python
valor_si_verdadero if condicion else valor_si_falso
```

#### Ejemplo 1: Asignación basada en una condición
```python
edad = 20
mensaje = "Mayor de edad" if edad >= 18 else "Menor de edad"
print(mensaje)  # Imprime "Mayor de edad"
```

#### Ejemplo 2: Usando un condicional dentro de una lista
```python
numeros = [1, 2, 3, 4, 5]
pares = [num for num in numeros if num % 2 == 0]
print(pares)  # Imprime [2, 4]
```

### Bucles `for` en Una Sola Línea

Los bucles `for` también pueden escribirse en una sola línea, lo que es particularmente útil en comprensiones de listas, conjuntos o diccionarios.

#### Ejemplo 3: Comprensión de listas con un bucle `for`
```python
cuadrados = [x**2 for x in range(5)]
print(cuadrados)  # Imprime [0, 1, 4, 9, 16]
```

#### Ejemplo 4: Usar `for` y `if` en la misma línea
Puedes combinar un bucle `for` y una condición `if` en una sola línea para filtrar elementos mientras se itera.

```python
numeros = [1, 2, 3, 4, 5]
dobles_pares = [x*2 for x in numeros if x % 2 == 0]
print(dobles_pares)  # Imprime [4, 8]
```

#### Ejemplo 5: Asignar una variable con el resultado de un bucle `for`
Puedes usar un bucle `for` en una sola línea para asignar el resultado a una variable.

```python
suma_cuadrados = sum(x**2 for x in range(5))
print(suma_cuadrados)  # Imprime 30 (0 + 1 + 4 + 9 + 16)
```

### Ejercicios Propuestos

Es recomendable solucionar los siguientes ejercicios primero en su version extendida para luego extrapolar la logica a una sola linea.

#### **Ejercicio 1**:

En un juego de estrategia, cada vez que un jugador recoge un objeto valioso, su poder se incrementa al elevar su valor al cubo, pero esto solo aplica si el valor del objeto es par. Dada una lista de valores correspondientes a los objetos recogidos por un jugador, crea una nueva lista que contenga los cubos de aquellos valores que sean pares, todo en una sola línea de código.

```python
valores = [15, 22, 9, 4, 18, 11, 6, 7, 10]
# Escribe tu código aquí para crear la lista de cubos de los valores pares
```

<details> <summary>Ver solución</summary>
```python
valores = [15, 22, 9, 4, 18, 11, 6, 7, 10]
print("Poder normal: \t\t" + ", ".join(str(i) for i in valores))
print("Poder incrementado: \t" + ", ".join(str(i ** 3 if i%2==0 else i) for i in valores))
```
</details>

#### **Ejercicio 2**:

Estás desarrollando una aplicación financiera que clasifica el balance de una cuenta bancaria según su estado: "Positivo" si el balance es mayor que cero, "Negativo" si es menor que cero, y "Cero" si es exactamente cero. Dado un balance, asigna uno de estos valores a una variable en una sola línea de código utilizando un operador ternario.

```python
balance = -150  # Puedes cambiar este valor para probar diferentes casos
# Escribe tu código aquí para asignar "Positivo", "Negativo", o "Cero"
```

<details> <summary>Ver solución</summary>
```python
balance = float(input("Digite un numero: "))
print("El numero es" , "positivo" if balance>0 else "negativo" if balance<0 else "cero")
```
</details>

#### **Ejercicio 3**:

En una aplicación de procesamiento de textos, es importante calcular la longitud de las palabras clave que son significativas para un análisis. Tienes una lista de palabras y necesitas crear una nueva lista que contenga las longitudes de aquellas palabras que tengan más de tres letras. Realiza esta operación en una sola línea de código.

```python
palabras = ["sol", "luz", "computadora", "teclado", "ratón", "pantalla"]
# Escribe tu código aquí para obtener las longitudes de las palabras con más de tres letras
```

<details> <summary>Ver solución</summary>
```python
palabras = ["sol", "luz", "computadora", "teclado", "ratón", "pantalla"]
new_list = [len(palabra) for palabra in palabras if len(palabra)>3]
print(new_list)
```
</details>

#### **Ejercicio 4**:

En una aplicación para gestionar eventos, necesitas crear una lista de invitados que sean mayores de edad para enviarles invitaciones especiales. Dado un diccionario que contiene nombres como claves y edades como valores, filtra los nombres de las personas que tienen 18 años o más en una sola línea de código.

```python
invitados = {"Luis": 17, "Ana": 21, "Pedro": 19, "Marta": 22, "Sofia": 16}
# Escribe tu código aquí para filtrar los nombres de los invitados mayores de edad
```

<details> <summary>Ver solución</summary>
```python
invitados = {"Luis": 17, "Ana": 21, "Pedro": 19, "Marta": 22, "Sofia": 16, "Rony": 22, "Chicho": 16, "Lupe": 4}
print("Invitados:",", ".join(f"{nombre}" for nombre, edad in invitados.items() if edad >= 18))
```
</details>

#### **Ejercicio 5**:

aaaaaaaaaaa

<details> <summary>Ver solución</summary>
```python
aaaaaaaaaaa
```
</details>#### **Ejercicio 4**:

En una aplicación de gestión de usuarios, tienes una base de datos en forma de diccionario donde las claves son los nombres de usuario en minúsculas y los valores son los correos electrónicos. Necesitas crear una lista de nombres de usuario formateados correctamente (con la primera letra en mayúscula) para mostrar en la interfaz de usuario. Realiza esta operación en una sola línea de código.

```python
usuarios = {"jdoe": "jdoe@example.com", "asmith": "asmith@example.com", "mbrown": "mbrown@example.com"}
```

<details> <summary>Ver solución</summary>
```python
usuarios = {"jdoe": "jdoe@example.com", "asmith": "asmith@example.com", "mbrown": "mbrown@example.com"}
lista_usuarios = [name.capitalize() for name, _ in usuarios.items()]
print(lista_usuarios)
```
</details>

#### **Ejercicio 6**:

Estás desarrollando un sistema de inventario para una tienda, y tienes una base de datos en forma de diccionario donde las claves son nombres de productos y los valores son las cantidades en stock. Necesitas crear una lista de los nombres de productos que tienen más de 10 unidades en stock, pero que también contengan la palabra "Premium" añadida al final de cada nombre de producto. Realiza esto en una sola línea de código.

```python
inventario = {
    "Televisor": 5,
    "Lavadora": 12,
    "Microondas": 8,
    "Refrigerador": 15,
    "Aspiradora": 9,
    "Horno": 11
}
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
    ```python
    inventario = {
        "Televisor": 5,
        "Lavadora": 12,
        "Microondas": 8,
        "Refrigerador": 15,
        "Aspiradora": 9,
        "Horno": 11
    }

    lista_premium = [(producto +" Premium") for producto, stock in inventario.items() if stock>10]
    print(", ".join(lista_premium))
    ```
</details>

#### **Ejercicio 7**:

En una aplicación de reseñas, tienes una base de datos en forma de diccionario donde las claves son identificadores de usuarios y los valores son comentarios de clientes. Necesitas crear una lista de identificadores de usuarios cuyos comentarios contengan la palabra "excelente" y que además no incluyan números en sus comentarios. Realiza esta operación en una sola línea de código.

```python
comentarios = {
    "user123": "Este producto es excelente, me encantó",
    "user456": "No es tan bueno como esperaba",
    "user789": "¡Excelente calidad y servicio!",
    "user101": "Es decente, pero el precio es alto",
    "user202": "No está mal, pero tiene fallos",
    "user303": "Increíblemente excelente, lo recomendaré a todos"
}
# Escribe tu código aquí
```

Estos ejercicios están diseñados para que practiques la manipulación de strings y el uso de condicionales junto con bucles en una sola línea de código, aplicando lo aprendido de manera efectiva.

<details> <summary>Ver solución</summary>
    ```python
    comentarios = {
        "user123": "Este producto es excelente, me encantó",
        "user456": "No es tan bueno como esperaba",
        "user789": "¡Excelente calidad y servicio!",
        "user101": "Es decente, pero el precio es alto",
        "user202": "No está mal, pero tiene fallos",
        "user303": "Increíblemente excelente, lo recomendaré a todos"
    }

    lista = [comment for comment in comentarios.values() if comment.lower().find("excelente") != -1]
    print("\n".join(lista))
    ```
</details>
