# GitHub Actions

Referencia oficial: [Documentación de GitHub Actions](https://docs.github.com/es/actions)

---

## Índice

- [GitHub Actions](#github-actions)
  - [Índice](#índice)
  - [¿Qué es GitHub Actions?](#qué-es-github-actions)
  - [¿Cómo funciona?](#cómo-funciona)
  - [Casos de uso](#casos-de-uso)
  - [Conceptos Clave](#conceptos-clave)
  - [Estructura basica](#estructura-basica)
  - [Jobs](#jobs)
  - [condicionales](#condicionales)
  - [Contextos](#contextos)
  - [variables de entorno](#variables-de-entorno)
  - [El comando `uses`](#el-comando-uses)
  - [Sintaxis YAML](#sintaxis-yaml)
  - [Secretos y Variables](#secretos-y-variables)
  - [Actions](#actions)
  - [marketplace](#marketplace)
  - [github output](#github-output)
  - [Step](#step)

---

## ¿Qué es GitHub Actions?

**GitHub Actions** es una plataforma de automatización integrada directamente en GitHub, diseñada para ayudar a automatizar tareas dentro del ciclo de vida de desarrollo de software.

Sus principales aplicaciones son:

- **CI (Continuous Integration - Integración Continua):** Automatizar la compilación y prueba de código cada vez que un desarrollador sube cambios.

- **CD (Continuous Deployment - Despliegue Continuo):** Automatizar el despliegue de la aplicación a producción después de que el código ha pasado las pruebas.

**Ventajas:**

- Es gratuito para repositorios públicos y ofrece minutos gratuitos para repositorios privados.

- No requiere configuración de servidores externos.

- Posee un ecosistema extenso de acciones reutilizables creadas por la comunidad.

---

## ¿Cómo funciona?

GitHub Actions permite definir flujos de trabajo (workflows) que se ejecutan automáticamente en respuesta a **eventos** específicos en tu repositorio, como:

- `push`: Alguien sube cambios.

- `pull_request`: Alguien crea o actualiza una Pull Request.

- `merge`: Una rama se fusiona.

- *Y muchos otros, como la creación de un issue o una programación de tiempo (cron).*

---

## Casos de uso

Puedes automatizar casi cualquier tarea de tu flujo de trabajo. Algunos ejemplos comunes son:

- **Build & Test:** Compilar el código y ejecutar pruebas unitarias o de integración.
- **Notificaciones:** Enviar alertas a servicios como Slack, correo electrónico, Notion o Asana.
- **Escaneo de seguridad:** Analizar el código en busca de vulnerabilidades.
- **Despliegue:** Publicar un sitio web, una aplicación o un paquete.

---

## Conceptos Clave

- **Workflow (Flujo de trabajo):**
    Es un proceso automatizado definido en un archivo YAML ubicado en el directorio `.github/workflows/` de tu repositorio. El nombre del archivo puede ser cualquiera, pero la ubicación es fundamental para que GitHub lo detecte. Un workflow se compone de uno o más *jobs*.

- **Trigger (Disparador):**
    Es el evento que inicia la ejecución de un workflow. Se define en el archivo YAML con la clave `on`.

- **Job (Trabajo):**
    Es una unidad de trabajo independiente dentro de un workflow. Por defecto, los jobs se ejecutan en paralelo. Cada job se ejecuta en una máquina virtual o contenedor llamado *runner*. Puedes configurar jobs para que se ejecuten en un orden específico si uno depende de otro.

- **Step (Paso):**
    Es una tarea individual dentro de un job. Los steps se ejecutan secuencialmente dentro del mismo runner. Un step puede ser un comando de shell o una *action*. Se definen usando las claves `name`, `uses` o `run`.

*Ejemplo de pasos en un job de despliegue:*

1. Conectar al servidor remoto.

2. Descargar la última versión del código (`git pull`).

3. Instalar dependencias (`npm install`, `pip install`).

4. Ejecutar migraciones de base de datos.

5. Generar archivos estáticos.

6. Reiniciar el servidor web (ej. Nginx).

7. Enviar una notificación de éxito.

- **Action (Acción):**

Es un bloque de código reutilizable que realiza una tarea específica. Las acciones simplifican los workflows al encapsular funcionalidades complejas en una sola línea. Por ejemplo, `actions/checkout@v4` es una acción oficial para descargar el código del repositorio.

- **Runner (Ejecutor):**

Es la máquina virtual (Ubuntu, Windows, macOS) que ejecuta los jobs. GitHub proporciona runners mantenidos por ellos, que ya vienen con software preinstalado (como Python, Node.js, etc.), o puedes configurar tus propios runners auto-hospedados. Se define con la clave `runs-on`.

---

## Estructura basica

Es necesario definir una estructura basica de archivos:

```arbol
nombre-del-proyecto/
├── .github/
    └── workflow/
        └── archivo_nombre.yml
 
```

## Jobs

la etiqueta del job es su id, por lo que es unico

- [ needs: ] permite definir si el job depende de que otro se ejecute antes que el, ej. [needs: name_job], tambien puede haceptar una lsita de jobs, apra ejecutarse cuando todos estos hayan temrminado

> en caso de un error, en un jopb, github actions lo detecta y deja de ejecutar el arbol de jobs dependientes

- [ name: ] permite colocar una etiqueta para personalizar el como se vera en el panel de gihtub actions en github

- [ outputs ] Nos permite enviar valores y varialbes para que sean compartidos entre jobs

## condicionales

se pueden suar en jobs y en steps debajo del nombre.

el condicional [ if ] permite controlar la ejeucion de un job o no

> solo se puede agragar un if por job pero puedes usar booleanos como || o &&

## Contextos

#{{  }}

ejemplo:

if: #{{ github.ref == 'refs/heads/main' }}

los contexxtos tambien se pueden suar en los steps par debuggin y regresar valor

## variables de entorno

env 

se puede usar a nivel job o a nivel step

## El comando `uses`

La clave `uses` permite incorporar en un *step* una **acción** creada por la comunidad o por GitHub. Esto fomenta la reutilización y simplifica enormemente la creación de workflows, ya que no tienes que escribir todo desde cero.

---

## Sintaxis YAML

```yaml
# Nombre del workflow, que aparecerá en la pestaña "Actions" de GitHub
name: Mi Primer Workflow

# Trigger: se ejecuta en cada 'push' a la rama principal
on:
  push:
    branches: [ main ]

jobs:
  # Nombre del job
  build-and-test:
    # Runner: se ejecutará en una máquina virtual con la última versión de Ubuntu
    runs-on: ubuntu-latest

    # Pasos del job
    steps:
    # 1. Descarga el código del repositorio al runner
    - name: Checkout repository
      uses: actions/checkout@v4

    # 2. Instala las dependencias del proyecto (ejemplo con Node.js)
    - name: Install dependencies
      run: npm install

    # 3. Ejecuta los tests
    - name: Run tests
      run: npm test

    # 4. Imprime un mensaje en la consola
    - name: Show success message
      run: echo "¡Todo listo!"
```

---

## Secretos y Variables

Para manejar datos sensibles como contraseñas, tokens de API o claves SSH sin exponerlos en tu código, GitHub Actions ofrece **Secretos**.

- Se configuran en el repositorio, en la sección:

    `Settings > Secrets and variables > Actions`.

- Una vez guardados, puedes usarlos en tu workflow como si fueran variables de entorno, pero su valor nunca se muestra en los logs.

## Actions

son paquetes reutilizables

se llana usando 

uses: nombre_repositorio/action_name@version_name

ejemplo:

uses: alejandoftb/checkout@v4

la directiva  [ with: ] te permite pasarle aprametros a la accion que es llamada, esto es util cuando las acciones lamadas te piden parametros

## marketplace

git hub marketplace

## github output

es una varibla de entorno con un valor y un archivo en texto plano donde se puede insertar o conatenar valores para poder leerlos dentro de otro job o step

pudes compartir variables entre jobs y steps

ejemplo:

´´´yml
steps:
  - name: working_dir
    id: steep_1
    run: echo "variable= hola mundo" >> $GITHUB_OUTPUT

  -name: obtener_mensaje
    run: echo "${{ steps.step_1.outputs.variable }}"
´´´

## Step

- [ id: ] permite asignarle un ID para poder hacer referenica a el.