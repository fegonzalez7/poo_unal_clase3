# Programación Orientada a Objetos - UNAL

## Clase 3: Resumen de Conceptos Clave en Python

## Identificadores y Variables

- **Identificadores** son nombres dados a entidades como variables, funciones, y clases. Deben comenzar con una letra o un guion bajo, no pueden contener caracteres especiales ni espacios, y no deben ser palabras reservadas de Python.

- **Variables** en Python son nombres que se refieren a valores almacenados en la memoria. La asignación de variables no requiere declaración de tipo, aunque es posible hacerlo para claridad y legibilidad.

## Guía de estilo PEP8

### Indentación

- Utiliza 4 espacios por nivel de indentación.

### Máximo de Líneas

- Limita todas las líneas a un máximo de 79 caracteres para texto y 72 para comentarios y docstrings.

### Importaciones

- Las importaciones deben estar en líneas separadas.
- Agrupa las importaciones en el siguiente orden: bibliotecas estándar, relacionadas con terceros, y locales/aplicación específica.

### Espacios en Blanco

- Utiliza espacios en blanco en expresiones y declaraciones:
    - Después de las comas: `sí`, `no = valores(1, 2)`.
    - Antes y después de los operadores de asignación: `x = 1`.

### Convenciones de Nombres

- **Clases**: `NombreDeClase`.
- **Funciones y variables**: `nombre_de_funcion`, `nombre_de_variable`.
- **Constantes**: `NOMBRE_DE_CONSTANTE`.
- **Módulos y paquetes**: `nombre_de_modulo`, `nombre_de_paquete`.

### Expresiones y Declaraciones

- No uses espacios extras en:
    - Dentro de paréntesis, corchetes, o llaves.
    - Entre el nombre de una función y el paréntesis: `funcion(argumento)`.

### Comentarios

- Los comentarios deben ser oraciones completas.
- El objetivo es explicar el qué y por qué de código más complejo.

### Convenciones de Docstrings

- Utiliza """Triple doble comillas""" para docstrings.
- Para funciones: breve descripción de lo que hace y cualquier argumento y valor de retorno.

### Consistencia de Codificación

- Sé consistente en tu uso de convenciones. Si adoptas un estilo, mantenlo a lo largo de tu código.

#### Referencias

Este resumen se basa en el [PEP 8](https://www.python.org/dev/peps/pep-0008/), la guía de estilo oficial para el código Python.


## Tipos de Datos

### Básicos

- **Enteros (`int`)**: Números sin parte decimal. Ejemplo: `x = 10`.
- **Flotantes (`float`)**: Números con parte decimal. Ejemplo: `pi = 3.1416`.
- **Booleanos (`bool`)**: Representan verdadero (`True`) o falso (`False`).

### Avanzados

- **Cadenas de caracteres (`str`)**: Texto encerrado en comillas simples o dobles. Ejemplo: `nombre = "Python"`.
- **Listas, Tuplas, Diccionarios**: Estructuras de datos para almacenar colecciones de valores.

## Operadores

### Aritméticos

- Suma (`+`), Resta (`-`), Multiplicación (`*`), División (`/`), Módulo (`%`), División entera (`//`), Potencia (`**`).

### De Asignación

- Asignación (`=`), Asignación con suma (`+=`), y otras variantes para operaciones aritméticas.

### Lógicos y Relacionales

- Comparaciones (`==`, `!=`, `<`, `>`, `<=`, `>=`) y booleanos (`and`, `or`, `not`).

## Ejemplos Prácticos

```python
# Declarar e inicializar variables
numero : int = 10
pi : float = 3.1416
es_valido : bool = True
nombre = "Python"
```

### Operaciones aritméticas
```python
suma = numero + 2
resta = numero - 2
multiplicacion = numero * 2
division = numero / 2
```

### Operaciones lógicas
```python
alpha : int = 10
beta : int = 11
alpha == beta
alpha != beta
alpha > beta
alpha < beta
alpha >= beta
alpha <= beta
```

### Operaciones relacionales
```python
1 and 0 
True and False
1 or 0 
True or False
not 0
not False
```

### Precedencia de operaciones
La prioridad más alta es la 1 y la más baja es la 9. Si dos operaciones tienen la misma prioridad se resuelve de izquierda a derecha.

<table cellspacing="1" bgcolor="">
	<tr style="text-align: center; vertical-align: middle;" bgcolor="#252582">
		<th><p align=center><b>Operador(es)</b></p></th>
    <th><b>Prioridad</b></th>
	</tr>
	<tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
		<td style="color:#141414">()</td>
    <td style="color:#141414">1</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">not &nbsp &nbsp &nbsp -(signo menos) &nbsp &nbsp &nbsp +(signo más) &nbsp &nbsp &nbsp **(potencia)</td>
    <td style="color:#141414">2</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">* &nbsp &nbsp &nbsp / &nbsp &nbsp &nbsp // &nbsp &nbsp &nbsp %</td>
    <td style="color:#141414">3</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">+ &nbsp &nbsp &nbsp -</td>
    <td style="color:#141414">4</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">< &nbsp &nbsp &nbsp > &nbsp &nbsp &nbsp <= &nbsp &nbsp &nbsp >=</td>
    <td style="color:#141414">5</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">== &nbsp &nbsp &nbsp ~=</td>
    <td style="color:#141414">6</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">and</td>
    <td style="color:#141414">7</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">or</td>
    <td style="color:#141414">8</td>
	</tr>
  <tr style="text-align: center; vertical-align: middle;" bgcolor="#e4e4ed">
    <td style="color:#141414">= &nbsp &nbsp &nbsp += &nbsp &nbsp &nbsp -= &nbsp &nbsp &nbsp *= &nbsp &nbsp &nbsp /= &nbsp &nbsp &nbsp //= &nbsp &nbsp &nbsp %=</td>
    <td style="color:#141414">9</td>
	</tr>
</table>

## Condicionales

## Estructura `if`

Permite ejecutar un bloque de código si una condición específica es verdadera.

```python
if <condicion>:
  # bloque_verdadero
```

```python
 n = 4
if n >= 2 and n <= 5:
  print("El número está entre 2 y 5")
print(n)
```

## Estructura `if-else`
Utilizada para ejecutar un bloque de código si una condición es verdadera, y otro bloque si la condición es falsa.

```python
if <condicion>:
  # bloque_verdadero
else:
  # bloque_falso
```

```python
n = int(input("Ingrese un numero entero: "))
if n >= 2 and n <= 5:
  print("El número " + str(n) + " está entre 2 y 5")
else:
  print("El número " + str(n) + " no está entre 2 y 5")
print(n)
```

## Estructura `if-elif-else`
Permite la evaluación de múltiples condiciones en secuencia, ejecutando el bloque de código correspondiente a la primera condición verdadera.
 
```python
if <condicion_1>:
  # bloque_1
elif <condicion_2>:
  # bloque_2
elif <condicion_n>:
  # bloque_n
else:
  # bloque_por_defecto
```

```python
n = int(input("Ingrese un número entero: "))
if n < 2:
  print("El número es menor que 2")
elif n <= 5:
  print("El número está entre 2 y 5")
else:
  print("El número es mayor que 5")
print(n)
```

## Estructura `match-case` (Python 3.10+)
Ofrece una forma de comparar la variable con diferentes valores y ejecutar un bloque de código cuando se encuentra una coincidencia. Es una alternativa a las múltiples estructuras `if-elif`.

```python
match <variable>:
  case <valor_1>:
    # bloque_1
  case <valor_2>:
    # bloque_2
  case _:
    # bloque_por_defecto
```

```python
lang = input("¿Qué lenguaje de programación desea aprender? ")
match lang:
  case "Python":
    print("Excelente elección!")
  case "Java":
    print("Gran opción para aplicaciones multiplataforma.")
  case _:
    print("¡Buena suerte aprendiendo " + lang + "!")
```

## Funciones

- **Funciones**: Bloques de código reutilizables diseñados para realizar una tarea específica, mejorando la abstracción, organización y reutilización del código.

- **Dominio y Rango**: En matemáticas, el dominio es el conjunto de entrada (tipo de argumentos) de una función, y el rango es el conjunto de salida (valor de retorno).

### Utilidad de las Funciones

- Permiten encapsular secuencias de código para su reutilización.
- Facilitan la organización de procesos de manera eficiente.
- Mejoran la abstracción de procesos complejos.

### Declaración de Funciones en Python

- Se utiliza la palabra reservada `def` seguida del nombre de la función y argumentos entre paréntesis, finalizando con `:`. Las instrucciones dentro de la función deben estar indentadas.


```python
def nombre_de_la_funcion(arg1, arg2, ..., argn):
  # Instrucciones de la función
  return # Datos que retorna la función
```

```python
def elevar_al_cuadrado(x: float) -> float:
  return x**2
```

### La Función `main`
Es el punto de entrada de cualquier programa Python ejecutado como script. Define el flujo principal del programa.

```python
if __name__ == "__main__":
  # Código a ejecutar
```

```python
def elevar_al_cuadrado(x: float) -> float:
  return x**2

if __name__ == "__main__":
  x = float(input("Ingrese un numero real: "))
  x_squared = elevar_al_cuadrado(x)
  print(f"El cuadrado de {x} es {x_squared}")
```

### Scope o Alcance de Variables
 - Local: La variable solo puede ser modificada dentro de la función donde es declarada.
 - Global: La variable puede ser modificada en cualquier parte del programa.

```python
mensaje = "Hola global"

def saludar():
  global mensaje
  mensaje = "Hola desde funcion"

if __name__ == "__main__":
  saludar()
  print(mensaje)  # Imprime "Hola desde funcion"
```