# Mini-guía rapida para YAML

---

## Indice

- [Mini-guía rapida para YAML](#mini-guía-rapida-para-yaml)
  - [Indice](#indice)
  - [Sobre YAML](#sobre-yaml)
    - [Que es YAML](#que-es-yaml)
    - [Cuándo usar YAML](#cuándo-usar-yaml)
    - [Cuándo no usar YAML](#cuándo-no-usar-yaml)
    - [Sintaxis Básica](#sintaxis-básica)
  - [Exteciones de archivo](#exteciones-de-archivo)
  - [Tipos de Datos](#tipos-de-datos)
    - [Escalares](#escalares)
    - [Listas](#listas)
    - [Mapas](#mapas)
    - [Estructuras Anidadas](#estructuras-anidadas)
  - [Características Avanzadas](#características-avanzadas)
    - [Anclas y Alias](#anclas-y-alias)
    - [Cadenas de Texto Multilínea](#cadenas-de-texto-multilínea)
    - [Etiquetas](#etiquetas)
  - [Buenas Prácticas](#buenas-prácticas)
  - [Ejemplo simple de Yaml](#ejemplo-simple-de-yaml)
  - [Ejercicios Prácticos](#ejercicios-prácticos)
    - [Práctica: Crear un archivo de configuración simple](#práctica-crear-un-archivo-de-configuración-simple)
    - [Práctica: Crear una lista de objetos](#práctica-crear-una-lista-de-objetos)
    - [Práctica: Usar anclas y alias para no repetir](#práctica-usar-anclas-y-alias-para-no-repetir)
  - [leer Yaml](#leer-yaml)
    - [Node-js](#node-js)
    - [JS web](#js-web)
    - [Python](#python)

---

## Sobre YAML

### Que es YAML

YAML (acrónimo de "YAML Ain't Markup Language") es un formato de serialización de datos legible por humanos. Se utiliza comúnmente para archivos de configuración, pero su uso se ha extendido a la transferencia de datos entre diferentes lenguajes de programación. Su diseño se centra en la simplicidad y la legibilidad.

### Cuándo usar YAML

Deberías usar YAML si:

- Necesitas un archivo de configuración que sea fácil de leer y escribir para personas no técnicas.
- Quieres definir configuraciones complejas con estructuras anidadas, como en Docker Compose, Kubernetes o GitHub Actions.
- Buscas una alternativa más legible a JSON o XML para ciertos tipos de datos.
- Necesitas definir datos jerárquicos de una manera clara y concisa.

### Cuándo no usar YAML

No deberías usar YAML si:

- La principal prioridad es el rendimiento del análisis (parsing). Formatos como JSON suelen ser más rápidos de procesar para las máquinas.
- Necesitas un esquema estricto y validación de datos integrada, donde XML con DTD/XSD podría ser más adecuado.
- El documento es principalmente texto con algunas anotaciones (Markup). En ese caso, Markdown o XML serían mejores opciones.
- La simplicidad de la herramienta es más importante que la legibilidad humana.

### Sintaxis Básica

La sintaxis de YAML se basa en la indentación para denotar la estructura.

- **Indentación:** Se usan espacios (generalmente 2 o 4) para anidar elementos. **No se deben usar tabulaciones**.
- **Comentarios:** Comienzan con el símbolo `#` y se extienden hasta el final de la línea.
- **Pares Clave-Valor:** Los mapas se definen con `clave: valor`. Es importante el espacio después de los dos puntos.
- **Listas:** Los elementos de una lista comienzan con un guion y un espacio (`- `).

---

## Exteciones de archivo

Yaml tiene dos extenciones viables de archivo que son equivalentes

- .yaml
- .yml

ambas son validas.

## Tipos de Datos

### Escalares

Son valores únicos como cadenas de texto, números o booleanos.

- **Cadenas de texto (Strings):**

```yaml
mi_string: Hola, mundo!
otro_string: "Si quieres usar 'comillas' dentro, encierra todo en comillas dobles."
tercer_string: 'O viceversa, para usar "comillas dobles".'
  ```

- **Números:**

```yaml
entero: 123
flotante: 3.1416
```

- **Booleanos:**

```yaml
es_verdadero: true
es_falso: false
```

- **Nulos:**

```yaml
sin_valor: null
```

### Listas

Lista o secuencia de elementos. Cada elemento se introduce con un guion (-) seguido de un espacio.

```yaml
# Una lista de frutas
frutas:
  - Manzana
  - Naranja
  - Plátano

# También se puede escribir en una sola línea (formato de flujo)
frutas_inline: [Manzana, Naranja, Plátano]
```

### Mapas

Los mapas o diccionarios son colecciones de pares clave-valor.

```yaml
# Un mapa que describe a una persona
persona:
  nombre: Juan Pérez
  edad: 30
  ciudad: "Ciudad de México"

# Formato de flujo
persona_inline: {nombre: "Juan Pérez", edad: 30}
```

### Estructuras Anidadas

Puedes combinar listas y mapas para crear estructuras más complejas.

```yaml
# Lista de usuarios, donde cada usuario es un mapa
usuarios:
  - nombre: Alice
    email: alice@example.com
    roles:
      - admin
      - editor
  - nombre: Bob
    email: bob@example.com
    roles:
      - lector
```

---

## Características Avanzadas

### Anclas y Alias

Tambien llados Anchors y Aliases en ingles, permiten reutilizar fragmentos de tu YAML para no repetir código (principio DRY: Don't Repeat Yourself).

- **Ancla (`&`):** Define un bloque de código con un nombre.
- **Alias (`*`):** Reutiliza el bloque de código definido por un ancla.

```yaml
# Definimos una configuración base para una base de datos
default_db_config: &db_config
  adapter: postgresql
  encoding: utf8
  pool: 5

# La usamos en diferentes entornos
development:
  database: myapp_dev
  <<: *db_config # Combina el ancla con el mapa actual

test:
  database: myapp_test
  <<: *db_config
```

### Cadenas de Texto Multilínea

YAML ofrece dos formas principales de manejar texto que abarca varias líneas.

- **Literal (`|`):** Conserva los saltos de línea.

```yaml
poema: |
En un lugar de la Mancha,
de cuyo nombre no quiero acordarme,
no ha mucho tiempo que vivía un hidalgo.
```

- **Plegado (`>`):** Pliega los saltos de línea en espacios. Ideal para párrafos largos.

```yaml
descripcion: >
Este es un párrafo largo que se escribirá
en una sola línea, aunque en el editor de código
ocupe varias. Los saltos de línea se convierten en espacios.
```

### Etiquetas

Las Etiquetas o Tags permiten especificar explícitamente el tipo de dato.

```yaml
# Forzar un número a ser tratado como string
codigo_postal: !!str 12345

# Especificar un tipo de dato personalizado
mi_dato: !mi_tipo
  valor: especial
```

---

## Buenas Prácticas

- **Consistencia en la indentación:** Elige 2 o 4 espacios y mantenlos en todo el documento. La mayoría de las guías de estilo recomiendan 2 espacios.

- **Usar comillas cuando sea necesario:** Aunque YAML a menudo no requiere comillas para las cadenas, es una buena práctica usarlas si el texto contiene caracteres especiales (`:`, `{`, `[`, `#`, etc.) o si empieza o termina con espacios.

- **Claridad y legibilidad:** Organiza tu archivo de forma lógica. Usa comentarios para explicar partes complejas.

- **Evitar tabulaciones:** Las tabulaciones son ambiguas y pueden ser interpretadas de manera diferente por distintos editores. Usa siempre espacios.

---

## Ejemplo simple de Yaml

´´´yaml
ciudad: Madrid
comillas: '245'
edad: 20
temperatura: 25.2
masa: 1e6
activo: true
verificado: yes
description: null
comentario: ~

´´´

---

## Ejercicios Prácticos

### Práctica: Crear un archivo de configuración simple

1. Crea un archivo llamado `config.yaml`.

2. Dentro del archivo, define una configuración para una aplicación web con los siguientes datos:

    - `nombre_app`: "Mi Gran App"
    - `version`: 1.2
    - `debug_mode`: true

3. Guarda el archivo. El resultado debería ser:

```yaml
nombre_app: "Mi Gran App"
version: 1.2
debug_mode: true
```

### Práctica: Crear una lista de objetos

1. En un nuevo archivo `inventario.yaml`, crea una lista de productos.

2. La lista debe llamarse `productos`.

3. Cada producto en la lista debe ser un mapa con las siguientes claves:

    - `id`: Un número único.
    - `nombre`: El nombre del producto.
    - `precio`: Un número con decimales.

4. Añade al menos dos productos. El resultado podría ser:

```yaml
productos:
    - id: 101
    nombre: "Laptop Pro"
    precio: 1499.99
    - id: 102
    nombre: "Mouse Inalámbrico"
    precio: 25.50
```

### Práctica: Usar anclas y alias para no repetir

1. Imagina que estás configurando dos servicios que comparten la misma configuración de reintentos.

2. Crea un archivo `servicios.yaml`.

3. Define un ancla llamada `retry_policy` con la siguiente configuración:

    - `intentos`: 3
    - `delay`: 5s

4. Crea dos servicios, `servicio_a` y `servicio_b`, y usa un alias para aplicarles la política de reintentos.

5. El resultado debería ser:

```yaml
retry_policy: &retry_policy
    intentos: 3
    delay: 5s

servicio_a:
    nombre: "Procesador de Pagos"
    config_reintentos: *retry_policy

servicio_b:
    nombre: "Notificador de Emails"
    config_reintentos: *retry_policy
```

## leer Yaml

### Node-js

npm install js-yaml

```node.js
const fs = require('fs');
const yaml = require('js-yaml');

try {
  const contenido = fs.readFileSync('./config.yaml', 'utf8');
  const datos = yaml.load(contenido);
  console.log(datos);
} catch (e) {
  console.error(e);
}
```

### JS web

```js
import yaml from 'js-yaml';

async function cargarConfiguracion() {
  const respuesta = await fetch('config.yaml');
  const texto = await respuesta.text();
  const datos = yaml.load(texto);
  console.log(datos);
}
```

### Python

pip install pyyaml

- **Desde un arcivo**

```python
import yaml

with open('configuracion.yaml', 'r') as archivo:
    datos = yaml.safe_load(archivo)

print(datos)
```

- **Desde una varialbe**

```python
import yaml

documento = """
servidor:
  puerto: 8080
  debug: true
"""

config = yaml.safe_load(documento)
print(config['servidor']['puerto'])´
```
