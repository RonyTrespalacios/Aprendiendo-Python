# Polimorfismo

### 5.1. Qué es el Polimorfismo
El polimorfismo es un concepto clave en la Programación Orientada a Objetos que permite a diferentes clases implementar métodos con el mismo nombre pero comportarse de manera distinta. En otras palabras, el polimorfismo permite que un mismo método funcione de diferentes maneras según el objeto que lo esté invocando.

### 5.2. Polimorfismo en Métodos
El polimorfismo se puede lograr mediante la sobrescritura de métodos en subclases. Diferentes clases pueden tener un método con el mismo nombre, pero cada uno implementa la lógica que es específica para esa clase.

#### Ejemplo en un contexto de videojuegos:
Imagina un videojuego de estrategia donde diferentes tipos de unidades pueden atacar. Cada unidad (por ejemplo, Soldado, Arquero, Mago) tiene un método `atacar()`, pero la forma en que atacan es diferente.

```python
class Unidad:
    def atacar(self):
        raise NotImplementedError("Este método debe ser sobrescrito por subclases")

class Soldado(Unidad):
    def atacar(self):
        print("El Soldado ataca con su espada")

class Arquero(Unidad):
    def atacar(self):
        print("El Arquero dispara una flecha")

class Mago(Unidad):
    def atacar(self):
        print("El Mago lanza un hechizo")

# Ejemplo de uso
unidades = [Soldado(), Arquero(), Mago()]
for unidad in unidades:
    unidad.atacar()
```

### 5.3. Polimorfismo y Herencia
El polimorfismo se suele utilizar junto con la herencia. Al heredar de una clase base, las subclases pueden sobrescribir los métodos para proporcionar comportamientos específicos.

#### Ejemplo en el sector empresarial:
Considera una aplicación para calcular el salario de empleados en una empresa. Existen diferentes tipos de empleados: empleados a tiempo completo, empleados a tiempo parcial y contratistas. Cada uno tiene una forma diferente de calcular su salario.

```python
class Empleado:
    def calcular_salario(self):
        raise NotImplementedError("Este método debe ser sobrescrito por subclases")

class EmpleadoTiempoCompleto(Empleado):
    def __init__(self, salario_base):
        self.salario_base = salario_base

    def calcular_salario(self):
        return self.salario_base

class EmpleadoTiempoParcial(Empleado):
    def __init__(self, horas_trabajadas, pago_por_hora):
        self.horas_trabajadas = horas_trabajadas
        self.pago_por_hora = pago_por_hora

    def calcular_salario(self):
        return self.horas_trabajadas * self.pago_por_hora

class Contratista(Empleado):
    def __init__(self, proyecto, tarifa):
        self.proyecto = proyecto
        self.tarifa = tarifa

    def calcular_salario(self):
        return self.tarifa

# Ejemplo de uso
empleados = [
    EmpleadoTiempoCompleto(3000),
    EmpleadoTiempoParcial(80, 20),
    Contratista("Desarrollo Web", 5000)
]

for empleado in empleados:
    print(f"Salario: {empleado.calcular_salario()}")
```

### 5.4. Métodos Abstractos y Clases Abstractas
En Python, puedes usar la biblioteca `abc` (Abstract Base Class) para crear clases y métodos abstractos. Las clases abstractas no pueden ser instanciadas directamente y sirven como plantillas para otras clases.

```python
from abc import ABC, abstractmethod

class Herramienta(ABC):
    @abstractmethod
    def usar(self):
        pass

class Martillo(Herramienta):
    def usar(self):
        print("Usando el martillo para clavar un clavo")

class Destornillador(Herramienta):
    def usar(self):
        print("Usando el destornillador para apretar un tornillo")

# Ejemplo de uso
herramientas = [Martillo(), Destornillador()]
for herramienta in herramientas:
    herramienta.usar()
```

El polimorfismo te permite escribir código más flexible y reutilizable al permitir que diferentes clases utilicen métodos con el mismo nombre pero con comportamientos diferentes.

- En un juego de simulación de granja, diferentes animales producen recursos: las vacas producen leche, las gallinas producen huevos, y las ovejas producen lana. Define una clase abstracta `Animal` con un método abstracto `producir()`. Luego, crea subclases `Vaca`, `Gallina`, y `Oveja` que implementen el método `producir()` de manera específica. Simula un día en la granja donde cada animal produce su recurso.

<br>

- En una aplicación de gestión de proyectos, diferentes tipos de empleados realizan diferentes tipos de trabajo. Los programadores escriben código, los diseñadores crean gráficos, y los gerentes organizan reuniones. Define una clase abstracta `Empleado` con un método abstracto `trabajar()`. Crea subclases `Programador`, `Diseñador`, y `Gerente` que sobrescriban el método `trabajar()` para realizar la tarea correspondiente.

<br>

- En una plataforma de comercio electrónico, diferentes métodos de pago pueden ser utilizados para completar una compra. Los pagos con tarjeta de crédito, PayPal, y criptomonedas requieren diferentes procesos. Define una clase abstracta `MetodoPago` con un método abstracto `procesar_pago()`. Crea subclases `TarjetaCredito`, `PayPal`, y `Criptomoneda` que implementen este método de acuerdo a sus procesos específicos.