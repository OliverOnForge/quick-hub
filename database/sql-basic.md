
# SQL

Mini-guia rapida

## Indice

- [SQL](#sql)
  - [Indice](#indice)
  - [Sobre SQL](#sobre-sql)
    - [¿Que es SQL?](#que-es-sql)
    - [¿Donde se usa SQL?](#donde-se-usa-sql)
    - [¿Que es una base de datos relacional?](#que-es-una-base-de-datos-relacional)
    - [¿Por que usar SQL?](#por-que-usar-sql)
    - [Ventajas de SQL](#ventajas-de-sql)
    - [Peligros de usar SQL](#peligros-de-usar-sql)
  - [SQL](#sql-1)
    - [Sintaxis](#sintaxis)
    - [Movimientos basicos](#movimientos-basicos)
    - [Parametros](#parametros)
    - [a](#a)

---

## Sobre SQL

Es un lenguaje estructurado de consulta dsieñado para crear y trabajar con basese de datos almacenados como un conjunto de tablas

base de datos relacional

Puede usar las instrucciones SQL para almacenar, actualizar, eliminar, buscar y recuperar información de la base de datos. También puede usar SQL para mantener y optimizar el rendimiento de la base de datos.


### ¿Que es SQL?

SQL o Structured Query Language es un lenguaje  estándar diseñado específicamente para interactuar con bases de datos relacionales. En términos sencillos, es el "idioma" que usamos para pedirle a una base de datos que guarde, organice, modifique o nos entregue información.

### ¿Donde se usa SQL?

Basicamente en todos los lugares donde se ocupe organizar y almacenar informacion.

popular que se usa con frecuencia en todos los tipos de aplicaciones. Los analistas y desarrolladores de datos aprenden y usan SQL porque se integra bien con los diferentes lenguajes de programación.

Por ejemplo, pueden incrustar consultas SQL con el lenguaje de programación Java para crear aplicaciones de procesamiento de datos de alto rendimiento con los principales sistemas de bases de datos SQL, como Oracle o MS SQL Server. Además, SQL es muy fácil de aprender, ya que en sus instrucciones se utilizan palabras clave comunes en inglés.

- Desarrollo web con base de datos
- Almacenamiento de datos
Pipelines de ingenieria de datos
- Generacion de reportes
- Analitica
- Prubas de softwaer
- En excel
- Abtener insights de datos
- Proteger la seguridad de los datos

### ¿Que es una base de datos relacional?

Una base de datos relacional almacena información en forma de tabla, con filas y columnas que representan diferentes atributos de datos y las diversas relaciones entre los valores de datos.

Una base de datos relacional es un tipo de base de datos que almacena y proporciona acceso a puntos de datos que están relacionados entre sí. Las bases de datos relacionales se basan en el modelo relacional, una forma intuitiva y directa de representar datos en tablas. En una base de datos relacional, cada fila de la tabla es un registro con una identificación única llamada clave (Primary Key), y las columnas de la tabla contienen atributos de los datos.

### ¿Por que usar SQL?
SQL (Structured Query Language) es el lenguaje estándar diseñado específicamente para comunicarse con y gestionar las bases de datos relacionales. Se utiliza para realizar tareas como crear estructuras, actualizar datos, recuperar información y gestionar el acceso. Es el núcleo de sistemas gestores de bases de datos relacionales (RDBMS) populares como MySQL, PostgreSQL, Oracle, Microsoft SQL Server y SQLite.

### Ventajas de SQL

- **Estandarizado:** Es un lenguaje estándar de la industria (ISO/ANSI), lo que significa que el conocimiento es transferible entre diferentes motores de bases de datos.

- **Sintaxis intuitiva:** Su estructura basada en el idioma inglés lo hace fácil de leer y aprender.

- **Procesamiento de conjuntos de datos:** A diferencia de lenguajes procedimentales, en SQL defines *qué* datos quieres, y el motor de base de datos se encarga de optimizar *cómo* obtenerlos.

- **Integridad de datos:** Permite definir restricciones (constraints) para asegurar que la información almacenada sea válida y coherente.

### Peligros de usar SQL

La inyección de código SQL es un ataque cibernético que implica engañar a la base de datos con consultas SQL. Los piratas informáticos usan la inyección de código SQL para recuperar, modificar o dañar los datos de una base de datos SQL. Por ejemplo, pueden rellenar una consulta SQL en vez del nombre de una persona en un formulario de envío para llevar a cabo un ataque de inyección de código SQL.

---

## SQL

### Sintaxis

SQL tiene una sintaxis felixble, lo que permite majenar varios tipos de colsultas de forma simple pero hay tres reglas importantes que se deben tomar en cuenta:

- **No distigue mayuscusculas y minusculas:** esto singinifa que puedes usar una, otra, o combinarlas, pero se recomienda usar

- **Se usa el espacio como separador ( ):**

- **Las linas de consutla deben terminar con un (;):**

### Movimientos basicos

#### Crear tabla

Sintaxis

~~~SQL
CREATE TABLE <nombre_tabla> ( <campo1> <campo2> <campo3> )
~~~

Ejemplo

~~~SQL
CREATE TABLE <nombre_tabla> ( <campo1> <campo2> <campo3> )
~~~

#### ID

Es un campo comun que se coloca por buena practica en cada tabla y sirve para que SQL genere un identificacor unico para cada parametro de la tabla

~~~SQL
ID <parametro1> <parametro2>
~~~

**Parametros:**

- Datatype: INTEGRER
- AUTO INCREMENT
- PRIMARY KEY

#### Leer


#### Actualziar

#### Eliminar

### Parametros

Los parametros de base de datos son las 

- **VARCHAR:** se usa para definir la cantidad de espacio que SLQ va a desginar a ese parametros
- DATATIME
- INTEGRER



### a


-- A cont. se crea y se elimina una base de datos. Los nombres de la base de
-- datos y de la tabla son sensibles a mayúsculas y minúsculas.
CREATE DATABASE someDatabase;
DROP DATABASE someDatabase;

-- Lista todas las bases de datos disponibles.
SHOW DATABASES;

-- Usa una base de datos existente en particular.
USE employees;

-- Selecciona todas las filas y las columnas de la tabla departments en la base
-- de datos actual. La actividad predeterminada es que el intérprete desplace
-- los resultados por la pantalla.
SELECT * FROM departments;

-- Recupera todas las filas de la tabla departments, pero sólo las columnas
-- dept_no y dept_name.
-- Separar los comandos en varias líneas está permitido.
SELECT dept_no,
       dept_name FROM departments;

-- Obtiene todas las columnas de departments, pero se limita a 5 filas.
SELECT * FROM departments LIMIT 5;

-- Obtiene los valores de la columna dept_name desde la tabla departments cuando
-- dept_name tiene como valor la subcadena 'en'.
SELECT dept_name FROM departments WHERE dept_name LIKE '%en%';

-- Recuperar todas las columnas de la tabla departments donde la columna
-- dept_name comienza con una 'S' y tiene exactamente 4 caracteres después
-- de ella.
SELECT * FROM departments WHERE dept_name LIKE 'S____';

-- Selecciona los valores de los títulos de la tabla titles, pero no muestra
-- duplicados.
SELECT DISTINCT title FROM titles;

-- Igual que el anterior, pero ordenado por los valores de title (se distingue
-- entre mayúsculas y minúsculas).
SELECT DISTINCT title FROM titles ORDER BY title;

-- Muestra el número de filas de la tabla departments.
SELECT COUNT(*) FROM departments;

-- Muestra el número de filas en la tabla departments que contiene 'en' como
-- subcadena en la columna dept_name.
SELECT COUNT(*) FROM departments WHERE dept_name LIKE '%en%';

-- Una unión (JOIN) de información desde varias tablas: la tabla titles muestra
-- quién tiene qué títulos de trabajo, según sus números de empleados, y desde
-- qué fecha hasta qué fecha. Se obtiene esta información, pero en lugar del
-- número de empleado se utiliza el mismo como una referencia cruzada a la
-- tabla employee para obtener el nombre y apellido de cada empleado (y se
-- limita los resultados a 10 filas).
SELECT employees.first_name, employees.last_name,
       titles.title, titles.from_date, titles.to_date
FROM titles INNER JOIN employees ON
       employees.emp_no = titles.emp_no LIMIT 10;

-- Se enumera todas las tablas de todas las bases de datos. Las implementaciones
-- típicamente proveen sus propios comandos para hacer esto con la base de datos
-- actualmente en uso.
SELECT * FROM INFORMATION_SCHEMA.TABLES
WHERE TABLE_TYPE='BASE TABLE';

-- Crear una tabla llamada tablename1, con las dos columnas mostradas, a partir
-- de la base de datos en uso. Hay muchas otras opciones disponibles para la
-- forma en que se especifican las columnas, como por ej. sus tipos de datos.
CREATE TABLE tablename1 (fname VARCHAR(20), lname VARCHAR(20));

-- Insertar una fila de datos en la tabla tablename1. Se asume que la tabla ha
-- sido definida para aceptar estos valores como aptos.
INSERT INTO tablename1 VALUES('Richard','Mutt');

-- En tablename1, se cambia el valor de fname a 'John' para todas las filas que
-- tengan un valor en lname igual a 'Mutt'.
UPDATE tablename1 SET fname='John' WHERE lname='Mutt';

-- Se borra las filas de la tabla tablename1 donde el valor de lname comience
-- con 'M'.
DELETE FROM tablename1 WHERE lname like 'M%';

-- Se borra todas las filas de la tabla tablename1, dejando la tabla vacía.
DELETE FROM tablename1;

-- Se elimina toda la tabla tablename1 por completo.
DROP TABLE tablename1;