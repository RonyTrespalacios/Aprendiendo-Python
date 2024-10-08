# Estructuras de Datos II

## Tuplas como claves en diccionarios

En Python, las claves de los diccionarios deben ser **inmutables**, es decir, su valor no debe cambiar una vez que han sido creadas. Esto es crucial porque los diccionarios en Python utilizan una estructura de datos llamada **tabla hash** para almacenar las claves y valores. Para que una clave funcione correctamente en una tabla hash, debe tener un valor constante (no debe cambiar durante su vida útil) y debe ser **hashable**.

### Diferencias entre listas y tuplas en este contexto:

- **Listas**: Son **mutables**, lo que significa que puedes cambiar sus elementos (añadir, eliminar o modificar elementos) después de haber sido creadas. Debido a esta mutabilidad, las listas no tienen un hash constante; su valor puede cambiar, lo que rompería el funcionamiento de la tabla hash. Por lo tanto, las listas no pueden ser utilizadas como claves en un diccionario.

- **Tuplas**: Son **inmutables**, lo que significa que una vez que una tupla es creada, sus elementos no pueden cambiar. Esta inmutabilidad garantiza que el valor hash de una tupla permanezca constante durante su vida útil. Debido a esto, las tuplas pueden ser usadas como claves en un diccionario, ya que cumplen con los requisitos de inmutabilidad y hashabilidad.

### Ejemplo en código:

```python
# Ejemplo usando una tupla como clave en un diccionario
mi_diccionario = {
    (1, 2, 3): "valor para la tupla (1, 2, 3)",
    ("a", "b"): "valor para la tupla ('a', 'b')"
}

# Acceder a un valor en el diccionario usando una tupla como clave
print(mi_diccionario[(1, 2, 3)])  # Output: valor para la tupla (1, 2, 3)
print(mi_diccionario[("a", "b")])  # Output: valor para la tupla ('a', 'b')

# Intentar usar una lista como clave en un diccionario (esto generará un error)
try:
    mi_diccionario = {
        [1, 2, 3]: "valor para la lista [1, 2, 3]"
    }
except TypeError as e:
    print(f"Error: {e}")
```

### Explicación:

1. **Tuplas como claves**: En la primera parte del código, usamos tuplas `(1, 2, 3)` y `("a", "b")` como claves en el diccionario. Estas son válidas porque las tuplas son inmutables y hashables. Cuando intentamos acceder a los valores usando estas tuplas como claves, obtenemos los resultados esperados.

2. **Listas como claves**: En la segunda parte, intentamos crear un diccionario con una lista `[1, 2, 3]` como clave. Esto genera un `TypeError`, porque las listas no son hashables debido a su mutabilidad. Python no permite que las listas sean usadas como claves en diccionarios por esta razón.

### Salida esperada:
```python
valor para la tupla (1, 2, 3)
valor para la tupla ('a', 'b')
Error: unhashable type: 'list'
```

Este ejemplo demuestra la diferencia clave entre tuplas y listas en el contexto de las claves de un diccionario.

## Conjuntos (Sets)

Los conjuntos, o `sets`, son una estructura de datos en Python que almacenan elementos únicos y no ordenados. Esto significa que un conjunto no permite elementos duplicados y no mantiene ningún orden particular. Los conjuntos son útiles para realizar operaciones matemáticas como la unión, intersección y diferencia de conjuntos.

### Creación de Conjuntos
Puedes crear un conjunto utilizando llaves `{}` o la función `set()`.

```python
# Creando un conjunto con llaves
mi_conjunto = {1, 2, 3, 4, 5}

# Creando un conjunto usando la función set()
otro_conjunto = set([3, 4, 5, 6, 7])
```

### Características de los Conjuntos
- **Elementos Únicos**: Si intentas agregar un elemento que ya existe en el conjunto, no se añadirá nuevamente.
- **No Ordenados**: Los elementos de un conjunto no tienen un orden específico, por lo que no puedes acceder a ellos mediante un índice como en listas o tuplas.

```python
mi_conjunto = {1, 2, 3, 4, 4, 5}
print(mi_conjunto)  # Imprime {1, 2, 3, 4, 5}, los duplicados se eliminan automáticamente
```

### Operaciones con Conjuntos

Los conjuntos permiten realizar diversas operaciones matemáticas, como:

- **Unión**: Combina los elementos de dos conjuntos, eliminando duplicados.
  
```python
conjunto_a = {1, 2, 3}
conjunto_b = {3, 4, 5}
union = conjunto_a | conjunto_b  # Unión: {1, 2, 3, 4, 5}
```

- **Intersección**: Encuentra los elementos comunes entre dos conjuntos.
  
```python
interseccion = conjunto_a & conjunto_b  # Intersección: {3}
```

- **Diferencia**: Encuentra los elementos que están en un conjunto pero no en el otro.
  
```python
diferencia = conjunto_a - conjunto_b  # Diferencia: {1, 2}
```

- **Diferencia Simétrica**: Encuentra los elementos que están en uno u otro conjunto, pero no en ambos.
  
```python
dif_simetrica = conjunto_a ^ conjunto_b  # Diferencia Simétrica: {1, 2, 4, 5}
```

### Métodos Comunes para Conjuntos
Los conjuntos en Python vienen con varios métodos útiles que te permiten manipularlos de diferentes maneras:

- `add()`: Agrega un elemento al conjunto.
- `remove()`: Elimina un elemento del conjunto. Si el elemento no existe, se genera un error.
- `discard()`: Elimina un elemento del conjunto, pero no genera un error si el elemento no existe.
- `pop()`: Elimina y retorna un elemento aleatorio del conjunto.
- `clear()`: Elimina todos los elementos del conjunto.

```python
mi_conjunto = {1, 2, 3}
mi_conjunto.add(4)  # Agrega el número 4 al conjunto
mi_conjunto.remove(2)  # Elimina el número 2 del conjunto
print(mi_conjunto)  # Imprime {1, 3, 4}
```

Los conjuntos son muy útiles cuando trabajas con elementos únicos y necesitas realizar operaciones de conjunto.

## Ejercicios Propuestos

### **Ejercicio 1**:

Supón que tienes dos conjuntos que representan las habilidades de dos empleados:
```python
habilidades_empleado1 = {"Python", "Excel", "Trabajo en equipo"}
habilidades_empleado2 = {"Excel", "Comunicación", "Gestión de proyectos"}
```
El problema es determinar qué habilidades tienen en común ambos empleados.

<details> <summary>Ver solución</summary>
```python
habilidades_empleado1 = {"Python", "Excel", "Trabajo en equipo"}
habilidades_empleado2 = {"Excel", "Comunicación", "Gestión de proyectos"}
comun = habilidades_empleado1 & habilidades_empleado2
print(comun)
```
</details>

### **Ejercicio 2**:

Imagina que tienes un conjunto que contiene todos los productos disponibles en una tienda:
```python
productos_tienda = {"manzana", "banana", "naranja", "pera", "uva"}
```
Un cliente te pide una "naranja". Escribe un código para verificar si el producto está disponible en la tienda y luego elimínalo del conjunto si se vendió.

<details> <summary>Ver solución</summary>
```python
productos_tienda = {"manzana", "banana", "naranja", "pera", "uva"}
print(productos_tienda)
productos_tienda.discard("naranja")
print(productos_tienda)
```
</details>

### **Ejercicio 3**:

Considera dos conjuntos que representan a los estudiantes inscritos en dos cursos diferentes:
```python
curso_a = {"Juan", "Ana", "Luis", "María"}
curso_b = {"Luis", "Pedro", "Ana", "Clara"}
```
Muestra la lista de estudiantes que están inscritos en ambos cursos, y aquellos que están inscritos en solo uno de los cursos.

<details> <summary>Ver solución</summary>
```python
curso_a = {"Juan", "Ana", "Luis", "María"}
curso_b = {"Luis", "Pedro", "Ana", "Clara"}
both = curso_a & curso_b
print("Están en ambos cursos:", ", ".join(both))
single = curso_a ^ curso_b
print("Estan en un solocurso:", ", ".join(single))
```
</details>
