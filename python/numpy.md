
# Numpy

## Indice

- [Numpy](#numpy)
  - [Indice](#indice)
  - [Sobre Numpy](#sobre-numpy)
    - [¿Qué es Numpy?](#qué-es-numpy)
    - [¿Qué puedo hacer con Nunpy?](#qué-puedo-hacer-con-nunpy)
    - [Caracteristicas](#caracteristicas)
    - [Porque usar Numpy](#porque-usar-numpy)
  - [mas](#mas)
    - [Tipos de datos](#tipos-de-datos)
    - [arryas](#arryas)
    - [Idexing](#idexing)
    - [Slice](#slice)
    - [Reshaping](#reshaping)
    - [Newaxist](#newaxist)
  - [Opereacoines artimeticas con vectores](#opereacoines-artimeticas-con-vectores)
  - [Universal Functions](#universal-functions)
  - [agraciones por ejes](#agraciones-por-ejes)
  - [Broadcasting](#broadcasting)
  - [Boolean indexing](#boolean-indexing)
  - [Fancy indexing](#fancy-indexing)
  - [Herramientas de medicion](#herramientas-de-medicion)
  - [Gestion de memoria](#gestion-de-memoria)
    - [dtype](#dtype)

---

## Sobre Numpy

### ¿Qué es Numpy?

Una biblioteca o toolkit para python

### ¿Qué puedo hacer con Nunpy?

### Caracteristicas

- **Fixed size**

- **Homogeneo**

- **Vectorizacion**

- **Implementacion en C**

### Porque usar Numpy

> Siempre que puedas usar numpy en python haslo!

## mas

### Tipos de datos

- **int32**
- **int**
- **float**
- **complex**
- **bool**
- **str**
- **object**
- **datetime**
- **time delta**
- **unit**

### arryas

#### Atributos

- **ndim**
- **shape**
- **size**
- **dtype**
- **itemsize**
- **nbytes**

- **zeros**
- **ones**
- **full**
- **arange**
- **linespace**
- **random**

~~~Python
np.random.random((4, 5))
~~~

- **randint**

~~~Python
np.random.randint((3, 20, size = (1, 3)))
~~~

### Idexing

~~~Python
arrid = [0,1,2,3,4,5,6,7,8,9]
arrid(0)
arrid(-1)
arrid(0)
arrid(2:6)
arrid(::2)
arrid(::-1)
~~~

### Slice

~~~Python
arri2d = [ [0,1,2,3,4],[0,1,2,3,4],[0,1,2,3,4],[0,1,2,3,4] ]
arri2d[0,0]
arri2d[2,3]
arri2d[1,:]
arri2d[:,2]
arri2d[0:2, 1:3]
~~~

> Los slice (:) son vistas o apuntadores del arrelo original no compias de este, lo que implica que modificar uno o una parte de estos modifica el valor en la posicion correspondiente en el array original

~~~Python
original = [0,1,2,3,4,5,6,7,8,9]
vista = original[0:4]
vista[0] = 100
print(original)
~~~

si deseas una copia enteonces es necesario expresarlo directamente

~~~Python
original = [0,1,2,3,4,5,6,7,8,9]
vista = original[0:4].copy()
vista[0] = 100
print(original)
~~~

### Reshaping

Permite modificar la forma del arreglo sin cambiar los datos. Al hacer reshape se crea un arreglo nuevo con las dimensiones especificadas.

> Al hacer un Reshape la cantidad de valores entre ambas formas deben ser los mismos, si falta o sobra un valor entonces python lanza un error

~~~Python
original = [0,1,2,3,4,5,6,7,8]
cambio = original.reshape(3,3)
print(original)
print(cambio)
~~~

- **Auto**

Puedes usar (-1) dentro de los parametros de shape para que numpy calcule ese valor de forma automatica, para ello numpy divide la cantidad todal de elementos entre el valor ya dado y toma el resultado como el valor que deberia tener el atributo (-1).

~~~Python
original = [0,1,2,3,4,5,6,7,8] # vavlores = 9
cambio = original.reshape(3,-1) # total_valores/3 = 9/3=3
print(original)
print(cambio)
~~~

> Esto es util para lograr que una cantidad de arroeglos mantengan una estructura basica definida.

#### Aplanar una matriz

- **Flatten** devuelve una copia

~~~Python
otiginal = [ [0,1,2,3,4],[0,1,2,3,4],[0,1,2,3,4],[0,1,2,3,4] ]
aplando = original.flatten()
print(original)
print(aplando)
~~~

- **Ravel** dvuelve una vista siempre que sea posible

~~~Python
otiginal = [ [0,1,2,3,4],[0,1,2,3,4],[0,1,2,3,4],[0,1,2,3,4] ]
aplando = original.ravel()
print(original)
print(aplando)
~~~

### Newaxist

~~~Python
original = [0,1,2,3,4,5,6,7,8] # vavlores = 9
agregar_axis = original.reshape(:,np.newaxis) # total_valores/3 = 9/3=3
print(original)
print(agregar_axis)
~~~

## Opereacoines artimeticas con vectores

En numpy existen herramientas que permine y manejanoperaciones esntre vectores, estas on:

- **Suma (+)**
- **Resta (-)**
- **Multiplicacion (*)**
- **Division (/)**
- **Potencia (**)**
- **Modulo (%)**

~~~Python
a = [0,1,2,3,4]
b = [4,5,6,7,8]
Suma = a+b 
Resta = a-b
Multiplicacion = a*b
Division = a/b
Potencia = a**2
Modulo = b%3
~~~

## Universal Functions

~~~Python
a = [0,1,2,3,4]
b = [4,5,6,7,8]

print()
~~~

## agraciones por ejes

## Broadcasting

Es la mecanica que usa numpy para operear entre arreglos de con shapes distintos

Reglas:

- Si los dos arreglso no tienen el mismo numero de dimenciones entonces la de forma menor se rellena con 1s en la parte faltante.

- Si la forma no conicide en alguna dimencion, entonce el array cuya forma sea 1 se estira para conicidir con esa forma.

- Si en alguna dimencion los tamaños no coinciden y ninguna es igual a 1 entonces se lanza un error.

## Boolean indexing

Permiten seleccionar elementos de una arreglo de forma expresiva.

~~~Python
arrey = [0,1,2,3,4,5,6,7,8,9]
mask = arrey > 5 
~~~

> posteriormene podemos aplicar esa mascara al areglo original para que solo nos regrese los valores que son true

np.where

## Fancy indexing

Permite seleccionar elementos al pasar un arreglo que contenga las pisiciones deseadas, este metodo siempre crea una copia y no una vista.

~~~Python
arrey = [0,1,2,3,4,5,6,7,8,9]
selec_values = [0,2,4,7]
values = arrey[selec_values]
~~~

## Herramientas de medicion

- timeit
- time.perf_counter

## Gestion de memoria

### dtype
