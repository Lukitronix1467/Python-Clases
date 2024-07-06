### Clase sobre Listas en Python

#### Objetivos de la Clase
1. Comprender qué es una lista y su utilidad.
2. Aprender a crear y manipular listas en Python.
3. Conocer las operaciones comunes con listas.
4. Aplicar conceptos a ejemplos prácticos.

### 1. ¿Qué es una Lista?
Una lista en Python es una colección ordenada de elementos que puede contener elementos de diferentes tipos. Las listas son mutables, lo que significa que sus elementos se pueden cambiar después de que la lista ha sido creada.

### 2. Crear una Lista

```python
# Crear una lista vacía
mi_lista_vacia = []

# Crear una lista con elementos
mi_lista = [1, 2, 3, "hola", True]
```

### 3. Acceder a Elementos de una Lista

```python
mi_lista = [10, 20, 30, 40, 50]

# Acceder al primer elemento (índice 0)
print(mi_lista[0])  # Salida: 10

# Acceder al tercer elemento (índice 2)
print(mi_lista[2])  # Salida: 30

# Acceder al último elemento (índice -1)
print(mi_lista[-1])  # Salida: 50
```

### 4. Modificar Elementos de una Lista

```python
mi_lista = [1, 2, 3, 4, 5]

# Cambiar el segundo elemento
mi_lista[1] = 20
print(mi_lista)  # Salida: [1, 20, 3, 4, 5]
```

### 5. Operaciones Comunes con Listas

#### 5.1 Añadir Elementos

```python
mi_lista = [1, 2, 3]

# Añadir un elemento al final de la lista
mi_lista.append(4)
print(mi_lista)  # Salida: [1, 2, 3, 4]

# Insertar un elemento en una posición específica
mi_lista.insert(1, 10)
print(mi_lista)  # Salida: [1, 10, 2, 3, 4]
```

#### 5.2 Eliminar Elementos

```python
mi_lista = [1, 2, 3, 4, 5]

# Eliminar un elemento específico
mi_lista.remove(3)
print(mi_lista)  # Salida: [1, 2, 4, 5]

# Eliminar el último elemento
ultimo_elemento = mi_lista.pop()
print(mi_lista)  # Salida: [1, 2, 4]
print(ultimo_elemento)  # Salida: 5

# Eliminar un elemento en una posición específica
elemento_pos_1 = mi_lista.pop(1)
print(mi_lista)  # Salida: [1, 4]
print(elemento_pos_1)  # Salida: 2
```

#### 5.3 Slicing (Corte) de Listas

```python
mi_lista = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

# Obtener una sublista
sub_lista = mi_lista[2:5]
print(sub_lista)  # Salida: [3, 4, 5]

# Obtener elementos con un paso
paso_lista = mi_lista[::2]
print(paso_lista)  # Salida: [1, 3, 5, 7, 9]
```

#### 5.4 Longitud de una Lista

```python
mi_lista = [1, 2, 3, 4, 5]

# Obtener la longitud de la lista
print(len(mi_lista))  # Salida: 5
```

#### 5.5 Comprobar Si un Elemento Está en una Lista

```python
mi_lista = [1, 2, 3, 4, 5]

# Verificar si un elemento está en la lista
print(3 in mi_lista)  # Salida: True
print(10 in mi_lista)  # Salida: False
```

### Ejemplos Prácticos

#### Ejemplo 1: Promedio de una Lista de Números

```python
def promedio(lista):
    return sum(lista) / len(lista)

numeros = [10, 20, 30, 40, 50]
print(f"El promedio es: {promedio(numeros)}")  # Salida: El promedio es: 30.0
```

#### Ejemplo 2: Encontrar el Mínimo y Máximo en una Lista

```python
def encontrar_min_max(lista):
    minimo = min(lista)
    maximo = max(lista)
    return minimo, maximo

numeros = [10, 20, 5, 40, 50]
minimo, maximo = encontrar_min_max(numeros)
print(f"El mínimo es: {minimo} y el máximo es: {maximo}")  # Salida: El mínimo es: 5 y el máximo es: 50
```

### Ejercicios para la Clase

#### Ejercicio 1: Sumar Elementos de una Lista
Escribe una función `sumar_elementos(lista)` que devuelva la suma de todos los elementos en una lista de números.

```python
def sumar_elementos(lista):
    return sum(lista)

# Prueba de la función
numeros = [1, 2, 3, 4, 5]
print(sumar_elementos(numeros))  # Salida: 15
```

#### Ejercicio 2: Contar Elementos en una Lista
Escribe una función `contar_elementos(lista, elemento)` que devuelva cuántas veces aparece un elemento específico en una lista.

```python
def contar_elementos(lista, elemento):
    return lista.count(elemento)

# Prueba de la función
numeros = [1, 2, 2, 3, 4, 2, 5]
print(contar_elementos(numeros, 2))  # Salida: 3
```

#### Ejercicio 3: Encontrar el Elemento Más Largo en una Lista de Cadenas
Escribe una función `elemento_mas_largo(lista)` que devuelva la cadena más larga en una lista de cadenas.

```python
def elemento_mas_largo(lista):
    return max(lista, key=len)

# Prueba de la función
cadenas = ["manzana", "banana", "cereza", "kiwi"]
print(elemento_mas_largo(cadenas))  # Salida: "manzana"
```

#### Ejercicio 4: Eliminar Duplicados de una Lista
Escribe una función `eliminar_duplicados(lista)` que devuelva una nueva lista sin elementos duplicados, manteniendo el orden original.

```python
def eliminar_duplicados(lista):
    lista_sin_duplicados = []
    for elemento in lista:
        if elemento not in lista_sin_duplicados:
            lista_sin_duplicados.append(elemento)
    return lista_sin_duplicados

# Prueba de la función
numeros = [1, 2, 2, 3, 4, 4, 5]
print(eliminar_duplicados(numeros))  # Salida: [1, 2, 3, 4, 5]
```

### Resumen
- Las listas son colecciones ordenadas y mutables de elementos.
- Puedes crear, acceder, modificar y eliminar elementos en listas.
- Las listas tienen varias operaciones útiles como añadir, eliminar, cortar (slicing) y buscar elementos.
- La práctica con listas incluye operaciones comunes y funciones que aprovechan la flexibilidad de las listas.

Estos conceptos y ejercicios proporcionan una base sólida para trabajar con listas en Python.
