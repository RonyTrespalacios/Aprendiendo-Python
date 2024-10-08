# Programación Orientada a Objetos en Python

## 1. Introducción a la Programación Orientada a Objetos (POO)
## 2. Definición de Clases en Python

### 1.1. Qué es la Programación Orientada a Objetos
La Programación Orientada a Objetos (POO) es un paradigma de programación que organiza el código en torno a "objetos" en lugar de funciones y procedimientos. Estos objetos son instancias de "clases", que definen sus propiedades (atributos) y comportamientos (métodos). La POO permite modelar problemas del mundo real de manera más intuitiva, y facilita la reutilización y la escalabilidad del código.

- **Ventajas de la POO:**
  - **Modularidad:** El código se organiza en clases, lo que facilita su mantenimiento y reutilización.
  - **Reutilización:** Puedes reutilizar clases existentes para crear nuevas funcionalidades mediante la herencia.
  - **Escalabilidad:** La POO facilita la creación de sistemas grandes y complejos mediante la definición clara de responsabilidades y relaciones entre objetos.

### 1.2. Conceptos Fundamentales de la POO

- **Objetos y Clases:**
  - **Clase:** Es un modelo o plantilla a partir de la cual se crean objetos. Define los atributos y métodos que el objeto tendrá.
  - **Objeto:** Es una instancia de una clase. Cada objeto creado a partir de una clase tiene sus propios valores para los atributos definidos en la clase.

- **Atributos y Métodos:**
  - **Atributos:** Son las propiedades o características de un objeto (por ejemplo, el color de un coche o la velocidad de un animal).
  - **Métodos:** Son las acciones o comportamientos que un objeto puede realizar (por ejemplo, arrancar un coche o cazar una presa).

- **Instanciación de Objetos:**
  - La instanciación es el proceso de crear un objeto a partir de una clase. Cuando instancias una clase, se crea un nuevo objeto en memoria con sus propios valores de atributos y métodos.

  Ejemplo básico de una clase e instanciación:
  ```python
  class Coche:
      def __init__(self, color, velocidad):
          self.color = color
          self.velocidad = velocidad

      def arrancar(self):
          print("El coche ha arrancado")

  # Instanciación de un objeto
  mi_coche = Coche("rojo", 120)
  mi_coche.arrancar()
  ```

### 2.1. Definición de Clases en Python
Una clase en Python se define utilizando la palabra clave `class`, seguida del nombre de la clase y dos puntos `:`. Dentro de la clase, defines los atributos y métodos que serán comunes a todas las instancias de la clase.

- **Sintaxis básica para definir una clase:**
  ```python
  class NombreDeLaClase:
      # Definir atributos y métodos
  ```

- **Atributos de Instancia vs. Atributos de Clase:**
  - **Atributos de Instancia:** Son específicos de cada objeto creado a partir de la clase. Se definen normalmente dentro del método `__init__`.
  - **Atributos de Clase:** Son compartidos por todas las instancias de la clase.

  Ejemplo:
  ```python
  class Coche:
      ruedas = 4  # Atributo de clase

      def __init__(self, color, marca):
          self.color = color  # Atributo de instancia
          self.marca = marca  # Atributo de instancia
  ```

### 2.2. Creación e Instanciación de Objetos
Una vez que has definido una clase, puedes crear objetos (instancias) de esa clase. Cada objeto es una instancia independiente con sus propios valores para los atributos definidos en la clase.

- **Sintaxis para crear un objeto:**
  ```python
  mi_objeto = NombreDeLaClase(parametros)
  ```

- **Acceso y modificación de atributos:**
  - Puedes acceder a los atributos de un objeto utilizando la sintaxis `objeto.atributo`.
  - Puedes modificar los atributos de un objeto asignándoles un nuevo valor con `objeto.atributo = nuevo_valor`.

  Ejemplo:
  ```python
  mi_coche = Coche("rojo", "Toyota")
  print(mi_coche.color)  # Imprime "rojo"
  mi_coche.color = "azul"  # Modifica el color
  print(mi_coche.color)  # Imprime "azul"
  ```

### 2.3. Métodos de Instancia
Los métodos de instancia son funciones definidas dentro de una clase que operan sobre los atributos del objeto. El primer parámetro de cualquier método de instancia es siempre `self`, que hace referencia al propio objeto.

- **Definición de un método:**
  ```python
  class Coche:
      def arrancar(self):
          print("El coche ha arrancado")
  ```

- **Llamada a un método:**
  ```python
  mi_coche.arrancar()  # Llama al método 'arrancar' del objeto 'mi_coche'
  ```

## Ejercicios propuestos

- Define una clase llamada `Persona` que tenga los atributos `nombre` y `edad`. Luego, crea un objeto de la clase `Persona` y muestra su nombre y edad en la pantalla.

<br>

- Crea una clase `Rectangulo` con los atributos `ancho` y `alto`. Define un método `area()` que calcule el área del rectángulo. Crea un objeto de `Rectangulo`, asigna valores a `ancho` y `alto`, y muestra el área calculada.

<br>

- Desarrolla una clase `Coche` con los atributos `marca` y `modelo`. Añade un método `arrancar()` que muestre un mensaje indicando que el coche ha arrancado. Luego, crea varios objetos de la clase `Coche` y llama al método `arrancar()` en cada uno de ellos.

<br>

- Define una clase `Libro` con los atributos `titulo` y `autor`. Crea un método `mostrar_info` que imprima el título y el autor del libro. Luego, crea un objeto de la clase `Libro` y llama al método `mostrar_info`.

<br>

- Crea una clase `CuentaBancaria` con los atributos `titular` y `saldo`. Define un método `depositar(cantidad)` que aumente el saldo de la cuenta, y un método `retirar(cantidad)` que disminuya el saldo si hay suficiente dinero en la cuenta. Crea un objeto de `CuentaBancaria`, realiza un depósito y una retirada, y muestra el saldo final.

<br>

- Desarrolla una clase `Coche` que tenga un atributo `kilometraje` y un método `conducir(kilometros)` que aumente el kilometraje del coche. Crea un objeto de la clase `Coche`, conduce el coche una cierta cantidad de kilómetros y muestra el kilometraje final.

<br>