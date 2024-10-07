# Estructuras de Datos I

## Listas

Las listas son una de las estructuras de datos más utilizadas en Python. Se utilizan para almacenar colecciones de elementos que pueden ser de cualquier tipo: números, cadenas, otros objetos, etc. A diferencia de otros lenguajes de programación, las listas en Python son dinámicas y pueden crecer o reducirse en tamaño según sea necesario.

### Creación de Listas
Puedes crear una lista utilizando corchetes `[]` y separando los elementos por comas.

```python
mi_lista = [1, 2, 3, 4, 5]  # Una lista de números enteros
otra_lista = ["manzana", "banana", "cereza"]  # Una lista de cadenas
lista_mixta = [1, "Hola", 3.14, True]  # Una lista con diferentes tipos de datos
```

### Acceso a Elementos de una Lista
Puedes acceder a un elemento en particular de la lista utilizando un índice. En Python, los índices comienzan en 0, es decir, el primer elemento tiene índice 0, el segundo tiene índice 1, y así sucesivamente.

```python
mi_lista = [10, 20, 30, 40, 50]
print(mi_lista[0])  # Imprime 10, el primer elemento
print(mi_lista[2])  # Imprime 30, el tercer elemento
```

### Modificación de Elementos
Puedes modificar un elemento de la lista accediendo a él por su índice y asignándole un nuevo valor.

```python
mi_lista = [10, 20, 30, 40, 50]
mi_lista[1] = 25  # Cambia el segundo elemento de 20 a 25
print(mi_lista)  # Imprime [10, 25, 30, 40, 50]
```

### Métodos Comunes para Listas
Las listas en Python vienen con varios métodos útiles que permiten manipular y trabajar con los elementos de la lista.

- `append()`: Agrega un elemento al final de la lista.
- `insert()`: Inserta un elemento en una posición específica.
- `remove()`: Elimina el primer elemento de la lista que coincida con el valor dado.
- `pop()`: Elimina y retorna el último elemento de la lista (o un elemento específico si se proporciona un índice).
- `sort()`: Ordena la lista en su lugar.
- `reverse()`: Invierte el orden de los elementos en la lista.

```python
frutas = ["manzana", "banana", "cereza"]
frutas.append("naranja")  # Agrega "naranja" al final de la lista
print(frutas)  # Imprime ['manzana', 'banana', 'cereza', 'naranja']

frutas.insert(1, "kiwi")  # Inserta "kiwi" en la segunda posición
print(frutas)  # Imprime ['manzana', 'kiwi', 'banana', 'cereza', 'naranja']

frutas.remove("banana")  # Elimina "banana" de la lista
print(frutas)  # Imprime ['manzana', 'kiwi', 'cereza', 'naranja']

ultimo = frutas.pop()  # Elimina y retorna el último elemento
print(ultimo)  # Imprime 'naranja'
print(frutas)  # Imprime ['manzana', 'kiwi', 'cereza']

frutas.sort()  # Ordena la lista alfabéticamente
print(frutas)  # Imprime ['cereza', 'kiwi', 'manzana']

frutas.reverse()  # Invierte el orden de la lista
print(frutas)  # Imprime ['manzana', 'kiwi', 'cereza']
```

### Ejercicios Propuestos

#### **Ejercicio 1**:

Crea una lista que contenga los nombres de tus tres libros favoritos. Luego, agrega otro libro al final de la lista y muestra la lista actualizada.

<details> <summary>Ver solución</summary>
```python
mi_lista = ["El principito", "El coronel no tiene quien le escriba", "Habitos Atomicos"]
mi_lista.append("Mentes")
print(mi_lista)
```
</details>

#### **Ejercicio 2**:

Crea una lista con los números del 1 al 5. Luego, cambia el segundo número de la lista por 10 y muestra la lista.

<details> <summary>Ver solución</summary>
```python
numbers = [1, 2, 3, 4, 5]
numbers[1] = 10
print(numbers)
```
</details>

#### **Ejercicio 3**:

Dada una lista de frutas `["manzana", "banana", "cereza", "naranja"]`, elimina "banana" de la lista, ordena las frutas alfabéticamente y luego invierte el orden. Muestra la lista final.

<details> <summary>Ver solución</summary>
```python
frutas = ["manzana", "banana", "cereza", "naranja"]
frutas.remove("banana")
frutas.sort()
print("La lista actual es:",frutas)
```
</details>

## Tuplas

Las tuplas son otra estructura de datos en Python, similar a las listas, pero con una diferencia clave: son inmutables. Esto significa que, una vez que se crea una tupla, no puedes cambiar sus elementos, agregar nuevos elementos o eliminar existentes. Las tuplas se utilizan cuando quieres almacenar un conjunto de elementos que no deben ser modificados a lo largo de la ejecución del programa.

### Creación de Tuplas
Puedes crear una tupla utilizando paréntesis `()` y separando los elementos por comas.

```python
mi_tupla = (1, 2, 3, 4, 5)  # Una tupla de números enteros
otra_tupla = ("manzana", "banana", "cereza")  # Una tupla de cadenas
tupla_mixta = (1, "Hola", 3.14, True)  # Una tupla con diferentes tipos de datos
```

### Acceso a Elementos de una Tupla
Al igual que con las listas, puedes acceder a un elemento específico de una tupla utilizando un índice. Los índices comienzan en 0.

```python
mi_tupla = (10, 20, 30, 40, 50)
print(mi_tupla[0])  # Imprime 10, el primer elemento
print(mi_tupla[2])  # Imprime 30, el tercer elemento
```

### ¿Por Qué Usar Tuplas?
Dado que las tuplas son inmutables, son más rápidas que las listas en términos de acceso y ocupan menos espacio en memoria. Se usan comúnmente para:
- Agrupar datos relacionados (por ejemplo, coordenadas (x, y)).
- Proteger datos que no deben cambiarse.
- Como claves en diccionarios, ya que las listas no pueden ser claves debido a su mutabilidad.

### Métodos Comunes para Tuplas
Las tuplas tienen menos métodos que las listas debido a su inmutabilidad, pero aún hay algunos métodos útiles:
- `count()`: Cuenta cuántas veces aparece un valor en la tupla.
- `index()`: Devuelve el índice de la primera aparición de un valor en la tupla.

```python
mi_tupla = (1, 2, 2, 3, 4, 2)
print(mi_tupla.count(2))  # Imprime 3, ya que el número 2 aparece tres veces en la tupla
print(mi_tupla.index(3))  # Imprime 3, que es el índice donde aparece el número 3
```

### Ejercicios Propuestos

#### **Ejercicio 1**:

Imagina que estás desarrollando una aplicación de mapas. Crea una tupla para almacenar las coordenadas de una ubicación específica (por ejemplo, (40.7128, -74.0060) para Nueva York). Muestra la latitud y la longitud por separado.

<details> <summary>Ver solución</summary>
```python
coords =  (40.7128, -74.0060)
print("Latitud: "+str(coords[0])+"\nLongitud: "+str(coords[1]))
```
</details>

#### **Ejercicio 2**:

Estás programando un sistema de registro de pacientes en un hospital. Crea una tupla que almacene la información de un paciente (nombre, edad, número de seguro social). Muestra cada uno de estos datos en la pantalla.

<details> <summary>Ver solución</summary>
```python
paciente = ("Elsa Pato", 19, "123-4321-21")
print("Nombre: "+str(paciente[0])+"\nEdad: "+str(paciente[1])+"\nNumero de seguro social: "+str(paciente[2]))
```
</details>

#### **Ejercicio 3**:

En un sistema de reservas de vuelos, necesitas almacenar la información del vuelo (número de vuelo, destino, hora de salida) en una tupla. Accede a la hora de salida e imprime un mensaje indicando a qué hora es el vuelo.

<details> <summary>Ver solución</summary>
```python
vuelo = ("LA-521", "BOG", "12:05 am")
print("El vuelo sale a las", vuelo[2])
```
</details>

## Diccionarios

Los diccionarios son una estructura de datos en Python que almacenan pares de clave-valor. Son muy útiles cuando necesitas asociar valores específicos con claves únicas. A diferencia de las listas y las tuplas, los diccionarios no mantienen un orden específico (aunque en versiones recientes de Python, mantienen el orden de inserción), y sus elementos se acceden a través de las claves en lugar de índices numéricos.

### Creación de Diccionarios
Puedes crear un diccionario utilizando llaves `{}` y separando las claves de los valores con dos puntos `:`.

```python
mi_diccionario = {
    "nombre": "Juan",
    "edad": 30,
    "ciudad": "Buenos Aires"
}
```

### Acceso a Valores en un Diccionario
Para acceder a un valor en un diccionario, se usa la clave correspondiente entre corchetes `[]`.

```python
print(mi_diccionario["nombre"])  # Imprime "Juan"
print(mi_diccionario["edad"])    # Imprime 30
```

### Modificación de Valores
Puedes modificar el valor asociado a una clave específica simplemente asignando un nuevo valor a esa clave.

```python
mi_diccionario["edad"] = 31  # Cambia la edad a 31
print(mi_diccionario["edad"])  # Imprime 31
```

### Agregar y Eliminar Pares Clave-Valor
Puedes agregar nuevos pares clave-valor al diccionario o eliminar un par existente.

```python
mi_diccionario["profesión"] = "Ingeniero"  # Agrega un nuevo par clave-valor
print(mi_diccionario)  # Imprime {'nombre': 'Juan', 'edad': 31, 'ciudad': 'Buenos Aires', 'profesión': 'Ingeniero'}

del mi_diccionario["ciudad"]  # Elimina el par clave-valor con la clave "ciudad"
print(mi_diccionario)  # Imprime {'nombre': 'Juan', 'edad': 31, 'profesión': 'Ingeniero'}
```

### Iteración a través de un Diccionario
Puedes iterar sobre un diccionario para obtener tanto las claves como los valores.

```python
for clave, valor in mi_diccionario.items():
    print(f"La clave es {clave} y el valor es {valor}")
```

### Diccionarios y JSON
El formato JSON (JavaScript Object Notation) es un estándar abierto utilizado para intercambiar datos. JSON es muy similar a los diccionarios de Python; ambos utilizan pares de clave-valor. De hecho, en Python, un diccionario puede ser fácilmente convertido a JSON y viceversa, lo que hace que trabajar con APIs y almacenar datos en archivos sea muy sencillo.

Un ejemplo de JSON que representa un objeto similar a un diccionario podría ser:

```json
{
    "nombre": "Juan",
    "edad": 30,
    "ciudad": "Buenos Aires"
}
```

La principal diferencia es que las claves en JSON deben ser cadenas y se escriben entre comillas dobles `"`, mientras que en los diccionarios de Python, las claves pueden ser de cualquier tipo inmutable, y las comillas simples también son válidas.

En Python se pueden crear diccionarios de diccionarios. Un diccionario de diccionarios es simplemente un diccionario en el que los valores son a su vez otros diccionarios. Este tipo de estructura es útil para representar datos jerárquicos o anidados.

```python
# Crear un diccionario de diccionarios
diccionario = {
    'persona1': {
        'nombre': 'Juan',
        'edad': 30,
        'ciudad': 'Madrid'
    },
    'persona2': {
        'nombre': 'María',
        'edad': 25,
        'ciudad': 'Barcelona'
    },
    'persona3': {
        'nombre': 'Pedro',
        'edad': 35,
        'ciudad': 'Valencia'
    }
}

# Acceder a los datos
print(diccionario['persona1']['nombre'])  # Salida: Juan
print(diccionario['persona2']['edad'])    # Salida: 25
print(diccionario['persona3']['ciudad'])  # Salida: Valencia
```

Los diccionarios te permiten manejar y organizar datos de manera eficiente y flexible, y su similitud con JSON los hace especialmente útiles para interactuar con datos externos.

### Ejercicios Propuestos

#### **Ejercicio 1**:

Tienes un diccionario que almacena información sobre un empleado:
```python
empleado = {
    "nombre": "Ana",
    "edad": 28,
    "departamento": "Recursos Humanos",
    "antigüedad": 5
}
```
El problema es que necesitas mostrar un mensaje que indique cuántos años tiene el empleado y en qué departamento trabaja.

<details> <summary>Ver solución</summary>
```python
empleado = {
    "nombre": "Ana",
    "edad": 28,
    "departamento": "Recursos Humanos",
    "antigüedad": 5
}
print(f"{empleado['nombre']} tiene {empleado['edad']} anios y trabaja en {empleado['departamento']}")
```
</details>

#### **Ejercicio 2**:

**Considera** un diccionario que representa los productos en una tienda:
```python
productos = {
  "manzana": 50,
  "banana": 30,
  "naranja": 20,
  "pera": 15
}
```
La tienda quiere saber cuántas `manzanas` tienen en stock. Escribe un código que acceda a esta información y la muestre.

<details> <summary>Ver solución</summary>
```python
productos = {
  "manzana": 50,
  "banana": 30,
  "naranja": 20,
  "pera": 15
}
print(f"El stock actual de las manzanas es de: {productos['manzana']}")
```
</details>

#### **Ejercicio 3**:

Se tiene un diccionario con las respuestas de una encuesta:
```python
encuesta = {
    "nombre": "Carlos",
    "edad": 35,
    "respuesta_1": "Sí",
    "respuesta_2": "No",
    "respuesta_3": "Sí"
}
```
Necesitas extraer y mostrar las respuestas de la encuesta de manera que se indique claramente a qué pregunta corresponde cada respuesta.

<details> <summary>Ver solución</summary>
```python
encuesta = {
    "nombre": "Carlos",
    "edad": 35,
    "respuesta_1": "Sí",
    "respuesta_2": "No",
    "respuesta_3": "Sí"
}
cont = 0
for clave, valor in encuesta.items():
  if "respuesta" in clave:
    cont += 1
    print(f"La respuesta a la pregunta {cont} es \'{valor}\'")
```
</details>

<div class="navigation-buttons">
    <a href="./#/class02" class="prev-button">← Clase Anterior</a>
    <a href="./#/class04" class="next-button">Clase Siguiente →</a>
</div>
