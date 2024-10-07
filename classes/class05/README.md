# Retos de Aprendizaje I

## **Listas**: 
Tienes una lista de tareas pendientes que incluye las siguientes actividades: "Lavar los platos", "Hacer la compra", "Estudiar Python". Es necesario agregar una nueva tarea "Sacar la basura", eliminar la tarea "Lavar los platos", y luego modificar la tarea "Hacer la compra" para que diga "Comprar frutas y verduras". Finalmente, muestra la lista actualizada.

```python
tareas = ["Lavar los platos", "Hacer la compra", "Estudiar Python"]
# Escribe el código para modificar la lista aquí
```

<details> <summary>Ver solución</summary>
```python
tareas = ["Lavar los platos", "Hacer la compra", "Estudiar Python"]
tareas.append("Sacar la basura")
print(tareas)
tareas.remove("Lavar los platos")
print(tareas)
tareas[tareas.index("Hacer la compra")] = "Comprar frutas y verduras"
print(tareas)
```
</details>

## **Tuplas**:
Se te pide almacenar las coordenadas geográficas (latitud, longitud) de tres lugares de interés: la Torre Eiffel, el Coliseo y la Estatua de la Libertad. Una vez almacenadas, muestra cada coordenada con un mensaje indicando de qué lugar se trata.

<details> <summary>Ver solución</summary>
```python
# Coordenadas (latitud, longitud) de los lugares de interés
torre_eiffel = (48.8584, 2.2945)
coliseo = (41.8902, 12.4922)
estatua_libertad = (40.6892, -74.0445)

print(f"Torre eiffel:\n latitud: {torre_eiffel[0]}, \n longitud: {torre_eiffel[1]}.\n")
print(f"Coliseo:\n latitud: {coliseo[0]},\n longitud: {coliseo[1]}.\n")
print(f"Estatua de la Libertad:\n latitud: {estatua_libertad[0]},\n longitud: {estatua_libertad[1]}.\n")
```
</details>

## **Diccionarios**: 
Crea una agenda de contactos donde puedas buscar la información de contacto de una persona a partir de su nombre. La agenda debe contener al menos tres contactos con los siguientes campos: nombre, teléfono y correo electrónico. Después, realiza una búsqueda para mostrar la información de contacto de uno de ellos.

```python
agenda = {
    "Juan": {"teléfono": "123-4567", "email": "juan@example.com"},
    "Ana": {"teléfono": "987-6543", "email": "ana@example.com"},
    "Luis": {"teléfono": "555-1234", "email": "luis@example.com"}
}
# Escribe el código para buscar y mostrar la información de contacto aquí
```

<details> <summary>Ver solución</summary>
```python
agenda = {
    "Juan": {"teléfono": "123-4567", "email": "juan@example.com"},
    "Ana": {"teléfono": "987-6543", "email": "ana@example.com"},
    "Luis": {"teléfono": "555-1234", "email": "luis@example.com"}
}

nombre = input("Digite el nombre: ")
for clave, valor in agenda.items():
  if clave == nombre.capitalize():
    print("teléfono:",valor['teléfono'])
    print("email:",valor['email'])
```
</details>

## **Conjuntos (sets)**: 
Tienes dos conjuntos que representan los intereses de dos usuarios en una red social. El primer usuario tiene los intereses "Fútbol", "Música", "Cine", mientras que el segundo usuario tiene los intereses "Música", "Viajes", "Cine". Determina qué intereses tienen en común ambos usuarios y muéstralos.

```python
usuario1 = {"Fútbol", "Música", "Cine"}
usuario2 = {"Música", "Viajes", "Cine"}
# Escribe el código para determinar y mostrar los intereses comunes aquí
```

<details> <summary>Ver solución</summary>
```python
usuario1 = {"Fútbol", "Música", "Cine"}
usuario2 = {"Música", "Viajes", "Cine"}
print("Gustos en comun:", ", ".join(usuario1 & usuario2))
```
</details>

<div class="navigation-buttons">
    <a href="./#/class04" class="prev-button">← Clase Anterior</a>
    <a class="next-button disabled">Clase Siguiente →</a>
</div>