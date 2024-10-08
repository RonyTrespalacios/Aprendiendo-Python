# Herencia

### 4.1. Concepto de Herencia en POO
La herencia es un principio fundamental en la Programación Orientada a Objetos que permite crear nuevas clases a partir de clases existentes. La clase nueva, llamada subclase o clase derivada, hereda atributos y métodos de la clase existente, conocida como superclase o clase base. Esto facilita la reutilización de código y la creación de estructuras jerárquicas.

- **Ventajas de la herencia:**
  - **Reutilización de código:** Permite extender las funcionalidades de clases existentes sin reescribir el código.
  - **Organización:** Facilita la creación de estructuras jerárquicas donde las clases se organizan de manera lógica.

### 4.2. Creación de Subclases
Para crear una subclase en Python, defines una nueva clase que hereda de una clase existente. Esto se hace colocando el nombre de la superclase entre paréntesis después del nombre de la subclase.

- **Sintaxis básica:**
  ```python
  class SuperClase:
      # Atributos y métodos de la superclase

  class SubClase(SuperClase):
      # Atributos y métodos adicionales de la subclase
  ```

Ejemplo:
```python
class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

    def hacer_sonido(self):
        print("El animal hace un sonido")

class Perro(Animal):
    def hacer_sonido(self):
        print("El perro ladra")
```

### 4.3. Sobrescritura de Métodos
Una subclase puede sobrescribir métodos de la superclase para alterar o extender su comportamiento. Esto es útil cuando necesitas que la subclase tenga un comportamiento diferente al de la superclase.

Ejemplo:
```python
class Animal:
    def hacer_sonido(self):
        print("El animal hace un sonido")

class Gato(Animal):
    def hacer_sonido(self):
        print("El gato maúlla")

gato = Gato("Michi")
gato.hacer_sonido()  # Imprime "El gato maúlla"
```

### 4.4. Uso de `super()`
El método `super()` se utiliza para llamar a métodos de la superclase desde la subclase. Esto es útil cuando quieres extender el comportamiento de un método de la superclase en lugar de sobrescribirlo por completo.

Ejemplo:
```python
class Animal:
    def __init__(self, nombre):
        self.nombre = nombre

    def hacer_sonido(self):
        print("El animal hace un sonido")

class Perro(Animal):
    def __init__(self, nombre, raza):
        super().__init__(nombre)
        self.raza = raza

    def hacer_sonido(self):
        super().hacer_sonido()  # Llama al método de la superclase
        print("El perro ladra")

perro = Perro("Rex", "Labrador")
perro.hacer_sonido()
# Imprime:
# El animal hace un sonido
# El perro ladra
```

La herencia te permite crear jerarquías de clases que reutilizan y extienden funcionalidades, lo que facilita la organización y escalabilidad del código.

## Ejercicios

- Define una clase `Vehiculo` con los atributos `marca` y `modelo`, y un método `arrancar()`. Luego, crea una subclase `Coche` que herede de `Vehiculo` y añade un atributo `puertas`. Sobrescribe el método `arrancar()` en `Coche` para que también indique el número de puertas. Crea un objeto de `Coche` y llama al método `arrancar()`.

<br>

- Crea una clase `Persona` con los atributos `nombre` y `edad`, y un método `presentarse()` que imprima un mensaje con estos datos. Luego, crea una subclase `Estudiante` que herede de `Persona` y añade un atributo `carrera`. Sobrescribe el método `presentarse()` en `Estudiante` para que también indique la carrera del estudiante. Crea un objeto de `Estudiante` y llama al método `presentarse()`.

<br>

- Desarrolla una clase `Empleado` con los atributos `nombre` y `salario`. Luego, crea una subclase `Gerente` que herede de `Empleado` y añade un atributo `departamento`. Sobrescribe el método `__str__()` en `Gerente` para que devuelva una cadena con toda la información del gerente, incluyendo su nombre, salario y departamento.

 