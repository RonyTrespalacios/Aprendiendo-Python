# Estructuras de Control de Flujo III

## Bucles `while`

Los bucles `while` en Python se utilizan para repetir un bloque de código mientras una condición sea verdadera. A diferencia de los bucles `for`, que iteran un número predefinido de veces, los bucles `while` continúan ejecutándose hasta que la condición se evalúa como `False`.

### Uso Básico de `while`
El bucle `while` verifica la condición antes de cada iteración. Si la condición es `True`, el código dentro del bucle se ejecuta; si es `False`, el bucle termina.

```python
contador = 1
while contador <= 5:
    print(f"Iteración {contador}")
    contador += 1
```

### Bucles Infinitos
Un bucle `while` que nunca alcanza una condición de finalización se convierte en un bucle infinito, lo que significa que se ejecutará para siempre. Esto generalmente se evita asegurando que la condición eventualmente se vuelva `False`.

```python
# Este bucle es infinito porque la condición nunca cambia
while True:
    print("Este bucle no termina nunca")
```

### Uso de `break` y `continue`
- **`break`**: Termina el bucle inmediatamente, independientemente de la condición.
- **`continue`**: Salta la iteración actual y vuelve al inicio del bucle para verificar la condición nuevamente.

```python
contador = 1
while contador <= 10:
    if contador == 5:
        break  # Salir del bucle cuando contador es 5
    print(f"Contador: {contador}")
    contador += 1
```

```python
contador = 0
while contador < 5:
    contador += 1
    if contador == 3:
        continue  # Saltar la iteración cuando contador es 3
    print(f"Contador: {contador}")
```

## Ejercicios Propuestos

### **Ejercicio 1**:

Escribe un programa que utilice un bucle `while` para contar de 1 a 10 y mostrar los números en pantalla.

```python
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>

### **Ejercicio 2**:

Desarrolla un programa que solicite al usuario que ingrese una contraseña. Utiliza un bucle `while` para permitir que el usuario intente ingresar la contraseña correcta hasta que lo logre.

```python
# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>

### **Ejercicio 3**:

Imagina que estás creando un juego de adivinanza de números. El programa debe generar un número aleatorio entre 1 y 100, y el usuario debe intentar adivinarlo. Utiliza un bucle `while` para permitir que el usuario siga adivinando hasta que acierte, y proporciona pistas como "mayor" o "menor" en cada intento.

```python
import random

numero_secreto = random.randint(1, 100)
adivinanza = None

# Escribe tu código aquí
```

<details> <summary>Ver solución</summary>
```python
No disponible.
```
</details>
