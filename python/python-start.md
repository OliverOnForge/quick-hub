

# Mini-guia de python

https://automatetheboringstuff.com/

https://ellibrodepython.com/

---

## Indice

- [Mini-guia de python](#mini-guia-de-python)
  - [Indice](#indice)
  - [Sobre python](#sobre-python)
    - [Por qué aprender Python](#por-qué-aprender-python)
    - [Qué puedo hacer con Python](#qué-puedo-hacer-con-python)
    - [Qué es python](#qué-es-python)
    - [¿Qué es un lenguaje de progemacion?](#qué-es-un-lenguaje-de-progemacion)
  - [Sintaxis de python](#sintaxis-de-python)
  - [Hola mundo](#hola-mundo)
  - [Comentarios](#comentarios)
  - [Tipos de datos I](#tipos-de-datos-i)
  - [Operaciones numericas basicas](#operaciones-numericas-basicas)
  - [Redondeo](#redondeo)
  - [Valor absoluto](#valor-absoluto)
  - [Operaciones de texto](#operaciones-de-texto)
  - [Variables](#variables)
    - [Guion bajo](#guion-bajo)
  - [Imprimir en consola](#imprimir-en-consola)
  - [Identificar tipos de datos](#identificar-tipos-de-datos)
  - [Convertir datos](#convertir-datos)
  - [Introducir datos](#introducir-datos)
  - [Comparadores](#comparadores)
  - [Tipos de datos II](#tipos-de-datos-ii)
  - [Estructuras de datos](#estructuras-de-datos)
    - [Boleanos](#boleanos)
    - [Listas](#listas)
    - [Matrices](#matrices)
    - [Tupla](#tupla)
    - [desempaquetado engrupo](#desempaquetado-engrupo)
  - [Longitud](#longitud)
  - [Condicionales](#condicionales)
  - [Operadores booleanos](#operadores-booleanos)
  - [Bulce definido](#bulce-definido)
  - [Bucle indefinido](#bucle-indefinido)
  - [Estructuras de datos 1](#estructuras-de-datos-1)
  - [Funciones](#funciones)
  - [Enviroments](#enviroments)
  - [Librerias](#librerias)
  - [Modulos](#modulos)
  - [pip freeze](#pip-freeze)
  - [Programacion Funcional](#programacion-funcional)
  - [threads](#threads)

---

## Sobre python

### Por qué aprender Python

Python es un lenguaje con sintaxis simple, lo que lo hace facil de aprender para cualquiera, desde programadores hasta no programadores, la forma en que tebraja hace que puedas aprender a tu ritmo, te enseña fundamentos de programacion que se extrapolan a otros lenguajes (te enseña a programar mejor), por ultimo es el lengujare mas multifacetico que existe hasta el momento.

### Qué puedo hacer con Python

Como ya mencione, Python es uno de los lenguajes más versátiles que existen actualmente, lo que quiere decir que se usa en una grn variedad de nichos, tecnologias y areas, solo nombrare las principales, puedes usar python para:

- Procesar grandes volúmenes de información, crear gráficos estadísticos y obtener conclusiones de negocios a partir de datos crudos (Ciencia de Datos y Análisis)

- Entrenar modelos que pueden reconocer rostros, predecir el comportamiento del mercado de valores o hacer funcionar asistentes de voz (Inteligencia Artificial y Machine Learning)

- Crear el "cerebro" de sitios web complejos, manejando bases de datos y usuarios de forma segura (Desarrollo Web Back-end)

- Escribir programas pequeños para realizar tareas repetitivas, como renombrar miles de archivos, extraer información de sitios web o enviar correos automáticos (Automatización de tareas y Scripting)

- Crear versiones iniciales de aplicaciones y software (Desarrollo de Software y Prototipado)

- En campos como la física, la biología y la astronomía para realizar simulaciones matemáticas complejas y cálculos numéricos de alta precisión (Computación Científica)

- En dispositivos como Raspberry Pi para controlar sensores, cámaras y sistemas de domótica en el hogar (Internet de las Cosas)

### Qué es python

- Python es un lenguaje de programación de alto nivel: Su sintaxis se parece mas al lenguje humano que a los 0 y 1 que es lo que entiende la maquina.

- Es un lenguaje interpretado: que la computadora puede leer diractamente sin convertir el archivo a otro.

- Posee una filosofía hace hincapié en la legibilidad de su código: que sea facil de escribir, leer y entender.

- Es multiparadigma: Soporta varias funciones o formas de programar de otros lenguajes.

- Es dinámico: Requiere menos explicacion sobre los valores y datos que maneja.

- Y multiplataforma: Esta disponible para instalarse y usarse en multiples sistemas operativos.

### ¿Qué es un lenguaje de progemacion?

Es un conjunto de reglas, símbolos y palabras que nos permiten dar instrucciones precisas a una computadora para que realice una tarea.

"Si la computadora fuera un chef, el codigo seria la receta"

## Sintaxis de python

## Hola mundo

Por tradicion la primera linea de codigo que uno aprende a escribir.

> print("hola mundo!")

## Comentarios

Son bloques de texto que python ignora a la hora de ejecutar el codigo, esto permite dejar explicaciones o referencias en el codigo haciendolo mas entendible.

- Comentario de una linea (#):

> \# este es un comentario simple

- Comentario de multi linea ("""):

> """
> Este es un comentario
> que se puede hacer en mas de una linea
> """

## Tipos de datos I

Python acepta tres tipos de datos principales

- **Numeros enteros:**

> -8, -2, 0, 1 ,8 ,10

- **Numeros con punto (float)**:

> -4.2, -2.5, 0, 0.5, 15.20

- **Texto (string):**

Para que python sea conciente que lo que introduces es texto este debe estar entre comilla simple ('') o comilla dobre ("")

> 'Ejemplo de texto con comilla simple'
> "Ejemplo de texto con comilla doble"

La puedes usar cualquiera sin problema, la idea de tener dos formas de hacerlo es para poder usar las otras comillas dentro del mismo texto:

> "ejemplo de uso de 'comillas simples' dentro de comillas dobles"
> 'ejemplo de uso de "comillas dobles" dentro de comillas simples'

## Operaciones numericas basicas

- **Suma (+):**

> 2 + 8
> 10

- **Resta (-):**

> 8 - 2
> 6

- **Multiplicaion (*):**

> 2 * 8
> 16

- **Division (/):**

> 16 / 2
> 8

- **Division entera (//):**

> 15 / 2
> 7

- **Residuo (%):**

> 15 % 2
> 1

- **Exponenete(`**`):**

~~~Python
4 ** 2
16
~~~

## Redondeo

La funcion **round()** permite redondear valores numericos con decimales, es recomendable experimentar un poco para entenderla del todo.

~~~Python
round(7.7)
8
~~~

Tambien permite redondear hasta cierdo numero de decimales al agregar una coma y la cantidad de decimales que quieres conservar, en el siguiente ejemplo queremos 2 decimales 0.00:

~~~Python
round(3.1415926434, 2)
3.14
~~~

## Valor absoluto

Tabien llamada funcion modulo **abs()**, basicamente convierte cualquier numero negativo en psoitivo.

~~~Python
abs(-25)
25
abs(-3.14)
3.14
~~~

## Operaciones de texto

- **Concatenacion (+):** Permite juntar dos o mas strings (textos)

~~~Python
"Maria" + " " + "Fernanda" + " " + "Gracia" + " " + "Jimenez"
~~~

- **Replicacion (*):** Perminte repetir o replciar un string (texto)

~~~Python
"Maria" * 5
MariaMariaMariaMariaMaria
"Hola " * 3
Hola Hola Hola
~~~

## Variables

Son espacios en memoria que permiten guardar informacion

~~~Python
nombre_variable = dato_a_guardar
~~~

Ejemplos:

~~~Python
nombre = 'Juan fernando'
edad = 24
resultado_operacion = 5 / 3
~~~

Es posible crear declarar multiples variables en una sola linea:

~~~Python
nombre, edad = 'Juan fernando', 24
~~~

> este metodo en particular usa [desempaquetado de tuplas](#desempaquetado-de-tuplas)

Aunque puedes nombrar tus variables prácticamente como quieras, Python tiene algunas restricciones. El nombre de tu variable debe cumplir las siguientes cuatro reglas:

- No puede contener espacios.
- Solo puede contener letras, números y el guion bajo (_).
- No puede comenzar con un número.

### Guion bajo

El guion bajo es una variable valida, sin embargo no se recomeinda su uso como una variable comun. Principalmete porque suele usarse de forma especial:

- para evitar valores en [tuplas](#tupla)

## Imprimir en consola

La fucnion **print()** es usada para que Python muestre/imprima en consola un valor o dato especifico.

> print()

Puedes imprimir:

- **Numeros:**

> print(4)

- **Resultados de operaciones:**

> print(8*2)

- **Texto:*

>print("texto")

- **Datos de variables:**

> edad_juan = 18
> print(edad_juan)

## Identificar tipos de datos

La funciion **type()** es una funcion que permite saber el tipo de dato.

> type(5)
> <class 'int'>
> type(7.5)
> <class 'float'>

Tambien te permite saber el tipo de dato que hay dentro de una variable

> nombre_usuario = 'Joseline'
> type(nombre_usuario)
> <class 'str'>

## Convertir datos

Convertir datos es una practica bastante comun en los lenguajes de programacion ya que normalmente no se pueden realizar operacion entre tipos de datos diferentes.

Usualmente python te avisa si estas intentando hacer operaciones entre tipos de datos diferentes con un error.

- **Convertir a entero ( int() ):** Te permite convertir los numeros con decimal (float) a valores numericos enteros, esto lo logra eliminando la parte decimal (no redondea)

> int(7.6)
> 7

- **Convertir a decimal ( float() ):** Permite convertir un numero entero a decimal, asignandole un valor de .0 al final.

> float(5)
> 5.0

- **Convertir a texto ( str() ):** Permite convertir valores numericos a texto.

> str(7.6)
> '7.6'
> str(5)
> '5'

## Introducir datos

- **Introducir datos ( input() ):** Puedes hacer que python te pida o pida al usuario que ingrese datos directamente, para que la informacion no se pierda es necesario guardarla en una variable.

> dato_usuario = imput()
> print(dato_usuario)

Tambien es posible escribir un mensaje para que la persona que va a introducir el dato tenga idea de que es lo que se le pide.

> nombre_completo = imput('Introduce tu nombre completo: ')
> print(nombre_completo)

## Comparadores

Se usan para realizar comparaciones entre datos.

> funcionan como pregunta y regresan un 'Si' (True) o un 'No' (False).

- ¿Es igual a?: ==
- ¿Es diferente de?: !=
- ¿Es mayor a?: >
- ¿Es menor a?: <
- ¿Es mayor o igual a?: >=
- ¿Es menor o igual a?: <=

Ejemplos:

- En texto: Es 8 igual a 9?
  Codigo: 8 == 8
  Resultado: False

- Es 'Juan' diferente de 'Carlos'?
  Codigo: 'Juan' != 'Carlos'
  Resutlado: True

- Es el valor guardado en la variable edad_ana mayor que el valor en la variable edad_pepe
  Codigo: edad_ana > edad_pepe
  Resultado: False


## Tipos de datos II

## Estructuras de datos

True

False

### Boleanos

### Listas

~~~Python
lista_numeros = [1,2,3,4]
lista_strings = ['palabra','segunda palabra']
~~~

#### sub listas

#### metodos de listas

- [.apend]
- [.insert]
- [.extend]
- .in
- .reove
- .pop
- .clear
- .copy
- .reverse (::-1)
- .sort (reverse = False/True)

### Matrices

### Tupla

son inmutables (al crearla se vuelve inmodificale hasta mientras se ejecuta el rpograma)

se puede crear usando parentesis '()'

~~~Python
tupla_numeros = (1,2,3,4)
tupla_strings = ('palabra','segunda palabra')
~~~

o solo usando comas:

~~~Python
tupla_numeros = 1, 2, 3, 4
tupla_strings = 'palabra', 'segunda palabra'
~~~

tambien se puede crear una tupla de un solo elemento

~~~Python
tupla_numeros = 1,
tupla_strings = 'palabra',
~~~

#### desempaquetado de tuplas

Uno de los metodos principales es asingar una variable a cada valor de una tupla

~~~Python
valor1, valor2, valor3, valor4 = 24,30,25,15
~~~

esto es equivalente a:

~~~Python
tupla_numeros = (24,30,25,15)
valor1, valor2, valor3, valor4 = tupla_numeros
~~~

#### usando guion en tuplas

> Esto es la que sucede cuando declaramos multiples [variables](#variables) en una sola linea

Tambien podemos evitar valores usando la [variable guion bajo](#guion-bajo) '_'

~~~Python
tupla_numeros = (24,30,25,15)
valor1, _, valor3, _ = tupla_numeros
~~~

### desempaquetado engrupo

es posible separar los valores en grupos:

~~~Python
tupla_numeros = (24,30,25,15)
valor1, *utimos_valores = tupla_numeros
*primera_mitad, *segunda_mitad = tupla_numeros
primer_valor, *_, ultimo_valor = tupla_numeros
~~~

## Longitud

- **Cantidad de caracteres ( len() ):** esta funcion te permite saber la cantidad de caracteres (inccluyendo espacio) que tiene una cadena

## Condicionales

- **if():**

- **else if():**

- **else:**

## Operadores booleanos

## Bulce definido

## Bucle indefinido

## Estructuras de datos 1

## Funciones

## Enviroments

## Librerias

## Modulos

## pip freeze

saber las dependencias intaladas y la version

## Programacion Funcional

## threads