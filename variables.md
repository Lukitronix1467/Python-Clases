### Clase sobre Variables en Python

#### Objetivos de la Clase
1. Comprender qué es una variable y su utilidad.
2. Aprender a declarar y asignar valores a variables en Python.
3. Conocer los diferentes tipos de datos que pueden almacenar las variables.
4. Aplicar conceptos a ejemplos prácticos.

### 1. ¿Qué es una Variable?
Una variable es un nombre simbólico que se refiere a un valor almacenado en la memoria del ordenador. Las variables permiten almacenar y manipular datos durante la ejecución de un programa.

### 2. Declarar y Asignar Valores a Variables

#### Declaración y Asignación
En Python, no es necesario declarar el tipo de la variable explícitamente. La declaración y la asignación se realizan en una sola línea.

```python
# Declarar y asignar una variable
nombre = "Juan"
edad = 25
pi = 3.14159
es_estudiante = True
```

### 3. Tipos de Datos Comunes en Python

#### 3.1 Enteros (int)
Números enteros positivos o negativos.

```python
a = 10
b = -5
```

#### 3.2 Flotantes (float)
Números con decimales.

```python
c = 3.14
d = -2.718
```

#### 3.3 Cadenas de Texto (str)
Secuencias de caracteres.

```python
e = "Hola, mundo"
f = 'Python es divertido'
```

#### 3.4 Booleanos (bool)
Valores de verdad (`True` o `False`).

```python
g = True
h = False
```

#### 3.5 Otros Tipos de Datos
Python también soporta otros tipos de datos como listas, tuplas, diccionarios y conjuntos.

```python
lista = [1, 2, 3]
tupla = (4, 5, 6)
diccionario = {"clave": "valor"}
conjunto = {7, 8, 9}
```

### 4. Operaciones con Variables

#### 4.1 Operaciones Aritméticas
Puedes realizar operaciones aritméticas con variables numéricas.

```python
x = 10
y = 5

suma = x + y
resta = x - y
multiplicacion = x * y
division = x / y

print(suma)          # Salida: 15
print(resta)         # Salida: 5
print(multiplicacion) # Salida: 50
print(division)       # Salida: 2.0
```

#### 4.2 Concatenación de Cadenas
Puedes concatenar (unir) cadenas de texto usando el operador `+`.

```python
saludo = "Hola"
nombre = "Ana"

mensaje = saludo + ", " + nombre
print(mensaje)  # Salida: Hola, Ana
```

#### 4.3 Operaciones Booleanas
Puedes realizar operaciones lógicas con variables booleanas.

```python
a = True
b = False

and_resultado = a and b
or_resultado = a or b
not_resultado = not a

print(and_resultado)  # Salida: False
print(or_resultado)   # Salida: True
print(not_resultado)  # Salida: False
```

### Ejemplos Prácticos

#### Ejemplo 1: Calcular el Área de un Círculo

```python
def area_circulo(radio):
    pi = 3.14159
    return pi * (radio ** 2)

radio = 5
print(f"El área del círculo con radio {radio} es: {area_circulo(radio)}")  # Salida: El área del círculo con radio 5 es: 78.53975
```

#### Ejemplo 2: Convertir Temperaturas de Celsius a Fahrenheit

```python
def celsius_a_fahrenheit(celsius):
    return (celsius * 9/5) + 32

temp_celsius = 25
print(f"{temp_celsius}°C es igual a {celsius_a_fahrenheit(temp_celsius)}°F")  # Salida: 25°C es igual a 77.0°F
```

#### Ejemplo 3: Verificar si un Año es Bisiesto

```python
def es_bisiesto(anio):
    if (anio % 4 == 0 and anio % 100 != 0) or (anio % 400 == 0):
        return True
    else:
        return False

anio = 2024
print(f"¿El año {anio} es bisiesto? {es_bisiesto(anio)}")  # Salida: ¿El año 2024 es bisiesto? True
```

### Ejercicios para la Clase

#### Ejercicio 1: Calcular el Perímetro de un Rectángulo
<details> 
  <summary> Escribe una función `perimetro_rectangulo(largo, ancho)` que devuelva el perímetro de un rectángulo dados su largo y ancho. </summary>

```python
def perimetro_rectangulo(largo, ancho):
    return 2 * (largo + ancho)

# Prueba de la función
largo = 10
ancho = 5
print(f"El perímetro del rectángulo es: {perimetro_rectangulo(largo, ancho)}")  # Salida: El perímetro del rectángulo es: 30
```
</details>

#### Ejercicio 2: Calcular el Interés Simple
<details> 
  <summary> Escribe una función `interes_simple(principal, tasa, tiempo)` que calcule el interés simple dados el capital principal, la tasa de interés y el tiempo. </summary>

```python
def interes_simple(principal, tasa, tiempo):
    return (principal * tasa * tiempo) / 100

# Prueba de la función
principal = 1000
tasa = 5
tiempo = 3
print(f"El interés simple es: {interes_simple(principal, tasa, tiempo)}")  # Salida: El interés simple es: 150.0
```
</details>

#### Ejercicio 3: Convertir Minutos a Horas y Minutos
<details> 
  <summary> Escribe una función `convertir_minutos(minutos)` que convierta una cantidad de minutos en horas y minutos. </summary>

```python
def convertir_minutos(minutos):
    horas = minutos // 60
    minutos_restantes = minutos % 60
    return horas, minutos_restantes

# Prueba de la función
total_minutos = 135
horas, minutos = convertir_minutos(total_minutos)
print(f"{total_minutos} minutos son {horas} horas y {minutos} minutos")  # Salida: 135 minutos son 2 horas y 15 minutos
```
</details>

#### Ejercicio 4: Calcular el Índice de Masa Corporal (IMC)
<details> 
  <summary> Escribe una función `calcular_imc(peso, altura)` que calcule el IMC dado el peso en kilogramos y la altura en metros. </summary>

```python
def calcular_imc(peso, altura):
    return peso / (altura ** 2)

# Prueba de la función
peso = 70
altura = 1.75
print(f"El IMC es: {calcular_imc(peso, altura)}")  # Salida: El IMC es: 22.857142857142858
```
</details>

### Resumen
- Las variables son nombres simbólicos que se refieren a valores almacenados en la memoria.
- Puedes declarar y asignar valores a variables en una sola línea en Python.
- Las variables pueden almacenar diferentes tipos de datos, como enteros, flotantes, cadenas y booleanos.
- Puedes realizar diversas operaciones con variables, incluidas operaciones aritméticas, concatenación de cadenas y operaciones lógicas.

Estos conceptos y ejercicios proporcionan una base sólida para trabajar con variables en Python.
