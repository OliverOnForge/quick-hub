
# Javascirpt

## Indice

- [Javascirpt](#javascirpt)
  - [Indice](#indice)
  - [Programacion Assincrona](#programacion-assincrona)
    - [Callbacks](#callbacks)
    - [Promesas](#promesas)
    - [Balbacks to Promesas](#balbacks-to-promesas)
    - [Crear propmesas](#crear-propmesas)
    - [Resolver Multiples promesas](#resolver-multiples-promesas)
    - [Encadenar promesas](#encadenar-promesas)
  - [Funcione asscync](#funcione-asscync)
    - [Assync](#assync)
    - [Await](#await)
    - [Errores en Assinc](#errores-en-assinc)
  - [Modulos](#modulos)
    - [Definir e importar modulos](#definir-e-importar-modulos)
    - [Valores por defecto](#valores-por-defecto)
    - [ReadOnly imports](#readonly-imports)
  - [Generadores e iteradores](#generadores-e-iteradores)
    - [Iteradores](#iteradores)
    - [Geenradores](#geenradores)
    - [Retunr en iteradores](#retunr-en-iteradores)
    - [Delegar generadores](#delegar-generadores)
    - [simbolos de js](#simbolos-de-js)
    - [Manejo de simbolos](#manejo-de-simbolos)
    - [Iterables con iteradores](#iterables-con-iteradores)
    - [Iterables y generadores](#iterables-y-generadores)
  - [Strings](#strings)
    - [Caracteres especiales](#caracteres-especiales)
    - [concatenacion e interpolacion](#concatenacion-e-interpolacion)
    - [Comparacion de cadenas](#comparacion-de-cadenas)
    - [Subcadenas y caracteres](#subcadenas-y-caracteres)
    - [Busqueda](#busqueda)
    - [Cadenas y arreglos](#cadenas-y-arreglos)
    - [Metodos de strings](#metodos-de-strings)
    - [Unicode](#unicode)
    - [planos unicode](#planos-unicode)
  - [Expresiones regulares](#expresiones-regulares)
    - [Busqueda en expresiones](#busqueda-en-expresiones)
    - [Remplazar patrones](#remplazar-patrones)
    - [Rangos regex](#rangos-regex)
    - [Agrupamiento](#agrupamiento)
    - [Cuantificadores](#cuantificadores)
    - [](#)

---

## Programacion Assincrona

En un lenguaje de programación asíncrono como JavaScript, las tareas pueden ejecutarse secuencialmente, esto significa que podemos indicar que algunas tareas se pasen a segundo plano y esperen a su turno para ser reanudadas y ejecutadas.

Esta característica del lenguaje existe para mejorar el rendimiento del mismo, porque nos permite aprovechar al máximo las capacidades del equipo en el que se está ejecutando nuestro código.

Por lo general las tareas que se esperan sean más tardadas, o que necesiten esperar respuesta de algún otro elemento del sistema, son candidatas a ser delegadas a este proceso de espera y ejecución.

JavaScript es un lenguaje de ejecución sobre un solo hilo, esto significa que sólo puede ejecutar una tarea a la vez. Cuando una operación tarda demasiado o está esperando la respuesta de otra, decimos que bloquea las demás instrucciones, precisamente porque JavaScript no puede ejecutar dos a la vez.

Para solucionar esto, JavaScript introduce el event loop, o ciclo de eventos. El event loop se compone de dos componentes principales, una cola de mensajes y un ciclo que se encuentra iterando esta cola de mensajes. La programación asíncrona en JavaScript funciona empujando ciertas operaciones a esta cola de actividades, para que no bloqueen la ejecución de código mientras terminan, el trabajo del event loop es estar preguntando las operaciones de la cola de actividades si ya han finalizado, y cuando lo hacen, reanuda la ejecución de dicha operación, la recupera por así decirlo.

Para que todo esto funcione, necesitas una forma de delegar ciertas operaciones a esta cola, y una forma de saber cuándo estas operaciones han terminado, para hacerlo JavaScript introdujo inicialmente el concepto de callbacks, y después el de promesas, finalmente a la sintaxis se introdujeron las funciones asíncronas, todos estos conceptos están diseñados para que esta comunicación entre el event loop, la cola de actividades y tu código, suceda.

### Callbacks

### Promesas

### Balbacks to Promesas

### Crear propmesas

### Resolver Multiples promesas

### Encadenar promesas

## Funcione asscync

Cuando programamos en JavaScript, constantemente trabajamos con operaciones asíncronas como solicitudes a un servicio web, cálculos, eventos, etc.

La complejidad de las operaciones asíncronas es que no se sabe cuándo van a terminar, por lo que debe existir un mecanismo que nos informe sobre si una tarea ha sido completada o no, qué resultado produjo y si se completó con éxito o hubo un error, y en caso de que haya habido un error, de qué error se trata.

Para solucionar esto se han introducido distintas estrategias, objetos y estructuras que permitan trabajar en un flujo de operaciones asíncronas, inicialmente teníamos los callbacks, funciones que se asignaban y eran llamadas cuando la operación asíncrona había retornado.
Eventualmente se introdujeron las promesas, objetos pensados para valores asíncronos con funcionalidad adicional pensada precisamente para trabajar con 1 o varias operaciones asíncronas en un programa.

Las promesas, como aprendimos antes, introdujeron incontables mejoras por sobre los callbacks, sin embargo, la sintaxis puede parecer confusa y poco legible, además de que es un concepto que puede ser desafiante para nuevos desarrolladores de JavaScript.

En versiones más nuevas del lenguaje se introdujo el concepto de funciones asíncronas, dentro de las que trabajar con promesas se vuelve más simple con el uso de la palabra reservada await.

En este bloque conocerás los detalles de las funciones asíncronas, la sintaxis, cómo funcionan y cómo puedes usarlas para manejar operaciones asíncronas, como podrás ver más adelante, esto significará que el código de manejo de operaciones asíncronas se vuelve más expresivo y sencillo, sin perder por supuesto la funcionalidad correspondiente.

Continuemos.

### Assync

### Await

### Errores en Assinc

## Modulos

### Definir e importar modulos

### Valores por defecto

### ReadOnly imports

## Generadores e iteradores

### Iteradores 

Cualquier methodo

### Geenradores

### Retunr en iteradores

### Delegar generadores

### simbolos de js

### Manejo de simbolos

### Iterables con iteradores

### Iterables y generadores

## Strings

- **Primitivo string**

- **Objeto string**

Como has visto a lo largo del curso, en JavaScript, el texto se representa a través de strings o cadenas, es probable que identifiques este tipo de valor porque aparecen entre comillas simples o dobles.

En términos técnicos, las cadenas según la definición del lenguaje, son secuencias ordenadas de 0 más valores unsigned int de 16bits, usados principalmente para representar texto. En un programa de Ecmascript cada uno de estos elementos se guardan en unidades de código UTF-16.

Históricamente, en ciencias de la computación nos hemos referido a las representaciones de texto como cadenas o strings, porque estas son una colección de elementos o caracteres, en un orden específico.

En JavaScript, a diferencia de otros lenguajes, no existe un tipo de dato para los caracteres que conforman una cadena, por lo que, sin importar si tu cadena está compuesta de 1 o varios elementos siempre serán una cadena.

El texto de una cadena se encuentra en formato UTF-16 lo que significa que podemos usar los 1,112,064 de puntos unicode existentes. En términos prácticos esto significa que podrás usar caracteres especiales y emojis, de hecho, más adelante en el bloque hablaremos más a fondo de emojis.

Otra característica importante de las cadenas es que son inmutables, esto significa que todas las operaciones que realices sobre una cadena, generarán nuevas cadenas, en lugar de modificar la original.

A lo largo de este bloque continuarás conociendo a fondo las propiedades de una string, cómo ejecutar operaciones comunes, partir cadenas, buscar en cadenas, entre otras cosas

### Caracteres especiales

### concatenacion e interpolacion

### Comparacion de cadenas

### Subcadenas y caracteres

### Busqueda

### Cadenas y arreglos

### Metodos de strings

### Unicode

### planos unicode

## Expresiones regulares

### Busqueda en expresiones

### Remplazar patrones

### Rangos regex

### Agrupamiento

### Cuantificadores

### 

