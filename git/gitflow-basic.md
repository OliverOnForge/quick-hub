
# Gitflow

## Indice

- [Gitflow](#gitflow)
  - [Indice](#indice)
  - [Que es git workflow](#que-es-git-workflow)
  - [Donde se aplica?](#donde-se-aplica)
  - [Como legir un workflow](#como-legir-un-workflow)
  - [Feature base](#feature-base)
  - [Gitflow](#gitflow-1)
  - [Trunck based](#trunck-based)
  - [Commits](#commits)
  - [Menajse de commit](#menajse-de-commit)
  - [nombrar ramas](#nombrar-ramas)
  - [merge](#merge)

## Que es git workflow

son lineamientos y estandares que se usan en el proyeccto que perminten mejorar la productividad al mantener un historial consistente

## Donde se aplica?

- nombramiento de ramas
- nombramiento de commits
- creacion de ramas
- merge de ramas

## Como legir un workflow

No esixte una linea unica de lineamientos, ya que cada equipo pude adaptarlo a si mismo, a la empresa y al pryoecto. Lo importante es que el flow nos permita responder a inicdencias de forma rapida y optima, asi como revertir cambios y arrreglar errores de forma eficiente.

- funciona para el equipo/empresa
- perimite responder a incidencias

## Feature base

Cada desarrollador crea una nueva rama para cada cambio que se v a introducir en el codigo y al terminar se envia un pull requests con el codigo que se quiere arreglar, a travez de un repositorio remoto.

- el codigo es revisado y verificado por los demas compañeros del equipo antes de agregarlo a la rama principal
- mejora la cadildad del codigo
- ayuda a encontrar errores antes de que estos se conviertan en correciones mayores.

**en que ayuda**

- Mejora la calidad del codigo
- fomenta la colaboracion en el equipo
- Aumenta el conocimiento del equipo
- Ahorra tiempo y recursos

## Gitflow

La estrategia mas usada por las empresas

utiliza dos ramas principales:

- main:  contiene la version estable del codigo
- develop: contiene la ultima version del codigo en desarrollo

tambien se pueden crear ramas secundarias para mejorar el flujo de trabajo, estas ramas se crean en develop y son:

- feature: estas se usas para desarrollar nuevas carateristicas del proyecto. y se fusionan con dev al completarla
- release: se utilizan para preparar una version del codigo para su lanzamiento
- fix: corregir errores comunes
- hotfix: se utilizan para corregir errores criticos en la rama main ya que es donde estan los errores mas criticos, despues se fusionan con la rama main y luego con la rama develop.

## Trunck based

especializado en desplieque continuo

se centra en la utilizacion de una unica rama principal para el desarrollo del proyecto, siendo que los trabajadores trabajan sonbre la rama principal, sin necesidad de crear ramas para features. las ramas que se llegan a crear son de corta vida y al pasar los test automatizados y son integradas con la rama principal, estas itenraciones son muy pequeñas y se integran directamente en el flujo principal cuando estan lsitas.

- este flow se centra en la iteracion y entrge ocntinua.
- requiere que los desarrolladores trabajen de la mano para lograr que los cambios se integren sin problema.

**ventajas**

- facil integracion en equipos pequeños.
- simplicidad
- promueve la entrega rapida.
- menor complejiddad
- mayor visibilidad

> este flow solo se recomienda para desarrolladores con mucha experiencia y proyectos que estan iniciando, no para porectos grandes o complejos

## Commits

has comits pequeños y de forma consecutiva, la idea es hacer commits cada vez que logras tener una pieza de codigo completa.

## Menajse de commit

buenos mensajes de commit, el mensaje debe ser lo minimo necesario para dar contexto a cada uno de los cambios.

- el titulo debe tener maximo 50 caracteres

- usa verbos imparativos como fixx, add, delete, update

- deja una linea en blanco entre el titulo y la descripcion

- enfocate en el que y porque. el como se debe responder al mirar el codigo no el commit.

- sigue las convenciones definiadas por el equipo

## nombrar ramas

los nombres al igual que los de commit deben ser descritivos.

- deben ser cortos y concisos

- descriptivos y que mapermitan identificart facilmente los cambios que hay ne cada rama

- se pueden usar los ID de los sisntema de tikets o issues.

- sin importan la nomenclatura que tenga el queipo debe ser el mismo para todos y debe ser concistente.

cuando crear una nueva rama?

cadavez que se ve a realizar un cambio en el codigo, como: agregar, arreglar, eliminar, modiicar

## merge