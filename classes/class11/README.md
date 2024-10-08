
# Introducción a Python y Strings


## Qué es un String

En Python, un *string* es una secuencia de caracteres, es decir, un conjunto de letras, números o símbolos que se agrupan para formar palabras, frases o cualquier tipo de texto. Los *strings* en Python se definen utilizando comillas simples (' ') o comillas dobles (" "). Por ejemplo:

```python
    # Definiendo un string en Python
    mi_string = 'Hola, Mundo'
    otro_string = "Bienvenido a Python"
```

Puedes usar tanto comillas simples como dobles, pero debes ser consistente, es decir, abrir y cerrar el string con el mismo tipo de comillas.

## Variables y Tipos de Datos

En Python, las *variables* son espacios en la memoria donde se almacenan datos que pueden ser utilizados más adelante. Los *strings* son uno de los tipos de datos más comunes en Python. Otros tipos incluyen enteros (int), flotantes (float), y booleanos (bool). Ejemplo de asignación de variables:

```python
    # Asignación de variables
    nombre = "Juan"
    edad = 25
    es_estudiante = True
```

## Índices y Acceso a Elementos

Cada carácter en un string tiene una posición (o índice) que comienza desde 0 para el primer carácter. Puedes acceder a un carácter específico en un string utilizando estos índices. Por ejemplo:

```python
    # Acceso a elementos en un string
    palabra = "Python"
    primer_caracter = palabra[0]  # Devuelve 'P'
    ultimo_caracter = palabra[-1]  # Devuelve 'n'
```

Los índices negativos permiten acceder a los caracteres desde el final de la cadena hacia el inicio.

## Slicing

El *slicing* es una técnica en Python que te permite extraer una porción (o subcadena) de un string. La sintaxis básica de slicing es `inicio:fin:paso`.

```python
    # Slicing en un string
    texto = "Aprendiendo Python"
    subcadena = texto[0:11]  # Devuelve 'Aprendiendo'
```

En este caso, `texto[0:11]` significa "toma los caracteres desde la posición 0 hasta la 11 (sin incluirla)". Puedes omitir `inicio` o `fin` para tomar todo el string desde el principio o hasta el final respectivamente.

```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Métodos de Acceso a Elementos y Slicing

## Slicing Avanzado

El *slicing* no solo te permite extraer subcadenas básicas; también puedes realizar operaciones más avanzadas, como invertir una cadena o extraer caracteres en intervalos específicos. A continuación, se presentan algunas técnicas avanzadas de slicing.

### Slicing con Paso Negativo

El *slicing* con un paso negativo permite invertir un string. Cuando especificas un paso negativo, Python recorre el string de derecha a izquierda.

```python
# Invertir un string usando slicing
texto = "Python"
texto_invertido = texto[::-1]  # Devuelve 'nohtyP'
```

### Slicing Omitiendo Inicio o Fin

Puedes omitir el índice de inicio o fin para tomar todo el string desde el principio o hasta el final respectivamente. Esto es útil cuando necesitas trabajar con una parte indefinida del string.

```python
# Omitir el índice de inicio
subcadena = texto[:4]  # Devuelve 'Pyth'

# Omitir el índice de fin
subcadena = texto[2:]  # Devuelve 'thon'
```

### Slicing con Paso Personalizado

Puedes definir un paso personalizado para seleccionar caracteres a intervalos específicos. Por ejemplo, tomar cada segundo carácter de una cadena.

```python
# Seleccionar cada segundo carácter
texto = "abcdefg"
resultado = texto[::2]  # Devuelve 'aceg'
```

## Acceso Directo a Elementos

Aparte del slicing, también puedes acceder directamente a elementos específicos de un string utilizando los métodos predefinidos de Python. Si bien los índices permiten acceder a un solo carácter, otros métodos permiten obtener partes más grandes o modificar la cadena.

### Acceso a Substrings

Python no tiene un método directo para obtener un substring específico como otros lenguajes, pero el slicing cubre esta necesidad. No obstante, es importante dominar el acceso mediante índices para manipular partes del string de manera eficiente.

### Acceso a Caracteres Únicos

Ya sea para extraer el primer o último carácter, o para verificar elementos en posiciones específicas, el acceso mediante índices es clave.

```python
# Acceder al primer y último carácter
primer_caracter = texto[0]
ultimo_caracter = texto[-1]
```

### Casos de Uso Empresariales

El slicing y el acceso a elementos son fundamentales cuando trabajas con datos textuales que requieren segmentación o análisis, como en el procesamiento de logs, la extracción de nombres o valores específicos, y la preparación de datos para análisis más detallados.


```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Operadores Básicos de Strings en Python

## Introducción

Python ofrece varios operadores básicos para comparar y verificar la presencia de subcadenas dentro de strings. Estos operadores son fundamentales en muchas operaciones de procesamiento de texto.

### Operador `in`

El operador `in` se utiliza para verificar si una subcadena está presente dentro de un string. Devuelve `True` si la subcadena se encuentra, y `False` en caso contrario.

```python
# Ejemplo con diccionario de diccionarios
empleados = {
    "empleado1": {"nombre": "Juan Perez", "departamento": "Ventas"},
    "empleado2": {"nombre": "Maria Lopez", "departamento": "Contabilidad"},
    "empleado3": {"nombre": "Carlos Gomez", "departamento": "IT"}
}

# Verificar si "Juan" está en el nombre del empleado1
resultado = "Juan" in empleados["empleado1"]["nombre"]  # Devuelve True
```

### Operador `not in`

El operador `not in` es lo opuesto a `in`. Verifica si una subcadena no está presente en un string.

```python
# Verificar si "Marketing" no está en el departamento del empleado2
resultado = "Marketing" not in empleados["empleado2"]["departamento"]  # Devuelve True
```

### Operador `==`

El operador `==` se utiliza para comparar dos strings. Devuelve `True` si las cadenas son exactamente iguales (sensibles a mayúsculas y minúsculas).

```python
# Comparar el departamento del empleado3 con "IT"
resultado = empleados["empleado3"]["departamento"] == "IT"  # Devuelve True
```

### Operador `!=`

El operador `!=` se utiliza para verificar si dos strings no son iguales. Devuelve `True` si las cadenas no son iguales.

```python
# Verificar si el nombre del empleado2 no es "Carlos Gomez"
resultado = empleados["empleado2"]["nombre"] != "Carlos Gomez"  # Devuelve True
```

## Ejercicios

### Ejercicio 1

Imagina que eres un gerente de recursos humanos y necesitas verificar si algún empleado en tu base de datos trabaja en el departamento de "Ventas". Utiliza los operadores `in` y `not in` para recorrer un diccionario de diccionarios que contiene la información de los empleados y retorna una lista con los nombres de aquellos que trabajan en "Ventas".

Ejemplo de diccionario de empleados:
```python
empleados = {
    "empleado1": {"nombre": "Juan Perez", "departamento": "Ventas"},
    "empleado2": {"nombre": "Maria Lopez", "departamento": "Contabilidad"},
    "empleado3": {"nombre": "Carlos Gomez", "departamento": "IT"},
    "empleado4": {"nombre": "Ana Martin", "departamento": "Marketing"},
    "empleado5": {"nombre": "Luis Hernandez", "departamento": "Ventas"}
}
```

### Ejercicio 2

Eres un desarrollador encargado de gestionar los accesos a una aplicación interna. Debes revisar una lista de usuarios con sus roles y asegurarte de que todos los administradores tienen el rol "admin". Si un usuario tiene el rol incorrecto, debes alertar sobre el problema. Utiliza operadores `==` y `!=` para resolver este problema.

Ejemplo de diccionario de usuarios:
```python
usuarios = {
    "user1": {"nombre": "admin1", "rol": "admin"},
    "user2": {"nombre": "usuario2", "rol": "user"},
    "user3": {"nombre": "admin2", "rol": "admin"},
    "user4": {"nombre": "usuario4", "rol": "user"},
    "user5": {"nombre": "admin3", "rol": "superuser"}
}
```

### Ejercicio 3

Como parte de un análisis de datos, necesitas verificar si ciertos productos están marcados como "disponibles" en una tienda online. Revisa un diccionario que contiene productos con sus estados y retorna una lista de aquellos que no están marcados como "disponibles". Utiliza los operadores `in` y `not in`.

Ejemplo de diccionario de productos:
```python
productos = {
    "producto1": {"nombre": "Camiseta", "estado": "disponible"},
    "producto2": {"nombre": "Pantalon", "estado": "no disponible"},
    "producto3": {"nombre": "Zapatos", "estado": "disponible"},
    "producto4": {"nombre": "Gorra", "estado": "no disponible"},
    "producto5": {"nombre": "Chaqueta", "estado": "disponible"}
}
```

# Método .strip() y .replace()

## Método .strip()

El método `.strip()` en Python se utiliza para eliminar los caracteres no deseados al inicio y al final de un string. Por defecto, elimina espacios en blanco, pero también puedes especificar otros caracteres a eliminar.

### Sintaxis
```python
    # Eliminando espacios en blanco
    texto = "   Hola, Mundo   "
    texto_sin_espacios = texto.strip()  # Devuelve 'Hola, Mundo'
```

### .lstrip() y .rstrip()
Existen también variantes como `.lstrip()` para eliminar caracteres solo al inicio de la cadena y `.rstrip()` para eliminarlos solo al final.

```python
    # Eliminando espacios en blanco solo al inicio
    texto_limpio_inicio = texto.lstrip()  # Devuelve 'Hola, Mundo   '

    # Eliminando espacios en blanco solo al final
    texto_limpio_final = texto.rstrip()  # Devuelve '   Hola, Mundo'
```

### Eliminación de Otros Caracteres
Puedes especificar qué caracteres deseas eliminar pasándolos como argumento al método `.strip()`.

```python
    # Eliminando caracteres específicos
    texto = "***Hola, Mundo***"
    texto_limpio = texto.strip('*')  # Devuelve 'Hola, Mundo'
```

## Método .replace()

El método `.replace()` se utiliza para reemplazar todas las ocurrencias de una subcadena en un string con otra subcadena. Es una herramienta fundamental para limpiar y modificar datos textuales.

### Sintaxis
```python
    # Reemplazando subcadenas
    texto = "Hola, Mundo"
    texto_reemplazado = texto.replace("Mundo", "Python")  # Devuelve 'Hola, Python'
```

### Reemplazo de Caracteres Especiales
Este método es particularmente útil para normalizar datos, por ejemplo, reemplazando caracteres especiales o eliminando partes no deseadas de un string.

```python
    # Reemplazando caracteres especiales
    texto = "Hola$Mundo$Python"
    texto_reemplazado = texto.replace("$", " ")  # Devuelve 'Hola Mundo Python'
```

### Casos de Uso Empresariales

El uso de `.strip()` y `.replace()` es crucial en el procesamiento y limpieza de datos textuales, donde es común recibir información con caracteres no deseados o formateada de manera inconsistente. Estos métodos ayudan a normalizar y preparar los datos para análisis posteriores.



```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Métodos .find() y .count()

El método `.find()` se utiliza para localizar la primera aparición de una subcadena dentro de un string. Este método devuelve el índice de la primera aparición de la subcadena o `-1` si la subcadena no se encuentra.

### Sintaxis
```python
    # Buscando una subcadena
    texto = "Hola, Mundo. Bienvenido al Mundo de Python"
    indice = texto.find("Mundo")  # Devuelve 6
```

En este ejemplo, el método `.find("Mundo")` devuelve `6` porque la primera aparición de "Mundo" comienza en el índice 6.

### .rfind()

El método `.rfind()` es similar a `.find()`, pero busca la última aparición de la subcadena dentro del string.

```python
    # Buscando la última aparición de una subcadena
    indice = texto.rfind("Mundo")  # Devuelve 24
```

## Método .count()

El método `.count()` se utiliza para contar cuántas veces aparece una subcadena en un string. Esto es útil cuando necesitas saber la frecuencia de un término específico dentro de un texto.

### Sintaxis
```python
    # Contando ocurrencias de una subcadena
    texto = "Hola, Mundo. Bienvenido al Mundo de Python"
    contador = texto.count("Mundo")  # Devuelve 2
```

En este ejemplo, el método `.count("Mundo")` devuelve `2` porque la subcadena "Mundo" aparece dos veces en el string.

### Uso Avanzado

Puedes combinar estos métodos para realizar búsquedas más complejas o para validar la presencia de una subcadena antes de realizar alguna operación.

```python
    # Buscando y reemplazando si se encuentra la subcadena
    if texto.find("Bienvenido") != -1:
        texto = texto.replace("Bienvenido", "Hola de nuevo")
```

### Casos de Uso Empresariales

Los métodos `.find()` y `.count()` son especialmente útiles en la minería de datos textuales, como en la búsqueda de patrones en registros de log, la verificación de la existencia de términos clave en descripciones de productos, o en el análisis de la frecuencia de palabras clave en documentos empresariales.



```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Métodos .split() y .join()

## Método .split()

El método `.split()` se utiliza para dividir un string en una lista de subcadenas, separando el string en cada ocurrencia de un delimitador especificado (por defecto, espacios en blanco).

### Sintaxis
```python
    # Dividiendo un string en palabras
    texto = "Aprendiendo Python paso a paso"
    palabras = texto.split()  # Devuelve ['Aprendiendo', 'Python', 'paso', 'a', 'paso']
```

### Especificar un Delimitador

Puedes especificar un delimitador personalizado para dividir el string según un carácter o conjunto de caracteres específicos.

```python
    # Dividiendo un string utilizando un delimitador específico
    texto = "nombre:Juan;edad:25;ciudad:Madrid"
    datos = texto.split(";")  # Devuelve ['nombre:Juan', 'edad:25', 'ciudad:Madrid']
```

En este ejemplo, el delimitador es el punto y coma `;`, lo que divide el string en subcadenas en cada aparición del delimitador.

### Limitar el Número de Divisiones

Puedes limitar el número de divisiones que se realizan utilizando el segundo argumento de `.split()`.

```python
    # Limitar las divisiones
    texto = "uno, dos, tres, cuatro, cinco"
    resultado = texto.split(", ", 2)  # Devuelve ['uno', 'dos', 'tres, cuatro, cinco']
```

Aquí, el string se divide solo en las dos primeras apariciones del delimitador `, `.

## Método .join()

El método `.join()` realiza la operación inversa a `.split()`. Toma una lista de subcadenas y las une en un único string, utilizando un delimitador especificado entre cada elemento.

### Sintaxis
```python
    # Uniendo una lista de palabras en un string
    palabras = ['Aprendiendo', 'Python', 'paso', 'a', 'paso']
    frase = " ".join(palabras)  # Devuelve 'Aprendiendo Python paso a paso'
```

### Usar un Delimitador Personalizado

Puedes unir los elementos de la lista utilizando cualquier string como delimitador.

```python
    # Uniendo con un delimitador personalizado
    datos = ['nombre:Juan', 'edad:25', 'ciudad:Madrid']
    texto = "; ".join(datos)  # Devuelve 'nombre:Juan; edad:25; ciudad:Madrid'
```

### Casos de Uso Empresariales

Los métodos `.split()` y `.join()` son muy útiles en la manipulación de datos textuales, como la transformación de datos estructurados (por ejemplo, CSV) en listas para procesamiento, o la conversión de listas de datos en strings formateados para reportes o almacenamiento en bases de datos.



```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Métodos .lower() y .upper()


## Método .lower()

El método `.lower()` en Python convierte todos los caracteres de un string a minúsculas. Este método es especialmente útil cuando se necesita normalizar el texto para comparaciones o almacenamiento.

### Sintaxis
```python
    # Convertir a minúsculas
    texto = "Hola, Mundo"
    texto_minusculas = texto.lower()  # Devuelve 'hola, mundo'
```

## Método .upper()

El método `.upper()` convierte todos los caracteres de un string a mayúsculas. Al igual que `.lower()`, es útil para normalizar datos textuales, especialmente en casos donde el formato uniforme es esencial, como en identificadores o claves.

### Sintaxis
```python
    # Convertir a mayúsculas
    texto = "Hola, Mundo"
    texto_mayusculas = texto.upper()  # Devuelve 'HOLA, MUNDO'
```

## Comparación Insensible a Mayúsculas y Minúsculas

Uno de los usos más comunes de `.lower()` y `.upper()` es realizar comparaciones de strings sin tener en cuenta las diferencias entre mayúsculas y minúsculas.

```python
    # Comparación insensible a mayúsculas/minúsculas
    texto1 = "Python"
    texto2 = "python"
    son_iguales = texto1.lower() == texto2.lower()  # Devuelve True
```

## Casos de Uso Empresariales

El uso de `.lower()` y `.upper()` es fundamental en escenarios donde se requiere la normalización de texto para asegurar la consistencia en las comparaciones y búsquedas. Esto es común en bases de datos, búsqueda de texto, y validaciones donde el formato del texto de entrada no es controlado, como en formularios de usuario o procesamiento de datos externos.



```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Métodos .startswith() y .endswith()


## Método .startswith()

El método `.startswith()` se utiliza para comprobar si un string comienza con una subcadena específica. Este método es muy útil para realizar validaciones o filtrados basados en el prefijo de un texto.

### Sintaxis
```python
    # Verificar si un string comienza con una subcadena
    texto = "Python es increíble"
    resultado = texto.startswith("Python")  # Devuelve True
```

Puedes especificar más de un prefijo como una tupla, y el método devolverá `True` si el string comienza con cualquiera de los prefijos proporcionados.

```python
    # Verificar múltiples prefijos
    resultado = texto.startswith(("Python", "Java"))  # Devuelve True
```

## Método .endswith()

El método `.endswith()` funciona de manera similar a `.startswith()`, pero verifica si un string termina con una subcadena específica.

### Sintaxis
```python
    # Verificar si un string termina con una subcadena
    texto = "Aprendiendo Python"
    resultado = texto.endswith("Python")  # Devuelve True
```

Al igual que con `.startswith()`, puedes proporcionar una tupla de posibles sufijos.

```python
    # Verificar múltiples sufijos
    resultado = texto.endswith(("Python", "Java"))  # Devuelve True
```

## Casos de Uso Empresariales

Los métodos `.startswith()` y `.endswith()` son esenciales en tareas como la validación de archivos (por ejemplo, asegurarse de que un archivo tiene una extensión específica), la verificación de formatos de datos, y el filtrado de registros en bases de datos que cumplen con ciertos criterios de inicio o finalización de texto.



```python
# Aqui puedes hacer pruebas de lo aprendido
```


# Método .isalnum()



## Método .isalnum()

El método `.isalnum()` se utiliza para verificar si todos los caracteres de un string son alfanuméricos, es decir, si el string contiene solo letras y números, sin espacios ni caracteres especiales. Este método es muy útil en la validación de entradas de usuario, como nombres de usuario, códigos de productos, o cualquier dato que deba ser exclusivamente alfanumérico.

### Sintaxis
```python
    # Verificar si un string es alfanumérico
    texto = "Python123"
    es_alfanumerico = texto.isalnum()  # Devuelve True
```

### Características y Consideraciones

- Si el string contiene solo letras y números, `.isalnum()` devuelve `True`.
- Si el string está vacío, contiene espacios, o incluye cualquier carácter no alfanumérico, el método devuelve `False`.

```python
    # Ejemplos adicionales
    "Python 123".isalnum()   # Devuelve False (contiene un espacio)
    "Python123!".isalnum()   # Devuelve False (contiene un carácter especial)
    "".isalnum()             # Devuelve False (cadena vacía)
```

### Casos de Uso Empresariales

El método `.isalnum()` es esencial en la validación de datos donde se espera que los usuarios ingresen solo caracteres alfanuméricos, como en formularios de registro, generación de códigos de producto, o validación de entradas que no deben contener espacios ni caracteres especiales para mantener la integridad del sistema.



```python
# Aqui puedes hacer pruebas de lo aprendido
```


# Método .isnumeric()

El método `.isnumeric()` en Python se utiliza para verificar si todos los caracteres en un string son numéricos. Esto incluye dígitos, subíndices y caracteres fraccionarios, pero no incluye números con punto decimal o signos como el negativo.

### Sintaxis
```python
# Verificar si un string es numérico
texto = "12345"
es_numerico = texto.isnumeric()  # Devuelve True
```

### Características y Consideraciones

- Si el string contiene solo caracteres numéricos (0-9) o caracteres que representen números, `.isnumeric()` devolverá `True`.
- Si el string contiene caracteres no numéricos, como letras, espacios, o puntuación, devolverá `False`.
- Este método es más inclusivo que `.isdigit()`, ya que también reconoce números en otros sistemas numéricos y caracteres especiales que representan números.

```python
# Ejemplos adicionales
"123.45".isnumeric()  # Devuelve False (punto decimal no es considerado numérico)
"½".isnumeric()       # Devuelve True (carácter fraccionario)
"2²".isnumeric()      # Devuelve True (subíndice)
"123abc".isnumeric()  # Devuelve False (contiene letras)
```

### Casos de Uso Empresariales

El método `.isnumeric()` es particularmente útil cuando necesitas asegurarte de que un string contiene solo números, como en la validación de números de teléfono, códigos postales, identificadores numéricos, o cualquier otra entrada donde los datos deben consistir exclusivamente en valores numéricos.



```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Método .isalpha()


## Método .isalpha()

El método `.isalpha()` en Python se utiliza para verificar si todos los caracteres en un string son letras del alfabeto. Este método es útil cuando necesitas validar que un string contiene únicamente caracteres alfabéticos, sin números, espacios, ni caracteres especiales.

### Sintaxis
```python
# Verificar si un string contiene solo letras
texto = "Python"
es_alfabetico = texto.isalpha()  # Devuelve True
```

### Características y Consideraciones

- Si el string contiene solo letras (a-z, A-Z) y no está vacío, `.isalpha()` devolverá `True`.
- Si el string contiene números, espacios, o cualquier carácter que no sea una letra, el método devolverá `False`.

```python
# Ejemplos adicionales
"Python3".isalpha()   # Devuelve False (contiene un número)
"Python!".isalpha()   # Devuelve False (contiene un carácter especial)
"Python Rocks".isalpha()  # Devuelve False (contiene un espacio)
"".isalpha()  # Devuelve False (cadena vacía)
```

### Casos de Uso Empresariales

El método `.isalpha()` es particularmente útil en la validación de nombres, apellidos, y otros campos donde se espera que la entrada contenga solo letras. Esto es común en formularios de registro, procesamiento de datos de clientes, y cualquier situación en la que se necesite asegurar que los datos textuales no incluyen números ni caracteres especiales.



```python
# Aqui puedes hacer pruebas de lo aprendido
```


# Manipulación Avanzada de Strings (Combinación de Métodos)

## Combinación de Métodos

La verdadera potencia de los métodos de manipulación de strings en Python se revela cuando se combinan varios métodos para resolver problemas más complejos. Esta sección explora cómo puedes encadenar métodos para realizar tareas de manipulación de texto de manera más eficiente.

### Ejemplo 1: Normalización de Nombres

Supongamos que tienes una lista de nombres que vienen en diferentes formatos y necesitas estandarizarlos para que todos tengan la primera letra en mayúscula y el resto en minúsculas.

```python
# Lista de nombres desordenados
nombres = ["JUAN", "Maria", "carlos", "LUISA"]

# Normalizar nombres
nombres_normalizados = [nombre.strip().capitalize() for nombre in nombres]

# Resultado: ['Juan', 'Maria', 'Carlos', 'Luisa']
```

En este ejemplo, usamos `.strip()` para eliminar cualquier espacio en blanco al inicio o al final, y luego `.capitalize()` para asegurarnos de que el nombre esté en el formato correcto.

### Ejemplo 2: Validación y Extracción de Datos

Considera un escenario donde tienes que extraer el dominio de correos electrónicos y verificar que todos los correos pertenezcan a un dominio específico.

```python
# Lista de correos electrónicos
correos = ["juan@gmail.com", "maria@empresa.com", "carlos@empresa.com"]

# Extracción y validación de dominio
dominio_objetivo = "empresa.com"
correos_validos = [correo for correo in correos if correo.endswith(dominio_objetivo)]

# Resultado: ['maria@empresa.com', 'carlos@empresa.com']
```

Aquí utilizamos `.endswith()` para filtrar los correos electrónicos que terminan con el dominio deseado.

### Ejemplo 3: Limpieza y Formateo de Datos

Imagina que tienes un conjunto de datos con números de teléfono que incluyen caracteres no deseados como paréntesis, guiones, y espacios. Necesitas limpiar estos números para dejarlos solo con dígitos.

```python
# Lista de números de teléfono
telefonos = ["(123) 456-7890", "987-654-3210", "456 789 1234"]

# Limpieza de números de teléfono
telefonos_limpios = [telefono.replace("(", "").replace(")", "").replace("-", "").replace(" ", "") for telefono in telefonos]

# Resultado: ['1234567890', '9876543210', '4567891234']
```

En este caso, usamos `.replace()` en combinación para eliminar los caracteres no deseados y dejar los números en un formato uniforme.

### Casos de Uso Empresariales

La combinación de métodos es crucial en tareas complejas de procesamiento de datos, como la limpieza y normalización de bases de datos, la preparación de datos para análisis, la generación de reportes automatizados, y la validación de entradas de usuario en aplicaciones web. Estos ejemplos ilustran cómo puedes utilizar múltiples métodos de strings juntos para realizar transformaciones y validaciones avanzadas de datos textuales de manera eficiente.



```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Validación de Datos con Strings

## Importancia de la Validación de Datos

La validación de datos es un proceso crucial en el manejo de información, especialmente en aplicaciones empresariales donde los datos incorrectos o mal formateados pueden llevar a errores significativos. Al trabajar con strings, Python proporciona una serie de métodos que ayudan a validar la estructura y contenido de los datos.

## Métodos de Validación Básica

### Uso de .isalnum(), .isalpha(), .isnumeric()

Estos métodos permiten verificar si un string contiene solo caracteres alfanuméricos, solo letras, o solo números respectivamente. Son útiles para validar entradas en formularios, asegurarse de que los códigos de productos sean válidos, o que los nombres no contengan números o caracteres especiales.

```python
# Validación de un nombre
nombre = "JuanCarlos"
if nombre.isalpha():
    print("Nombre válido")
else:
    print("Nombre inválido")

# Validación de un código de producto
codigo_producto = "AB12345"
if codigo_producto.isalnum():
    print("Código de producto válido")
else:
    print("Código de producto inválido")
```

### Validación de Correos Electrónicos con .find() y .split()

Aunque los métodos como `.find()` y `.split()` no están diseñados específicamente para la validación, pueden ser combinados para verificar la estructura de un correo electrónico básico.

```python
# Validación simple de correo electrónico
correo = "usuario@dominio.com"
if correo.find("@") != -1 and correo.split("@")[1].find(".") != -1:
    print("Correo electrónico válido")
else:
    print("Correo electrónico inválido")
```

## Uso de Expresiones Regulares (Breve Introducción)

Para validaciones más complejas, como asegurar que un correo electrónico, un número de teléfono, o un código postal cumple con un formato específico, Python ofrece las expresiones regulares (regex). Aunque no profundizaremos en regex aquí, es importante saber que es una herramienta poderosa para validación avanzada.

```python
import re

# Validación avanzada de correo electrónico usando regex
correo = "usuario@dominio.com"
patron = r'^\w+@\w+\.\w+$'
if re.match(patron, correo):
    print("Correo electrónico válido")
else:
    print("Correo electrónico inválido")
```

## Casos de Uso Empresariales

La validación de datos es esencial en cualquier aplicación que maneje información de usuarios, como registros en bases de datos, procesamiento de formularios en aplicaciones web, o sistemas de control de inventarios. Asegurar que los datos sean correctos y estén en el formato adecuado ayuda a evitar errores en el procesamiento y análisis, mejora la calidad de los datos y, en última instancia, la toma de decisiones basada en esos datos.

```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Limpieza y Normalización de Datos Textuales

## Importancia de la Limpieza y Normalización

En el análisis de datos, especialmente cuando se trabaja con datos textuales, la limpieza y normalización son pasos fundamentales para asegurar la calidad de los datos. Los datos textuales en bruto suelen venir con inconsistencias como espacios en blanco adicionales, caracteres especiales, y variaciones en mayúsculas y minúsculas. Estas inconsistencias pueden afectar el análisis y los resultados obtenidos.

## Métodos Comunes para Limpieza y Normalización

### Eliminar Espacios en Blanco con .strip(), .lstrip(), .rstrip()

Uno de los problemas más comunes es la presencia de espacios en blanco al inicio o al final de un string. Utiliza `.strip()`, `.lstrip()`, y `.rstrip()` para eliminar estos espacios.

```python
# Eliminación de espacios en blanco
texto = "   Análisis de Datos   "
texto_limpio = texto.strip()  # Devuelve 'Análisis de Datos'
```

### Reemplazar o Eliminar Caracteres Especiales con .replace()

Otro paso clave en la limpieza de datos es el manejo de caracteres especiales que pueden interferir con el análisis. Utiliza `.replace()` para reemplazar o eliminar estos caracteres.

```python
# Reemplazo de caracteres especiales
texto = "Análisis@de#Datos!"
texto_limpio = texto.replace("@", "").replace("#", "").replace("!", "")  # Devuelve 'Análisis de Datos'
```

### Normalizar Mayúsculas y Minúsculas con .lower() y .upper()

Para asegurar que las comparaciones y búsquedas en strings sean consistentes, es común normalizar todos los textos a minúsculas o mayúsculas.

```python
# Normalización a minúsculas
texto = "Análisis de Datos"
texto_normalizado = texto.lower()  # Devuelve 'análisis de datos'
```

### Eliminar Múltiples Espacios con .split() y .join()

A veces los textos contienen múltiples espacios entre palabras, lo que puede complicar su procesamiento. Un truco útil es dividir el texto en palabras y luego volver a unirlo, lo que elimina los espacios adicionales.

```python
# Eliminación de espacios adicionales
texto = "Análisis     de   Datos"
texto_limpio = " ".join(texto.split())  # Devuelve 'Análisis de Datos'
```

## Casos de Uso Empresariales

La limpieza y normalización de datos textuales son cruciales en cualquier proceso de análisis de datos, ya que mejoran la precisión de las búsquedas, comparaciones y análisis. Por ejemplo, en la minería de datos, la generación de informes, o en la preparación de datos para modelos de machine learning, tener datos limpios y consistentes es esencial para obtener resultados confiables y significativos.

```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Generación Dinámica de Strings


## Introducción a la Generación Dinámica de Strings

En muchos casos, necesitarás generar cadenas de texto dinámicamente a partir de variables o combinando diferentes elementos. Esto es particularmente útil en la creación de mensajes personalizados, generación de informes, o construcción de queries SQL de forma programática.

## Uso de F-Strings para Formateo de Strings

Las *f-strings* son una forma eficiente y legible de insertar valores de variables dentro de un string. Las *f-strings* se introdujeron en Python 3.6 y permiten incluir expresiones dentro de llaves `{}` que se evaluarán en tiempo de ejecución.

### Sintaxis
```python
# Uso de f-strings
nombre = "Juan"
edad = 28
mensaje = f"Hola, mi nombre es {nombre} y tengo {edad} años."
# Devuelve: 'Hola, mi nombre es Juan y tengo 28 años.'
```

Las *f-strings* son flexibles y pueden incluir cualquier expresión válida de Python.

```python
# Expresiones dentro de f-strings
numero = 10
mensaje = f"El doble de {numero} es {numero * 2}."
# Devuelve: 'El doble de 10 es 20.'
```

## Método .format() para Formateo

Antes de las *f-strings*, el método `.format()` era la forma más común de formatear strings en Python. Aunque más verboso que las *f-strings*, sigue siendo útil y compatible con versiones anteriores de Python.

### Sintaxis
```python
# Uso de .format()
nombre = "Ana"
edad = 30
mensaje = "Hola, mi nombre es {} y tengo {} años.".format(nombre, edad)
# Devuelve: 'Hola, mi nombre es Ana y tengo 30 años.'
```

Puedes especificar los valores por posición o nombre, lo que permite una mayor flexibilidad.

```python
# Formateo nombrado
mensaje = "Hola, mi nombre es {nombre} y tengo {edad} años.".format(nombre="Luis", edad=35)
# Devuelve: 'Hola, mi nombre es Luis y tengo 35 años.'
```

## Concatenación Avanzada de Strings

Otra técnica útil para generar strings dinámicamente es la concatenación, donde se combinan varios strings o variables para formar uno nuevo. Aunque menos eficiente que las *f-strings* o `.format()`, sigue siendo una herramienta básica.

### Sintaxis
```python
# Concatenación de strings
saludo = "Hola, "
nombre = "Marta"
mensaje = saludo + nombre + "!"
# Devuelve: 'Hola, Marta!'
```

## Casos de Uso Empresariales

La generación dinámica de strings es esencial en muchas aplicaciones empresariales, como la creación de correos electrónicos personalizados, generación de reportes, plantillas dinámicas, o incluso la construcción de comandos y consultas SQL en bases de datos. La capacidad de construir strings de manera flexible y eficiente es una habilidad clave en el desarrollo de software y análisis de datos.



```python
# Aqui puedes hacer pruebas de lo aprendido
```

# Ejercicios Combinados de Manipulación de Strings - Grupo 1

## Ejercicio 1


Tienes una lista de nombres de empleados en una empresa, algunos de los cuales están en mayúsculas y otros en minúsculas. Necesitas normalizar los nombres para que todos comiencen con una letra mayúscula y el resto en minúsculas. Además, elimina cualquier espacio en blanco al inicio o final de los nombres.

Ejemplo de lista de nombres:
```python
nombres_empleados = ["juan perez", "MARIA LOPEZ", "Ana MARTIN", " lucas DIAZ "]
```

## Ejercicio 2


Se te proporciona un diccionario con productos y sus códigos. Algunos códigos contienen caracteres especiales que no deberían estar presentes. Tu tarea es limpiar los códigos eliminando cualquier carácter especial y dejar solo letras y números. Luego, muestra los productos con sus códigos limpios.

Ejemplo de diccionario:
```python
productos = {
    "Producto A": "AB#123!",
    "Producto B": "CD@456$",
    "Producto C": "EF-789&"
}
```


## Ejercicio 3

En una base de datos de correos electrónicos, necesitas extraer solo aquellos correos que pertenecen al dominio "empresa.com". Los correos están almacenados en una lista. Extrae los correos válidos y muéstralos.

Ejemplo de lista de correos:
```python
correos = ["juan@gmail.com", "maria@empresa.com", "carlos@empresa.com", "ana@yahoo.com"]
```

## Ejercicio 4

Un sistema de gestión de inventarios te proporciona una lista de números de serie que contienen espacios y caracteres no numéricos. Debes limpiar los números de serie para que contengan solo los dígitos. Luego, verifica si todos los números de serie tienen exactamente 10 dígitos y muestra cuáles son válidos.

Ejemplo de lista de números de serie:
```python
numeros_serie = ["123 456 7890", "987-654-321", "1112223333", "12345abcde"]
```

## Ejercicio 5


Solicita al usuario que ingrese un nombre completo (nombre y apellido). Luego, verifica que el nombre completo no contenga números ni caracteres especiales. Si es válido, muestra el nombre formateado en mayúsculas para el apellido y capitalizado para el nombre.

Entrada del usuario:
```python
input("Por favor, ingrese su nombre completo: ")
```


# Ejercicios Combinados de Manipulación de Strings - Grupo 2

## Ejercicio 6 - Electrónica

En una empresa de electrónica, los ingenieros necesitan verificar que los números de modelo de los componentes cumplan con un formato específico: deben comenzar con "MOD-", seguido de exactamente 5 dígitos. Tienes una lista de números de modelo y necesitas filtrar cuáles cumplen con este formato.

Ejemplo de lista de números de modelo:
```python
modelos = ["MOD-12345", "MOD-6789A", "MOD-98765", "12345-MOD"]
```

## Ejercicio 7 - Finanzas

Un analista financiero está revisando un archivo de texto que contiene una lista de transacciones con sus montos. Algunas transacciones están mal formateadas, con símbolos de moneda adicionales o espacios innecesarios. Limpia cada transacción para que solo contenga el monto en formato numérico, sin símbolos de moneda ni espacios.

Ejemplo de lista de transacciones:
```python
transacciones = ["$ 1,200.50", "3000 ", " 1500.75$", "$200"]
```

## Ejercicio 8 - Agroindustria

En una empresa agroindustrial, se necesita extraer el tipo de cultivo de una lista de identificadores de lote. Cada identificador sigue el formato "LOTE-XXX-CULTIVO", donde "CULTIVO" es el nombre del cultivo. Extrae el nombre del cultivo y muestra una lista con todos los tipos de cultivo presentes.

Ejemplo de lista de identificadores:
```python
lotes = ["LOTE-001-MAIZ", "LOTE-002-TRIGO", "LOTE-003-SOYA", "LOTE-004-MAIZ"]
```

## Ejercicio 9 - Mecánica

Un taller de mecánica recibe piezas con números de serie que incluyen el tipo de material. El formato del número de serie es "SERIE-TIPO-MATERIAL". Necesitas agrupar las piezas por el tipo de material y mostrar cuántas piezas de cada tipo hay.

Ejemplo de lista de números de serie:
```python
piezas = ["123-ACERO-1", "456-HIERRO-2", "789-ACERO-3", "321-HIERRO-4", "654-PLASTICO-5"]
```

## Ejercicio 10 - Mercadeo



El equipo de mercadeo necesita crear una campaña personalizada utilizando los nombres de los clientes. Tienes una lista de nombres completos, pero necesitan ser formateados correctamente: cada palabra debe comenzar con mayúscula y los nombres deben ser separados por comas en un único string.

Ejemplo de lista de nombres:
```python
nombres = ["juan perez", "MARIA LOPEZ", "carlos MENDOZA", "Ana garcia"]
```


# Ejercicios Combinados de Manipulación de Strings - Grupo 3

## Ejercicio 11 - Tecnología

Imagina que eres un ingeniero de software en una empresa de tecnología encargada de manejar una plataforma global de usuarios. Tu equipo ha identificado que los nombres de usuario deben ser únicos y estar formateados correctamente antes de almacenarse en la base de datos. Se ha descubierto que algunos nombres contienen espacios, caracteres especiales o están duplicados. Tu tarea es procesar una lista de nombres de usuario para eliminar duplicados, asegurar que estén en minúsculas, y que no contengan espacios ni caracteres especiales. Luego, deberás generar una lista final de usuarios únicos listos para ser almacenados.

Ejemplo de lista de nombres de usuario:
```python
usuarios = ["User_01", "user 02", "USER03", "User-04", "user_01", "user02", "USER-05", "user-06", "USER07 ", " User08", "user_01", "User-09", "user10"]
```

## Ejercicio 12 - Biotecnología

Imagina que trabajas en un laboratorio de biotecnología que maneja una base de datos de muestras genéticas. Cada muestra tiene un identificador que sigue el formato "GENOMA-XX-XXXX", donde las primeras seis letras indican el tipo de genoma, el siguiente segmento indica el lote, y el último segmento es el número de la muestra. Necesitas extraer el tipo de genoma de cada identificador y agrupar las muestras por tipo de genoma para un informe de análisis. Además, asegúrate de que los identificadores estén limpios de cualquier carácter no deseado antes de agruparlos.

Ejemplo de identificadores de muestras:
```python
muestras = ["GENOMA-A1-BB01", "GENOMA-B2-CC02", "GENOMA-A1-DD03", "GENOMA-B2-EE04", "GENOMA-A1-FF05", "GENOMA-C3-GG06", "GENOMA-C3-HH07", "GENOMA-A1-II08", "GENOMA-B2-JJ09", "GENOMA-C3-KK10"]
```

## Ejercicio 13 - Salud

Imagina que eres un analista de datos en un hospital que debe procesar una gran base de datos de pacientes. Los datos están almacenados en un formato de string "Nombre_Apellido_Edad". Tu tarea es extraer el apellido y la edad de cada paciente, y luego crear un diccionario donde las claves sean los apellidos y los valores sean las edades. Además, asegúrate de que no haya duplicados y que los datos estén correctamente formateados antes de crear el diccionario.

Ejemplo de lista de pacientes:
```python
pacientes = ["Juan_Perez_30", "Maria_Lopez_25", "Carlos_Gomez_45", "Ana_Martin_32", "Lucia_Garcia_28", "Pedro_Rodriguez_50", "Luis_Hernandez_33", "Jorge_Perez_40", "Ana_Martin_32", "Carlos_Gomez_45"]
```

## Ejercicio 14 - Retail

Imagina que trabajas en una gran empresa de retail que está a punto de lanzar una campaña promocional masiva. Necesitas generar códigos de descuento únicos para los clientes que participen en la campaña. Cada código debe estar formado por las iniciales del cliente y un número aleatorio de 4 dígitos. Además, todos los códigos deben estar en mayúsculas y no deben repetirse. Después de generar los códigos, asegúrate de que todos son únicos y compártelos con el equipo de marketing.

Ejemplo de lista de nombres de clientes:
```python
clientes = ["Juan Perez", "Maria Lopez", "Carlos Gomez", "Ana Martin", "Lucia Garcia", "Pedro Rodriguez", "Luis Hernandez", "Jorge Perez", "Ana Martin", "Carlos Gomez"]
```

## Ejercicio 15 - Automotriz

Imagina que eres un ingeniero en una empresa automotriz que ha recibido una lista de números de serie de piezas provenientes de diferentes proveedores. Los números de serie están en diferentes formatos y algunos contienen caracteres no deseados que deben ser eliminados antes de que puedan ser utilizados en el sistema de inventario. Debes limpiar los números de serie, extraer los componentes válidos, y generar un informe donde cada número de serie esté en un formato uniforme listo para ser ingresado en la base de datos de inventario.

Ejemplo de lista de números de serie:
```python
series = ["1234-ABC-5678", "8765-XYZ 4321", "1357- DEF -2468", "2468GHI3579", "9876-JKL-5432", "6543-MNO 2109", "3210-PQR-8765", "4321-STU 0987", "7654-VWX-1234", "5432-YZA-6789"]
```


# Ejercicios Combinados de Manipulación de Strings - Grupo 4 (Avanzado)

## Ejercicio 16

Tienes una base de datos de empleados almacenada como una lista de tuplas, donde cada tupla contiene el nombre completo del empleado, su número de identificación, y su departamento. Debes generar un reporte que liste los nombres de los empleados en orden alfabético por apellido, pero también debes incluir solo los empleados cuyo número de identificación termine en un dígito par. Además, el formato de salida debe ser "Apellido, Nombre (ID) - Departamento".

Ejemplo de base de datos:
```python
empleados = [("Juan Perez", "12345", "Ventas"),
             ("Maria Lopez", "67890", "Contabilidad"),
             ("Carlos Gomez", "54321", "IT"),
             ("Ana Martin", "09876", "Marketing"),
             ("Luis Hernandez", "24680", "Ventas"),
             ("Jorge Garcia", "13579", "IT"),
             ("Lucia Rodriguez", "86420", "Contabilidad"),
             ("Pedro Alvarez", "11223", "Marketing"),
             ("Sofia Martinez", "55667", "IT"),
             ("Miguel Suarez", "90876", "Ventas")]
```

Salida esperada:
```python
Alvarez, Pedro (11223) - Marketing
Hernandez, Luis (24680) - Ventas
Lopez, Maria (67890) - Contabilidad
Martin, Ana (09876) - Marketing
Rodriguez, Lucia (86420) - Contabilidad
Suarez, Miguel (90876) - Ventas
```

## Ejercicio 17

Se te proporciona una lista de transacciones financieras realizadas durante un mes. Cada transacción está en formato de string que contiene la fecha, el tipo de transacción (crédito o débito), y el monto. Debes procesar la lista para calcular el balance total al final del mes. Además, asegúrate de que las fechas estén en el formato "DD/MM/YYYY" y los montos estén correctamente formateados sin caracteres extraños. Las transacciones de crédito aumentan el balance y las de débito lo disminuyen.

Ejemplo de lista de transacciones:
```python
transacciones = ["01/07/2024, crédito, +1500.00",
                 "03-07-2024, débito, -200.50",
                 "05/07/2024, crédito, +1000",
                 "07/07/2024, debito, -500",
                 "09/07/2024, crédito, +2000.50",
                 "11/07/2024, debito, -750.25",
                 "13/07/2024, crédito, +3000.75",
                 "15-07-2024, debito, -1200.00",
                 "17/07/2024, crédito, +400.00",
                 "19/07/2024, debito, -300"]
```

Salida esperada:
```python
Balance final: 7950.50
```

## Ejercicio 18

Tienes una lista de correos electrónicos y necesitas verificar cuáles son válidos. Un correo electrónico es válido si tiene exactamente un símbolo "@" y al menos un punto después de "@" en el dominio. Además, los correos deben estar en minúsculas. Genera una lista con los correos válidos y formatea la salida para que cada correo esté precedido por su índice en la lista original.

Ejemplo de lista de correos:
```python
correos = ["Usuario@dominio.com", "usuario2@dominio", "usuario3@dominio.net",
           "usuario4@otrodominio.com", "Usuario5@dominio.", "usuario6@dominio.com",
           "usuario7@@dominio.com", "usuario8@dominio.org", "usuario9@dominio",
           "usuario10@dominio.com"]
```

Salida esperada:
```python
0: usuario@dominio.com
2: usuario3@dominio.net
3: usuario4@otrodominio.com
5: usuario6@dominio.com
7: usuario8@dominio.org
9: usuario10@dominio.com
```

## Ejercicio 19

Imagina que estás desarrollando una aplicación para gestionar el inventario de una tienda online. Tienes una lista de productos donde cada producto es un string que contiene el nombre del producto, el código de identificación, y la cantidad disponible en stock. Debes generar un reporte de todos los productos cuyo stock esté por debajo de un umbral de seguridad (5 unidades). Además, los códigos de identificación deben ser validados: deben contener solo letras y números, y deben tener exactamente 6 caract...

Ejemplo de lista de productos:
```python
productos = ["Camiseta, ABC123, 10",
             "Pantalon, DEF456, 3",
             "Zapatos, GHI789, 0",
             "Gorra, JKL012, 6",
             "Cinturon, MNO345, 2",
             "Chaqueta, PQR678, 5",
             "Bufanda, STU901, 1",
             "Calcetines, VWX234, 8",
             "Reloj, YZA567, 4",
             "Bolso, BCD890, 9"]
```

Salida esperada:
```python
Productos con stock bajo:
Pantalon (DEF456): 3 unidades
Zapatos (GHI789): 0 unidades
Cinturon (MNO345): 2 unidades
Bufanda (STU901): 1 unidades
Reloj (YZA567): 4 unidades
```

## Ejercicio 20

Eres un ingeniero de datos que debe procesar una base de datos de clientes donde cada registro contiene el nombre completo, la dirección, y el número de teléfono del cliente, todo en un solo string. Debes extraer y validar los datos de cada cliente. Las direcciones deben ser capitalizadas correctamente, los números de teléfono deben contener solo dígitos y tener exactamente 10 dígitos, y los nombres deben estar en formato "Apellido, Nombre". Finalmente, genera un informe con todos los datos procesados en...

Ejemplo de base de datos de clientes:
```python
clientes = ["Juan Perez, calle falsa 123, 123-456-7890",
            "Maria Lopez, Av. siempre viva 742, (098) 765-4321",
            "Carlos Gomez, 1ª calle 555, 987654321",
            "Ana Martin, avenida siempreviva 123, 0123456789",
            "Lucia Garcia, Camino Real, 654-321-0987",
            "Pedro Rodriguez, calle 123, 1234567890",
            "Luis Hernandez, av. principal 123, 321-654-9870",
            "Jorge Perez, 5ta avenida 321, 4321098765",
            "Ana Martin, paseo de la reforma, 9876543210",
            "Carlos Gomez, calle uno, 5678901234"]
```

Salida esperada:
```python
Perez, Juan - Calle Falsa 123 - 1234567890
Lopez, Maria - Av. Siempre Viva 742 - 0987654321
Gomez, Carlos - 1ª Calle 555 - 0987654321
Martin, Ana - Avenida Siempreviva 123 - 0123456789
Garcia, Lucia - Camino Real - 6543210987
Rodriguez, Pedro - Calle 123 - 1234567890
Hernandez, Luis - Av. Principal 123 - 3216549870
Perez, Jorge - 5ta Avenida 321 - 4321098765
Martin, Ana - Paseo De La Reforma - 9876543210
Gomez, Carlos - Calle Uno - 5678901234
```

