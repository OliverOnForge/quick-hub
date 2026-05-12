# Mini-guía rapida para JSON

---

## Indice

- [Mini-guía rapida para JSON](#mini-guía-rapida-para-json)
  - [Indice](#indice)
  - [Sobre JSON](#sobre-json)
    - [Qué es JSON](#qué-es-json)
    - [Cuando usar JSON](#cuando-usar-json)
    - [Cuándo no usar JSON](#cuándo-no-usar-json)
    - [Sintaxis Básica](#sintaxis-básica)
  - [Tipos de Datos](#tipos-de-datos)
    - [Objetos](#objetos)
    - [Arrays](#arrays)
    - [Valores](#valores)
  - [Estructura y Anidamiento](#estructura-y-anidamiento)
  - [Buenas Prácticas](#buenas-prácticas)
  - [Ejemplo simple de JSON](#ejemplo-simple-de-json)
  - [Ejercicios Prácticos](#ejercicios-prácticos)
    - [Práctica: Crear un objeto de configuración](#práctica-crear-un-objeto-de-configuración)
    - [Práctica: Crear un array de objetos](#práctica-crear-un-array-de-objetos)
  - [Leer e interpretar JSON](#leer-e-interpretar-json)
    - [Node.js y JavaScript](#nodejs-y-javascript)
    - [Python](#python)

---

## Sobre JSON

### Qué es JSON

JSON (JavaScript Object Notation) es un formato de texto ligero para el intercambio de datos. Aunque deriva de JavaScript, es independiente del lenguaje y es soportado por la mayoría de los lenguajes de programación modernos. Su diseño se centra en ser fácil de leer para los humanos y fácil de interpretar y generar para las máquinas.

### Cuando usar JSON

Deberías usar JSON si:

- Necesitas intercambiar datos entre un servidor y una aplicación web (es el estándar de facto para APIs REST).
- Buscas un formato que sea rápido y fácil de "parsear" (interpretar) por cualquier lenguaje de programación.
- Necesitas almacenar datos estructurados de una forma compacta y universalmente entendida.
- La interoperabilidad entre diferentes sistemas y lenguajes es una prioridad.

### Cuándo no usar JSON

No deberías usar JSON si:

- Necesitas un archivo de configuración que sea mantenido principalmente por personas y donde la legibilidad y la facilidad para añadir comentarios sean cruciales (YAML es a menudo mejor para esto).
- El documento es muy complejo y necesitas características avanzadas como referencias o tipos de datos personalizados (YAML o XML pueden ser más adecuados).
- Necesitas almacenar grandes cantidades de datos binarios.

### Sintaxis Básica

La sintaxis de JSON es más estricta que la de YAML y se basa en la de los objetos de JavaScript.

- **Objetos:** Se encierran en llaves `{}`. Consisten en pares clave-valor.
- **Claves:** Deben ser cadenas de texto y estar siempre encerradas en comillas dobles `""`.
- **Valores:** Pueden ser un string, número, booleano, `null`, un array u otro objeto.
- **Pares Clave-Valor:** Se separan por dos puntos `:`.
- **Separación:** Los elementos en objetos y arrays se separan por comas `,`. **No se permiten comas al final del último elemento**.
- **Arrays:** Se encierran en corchetes `[]` y contienen una lista de valores.
- **Comentarios:** JSON **no soporta comentarios**.

---

## Tipos de Datos

### Objetos

Un objeto es una colección desordenada de pares `clave: valor`.

```json
{
  "nombre": "Juan Pérez",
  "edad": 30,
  "activo": true,
  "ciudad": "Ciudad de México"
}
```

### Arrays

Un array o lista es una colección ordenada de valores.

```json
{
  "frutas": [
    "Manzana",
    "Naranja",
    "Plátano"
  ]
}
```

### Valores

Los valores en JSON pueden ser de los siguientes tipos:

- **String:** Una cadena de texto entre comillas dobles.
  `"Hola, mundo!"`
- **Number:** Un número (entero o de punto flotante).
  `123`, `3.1416`
- **Boolean:** `true` o `false`.
- **null:** Representa un valor nulo o vacío.
- **Object:** Otro objeto JSON.
- **Array:** Otro array JSON.

---

## Estructura y Anidamiento

Puedes anidar objetos dentro de otros objetos y arrays dentro de objetos (y viceversa) para crear estructuras de datos complejas.

```json
{
  "usuarios": [
    {
      "id": 1,
      "nombre": "Alice",
      "email": "alice@example.com",
      "roles": ["admin", "editor"],
      "direccion": {
        "calle": "Av. Principal",
        "numero": 123
      }
    },
    {
      "id": 2,
      "nombre": "Bob",
      "email": "bob@example.com",
      "roles": ["lector"],
      "direccion": null
    }
  ]
}
```

---

## Buenas Prácticas

- **Siempre comillas dobles:** Todas las claves y los valores de tipo string deben usar comillas dobles `""`.
- **Sin comas finales (trailing commas):** El último elemento de un objeto o un array no debe tener una coma después. Esto es un error de sintaxis común.
- **Validar el JSON:** Antes de usar un archivo JSON, especialmente si fue editado manualmente, es una buena práctica validarlo con una herramienta online o una librería para asegurar que la sintaxis es correcta.
- **Extensión `.json`:** Usa siempre la extensión de archivo `.json` para identificar estos archivos.

---

## Ejemplo simple de JSON

```json
{
  "ciudad": "Madrid",
  "edad": 20,
  "temperatura": 25.2,
  "activo": true,
  "descripcion": null,
  "permisos": ["lectura", "escritura"]
}
```

---

## Ejercicios Prácticos

### Práctica: Crear un objeto de configuración

1. Crea un archivo llamado `config.json`.

2. Dentro del archivo, define un objeto de configuración para una aplicación web con los siguientes datos:

    - `nombre_app`: "Mi Gran App"
    - `version`: 1.2
    - `debug_mode`: true

3. Guarda el archivo. El resultado debería ser:

```json
    {
      "nombre_app": "Mi Gran App",
      "version": 1.2,
      "debug_mode": true
    }
```

### Práctica: Crear un array de objetos

1. En un nuevo archivo `inventario.json`, crea un objeto principal que contenga una clave `productos`.
2. El valor de `productos` debe ser un array donde cada elemento es un objeto que representa un producto.
3. Cada producto debe tener las siguientes claves:

    - `id`: Un número único.
    - `nombre`: El nombre del producto.
    - `precio`: Un número con decimales.

4. Añade al menos dos productos. El resultado podría ser:

```json
    {
      "productos": [
        {
          "id": 101,
          "nombre": "Laptop Pro",
          "precio": 1499.99
        },
        {
          "id": 102,
          "nombre": "Mouse Inalámbrico",
          "precio": 25.50
        }
      ]
    }
```

---

## Leer e interpretar JSON

### Node.js y JavaScript

En JavaScript, trabajar con JSON es nativo y muy sencillo.

- **Desde una variable (string):**

```javascript
const jsonString = '{"nombre": "Ana", "edad": 25}';
const datos = JSON.parse(jsonString);
console.log(datos.nombre); // Muestra "Ana"
```

- **Convertir un objeto a string JSON:**

```javascript
const objeto = { nombre: "Ana", edad: 25 };
const jsonString = JSON.stringify(objeto);
console.log(jsonString); // Muestra '{"nombre":"Ana","edad":25}'
```

- **En Node.js (leyendo un archivo):**

```javascript
const fs = require('fs');
const contenido = fs.readFileSync('./config.json', 'utf8');
const datos = JSON.parse(contenido);
console.log(datos);
```

### Python

El módulo `json` de la librería estándar de Python facilita el trabajo con JSON.

- **Desde un archivo:**

```python
import json

with open('config.json', 'r') as archivo:
    datos = json.load(archivo)

print(datos)
print(datos['nombre_app'])
```

- **Desde una variable (string):**

```python
import json

json_string = """
{
    "nombre": "Carlos",
    "edad": 40
}
"""
datos = json.loads(json_string)
print(datos['nombre']) # Muestra "Carlos"
```
