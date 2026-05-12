
# Git

Mini-guia rapida

---

## Indice

- [Git](#git)
  - [Indice](#indice)
  - [Sobre git](#sobre-git)
    - [Cuándo usar git](#cuándo-usar-git)
    - [Cuándo no usar git](#cuándo-no-usar-git)
    - [Qué es git?](#qué-es-git)
    - [Qué es un repositorio](#qué-es-un-repositorio)
    - [Cómo funciona](#cómo-funciona)
    - [Partes principales](#partes-principales)
    - [Servidores y repositorios remotos](#servidores-y-repositorios-remotos)
    - [Buenas preacticas de Git](#buenas-preacticas-de-git)
    - [Buenos commits](#buenos-commits)
    - [Herramientas útiles](#herramientas-útiles)
  - [Crear repositorios](#crear-repositorios)
    - [git init](#git-init)
    - [git clone](#git-clone)
  - [Estado y Seguimiento de Cambios](#estado-y-seguimiento-de-cambios)
    - [git status](#git-status)
    - [git stash](#git-stash)
    - [git add](#git-add)
    - [git diff](#git-diff)
    - [git clean](#git-clean)
  - [Historial de Versiones](#historial-de-versiones)
    - [git commit](#git-commit)
    - [git log](#git-log)
    - [git restore](#git-restore)
    - [git revert](#git-revert)
    - [git reset](#git-reset)
  - [Gestión de Ramas](#gestión-de-ramas)
    - [git branch](#git-branch)
    - [git switch](#git-switch)
    - [git checkout](#git-checkout)
    - [git merge](#git-merge)
    - [git cherry-pick](#git-cherry-pick)
    - [git rebase](#git-rebase)
  - [Repositorios Remotos](#repositorios-remotos)
    - [git remote](#git-remote)
    - [git fetch](#git-fetch)
    - [git pull](#git-pull)
    - [git push](#git-push)
  - [Mecanismos fundamentales](#mecanismos-fundamentales)
    - [staged](#staged)
    - [Puntero HEAD](#puntero-head)
    - [Paginador](#paginador)
    - [Filtros para logs](#filtros-para-logs)
    - [Editor de hunks](#editor-de-hunks)
    - [Editor de commits](#editor-de-commits)
    - [Trabajar con ramas](#trabajar-con-ramas)
    - [Revertir cambios](#revertir-cambios)
    - [Restaurar un archivo](#restaurar-un-archivo)
    - [Solucionar conflictos](#solucionar-conflictos)
  - [Ejercicios practicos](#ejercicios-practicos)
    - [P. Crear repositorio](#p-crear-repositorio)
    - [P. Stanging area](#p-stanging-area)
    - [P. Guardar cambios](#p-guardar-cambios)
    - [P. Deshacer cambios no guardados](#p-deshacer-cambios-no-guardados)
    - [P. Navegar por commits](#p-navegar-por-commits)
    - [P. Guardar cambios temporalmente](#p-guardar-cambios-temporalmente)
    - [P. Deshacer cambios](#p-deshacer-cambios)
    - [P. Crear y eliminar ramas](#p-crear-y-eliminar-ramas)
    - [P. Moverse entre ramas](#p-moverse-entre-ramas)
    - [P. Ver grafica de commits](#p-ver-grafica-de-commits)
    - [P. Fusionar ramas](#p-fusionar-ramas)
    - [P. Resolver conflictos](#p-resolver-conflictos)
    - [P. Crear repositorio remoto](#p-crear-repositorio-remoto)
    - [P. conectar a repo remoto](#p-conectar-a-repo-remoto)
    - [P. Enviar cambios a remoto](#p-enviar-cambios-a-remoto)
    - [P. Clonar repo remoto](#p-clonar-repo-remoto)
    - [P. Obtener cambios de remoto](#p-obtener-cambios-de-remoto)
  - [Acciones comunes](#acciones-comunes)
    - [Llamar un archivo de otra rama](#llamar-un-archivo-de-otra-rama)
  - [Consejos](#consejos)
    - [git ignore](#git-ignore)
    - [Resolver conflictos](#resolver-conflictos)
    - [Prevenir conflictos](#prevenir-conflictos)

---

## Sobre git

### Cuándo usar git

Deberias usar git si:

- Trabajas con más de una persona en los mismos archivos y quieres evitar sobrescribir los cambios de otros.

- Quieres reescribir ideas o hacer cambios grandes sin el miedo de arruinar tu proyecto.

- Tienes que manejar diferentes versiones de tu proyecto. por ejemplo: tener una versión para tu cliente y otra para tu equipo.

- Te gustaría tener un historial completo de cambios en tu trabajo, como quién, qué y cuándo se modificó un archivo.

- Necesitas restaurar (hacer Ctrl+Z) y regresar a una versión anterior de tu proyecto o carpeta.

### Cuándo no usar git

No deberias usar git si:

- Tu proyecto es un archivo único y sencillo que no planeas modificar con el tiempo.

- Solo trabajas con archivos muy grandes y binarios como videos, audios o modelos 3D.

- Solo necesitas compartir archivos de forma rápida, y no te preocupa gaurdar los cambios.

- El proyecto muy simple y el tiempo para aprender Git supera los beneficios que obtienes.

### ¿Qué es git?

Git es un sistema de control de versiones: diseñado para buscar cambios en archivos y mejorar el trabajo entre programadores. Permite regresar a versiones anteriores de un proyecto (Ctrl+Z) y es una herramienta esencial en el desarrollo de software.

### ¿Qué es un repositorio?

Un repositorio (repo), es una carpeta especial que guarda: los archivos, el código y los cambios realizdos en tu proyecto. Proporciona una copia de seguridad en caso de fallos o alteraciones en los archivos. Aunque primer debes sleccionar que cambios guardar desde el [Área de staging](#área-de-staging)

### ¿Cómo funciona?

Git guarda todos los archivos y los cambios del proyecto en un archivo/carpeta comprimida. Funciona tomando una "fotografia" de todos los archivos cada vez que guardas un cambio, pero en lugar de copiar todo, guarda solo los cambios o modificaciones cada vez, lo que lo hace muy eficiente y no ocupa mucho espacio.

### Partes principales

Git se divide en 3 partes principales:

- [Area de trabajo](#área-de-trabajo) Es la carpeta "nomral" donde guardas todos los archivos de tu proyecto, donde interactuas con ellos (crear, agregar, editar y eliminar).

- [Area de staging](#área-de-staging) Es un area especial de git que permite seleccionar que archivos o cambios deseas guardar, una ves seleccionados se envian al [repositorio](#qué-es-un-repositorio)

- [Repositorio](#qué-es-un-repositorio) Es el area donde se guardan todos los cambios realizados asi como una compia de tus archivos, puedes acceder a su historial para deshacer cualquier cambio que hayas guardado previamente.

#### Área de trabajo

Esta es la carpeta donde tienes todos tus archivos, es una carpeta normal en tu computadora. Aqui puedes interactuar como siempre con tus archivos (crear, agregar, editar y eliminar), esta diseñada para que trabajes como siempre lo haces solo envia la informacion de los cambios hechos a git para que la observes en el [Área de staging](#área-de-staging).

#### Área de staging

Es un area especial de git que permite observar los cambios que hiciste en el [Área de trabajo](#área-de-trabajo) y seleccionar que archivos o cambios vas a envar al [Repositorio](#qué-es-un-repositorio) y asi tener una copia segura del estado de tus archivos en ese momento.

#### Repositorio

El repositorio, contiene la logica y la estructura intera que permitenque git funcione (es la forma que usa git para  guardas tus cambios).

#### Directorio de Git

Es la carpeta comprimida fisica donde git guarda todo lo que necesita para funcionar (es la carpeta .git, ahi se guardan todos tus cambios y las copias de tus archivos).

#### gitignore

Es un archivo que te permite decirle a git que archivos no quieres que tome en cuenta (ignore) y no guarde sus cambios. Para ello solo colocas en nombre del archivo o su extencion si no deseas guardar ningun archivo de ese tipo, Ej. *.txt

#### Commits

Es la forma en que git regista tus cambios, git recuerda como estaban todos los archivos en ese momento (como si le tomara una foto) y lo convierte en un punto de guardado al cual puedes volver.

#### Ramas

Son otra herramienta importante en git, funcionan como universos alternos de tu proyecto que puedes crear y eliminar a voluntad. Son muy utiles si quieres hacer grandes cambios o ir por una ruta diferente pero sin efectar el proyecto pincipal. Puedes crear nuevas, modificarlas, eliminarlas, y combinarlas si lo deseas.

#### Fusionar

Es la accion de unir dos ramas, en una sola. Permite crear una rama para hacer pruebas (test) y si todo salio bien puedes combinar esta rama con la principal sin necesidad de reescribir el trabajo y sin el peligro de perder el proyecto original.

### Servidores y repositorios remotos

Son servicios conectan tu repostorio con la nube y te permite guardar una copia en linea, esto te da mayor seguridad, ademas te permite descargar el proyecto para poder trabajar desde cualquier lugar.

### Buenas preacticas de Git

- Commits atómicos: Cada commit debe contener un solo cambio lógico.

- Mensajes de commit claros: Usa mensajes concisos, descriptivos y en inglés (imperativo).

- Ramas de corta duración: Crea ramas para nuevas funcionalidades o correcciones y bórralas después de fusionar.

- Flujo de trabajo estable: Usa un flujo de trabajo (como GitFlow o GitHub Flow) consistente en el equipo.

- Rebase para limpiar el historial: Usa git rebase -i para limpiar y organizar el historial de commits antes de fusionar.

- Evita el merge commit innecesario: Prefiere rebase a merge para mantener un historial lineal y limpio.

- No commitear código roto: Asegúrate de que tu código compile y pase las pruebas básicas antes de hacer un commit.

- Ignorar archivos innecesarios: Usa el archivo .gitignore para evitar subir archivos temporales, de compilación o de configuración personal.

- Sincronizar frecuentemente: Haz pull de la rama principal frecuentemente para evitar conflictos grandes.

- Revisión de código: Realiza revisiones de código (pull requests) antes de fusionar en la rama principal.

### Buenos commits

El commit debe responder las preguntas ¿Qué? y ¿Por qué? se hizo el cambio. Se conforma de la sig. manera:

- [Encabezado del commit](#encabezado-del-commit)

- Separacion (salto de linea / linea vacia)

- [Cuerpo del commit](#cuerpo-del-commit)

#### Encabezado del Commit

[Tipo-de-commit] [Alcance]: [resumen-del-cambio]

> Obligatorio
> Máximo de 50 caracteres. (Si es muy largo debería fraccionarse en varios commits más pequeños).
> Sin signos de puntucaion.

- **Tipo-de-commit** Indica el propósito del cambio:

  - feat: Una nueva característica para el usuario.
  - fix: Arregla un bug que afecta al usuario.
  - refactor: Refactorización del código, como cambios de nombre de variables o funciones.
  - docs: Cambios en la documentación.
  - style: Cambios de formato (espacios, tabulaciones, puntos y coma) que no afectan al usuario.
  - test: Añade o refactoriza pruebas.
  - perf: Cambios que mejoran el rendimiento.
  - build: Cambios en el sistema de build, tareas de despliegue o instalación.
  - ci: Cambios en la integración continua.
  - chore: Mantenimiento de código regular.

- **Alcance** Indica que parte del proyecto fue afectada por el commit (Backend, database, readme, ui, archivo.txt)

- **Descripción-corta-del-cambio** Una explicación clara y directa de los cambios realizados (Mejorar la lógica del carrito de compras, Añadir pruebas unitarias,  Corregir error de inicio de sesión).

#### Cuerpo del Commit

- Se usa para explicar los cambios realizados (a detalle) y el ¿Por qué?
- Se recomienda usar 72 caracteres (redaccion libre)
- Es recomendable añadir una referencia al problema como: Soluciona: "Error: 123-A".

---

### Herramientas útiles

Existen varias herramientas para mantener la consistencia en los mensajes de commit:

- Husky: Permite ejecutar scripts o comandos antes de realizar diferentes acciones sobre el repositorio. Se puede usar Husky para ejecutar pruebas antes de subir los cambios al repositorio remoto o para validar los commits.

- Commitlint: Se utiliza para asegurar que los commits sean semánticos, legibles y sigan una convención establecida. Esta herramienta ayuda a hacer cumplir las reglas de formato y contenido de los mensajes de commit.

- Commitizen: Una línea de comandos te guiará para elegir el tipo de commit, evitando así tener que depender de realizar esto manualmente en el mensaje del commit. Su propósito es guiar en la escritura de mensajes de commit siguiendo convenciones.

- Conventional-changelog: Permite leer el historial de commits para generar nuevas versiones de un paquete, desplegar nuevas versiones de una aplicación o generar un CHANGELOG con todos los cambios de forma automatizada.

---

## Crear repositorios

### git init

Inicia el repositorio de git en un directorio definido.

- ( ) Crea un repositorio git en el directorio actual.

- (direccion_carpeta) Crea un repositorio de git en la carpeta [direccion_carpeta].

- (--initial-branch=nombre) Crea un repositorio de git en el directorio actual con la rama [nombre] como rama principal.

- (--bare) Crea un repositorio git sin directorio de trabajo en el directorio actual (ideal como repositorio remoto).

### git clone

Crea una copia local de un repositorio de Git que existe en otro lugar.

- (dir1 dir2) Clona/copia tu repositorio local de la direccion [dir1] en otro directorio [dir2].

- (url) Clona/descarga un repositorio desde un repositorio remoto [github] [gitlab].

- (-b nombre_rama nombre_repo)(--branch) Clona/descarga solo una rama [nombre_rama] de un repositorio especificado o url [nombre_repo].

- (--depth num_commits) Clona/descarga solo un numero [num_commits] especifico de commits desde el ultimo realizado hacia atras.

- (--bare) Clona/crea una copia del repositorio tomando en cuenta solo los archivos de Git, sin archivos editables (ideal para crear repositorios crentrales o remotos que sean ligeros)

---

## Estado y Seguimiento de Cambios

### git status

Muestra los archivos modificados y si se encuentran agregados para un commit.

- (-b)(--branch) muestra la rama actual y su estado de seguimiento en un formato más conciso.

- (-v)(--verbose) muestra una versión más detallada de la salida de git status (también muestra un diff para los archivos que están en el staging area y los que no lo están).

### git stash

Guarda temporalmente los cambios sin commit en una pila, para que puedas cambiar de rama sin perder el trabajo.

- ( ) Guarda todos los cambios del "staging area" y directorio de trabajo.

- (list) Muestra una lista de todos los stashes guardados.

- (pop) Aplica el stash más reciente y lo elimina de la pila.

- (apply) Aplica el stash más reciente sin eliminarlo de la pila.

### git add

- (nombre_archivo) Revierte todos los cambios en [nombre_archivo] y lo devuelve al estado del ultimo commit (no debe estar en el [area de staging](#staged)).

Agrega los cambios al arbol y los prepara para el siguiente commit.

- (nombre_archivo) Agrega el archivo de nombre [nombre_archivo] al [area de staging](#staged).

- ( . ) Agrega todos los archivos dentro de la carpeta o directorio actual al [area de staging](#staged).

- (-A) (--all) Toma en cuenta la carpeta/directorio raiz del repositorio y agrega todos los archivos modificados al [area de staging](#staged).

- (-p)(--patch) Permite agregar un archivo por partes al área de [area de staging](#staged) de manera interactiva, usa por defecto el [Editor de hunks](#editor-de-hunks).

- (-u)(--update) Toma en cuenta los archivos previamente rastreados y los agrega al [area de staging](#staged), los archivos recien creados no seran agregados.

### git diff

Muestra las diferencias entre dos estados de Git (commits, ramas, etiquetas o directorio de trabajo).

- ( ) Muestra las diferencias entre los archivos en el directorio de trabajo y el [area de staging](#staged).

- (--staged)(--cached) Muestra las diferencias entre el "staging area" y el último commit.

- (--name-only) Muestra una lista solo con los nombres de los archivos que han sido modificados **usar en combinacion con otros**.

- (--stat) Muestra un resumen estadístico de los cambios pendientes (archivos modificados y número de líneas añadidas o eliminadas) **usar en combinacion con otros**.

- (--color-words) Muestra las diferencias a nivel de palabra en lugar de a nivel de línea **usar en combinacion con otros**.

- (commit_1 commit_2) Muestra las diferencias entre [commit_1] y [commit_2].

- (rama_1 rama_2) Muestra las diferencias entre [rama_1] y [rama_2].

### git clean

Elimina los archivos no rastreados del directorio de trabajo.

> Usar con precaucion, los archivos son eliminados de forma **permanente**.

- (-n)(--dry-run) Muestra una lista con archivos que serían eliminados.

- (-f)(--force) Elimina archivos no rastreados (no incluye directorios o carpetas, tampoco archivos listados en .gitignore).

- (-d)(--delete) Elimina directorios o carpetas completas no rastreadas (no incluye archivos sueltos o listados en .gitignore).

- (-fd) Combina las opciones -f y -d, eliminando cualquier cosa no reatreada (no incluye archivos listados en .gitignore).

- (-x) Elimina todos los archivos, directorios o carpetas incluyendo los listados en .gitignore.

---

## Historial de Versiones

### git commit

Guarda todos los cambios que se encuentren en el arbol de cambios.

- ( ) Despliega un editor de texto en cosola [Vim] para escribir un mensaje de commit.

- (-m)(--message) Agrega un mensaje de commit al commit actual.

- (-a) Agrega automaticamente todos los archivos modificados al arbol de cambios (no agrega archivos nuevos).

- (--amend) Permite modificar el ultimo commit realizado, como agregar un archivo [git add nombre_archivo] + [git commit --amend] o modificar el mensaje del commit [git commit --amend -m "nuevo mensaje"].

### git log

Muestra el historial de commits del repositorio.

> git log tiene un modo de navegacion para navegar por los diferentes commits llamado [Paginador](#paginador)
> Puedes usar [filtros para logs](#filtros-para-logs) hacer más eficiente y rapida la busqueda.
> para salir del [Paginador](#paginador) presiona 'q'

- ( ) Por defecto muestra el hash o id del commit, Nombre y correo del autor, Fecha y hora, y Mensaje del commit en un modo de navegacion de logs.

- (--oneline) Muestra cada commit de forma más concisa (en una sola línea) **se puede combinar con otros**.

- (--graph) Muestra el historial de commits en un gráfico ASCII **se puede combinar con otros**.

- (--decorate) Muestra los nombres de las ramas y etiquetas junto a sus commits **se puede combinar con otros**.

- (--first-parent) Mestra solo los commits de la rama actual **se puede combinar con otros**.

- (--all) Muestra el historial de commits de todas las ramas, no solo la actual **se puede combinar con otros**.

- (-p)(--patch) Muestra los commits junto con los cambios introducidos en cada uno.

- (--stat) Muestra un resumen indicando la cantidad de archivos modificados y las líneas modificadas de cada uno.

- (-numero) Limita la visibilidad de commits a [numero] de commits anteriores visibles.

### git restore

Revierte modificaciones no confirmadas (sin commit) en el directorio de trabajo local.

> Si buscas otras formas de deshacer cambios revisa la seccion [Revertir cambios](#revertir-cambios)

- (nombre_archivo) Revierte todos los cambios en [nombre_archivo] y lo devuelve al estado del ultimo commit (no debe estar en el [area de staging](#staged)).

- ( . ) Revierte los cambios en todos los archivos que no están en el [area de staging](#staged) al estado del ultimo commit.

- (archivo_1 archivo_2) Puedes restaurar varios archivos a la vez simplemente listándolos.

- (--source ) Permite actualziar el contenido de un archivo desde un punto específico de la historia (un commit, una rama o un tag) y traerlo al directorio de trabajo actual. [git restore --source nombre_rama nombre_archivo]

- (--staged nombre_archivo) Desmarca o baja un archivo del [area de staging](#staged) (revierte el comando [git add](#git-add)).

- (--staged . ) Desmarca o baja todos los archivos del [area de staging](#staged) (revierte el comando [git add](#git-add)).

### git revert

Vuelve hasta un punto anterior, deshace los cambios uno por uno y crea un nuevo commit para cada commit revertido.

> Es la forma mas segura de revertir cambios y no afecta otras ramas o usuarios.
> Si buscas otras formas de deshacer cambios revisa la seccion [Revertir cambios](#revertir-cambios)

- (--no-commit) Deshace los cambios realizados pero no realiza el commit, **usar en combinacion con otros**.

- (--no-edit) Evita abrir el editor de texto para cada commit nuevo, **usar en combinacion con otros**.

- (id_commit) Deshace los cambios realizados hasta el commit [id_commit] y crea un nuevo commit con los cambios aplicados.

- (id_commit_1 id_commit_2) Deshace los cambios de los commits especificados [id_commit ...] uno a uno en orden cronologio y crea un commit en cada punto especificado.

- (HEAD) Deshace el ultimo commit y crea un nuevo commit deshaciendo los cambios, hace uso del [Puntero HEAD](#puntero-head).

- (HEAD -m "mensaje_commit") Deshace al ultimo commit y coloca [mensaje_commit] como mensaje para el nuevo commit, hace uso del [Puntero HEAD](#puntero-head).

- (HEAD~numero) Deshace los commits desde el ultimo commit hacia atras hasta [numero] y crea nuevos commits para cada unode ellos (Ej, Head~3), hace uso del [Puntero HEAD](#puntero-head).

- (-n HEAD~numero..HEAD)(--no-commit HEAD~numero..HEAD) Deshace los ultimos [numero] de commits, pero te permita a ti crear el nuevo commit con todos los cambios aplicados, hace uso del [Puntero HEAD](#puntero-head).

### git reset

Permite deshacer cambios y reescribir el historial del repositorio.

> Usar con precaucion, es posible perder avances guardados (commits) de forma **permanente**.
> Si buscas otras formas de deshacer cambios revisa la seccion [Revertir cambios](#revertir-cambios)

- ( ) Desmarca o baja los archivos en el [area de staging](#staged) (revierte el comando [git add](#git-add)).

- (nombre_archivo) Desmarca o baja el archivo [nombre_archivo] del [area de staging](#staged).

- (--soft id_commit) Elimina los commits y sus cambios hasta [id_commit], pero conserva estos cambios en el "staging area".

- (--mixed id_commit) Elimina los commits y sus cambios hasta [id_commit], pero mueve los cambios al directorio de trabajo (por defecto).

- (--hard id_commit) Elimina los commits y todos los cambios hasta [id_commit] **permanentemente**.

- (id_commit -- ruta_archivo) Esto restaura el archivo [ruta_archivo] a su estado en el commit [id_commit] sin afectar el resto del repositorio.

- (HEAD~numero) Elimina desde el último commit hacia atras hasta [numero], si no se especifica (soft, mixed o hard) usara --mixed, [Puntero HEAD](#puntero-head).

---

## Gestión de Ramas

### git branch

Administra las diferentes ramas de un repositorio.

> Si buscas mas opciones revisa la seccion [Trabajar con ramas](#trabajar-con-ramas)

- ( ) Muestra las ramas locales en el repositorio.

- (a)(--all) Muestra las ramas locales y remotas en el repositorio.

- (nombre_rama) Crea [nombre_rama] como una nueva rama local.

- (-d nombre_rama) Elimina la rama local [nombre_rama].

- (-D nombre_rama) Fuerza la eliminación de la rama [nombre_rama] aun si tiene cambios sin fusionar.

- (--merged) Muestra las ramas que ya han sido fusionadas con la rama actual.

- (--no-merged) Muestra las ramas que aún no han sido fusionadas con la rama actual.

- (-m nombre_antiguo nombre_nuevo) Modifica el nombre de la rama [][nombre_antiguo] a [nombre_nuevo].

### git switch

Administra el movimiento entre de ramas.

> Si buscas mas opciones revisa la seccion [Trabajar con ramas](#trabajar-con-ramas)

- (nombre_rama) Cambia a la rama [nombre_rama].

- (--detach id_commit) Permite ir/visitar el commit [id_commit] sin realizar cambios.

- (-c nombre_rama)(--create nombre_rama ) Crea la rama [nombre_rama] y te mueve hacia ella.

- ( - ) Te permite volver a la rama anterior.

- (-c nueva_rama punto_partida)(--create nueva_rama punto_partida) Crea la rama [nueva_rama] a partir de la rama o commit [punto_partida] y te mueve hacia ella.

### git checkout

Administra la navegaccion o el movimiento entra ramas y commits.

> Actualmente en desuso, se recomienda sustituir por **switch** y **restore**.
> Usar solo para versiones antiguas, tareas especificas o funciones avanzadas.

- (nombre_rama) Te permite ir a la rama [nombre_rama] y te coloca en el utimo commit de esa rama.

- (-b nombre_rama) Crea la rama [nombre_rama] y te cambia a ella inmediatamente.

- (-- nombre_archivo) Descarta los cambios en [nombre_archivo] y lo regresa al estado de el último commit.

- (id_commit) Te permite cambiar ir al commit [id_commit].

### git merge

Fusiona el historial de commits de otra rama con la rama actual.

- (nombre_rama) Fusiona la rama [nombre_rama] rama con la rama actual.

- (--abort) Revierte el merge y los cambios si el intento de fusion falló.

- (--no-ff -m "mensaje_commit") Se forzara la creacion de un nuevo commit de fusión explícito con el mensaje [mensaje_commit].

- (--no-commit) Realiza la fusión, pero deja los cambios en el área de staging sin crear un commit.

- (--squash nombre_rama) Toma todos los commits de [nombre_rama] los agrupa y los fusiona con la rama actual, esto no guarda los cambios (commit).

> Merge puede o no hacer commit dependiendo de la situacion, veirficar o hacer commit luego de usarlo

### git cherry-pick

Aplica el contenido de uno o varios commits existentes sobre la rama actual, creando nuevos commits con los mismos cambios.

- (id_commit) Aplica el commit [id_commit] a la rama actual como un nuevo commit.

- (id_commit_1 id_commit_2 ...) Aplica varios commits en orden, uno por uno.

- (--no-commit) Aplica los cambios del commit sin crear el commit, permitiendo revisar o modificar antes de confirmar.

- (--edit) Abre el editor para cambiar el mensaje del commit aplicado.

- (--continue) Continúa el cherry-pick después de resolver conflictos.

- (--abort) Cancela el cherry-pick y vuelve al estado anterior.

> Ir a la rama donde estan los cambios
> identificar el ID del commit que queremos

### git rebase

Reescribe el historial de un proyecto aplicando los commits de una rama sobre otra, creando una secuencia lineal de commits.

- (nombre_rama) Vuelve a un commit en comun, aplica los commits de [nombre_rama] y despues de eso aplica los commits de la rama actual, uniendo ambas en un solo historial de commits.

- (-i id_commit)(-i nombre_rama) Abre el [Editor de commits](#editor-de-commits) con la lista de los commits que se van a reubicar (i = interactive) .

- (-i HEAD~numero) Combinar los ultimos [numero] de commits en uno solo y cambia el mensaje de commit, hace uso del [Puntero HEAD](#puntero-head).

---

## Repositorios Remotos

### git remote

Administra las conexiones a los repositorios remotos.

- ( ) Muestra una lista de los repositorios remotos que están conectados a tu repositorio local.

- (-v)(--verbose) Muestra la misma lista, pero con las URLs asociadas a cada remoto. Esto es útil para verificar que la URL del repositorio sea la correcta.

- (add nombre_id "ruta_dir") Agrega la conexion con un repositorio remoto localizado en ruta_dir y le asigna el id nombre_id (asegurate de colocar la ruta entre comillas para evitar errores).

- (add nombre_id url_repositorio) Agrega un nuevo repositorio con [nombre_id] y le asigna [url_repositorio] como URL.

- (rm nombre_id)(remove nombre_id) Elimina la conexion del repositorio existente [nombre_id].

- (rename id_antiguo id_nuevo) Cambia el nombre del repositorio de [id_antiguo] a [id_nuevo].

- (set-url id_nombre nueva_url) Toma a [id_nombre] y le asigna una [nueva_url].

### git fetch

Descarga los cambios de un repositorio remoto sin fusionarlos en la rama local.

> Usa [git pull](#git-pull) si buscas fusionar/aplicar automáticamente los cambios en tu repositorio.

- (-n)(--dry-run) Muestra una lista de ramas y cambios que se descargaran, pero no modifica el repositorio.

- (nombre-remoto) Descarga todos los cambios de todas las ramas del repositorio remoto especificado. Por defecto, el nombre del remoto suele ser, [git remote](#git-remote)

- (--all) Descarga todos los cambios de todos los repositorios remotos que tengas configurados en [git remote](#git-remote).

- (nombre_remoto nombre_rama) Descarga solo los cambios de repositorio remoto seleccionado [nombre_remoto] y de la rama [nombre_rama], puedes revisar lista de repositorios en [git remote](#git-remote).

- (-p)(--prune) Descarga los cambios y, si alguna rama ha sido eliminada, también la elimina del repositorio local.

- (--tags) Descarga todas las etiquetas del repositorio remoto sin necesidad de descargar todos los commits asociados.

### git pull

Descarga y fusiona los cambios de una rama remota en tu rama local.

> Usa [git fetch](#git-fetch) si deseas ver los cambios antes de fusionarlos/aplicarlos sobre los tuyos.

- (repositorio_remoto nombre_rama) Descarga los cambios del [repositorio_remoto], de [nombre_rama] y los fusiona automáticamente en la rama actual.

- (--rebase) En lugar de realizar una fusión (creando un "merge commit"), git pull --rebase toma tus commits locales, los "aplica de nuevo" sobre los nuevos commits que vienen del repositorio remoto.

- (--no-commit) Descarga los cambios remotos y realiza la fusión, pero no crea automáticamente un commit de fusión. Los cambios se aplican en tu directorio de trabajo, pero quedan en el área de staging para que puedas revisarlos y, si es necesario, modificarlos antes de hacer el commit final.

### git push

Envia los cambios que has guardado (commits) a tu repositorio local a un repositorio remoto.

- (-f)(--force) Permite sobrescribir el historial de una rama remota con el tuyo local, incluso si los historiales difieren

- (repositorio_remoto nombre_rama) Envia los cambios a [nombre_remoto] y a [nombre_rama].

- (-u)(--set-upstream) Establece una rama remota como rama de seguimiento (permite usar git push sin argumentos).

- (-u id_nombre nombre_rama) Establece la rama de nombre_rama como la princial para conectarse con el repositorio de id_nombre, puedes ver la lista de id usando [git remote](#git-remote)  

---

## Mecanismos fundamentales

### staged

Area que administra los archivos que estan listos para guardar cambios (commit).

- (git status) Permite visulizar el estado de los archivos modificados y si estan en el area de staging, ir a la seccion [comando status](#git-status).

- (git add nombre_archivo) Agrega o sube el archivo [nombre_archivo] al area de staging, ir a la seccion [comado add](#git-add).

- (git add . ) Agrega o sube todos los archivos del area de staging, ir a la seccion [comado add](#git-add).

- (git restore --staged nombre_archivo) Desmarca o baja el archivo con [nombre_archivo] del area de staging, ir a la seccion [comando restore](#git-restore)

- (git restore --staged . ) Desmarca o baja todos los archivos del area de staging, ir a la seccion [comando restore](#git-restore)

- (git diff --staged) Muestra los cambios apliacdos sobre los archivos en el area de staging, tomando en cuenta el utimo commit, ir a la seccion [comando diff](#git-diff).

### Puntero HEAD

Es un puntero dinamico que apunta a una rama en concreto, se ajusta al historial del repositorio y puede ser usado como punto de referencia en multiples comandos.

> comandos que hacen uso del puntero HEAD: [git checkout](#git-checkout), [git reset](#git-reset), [git revert](#git-revert) y [git rebase](#git-rebase)

- (git show HEAD) Muestra la información y los cambios introducidos en el commit al que apunta HEAD.

#### checkout HEAD

- (git checkout id_commit) Mueve el HEAD al commit [id_commit]

- (git checkout HEAD~numero) Mueve el HEAD un [numero] de commits hacia atrás.

#### reset HEAD

- (git reset HEAD~numero) Elimina desde el último commit hacia atras hasta [numero], si no se especifica (soft, mixed o hard) usara --mixed.

#### revert HEAD

- (git revert HEAD) Deshace el ultimo commit y crea un nuevo commit deshaciendo los cambios.

- (git revert HEAD -m "mensaje_commit") Deshace al ultimo commit y coloca [mensaje_commit] como mensaje para el nuevo commit.

- (git revert HEAD~numero) Deshace los commits desde el ultimo commit hacia atras hasta [numero] y crea nuevos commits para cada unode ellos (Ej, Head~3).

- (git revert -n HEAD~numero..HEAD)(--no-commit HEAD~numero..HEAD) Deshace los ultimos [numero] de commits, pero te permita a ti crear el nuevo commit con todos los cambios aplicados.

#### rebase HEAD

- (-i HEAD~numero) Combinar los ultimos [numero] de commits en uno solo y cambia el mensaje de commit.

### Paginador

Es una herramienta de terminal (como less). Se usa para visualizar archivos de texto largos o comandos que no caben en una sola pantalla.

> Se abre automaticamente al usar [git log](#git-log).
> Los comandos aqui se basan en presionar teclas.

#### Comandos para navegar

- (q) Salir del paginador y volver a la terminal.

- (j)(↓) Avanzar una línea.

- (↑)(k) Retroceder una línea

- (Espacio)(Page Down) Avanzar una página.

- (b)(Page Up) Retroceder una página.

- (g)(gg) Ir al inicio.

- (G) Ir al final.

#### Buscar y filtrar

1. Presiona la tecla (/).
2. Escribe la palabra clave que quieres buscar.
3. Presiona (Enter).
4. navega entre los resultados.

- (n) Para ir a la siguiente coincidencia.

- (N) Para ir a la coincidencia anterior.

### Filtros para logs

Estos comandos te permiten filtrar los logs por una caracteristica especifica.

> Los comandos deben comenzar con [git log](#git-log)
> Los filtros pueden combinarse para una busqueda mas precisa.

- (-- nombre_archivo) Muestra solo los commits donde se modifico el archivo [nombre_archivo].

- (-- nombre_dir) Muestra el historial de cambios de relacionados con la carpeta, directorio o ruta [nombre_dir].

- (nombre) Fucniona igual que los anteriores pero comete errores si hay ramas que se llamen [nombre].

- (--author="nombre_autor") Muestra solo los commits del la persona [nombre_autor].

- (--committer="nombre_committer") Muestra solo los commits de la persona que hizo los commits [nombre_committer].

- (--since="fecha")(--after="fecha") Muestra los commits realizados despues de la [fecha] especificada.

- (--until="fecha")(--before="fecha") Muestra los realizados antes de la [fecha] especificada.

- (--grep="texto") Muestra los commits que contienen la palabra o frase que contengan [texto] en el mensaje del commit.

- (--grep="texto" -i) ignora mayusculas y minusculas.

- (-G"texto") Muestra los commits donde el [texto] especificado cambie (aplica solo al texto dentro del archivo, no toma en cuenta el mensaje del commit).

- (-S"palabra") Muestra los comits donde se modifico la cantidad de apariciones de [palabra] en el texto (aplica solo al texto dentro del archivo, no toma en cuenta el mensaje del commit).

### Editor de hunks

Muestra las líneas que fueron agregadas, eliminadas o modificadas y te da varias opciones para elegir.

> Herramienta por defecto para agregar partes de un archivo en [git add](#git-add)

- (y) El comando [sí] Prepara este hunk para el commit.

- (n) El comando [no] Ignora este hunk, dejando los cambios en tu directorio de trabajo.

- (e) El comando [editar] Abre el hunk en un editor de texto, permitiéndote seleccionar manualmente qué líneas quieres agregar. Es muy útil cuando el hunk es muy grande y necesitas un control más detallado.

- (s) El comando [dividir] Intenta dividir el hunk en hunks más pequeños. Esto es útil cuando Git agrupa cambios que quieres tratar por separado.

- (d) El comando [listo] Sale del modo interactivo sin preparar más hunks.

- (q) El comando [salir] Sale del modo interactivo.

- (?) El comando [ayuda] Muestra la lista de opciones nuevamente.

### Editor de commits

Un editor de texto que muestra una lista de commits y comandos con instrucciones específicas.

> Herramienta por defecto para trabajar con [git rebase](#git-rebase).

- (p) El comando [pick] mantiene el commit sin cambios (Es la opción por defecto).

- (r) El comando [reword] cambia el mensaje del commit (Git pausará el proceso para editar el mensaje).

- (e) El comando [edit] pausa el rebase después de aplicarlo y permite hacer cambios adicionales en los archivos, ( para continuar usa (git rebase --continue) ).

- (s) El comando [squash] Combina el commit actual con el commit que está justo encima de él en la lista.

- (f) El comando [fixup], similar a (s) o [squash], paro descarta el mensaje de commit del commit actual y usa el mensaje del commit anterior.

- (d) El comando [drop] elimina el commit por completo de forma **permanente**.

### Trabajar con ramas

Existen una gran variedad de comnados que permiten trabajar con ramas.

- Si deseas ver, crear, editar o eliminar ramas visita la seccion [git branch](#git-branch)

- Si deseas navegar entre distintas ramas visita la seccion [git switch](#git-switch)

- Si deseas navegar entre ramas y comits visita la seccion [git checkout](#git-checkout)

- Si deseas fusionar distintas ramas visita la seccion [git merge](#git-merge)

- Si deseas fusionar y reordenar ramas en una sola visita las seccion [git rebase](#git-rebase)

### Revertir cambios

- (git restore) Revierte modificaciones no confirmadas (sin commit) en el directorio de trabajo local, ir a la seccion [git restore](#git-restore).

- (git revert) Vuelve hasta un punto anterior, deshace los cambios uno por uno y crea un nuevo commit para cada commit revertido, ir a la seccion [git revert](#git-revert).

- (git reset) Permite deshacer cambios y reescribir el historial del repositorio, ir a la seccion [git reset](#git-reset).

### Restaurar un archivo

A continuacion se muestran la forma moderna para lograr restaurar un solo archivo a un commit anterior sin modificar los otros archivos.

1. Usa [git log](#git-log) para encontrar el id del commit(hash) que contiene los cambios que quieres deshacer.

2. Usa [git revert](#git-revert) con la opcion (--no-commit). Esto aplica revert pero no crea el commit.

3. Deshaz los cambios de los demás archivos usando [git restore](#git-restore).

4. Crea un nuevo commit usando [git commit](#git-commit) guardando solo los cambios de tu archivo.

### Solucionar conflictos

Los conflictos en Git ocurren cuando intentas fusionar (merge) o rebasar (rebase) ramas que tienen cambios opuestos o incompatibles en la misma parte de un archivo. Git no puede decidir qué cambio mantener y detiene el proceso para que tú lo resuelvas manualmente.

Pasos para solucionar un conflicto:

1. Identifica los archivos en conflicto.

2. Usa git status para ver qué archivos tienen conflictos sin resolver. Git los marcará como "unmerged paths".

3. Abre el archivo y resuelve el conflicto (Git inserta marcadores especiales en el código para mostrarte los cambios).

~~~Git
<<<<<<< HEAD: Indica el comienzo de los cambios en la rama actual (la que estás fusionando).

=======: Separa los cambios de la rama actual de los de la otra rama.

>>>>>>>: Indica el final de los cambios de la otra rama (la que intentas fusionar).
~~~

1. Borra estos marcadores y edita el archivo (manualmente) dejando contenido como deseas. Puedes elegir los cambios de una rama, de la otra, o una combinación de ambos.

2. Marca el archivo como resuelto con [git add](#git-add).

3. Termina el proceso creando un nuevo commit con [git commit](#git-commit).

## Ejercicios practicos

> Advertencia: Estas practicas estan diseñadas para aprender (y equivocarse libremente), por lo tanto deben realizarse en un ambiente nuevo y seguro, nunca en un proyecto existente pues se corre el riezgo de afectar archivos importantes.

### P. Crear repositorio

1. Crea una carpeta
2. Inicia un repositorio [git init](#git-init).
3. Crea un archivo de texto (.txt) o de marcado (.md).
4. Has tu primer [git add](#git-add).
5. Realiza tu primer commit [git commit](#git-commit).

### P. Stanging area

1. Crea dos archivos de texto.
2. Modifica su contenido.
3. Revisa si git registro los cabios [git status](#git-status).
4. Sube los archivos al [área de staging](#staged) usando [git add](#git-add).
5. Revisa si git subio los archivos usando [git status](#git-status).
6. Baja uno de los archivos del [área de staging](#staged).
7. Revisa si git desmarco el archivo uando [git status](#git-status).

### P. Guardar cambios

1. Crea o modifca un archivo de texto.
2. Agrega el archivo al [área de staging](#staged) usando [git add](#git-add).
3. Revisa que el archibo fue subido usando [git status](#git-status).
4. Realiza un [commit](#git-commit).
5. Repite el proceso 3 o 4 veces.

### P. Deshacer cambios no guardados

1. Revisa que no tengas cambios sin guradar [git status](#git-status).
2. Si tinenes cambios sin guardar, guradalos [commit](#git-commit).
3. Modifica un archivo de texto.
4. Revisa que git registro tus cambios [git status](#git-status).
5. Deshaz los cambios no guardados usando [git restore](#git-restore).

### P. Navegar por commits

1. Revisa que no tengas cambios sin guradar [git status](#git-status), si tienes ve a [Guardar cambios](#p-guardar-cambios).
2. Revisa los puntos de guardado usando [git log](#git-log).
3. Identifica un punto al que desees ir y recuerda o copia su ID.
4. Mueve al punto de interes usando [git switch](#git-switch).
5. revisa el proyecto o un archivo para verificar que estas en un punto anterior.
6. Regresa al commit mas actual usado [git switch](#git-switch).

### P. Guardar cambios temporalmente

> Util para moverte entre ramas o commits sin perder los cambios no guardados.

1. Crea o modifca un archivo de texto.
2. Revisa si git registro los cabios [git status](#git-status).
3. Guarda temporalemnte los cambios usando [git stash](#git-stash).
4. Cambia de rama o de commit usando [git switch](#git-switch).
5. Regresa a el utimp commit o la rama anterior usando [git switch](#git-switch).
6. Abre un archivo para revisar que no estan los cambios realizados.
7. Recupera tus cambios usando [git stash](#git-stash).
8. Abre un archivo para revisar que recuperaste los cambios.

### P. Deshacer cambios

1. Crea o modifica un archivo.
2. Ahora [Guarda los cambios](#p-guardar-cambios).
3. Identifica un punto al que desees retroceder y recuerda o copia su ID.
4. Revierte los cambios usando [git revert](#git-revert).

### P. Crear y eliminar ramas

1. Antes de comenzar [Guarda los cambios](#p-guardar-cambios).
2. Revisa la lista de ramas usando [git branch](#git-branch).
3. Crea dos nuevas ramas usando [git branch](#git-branch).
4. Revisa la lista de ramas usando [git branch](#git-branch).
5. Elimina solo una de las dos ramas nuevas usando [git branch](#git-branch).
6. Revisa la lista de ramas usando [git branch](#git-branch).

### P. Moverse entre ramas

> Debiste haber realizado la [Practica Crear y eliminar ramas](#p-crear-y-eliminar-ramas)

1. Revisa la lista de ramas usando [git branch](#git-branch).
2. Crea un archivo de texto en la rama actual [rama1.txt].
3. [Guarda los cambios](#p-guardar-cambios).
4. Cambia a la otra rama usando [git switch](#git-switch).
5. Compruba que el archivo [rama1.txt] ha desaparecido.
6. Crea un archivo de texto en la rama actual [rama2.txt].
7. [Guarda los cambios](#p-guardar-cambios).
8. Regresa a la rama princpial usando [git switch](#git-switch).
9. Compruba que el archivo [rama2.txt] ha desaparecido pero [rama1.txt] sigue ahí.

### P. Ver grafica de commits

> Debiste haber realizado la [Practica moverse entre ramas](#p-moverse-entre-ramas)

1. Abre el gráfico ASCII usando [git log](#git-log)
2. Cierra el grafico presionando (q)

### P. Fusionar ramas

> Debiste haber realizado la [Practica Crear y eliminar ramas](#p-crear-y-eliminar-ramas)

1. Revisa las ramas usando la [Grafica ascii](#p-ver-grafica-de-commits).
2. Cierra la grafica.
3. Muevete a la rama principal.
4. Fusiona la rama nueva con la rama principal usando [git merge](#git-branch).
5. Revsia que ambos archivos esten ahora en la rama principal.
6. Revisa el cambio usando la [Grafica ascii](#p-ver-grafica-de-commits).
7. Cierra la grafica.
8. Elimina la rama y conserva solo la rama principal usando [git branch](#git-branch)

### P. Resolver conflictos

1. Crea un nuevo archivo de texto en la rama principal
2. [Guarda los cambios](#p-guardar-cambios).
3. [Crea una nueva rama](#p-crear-y-eliminar-ramas)
4. Modifica las primeras 4 lineas del achivo agregando el texto en la rama principal.
5. [Guarda los cambios](#p-guardar-cambios).
6. [Muevete a otra rama](#p-moverse-entre-ramas)
7. Modifica las primeras 2 lineas del achivo agregando creando un texto diferente en esta rama.
8. [Guarda los cambios](#p-guardar-cambios).
9. Vuelve a la rama principal usando [git swtich](#git-switch)
10. [Fusona ambas ramas](#p-fusionar-ramas)
11. Revisa el archivo.

> El archivo debera verse asi:
>
> `<<<<<<<` [nombre de la rama actual]
> [texto de la rama actual]
> `=======`
> [texto de la rama a fusionar]
> `>>>>>>` [Nobre de la rama a fusionar]

1. Ajusta, edita, cambia, combina o elimina los cambios a mano.
2. Elimina los marcadores [<<<<<<<] [=======] [>>>>>>].
3. Asegurate que el archivo quedo como querias.
4. [Guarda los cambios](#p-guardar-cambios).
5. Revisa que el archivo se guardo correctamente.

### P. Crear repositorio remoto

1. Crea un proyecto/carpeta nueva.
2. Crea dos carpetas dentro [proyecto] y [remoto].
3. Entra a [remoto] y crea un repositorio sin directorio de trabajo usando [git init](#git-init).

### P. conectar a repo remoto

> Debiste haber realizado la [Practica Crear remoto](#p-crear-repositorio-remoto).

1. Entra a la carpeta [proyecto] y [crea un repositorio](#p-crear-repositorio).
2. Revisa las conecciones del repositorio [git remote](#git-remote).
3. Crea una conoexion nueva con el id que mas te guste usando [git remote](#git-remote).
4. Indica al repositorio que rama debe de seguir usando [git push -u origin main]
5. Revisa que la conexion este correcta, debes tener una conexionpara [push] y otra para [pull] con el mismo nombre, usa [git remote](#git-remote).

### P. Enviar cambios a remoto

> Debiste haber realizado la [Practica conectar a remoto](#p-conectar-a-repo-remoto).

1. Debes estar en la carpeta [proyecto] que creaste en [Practica crear remoto](#p-crear-repositorio-remoto)
2. Revisa que la conexion conexion con el repositorio remoto, debes tener una conexionpara [push] y otra para [pull] con el mismo nombre, usa [git remote](#git-remote).
3. Crea un archivo de texto y coloca texto dentro de el.
4. Guarde los cambios igual que en [Practica Guardar cambios](#p-guardar-cambios)
5. Sube/Envia los cambios al repositorio remoto usando [git push](#git-push)
6. Si ocurre algun error revisa las practias anteriores o elimina la conexion y vuelve a crearla usando [git remote](#git-remote)

### P. Clonar repo remoto

> Debiste haber realizado la [Practica enviar cambios a remoto](#p-enviar-cambios-a-remoto).

1. Dirigite a otra parte del disco diferente al de la carpeta creada en [Practica crear remoto](#p-crear-repositorio-remoto)
2. Crea una nueva carpeta con un nombre diferente como [copia].
3. Abre la tarminal y clona el repositorio remoto usando la direecion original y [git clone](#git-clone)
4. Comprueba que los archivos fueron clonados.

### P. Obtener cambios de remoto

> Debiste haber realizado la [Practica enviar cambios a remoto](#p-enviar-cambios-a-remoto).

1. Desde esta carpeta [copia] abre el archivo de texto y modificalo.
2. Guarda los cambios usando [git commit](#git-commit)
3. Envia los cambios al repositorio remoto usando [git push](#git-push)
4. Vuelve a la carpeta princial [proyecto]
5. Revisa el archivo y comprueba que no se ha modificado el archivo.
6. Descarga los cambios sin aplicarlos a tus archivos usando [git fetch](#git-fetch)
7. Revisa si tu rama esta actualizada [up to date] o no lo esta [is behind], usando [git init](#git-init)
8. Actualiza los cambios usando el comando [git pull](git-push)
9. Revisa que se hayan aplicado los cambios.
10. En caso de coflictos resuelvelo como en [Practica Resolver conflictos](#p-resolver-conflictos)

## Acciones comunes

### Llamar un archivo de otra rama

En ocaciones sera necesario modificar o actulaizar solo un archivo de otra rama para ello:

1. Ve a la rama donde necesitas el archivo actualizado usando [git switch](#git-switch)
2. Llama el ultimo commit del archivo usando [git restore](#git-restore)
3. Has un commit para guardar los cambios

## Consejos

### git ignore

se usa para listar lo archivos que queremos que git ingonre

se ua principalemtne para que git no suba archivos.

ej:

archivos con datos sensibles, claves de acceso o credencioes .env

arcvhivos compilados.

librerias y modulos.

pueden ser carpeteas, archivos especificos y tipos de archivos.

para ignoara capetas

carpeta_nombre/
archivo.log

ignorar todos los .zip

*.zip

### Resolver conflictos

- eliminar manualmente la lienas de codigo que no necesitamos

- git checkout --ours  nombre_archovo(conservar los cambios de la rama padre)

-- git checkout theirs nombre_archovo(conservar los cambios de la rama hijo)

- cmbiar manualmente desde elo deditor de texto usando las opciones integradas para conservar el cambio necesario

### Prevenir conflictos

- realiza pequeños comits, y haslos de forma frecuente.

- escribe mensajes de commits descriptivos y detalladso.

- catualiza constantemente el repositorio local.

- trabaja en ramas propias
