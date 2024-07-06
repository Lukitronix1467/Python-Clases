### Clase sobre Funciones en Python

#### Objetivos de la Clase
1. Comprender qué es una función y su utilidad.
2. Aprender a definir y llamar funciones en Python.
3. Explorar parámetros, argumentos y valores de retorno.
4. Conocer las funciones anónimas (lambda).
5. Aplicar conceptos a ejemplos prácticos.

#### 1. ¿Qué es una Función?
Una función es un bloque de código reutilizable diseñado para realizar una tarea específica. Las funciones permiten dividir un programa en partes más manejables y reutilizables.

#### 2. Definir y Llamar Funciones

##### Definición de una Función
Para definir una función en Python, usamos la palabra clave `def`, seguida del nombre de la función, paréntesis y dos puntos. El cuerpo de la función se escribe indentado.

```python
def nombre_de_la_funcion():
    # Código de la función
    print("Hola, esta es una función.")
```

##### Llamar a una Función
Para llamar a una función, escribimos su nombre seguido de paréntesis.

```python
nombre_de_la_funcion()  # Salida: Hola, esta es una función.
```

#### 3. Parámetros y Argumentos

##### Parámetros
Son variables listadas dentro de los paréntesis en la definición de la función.

```python
def saludar(nombre):
    print(f"Hola, {nombre}")
```

##### Argumentos
Son los valores que se pasan a la función cuando se llama.

```python
saludar("Ana")  # Salida: Hola, Ana
```

##### Múltiples Parámetros
Podemos definir funciones con múltiples parámetros.

```python
def sumar(a, b):
    return a + b

resultado = sumar(3, 4)
print(resultado)  # Salida: 7
```

#### 4. Valores de Retorno

Las funciones pueden devolver valores usando la palabra clave `return`.

```python
def cuadrado(x):
    return x * x

resultado = cuadrado(5)
print(resultado)  # Salida: 25
```

#### 5. Funciones Anónimas (Lambda)

Las funciones lambda son funciones pequeñas y anónimas definidas usando la palabra clave `lambda`. Generalmente se utilizan para tareas simples.

```python
suma = lambda x, y: x + y
print(suma(2, 3))  # Salida: 5
```

#### Ejemplos Prácticos

##### Ejemplo 1: Calcular el Factorial de un Número

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # Salida: 120
```

##### Ejemplo 2: Filtrar Números Pares de una Lista

```python
numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
pares = list(filter(lambda x: x % 2 == 0, numeros))
print(pares)  # Salida: [2, 4, 6, 8, 10]
```

### Resumen
- Las funciones son bloques reutilizables de código que realizan tareas específicas.
- Se definen usando `def`, seguido del nombre de la función y paréntesis.
- Las funciones pueden aceptar parámetros y devolver valores.
- Las funciones lambda son útiles para operaciones sencillas y rápidas.

### Ejercicio 1: Suma de dos números
<details> 
  <summary> Crea una función que sume dos números y devuelva el resultado. </summary>

```python
def suma(a, b):
    return a + b
# Prueba de la función
resultado = suma(3, 4)
print(f"La suma de 3 y 4 es: {resultado}")
```
</details>

### Ejercicio 2: Cuadrado de un número
<details> 
  <summary> Crea una función que calcule el cuadrado de un número. Luego, crea otra función que sume los cuadrados de dos números. </summary>

```python
def cuadrado(x):
    return x * x

def suma_de_cuadrados(a, b):
    return cuadrado(a) + cuadrado(b)

# Prueba de las funciones
resultado = suma_de_cuadrados(3, 4)
print(f"La suma de los cuadrados de 3 y 4 es: {resultado}")
```
</details>

### Ejercicio 3: Comprobación de número par o impar
<details> 
  <summary> Crea una función que determine si un número es par o impar. Luego, crea otra función que use esta información para sumar solo números pares. </summary>

```python
def es_par(n):
    return n % 2 == 0

def suma_solo_pares(a, b):
    suma = 0
    if es_par(a):
        suma += a
    if es_par(b):
        suma += b
    return suma

# Prueba de las funciones
resultado = suma_solo_pares(3, 4)
print(f"La suma de solo los números pares de 3 y 4 es: {resultado}")
```
</details>

### Ejercicio 4: Función principal con condicionales
<details> 
  <summary> Crea una función que reciba tres números y realice diferentes operaciones basadas en si son positivos o negativos. Si son todos positivos, devuelve la suma de sus cuadrados. Si al menos uno es negativo, devuelve la suma de solo los positivos. </summary>

```python
def cuadrado(x):
    return x * x

def es_positivo(n):
    return n > 0

def operacion_con_numeros(a, b, c):
    if es_positivo(a) and es_positivo(b) and es_positivo(c):
        return cuadrado(a) + cuadrado(b) + cuadrado(c)
    else:
        suma = 0
        if es_positivo(a):
            suma += a
        if es_positivo(b):
            suma += b
        if es_positivo(c):
            suma += c
        return suma

# Prueba de las funciones
resultado1 = operacion_con_numeros(3, 4, 5)
resultado2 = operacion_con_numeros(3, -4, 5)
print(f"Operación con (3, 4, 5): {resultado1}")
print(f"Operación con (3, -4, 5): {resultado2}")
```
</details>

### Explicación de los Ejercicios

1. **Ejercicio 1**: Introduce cómo definir una función simple que sume dos números.
2. **Ejercicio 2**: Introduce el concepto de funciones que llaman a otras funciones y el cálculo de cuadrados.
3. **Ejercicio 3**: Introduce condicionales y cómo usarlos en funciones para realizar tareas específicas (sumar solo números pares).
4. **Ejercicio 4**: Combina varias funciones y usa condicionales más complejos para decidir qué operación realizar basada en la naturaleza de los números (positivos o negativos).
