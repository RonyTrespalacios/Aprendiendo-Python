# Sintaxis Básica y Tipos de Datos

## Estructura de un Programa en Python
La estructura básica de un programa en Python es simple y clara. Cada instrucción se escribe en una línea, y el uso de sangrías (espacios en blanco al principio de la línea) es crucial para definir bloques de código como funciones o estructuras de control. Python utiliza la indentación para delimitar estos bloques de código, lo cual es diferente de otros lenguajes que usan llaves `{}`.

## Declaración de Variables
Una variable en Python se declara simplemente asignándole un valor con el signo igual `=`. Python es un lenguaje de tipado dinámico, lo que significa que no necesitas declarar el tipo de la variable explícitamente; este se infiere automáticamente a partir del valor que se le asigna.

```python
nombre = "Juan"  # Una variable de tipo cadena (string)
edad = 30        # Una variable de tipo entero (int)
```

### Buenas Prácticas en la Declaración de Variables
- Utiliza nombres descriptivos para las variables que indiquen claramente lo que representan.
- Los nombres de las variables deben comenzar con una letra o un guion bajo (_), seguidos por letras, números o guiones bajos. No deben contener espacios.

## Tipos de Datos

### Enteros y Flotantes
Los enteros son números sin parte decimal, mientras que los flotantes son números con parte decimal. Estos tipos de datos se utilizan para representar números en cálculos matemáticos.

```python
numero_entero = 10
numero_flotante = 10.5
```

### Cadenas de Texto
Las cadenas (o strings) son secuencias de caracteres encerradas entre comillas simples o dobles. Las cadenas se usan para almacenar texto, como palabras o frases.

```python
mensaje = 'Hola, Mundo'
```

#### Concatenación de Cadenas
Puedes combinar (concatenar) cadenas utilizando el operador `+`. Esto es útil cuando quieres formar una frase o un mensaje a partir de múltiples partes.

```python
saludo = "Hola"
nombre = "Juan"
mensaje_completo = saludo + " " + nombre  # Combina el saludo con el nombre, separándolos por un espacio
print(mensaje_completo)  # Esto imprimirá "Hola Juan"
```

### Booleanos
Los valores booleanos representan verdad (`True`) o falsedad (`False`). Se utilizan en condiciones y decisiones lógicas en el programa. Estos valores son fundamentales cuando se desea realizar verificaciones o condiciones en el código, pero estos conceptos serán explorados más a fondo en las secciones posteriores.

```python
es_mayor_de_edad = True
```

## Uso de la Función `print()`
La función `print()` se utiliza para mostrar información en la pantalla. Es una de las funciones más básicas y útiles en Python, especialmente cuando estás depurando código o simplemente mostrando resultados.

```python
nombre = "Juan"
print(nombre)  # Esto imprimirá "Juan"
```

## Ejercicios Propuestos

### **Ejercicio 1**:

Declara una variable `nombre` y asígnale tu nombre como valor. Luego, utiliza la función `print()` para mostrar tu nombre en la pantalla.

<details> <summary>Ver solución</summary>
```python
nombre = "Rony"
print(nombre)
```
</details>

### **Ejercicio 2**:

Crea dos variables que almacenen números enteros, súmalos y muestra el resultado utilizando `print()`.

<details> <summary>Ver solución</summary>
```python
a = 2
b = 3
c = a + b
print("La suma entre "+str(a)+" y "+str(b)+" da "+str(c))
```
</details>

### **Ejercicio 3**:

Declara dos variables de tipo cadena que representen tu nombre y tu apellido. Luego, concaténalos para formar tu nombre completo y muestra el resultado en la pantalla.

<details> <summary>Ver solución</summary>
```python
nombre = "Rony"
apellido = "Trespalacios"
print("Hola, "+ nombre +" "+ apellido +"!")
```
</details>

<div class="navigation-buttons">
    <a href="./#/class02" class="next-button">Clase Siguiente →</a>
</div>