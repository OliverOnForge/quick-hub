
# HTML

fast guide

---

## Indice

- [HTML](#html)
  - [Indice](#indice)
  - [¿Que es html?](#que-es-html)
  - [¿En que consiste html?](#en-que-consiste-html)
  - [Conejos de carga rapida](#conejos-de-carga-rapida)
    - [Reducir el peso de las páginas web](#reducir-el-peso-de-las-páginas-web)
    - [Minimizar el número de archivos](#minimizar-el-número-de-archivos)
    - [Reducir la busqueda de dominios](#reducir-la-busqueda-de-dominios)
    - [Reutilización de contenido de cache](#reutilización-de-contenido-de-cache)
  - [Usar Javascript](#usar-javascript)
  - [accesibilidad](#accesibilidad)
  - [Metadatos](#metadatos)
  - [Media](#media)
  - [Sectioning content](#sectioning-content)
  - [Heading content](#heading-content)
  - [Embedded content](#embedded-content)

---

## ¿Que es html?

HTML (Lenguaje de Marcado de Hipertexto) es el componente básico de la web.

- Lenguaje: Un sistema de comunicación estructurado (con reglas definidas) que permite a la computadora organizar o ller informacion.
- de Marcado: Define el formato, la estructura o como mostrar la información de un documento.
- de Hipertexto: posee enlaces que conectan partes entre si o con otros documentoss.

> Se utiliza para definir que informacion tiene una pagina web

## ¿En que consiste html?

Un documento html es un conjuto de informacion y etiquetas, que consisten en el nombre del elemento entre los caracteres '<>'.

Este elemento o etiqueta puede escribirse en mayúsculas, minúsculas o una combinación de ambas.

Por ejemplo, la etiqueta **title** podria escribirse como:

~~~html
<Title>
<TITLE>
~~~

Sin embargo, la convención y la práctica recomendada es escribir las etiquetas siempre en minúsculas.

## Conejos de carga rapida

Una página web optimizada no solo provee una mayor respuesta a su sitio por parte de los visitantes, sino que también reduce la carga en su servidores web y en su conexión de internet. Esto puede ser crucial para sitios con alto volumen o sitios que tienen un pico de trafico debido a circunstancias inucuales como noticias de ultima hora.

### Reducir el peso de las páginas web

El peso de las páginas web es por mucho el factor más importante en el rendimiento de carga de una página.

Reducir el peso de la página mediante la eliminación de espacios en blanco innecesarios y comentarios, comunmente se coonoce como minimalización, y al mover "inline-script" y "CSS" a un archivo externo, puede mejorar el rendimiento de la descarga con minimas necesidades de otros cambios en la estructura de la página.

Herramientas: 

- HTML Tidy: pueden quitar automáticamente espacios en blanco y las líneas en blanco adicionales de código fuente HTML valido

 Otras herramientas pueden "comprimir" JavaScript al reformatear el codigo fuente o por ofuscación la fuente y la sustitución de los identificadores largos con versiones mas cortas.

### Minimizar el número de archivos

Reducir el número de archivos referentes en una pagina web baja el número de conexiones HTTP requeridas para bajar la página.

Dependiendo de la configuración de cache de un navegador, puede enviar una petición "If-Modified-Since" al servidor web para cada "CSS", JavaScript o archivo de imágen, preguntando si el archivo ha sido modificado desde la ultima vez que fué descargado.

Al reducir el número de archivos que son refereciados dentro de una página web, se reduce el tiempo necesario para que estas solicitudes se envíen, y para que sus respuestas que se reciban.

Si se usan muchas imágenes de fondo en sus "CSS", puedes reducir la cantidad de busquedas HTTP necesarias al combinar las imagenes en una, conocido como "image sprite". Luego solamente se aplica la misma imagen cada vez que lo necesite para un fondo, ajustando las coordenadas el eje (X / Y) adecuadamente. Estas técnica trabaja mejor con elementos que tendrán dimensiones limitadas, no funcionará para todos los usos de imagenes de fondo, sin embargo, la menor cantidad de pedidos HTTP y el uso de una única imágen en caché puede reducir el timepo de carga de una página.

Demasiado tiempo gastado en consultar la ultima modificación de los archivos referenciados puede demorar la pantalla inicial de una página web, ya que el explorador debe comprobar la fecha de modificación de cada archivo CSS o JavaScript, antes de pintar la página.

### Reducir la busqueda de dominios

Debido a que cada dominio separado cuesta tiempo en una busqeuda DNS, el tiempo de carga de la página crecerá junto con el número de dominios que aparecen en enlace CSS (s), JavaScript y recursos de imagen.

Esto no puede ser siempre práctico; sin embargo siempre se debe tener cuidado de usar sólo el número mínimo necesario de los diferentes dominios en sus páginas.

### Reutilización de contenido de cache

Asegúrese de que cualquier contenido que se pueden almacenar en caché, se almacena en caché, y con fechas de caducidad correspondientes.

En particular, prestar atención a la cabecera "Last-Modified". Permite el eficiente almacenamiento en cache de la página; por medio de esta cabecera, la información se transmite al agente de usuario sobre el archivo que quiere cargar, por ejemplo, como cuando fue modificada por última vez. La mayoría de los servidores web añadirá automáticamente la cabecera Last-Modified para páginas estáticas (por ejemplo .html, .css), basado en la fecha de última modificación almacenada en el sistema de archivos. Con páginas dinámicas (por ejemplo, .php, .aspx), esto, por supuesto, no se puede hacer, y la cabecera no se envía.

Así, en particular para las páginas que se generan de forma dinámica, un poco de investigación sobre este tema es beneficioso. Puede ser un poco complicada, pero se ahorrará mucho en las solicitudes de página en las páginas que normalmente no serían cacheable.

---

Uso de comentarios HTML <!-- … -->

Un comentario HTML se utiliza para añadir notas explicativas al código o para evitar que el navegador interprete partes específicas del documento.

Los comentarios comienzan con la cadena <!-- y terminan con la cadena -->, generalmente con texto entre medias. Este texto no puede comenzar con > ni ->, no puede contener --> ni --!>, ni terminar con <!-, aunque <! está permitido.

El navegador ignora los comentarios al renderizar el código. En otras palabras, no son visibles en la página, solo en el código. Los comentarios HTML son una forma de escribir notas útiles sobre el código o la lógica.

Lo anterior también se aplica a los comentarios XML. Además, en XML, como en el marcado SVG o MathML, un comentario no puede contener la secuencia de caracteres --.

Los comentarios pueden usarse en una sola línea o abarcar varias líneas. Se pueden usar en los siguientes lugares:

sintaxis:

~~~html
<!-- Comment -->
~~~

~~~html
<!--
Este es
un comentario
de varas lienas
-->
~~~

Los comentarios HTML solo se permiten como contenido. No se pueden usar dentro de una etiqueta, como antes de un atributo HTML.

Al igual que en la mayoría de los lenguajes de programación que usan la sintaxis de comentarios <!-- -->, los comentarios no se pueden anidar. En otras palabras, la primera instancia de --> que sigue a una instancia de <!-- cierra el comentario.

Si bien los comentarios comienzan con < y terminan con >, un comentario no es un elemento HTML.

## Usar Javascript

Importar archivo externo de javascript:

~~~html
<script src="path/to/my/script.js"></script>
~~~

Ejecutando javascript directamente en html:

~~~html
<script>
  console.log("Some code");
</script>
~~~

> Nota: Tanto para los scripts en línea como para los scripts externos sin los atributos `defer` o `async`, el script se ejecuta inmediatamente cuando el navegador encuentra el elemento `<script>` al analizar el HTML. Esto significa que el script no puede acceder a ningún elemento HTML que aparezca más adelante en el documento. Para acceder a dichos elementos, considere mover el script al final del cuerpo del documento (justo antes de la etiqueta de cierre `</body>`) o usar el atributo `defer` en los scripts externos.

## accesibilidad

La accesibilidad es fundamental en cualquier desarrollo de software. JavaScript puede mejorar la accesibilidad de tu sitio web si lo usas correctamente, o puede convertirse en un desastre si lo utilizas sin cuidado. Para que JavaScript te beneficie, conviene conocer algunas buenas prácticas:

Haz que todo el contenido esté disponible como texto (estructurado). Utiliza HTML para tu contenido siempre que sea posible. Por ejemplo, si has implementado una barra de progreso con JavaScript, asegúrate de complementarla con porcentajes de texto correspondientes dentro del HTML. Del mismo modo, tus menús desplegables deben estar estructurados como listas de enlaces sin ordenar.

Haz que todas las funciones sean accesibles mediante el teclado.

Permite a los usuarios navegar por todos los controles (por ejemplo, enlaces y campos de formulario) con la tecla Tab en un orden lógico.

Si utilizas eventos de puntero (como eventos de ratón o táctiles), duplica la funcionalidad con eventos de teclado.

Prueba tu sitio web usando solo el teclado.

No establezcas ni intentes establecer límites de tiempo. Navegar con el teclado o escuchar el contenido leído requiere tiempo adicional. Es prácticamente imposible predecir cuánto tiempo tardarán los usuarios o navegadores en completar un proceso (especialmente acciones asíncronas como la carga de recursos).

Mantén las animaciones sutiles y breves, sin parpadeos. Los parpadeos son molestos y pueden provocar convulsiones. Además, si una animación dura más de un par de segundos, ofrece al usuario la opción de cancelarla.

Deja que los usuarios inicien las interacciones. Esto significa no actualizar el contenido, redirigir ni recargar automáticamente. No uses carruseles ni muestres ventanas emergentes sin previo aviso.

Ten un plan B para los usuarios sin JavaScript. Es posible que algunos usuarios tengan JavaScript desactivado para mejorar la velocidad y la seguridad, y a menudo experimentan problemas de red que impiden la carga de scripts. Además, los scripts de terceros (anuncios, scripts de seguimiento, extensiones del navegador) podrían interferir con tus scripts.

Como mínimo, incluye un breve mensaje con <noscript> como este: <noscript>Para usar este sitio, habilita JavaScript.</noscript>

Lo ideal es replicar la funcionalidad de JavaScript con HTML y scripts del lado del servidor siempre que sea posible.
Si solo buscas efectos visuales sencillos, CSS suele ser una opción aún más intuitiva.

Dado que casi todo el mundo tiene JavaScript habilitado, la etiqueta <noscript> no justifica la escritura de scripts inaccesibles.

## Metadatos

> Este elemento incluye [Elementos globales](#elementos-globales)

El elemento HTML `<meta>` representa metadatos que no pueden ser representados por otros elementos relacionados con metadatos, como `<base>`, `<link>`, `<script>`, `<style>` o `<title>`.

El tipo de metadatos que proporciona el elemento `<meta>` puede ser uno de los siguientes:

Si se establece el atributo `name`, el elemento `<meta>` proporciona metadatos a nivel de documento que se aplican a toda la página.

Si se establece el atributo `http-equiv`, el elemento `<meta>` actúa como una directiva pragma para simular directivas que de otro modo se especificarían en una cabecera HTTP.

Si se establece el atributo `charset`, el elemento `<meta>` es una declaración de conjunto de caracteres, que indica la codificación de caracteres en la que está codificado el documento.

Si se establece el atributo `itemprop`, el elemento `<meta>` proporciona metadatos definidos por el usuario.

charset

Este atributo declara la codificación de caracteres del documento. Si el atributo está presente, su valor debe coincidir con la cadena "utf-8" (sin distinción de mayúsculas y minúsculas), ya que UTF-8 es la única codificación válida para documentos HTML5. Los elementos <meta> que declaran una codificación de caracteres deben estar ubicados completamente dentro de los primeros 1024 bytes del documento.

content

Este atributo contiene el valor del atributo http-equiv o name, según se utilice.

http-equiv

Define una directiva pragma, que son instrucciones para que el navegador procese el documento. El nombre del atributo es la abreviatura de http-equivalent, ya que los valores permitidos son nombres de encabezados HTTP equivalentes.

media

El atributo media define a qué medios se debe aplicar el color del tema definido en el atributo content. Su valor es una consulta de medios, que por defecto es "all" si el atributo no está presente. Este atributo solo es relevante cuando el atributo name del elemento está configurado como theme-color. De lo contrario, no tiene efecto y no debe incluirse.
nombre

Los atributos nombre y contenido se pueden usar juntos para proporcionar metadatos del documento en términos de pares nombre-valor, donde el atributo nombre proporciona el nombre del metadato y el atributo contenido proporciona el valor.

Configurar una meta descripción

La siguiente etiqueta <meta> proporciona una descripción como metadatos para la página web:

~~~html
<meta
  name="description"
  content="The HTML reference describes all elements and attributes of HTML, including global attributes that apply to all elements." />
~~~

Redireccionamiento de página

El siguiente ejemplo utiliza `http-equiv="refresh"` para indicar al navegador que realice un redireccionamiento. El atributo `content="3;url=https://www.mozilla.org"` redirigirá la página a https://www.mozilla.org después de 3 segundos.

~~~html
<meta http-equiv="refresh" content="3;url=https://www.mozilla.org" />
~~~

## Media

Contenido de imagen, audio y video

Desde sus inicios, la web ha incluido soporte para la presentación de contenido multimedia visual. Inicialmente, estas capacidades eran limitadas y se ampliaron de forma orgánica, a medida que los diferentes navegadores encontraban sus propias soluciones a los problemas relacionados con la inclusión de imágenes fijas y videos en la web. La web moderna cuenta con potentes funciones para la presentación y manipulación de contenido multimedia, con varias API relacionadas que admiten diversos tipos de contenido. En general, los formatos multimedia compatibles con un navegador dependen completamente de sus creadores, lo que puede complicar el trabajo de un desarrollador web.

Esta guía ofrece una descripción general de los tipos de archivos multimedia, códecs y algoritmos que pueden conformar el contenido multimedia utilizado en la web. También proporciona información sobre la compatibilidad de los navegadores con diversas combinaciones de estos elementos y sugerencias para priorizar formatos, así como información sobre qué formatos destacan para tipos de contenido específicos.

## Sectioning content

Sectioning content, a subset of flow content, creates a section in the current outline defining the scope of <header> and <footer> elements.

The sectioning elements are:

    <article>
    <aside>
    <nav>
    <section>

## Heading content

Heading content, a subset of flow content, defines the title of a section. This definition applies both to sections marked by an explicit sectioning content elements and to those implicitly defined by the heading content itself.

The heading elements are:

    <h1>-<h6>
    <hgroup>

## Embedded content

Embedded content, a subset of flow content, imports another resource or inserts content from another markup language or namespace into the document.

The embedded content elements are:

    <audio>
    <canvas>
    <embed>
    <iframe>
    <img>
    <math>
    <object>
    <picture>
    <svg>
    <video>
