# Encapsulamiento

### 3.1. Principio de Encapsulamiento
El encapsulamiento es uno de los principios fundamentales de la Programación Orientada a Objetos. Consiste en restringir el acceso directo a los atributos y métodos de un objeto, exponiendo únicamente lo necesario para interactuar con el objeto. Esto se hace para proteger la integridad de los datos y evitar modificaciones accidentales o no deseadas.

### 3.2. Atributos y Métodos Privados
En Python, no existen verdaderos modificadores de acceso como `private` o `protected` que se encuentran en otros lenguajes de programación. Sin embargo, hay convenciones para indicar que un atributo o método debe ser tratado como privado:

- **Atributos y Métodos Privados:** Se indica anteponiendo un guion bajo `_` al nombre del atributo o método. Esto sugiere que no debe ser accedido desde fuera de la clase.

- **Atributos y Métodos Protegidos:** Se indica anteponiendo dos guiones bajos `__`, lo que hace que el nombre del atributo sea "mangling" (transformado) para que sea menos accesible desde fuera de la clase.

Ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self._nombre = nombre  # Atributo "privado"
        self.__edad = edad  # Atributo "protegido"

    def _mostrar_nombre(self):
        print(f"Nombre: {self._nombre}")

    def __mostrar_edad(self):
        print(f"Edad: {self.__edad}")
```

### 3.3. Métodos `getter` y `setter`
Para acceder o modificar los atributos privados de un objeto de manera controlada, se utilizan métodos `getter` y `setter`.

- **Métodos `getter`:** Permiten obtener el valor de un atributo privado.
- **Métodos `setter`:** Permiten modificar el valor de un atributo privado, aplicando validaciones si es necesario.

Ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self._nombre = nombre
        self.__edad = edad

    # Método getter para edad
    def get_edad(self):
        return self.__edad

    # Método setter para edad
    def set_edad(self, nueva_edad):
        if nueva_edad > 0:
            self.__edad = nueva_edad
        else:
            print("La edad debe ser un número positivo")

persona = Persona("Ana", 30)
print(persona.get_edad())  # Imprime 30
persona.set_edad(35)  # Cambia la edad a 35
print(persona.get_edad())  # Imprime 35
```

### 3.4. Métodos Especiales (`__init__`, `__str__`, etc.)
Python proporciona métodos especiales, también conocidos como métodos mágicos, que tienen un significado especial en la POO:

- **`__init__`:** Es el constructor de la clase, se llama automáticamente cuando se crea una nueva instancia de la clase.
- **`__str__`:** Devuelve una representación en cadena del objeto, útil para imprimir la información del objeto de manera legible.

Ejemplo:
```python
class Persona:
    def __init__(self, nombre, edad):
        self._nombre = nombre
        self.__edad = edad

    def __str__(self):
        return f"Nombre: {self._nombre}, Edad: {self.__edad}"

persona = Persona("Carlos", 40)
print(persona)  # Imprime "Nombre: Carlos, Edad: 40"
```

El encapsulamiento te ayuda a mantener la integridad de los datos y a controlar cómo se accede y modifica la información dentro de un objeto.

## Ejercicios propuestos:

- Define una clase `CuentaBancaria` con un atributo privado `__saldo`. Crea métodos `depositar` y `retirar` para modificar el saldo, y un método `consultar_saldo` que retorne el saldo actual. Asegúrate de que no sea posible retirar más dinero del que está disponible.

<br>

- Crea una clase `Libro` con los atributos `titulo`, `autor`, y `__precio`. Define métodos `get_precio` y `set_precio` para acceder y modificar el precio del libro. Implementa validación en el método `set_precio` para asegurar que el precio no sea negativo.

<br>

- Desarrolla una clase `Empleado` con los atributos `nombre`, `cargo`, y `__salario`. Implementa un método `__str__` que retorne una cadena con la información del empleado en un formato legible. Añade métodos para modificar el salario y cargo del empleado, pero asegúrate de que el salario no sea inferior a un valor mínimo.