
# Javascritp Web

## Indice 

- []()
  - []()

---

## Variablss

## Constantes

## Valores numericos

## Operaciones aritmeticas

## Tipos de datos

## Coercion de tipos

## Bolleanos

## Truthy & Falsi

En JavaScript y a lo largo del curso me escucharás usar dos conceptos que de hecho son bastante divertidos de pronunciar, los valores Truthy y Falsy.

Decimos que un valor es Falsy cuando su representación booleana es falso, como mencioné en el tema anterior, los valores Nan, null, 0, -0, “”, y false son los considerados falsy.

Los valores truthy por su parte, son todos aquellos que no sean falsy, es decir que su representación booleana sea verdadero.

En muchos contextos del lenguaje, decir que retorna verdadero o falso no es correcto si no están retornando un booleano, por eso solemos usar las expresiones truthy para referrnos a cualquier valor verdadero, no solamente true, y falsy, para referirnos a cualquier valor falso, no solamente false.

Cuando el intérprete necesita saber si un valor es truthy o falsy hace un proceso llamado type coercion, del que hablaremos más adelante, que en términos simples significa que hará una conversión implícita, si lo simplificamos más significa que el lenguaje convertirá el valor a verdadero para evaluar si es truthy o falsy. Esta conversión es, digamos, momentánea, el valor original o la variable no cambian su valor, javaScript sólo obtendrá su representación booleana para saber si es truthy o falsy, sin modificar el valor original.

Continuemos.

## Comparadores

## Condicionales

## Cliclos

## Undefined null nan

## Funciones

### Scope alcnace

### alcance de funcion y de bloque

### argumentos de funcionaes

### Pase por valor y por referencia

### Funciones puras

### first class objects

### hoisting

## Arreglos

### Operaciones funcinales con arreglos

En versiones modernas de javaScript, los arreglos poseen una serie de métodos que nos permiten realizar operaciones para, recorrerlos, inspeccionarlos, o modificarlos.

Estas operaciones se introducen en la revisión de 2009 del lenguaje, conocida como ES5. ES5 es una de las revisiones más importantes que se han hecho al lenguaje, en parte por la introducción de estas operaciones.

Lo que tienen en común las operaciones forEach, map, reduce, filter y find, es que son métodos que puedes usar en cualquiera arreglo, y que operan a través de funciones que enviamos como argumento para estos métodos, la sintaxis la iremos destacando en vídeos individuales para cada operación.

Este tipo de trabajo adopta prácticas del paradigma de programación funcional, en el que la mayoría del código se estructura a través del uso de funciones.

El uso de las operaciones que verás en los próximos temas normalmente reduce la complejidad y lo verboso del código, es decir, lo hace más sencillo de comprender y reduce la cantidad de líneas que debes escribir para realizar una operación.

Es importante aclarar que un bloque de código no es mejor cuando es más pequeño que otro, cuando programamos debemos buscar que el código sea comprensible, no corto. Para evaluar este aspecto veamos las siguientes operaciones, ambas realizan lo mismo utilizando diferentes enfoques:

for(let i = 0;i < arreglo.length; i++){
   let element = arreglo[i];
   console.log(element);
}

arreglo.forEach(function(element){ console.log(element) });

En este escenario, además de que usar un método del arreglo hace el código más corto, e incluso lo puede resumir en una sola línea, también es más expresivo, forEach nos da un indicio de que hace el código, para cada uno de los elementos.

Veamos en los siguientes temas más detalles de cómo funcionan estas operaciones funcionals sobre arreglos.

### REcorrer un areglo con for forEach

### modificar arreglos con map

### Filtrar elementos con filter

### reducir arrelo a un elemento con reduce

### Buscar elementos con uin arreglo

### spread y rest sintaxis

## Objetos y Json

### Declar objeto

### Shordthad sintaxis

### Duplicar y cobianr objetos

### Destructurin assignament

### Funciones constructoras

## Contexto

### This

### Arrow functions

### This y arrow function

### Bind, call y apply

## Clases

### Definir Clase

### Metodos y propiedades

### Alcence de Propiedades

### Metodo constructor

### Herencia de clasese

### Metodos Accesores

### Metodos y propiedadees estaticas

## Prototipos

### Programacion oriendada a prototipos

### Conceptos de prototipos

### Prototipos en la practica

### Herencia de prototipos

