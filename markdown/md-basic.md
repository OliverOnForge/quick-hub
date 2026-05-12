
# Markdown

Una guía práctica para aprender y utilizar el formato Markdown.

---

## Índice

- [Markdown](#markdown)
  - [Índice](#índice)
  - [Sobre Markdown](#sobre-markdown)
    - [Que es Markdown](#que-es-markdown)
    - [Cuándo usar Markdown](#cuándo-usar-markdown)
    - [Cuándo no usar Markdown](#cuándo-no-usar-markdown)
  - [Sintaxis Básica](#sintaxis-básica)
    - [Encabezados](#encabezados)
    - [Párrafos y Saltos de Línea](#párrafos-y-saltos-de-línea)
    - [Énfasis](#énfasis)
    - [Citas](#citas)
    - [Listas](#listas)
    - [Líneas Horizontales](#líneas-horizontales)
  - [Elementos Avanzados](#elementos-avanzados)
    - [Enlaces](#enlaces)
    - [Imágenes](#imágenes)
    - [Código](#código)
    - [Tablas](#tablas)
    - [Listas de Tareas](#listas-de-tareas)
  - [Buenas Prácticas](#buenas-prácticas)

---

## Sobre Markdown

### Que es Markdown

Markdown es un lenguaje de marcado ligero creado por John Gruber. Su objetivo es permitir que las personas "escriban usando un formato de texto plano fácil de escribir y fácil de leer, y que luego pueda convertirse a HTML (u otros formatos) estructuralmente válido". No es un lenguaje de programación, sino una forma de dar formato al texto.

### Cuándo usar Markdown

- **Documentación:** Para escribir archivos `README.md`, wikis y documentación de proyectos.

- **Contenido web:** Para escribir posts en blogs, comentarios o contenido en sitios estáticos (como Jekyll, Hugo).

- **Notas:** Para tomar notas rápidas en muchas aplicaciones que soportan este formato.

- **Comunicación:** En plataformas como GitHub, GitLab, Slack y Discord para dar formato a los mensajes.

### Cuándo no usar Markdown

- **Diseños complejos:** Si necesitas un control preciso sobre el diseño visual, como en una revista o un folleto, herramientas como InDesign o un editor WYSIWYG son más adecuadas.
- **Documentos interactivos:** Para contenido que requiere interactividad compleja, es mejor usar HTML, CSS y JavaScript directamente.

---

## Sintaxis Básica

### Encabezados

Se crean usando el símbolo de almohadilla (#). El número de almohadillas corresponde al nivel del encabezado (del 1 al 6).

### Párrafos y Saltos de Línea

Los párrafos son simplemente una o más líneas de texto consecutivas, separadas por una o más líneas en blanco. Si quieres forzar un salto de línea sin crear un párrafo nuevo, puedes terminar una línea con dos o más espacios en blanco.

### Énfasis

- **Negrita:** `**texto en negrita**` o `__texto en negrita__` → **texto en negrita**

- *Cursiva:* `*texto en cursiva*` o `_texto en cursiva_` → *texto en cursiva*

- ***Negrita y Cursiva:*** `***texto importante***` → ***texto importante***

- ~~Tachado:~~ `~~texto tachado~~` → ~~texto tachado~~

### Citas

Se usan para resaltar texto citado de otra fuente. Se crean con el símbolo (>).

> La imaginación es más importante que el conocimiento.
>
> - Albert Einstein

### Listas

- **Listas Desordenadas (Viñetas):**

Usa guiones (-), asteriscos (*) o signos de suma (+) seguidos de un espacio.

> Se recomienda solo usar uno, por convencion es mejor usar (-)

- **Listas Ordenadas (Numeradas):**

Usa números seguidos de un punto (.).

1. Primer paso
2. Segundo paso
3. Tercer paso

### Líneas Horizontales

Para crear una línea divisoria, usa tres o más guiones (-), asteriscos (*) o guiones bajos (_) en una línea.

---

## Elementos Avanzados

### Enlaces

La sintaxis es `[texto del enlace](URL "título opcional")`.

Visita [Google](https://www.google.com "El buscador más popular").

### Imágenes

La sintaxis es similar a los enlaces, pero con un signo de exclamación al principio: `![texto alternativo](URL)`.

![Logo de Markdown](https://markdown-here.com/img/icon256.png)

### Código

- **Código en línea:** Envuelve el código con acentos graves (`).

Ejemplo: La función se llama `miFuncion()`.

- **Bloques de código:** Usa tres acentos graves (`) o tres tildes (~) para encerrar el bloque. Puedes especificar el lenguaje para activar el resaltado de sintaxis.

~~~Markdown
function greet(name) {
    console.log("Hello, " + name);
}
~~~

### Tablas

Crea tablas usando barras verticales (|) para separar columnas y guiones (-) para definir la cabecera.

~~~markdown
| Cabecera 1 | Cabecera 2 | Cabecera 3 |
|------------|:----------:|-----------:|
| Contenido  | Centrado   | Derecha    |
| Celda      | Celda      | Celda      |
~~~

- Los dos puntos (:) en la línea de guiones controlan la alineación de la columna.

### Listas de Tareas

Son listas con casillas de verificación.

~~~markdown
- [x] Tarea completada
- [ ] Tarea pendiente
- [ ] Otra tarea por hacer
~~~

---

## Buenas Prácticas

- **Consistencia:** Usa el mismo marcador para listas (ej. siempre `-`) y énfasis (ej. siempre `**` para negrita).

- **Saltos de línea:** Añade una línea en blanco alrededor de elementos como listas, bloques de código y tablas para asegurar una correcta renderización y mejorar la legibilidad del texto fuente.

- **Texto alternativo:** Siempre proporciona un texto alternativo descriptivo en las imágenes para accesibilidad.
