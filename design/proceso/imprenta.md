
## Guía Definitiva de Arte Final: Cómo Preparar Archivos para Imprenta

El "Arte Final" o "Pre-prensa" es el proceso de preparar y revisar un archivo de diseño para asegurar que se imprima de manera correcta, consistente y sin errores. Es el último paso y el puente entre la creatividad en tu pantalla y el producto físico final. Ignorar estas reglas puede resultar en costosos errores de producción.

Aquí tienes una checklist con los puntos esenciales.

---

### 1. Modo y Perfil de Color: La Base de Todo

Antes de empezar a diseñar, debes configurar correctamente el color.

* **Modo de Color:** En el 95% de los casos de impresión tradicional (offset), el modo de color correcto es **CMYK**. Si bien algunas imprentas digitales modernas pueden trabajar con perfiles RGB para obtener una gama de color más amplia, esto no es la norma.
* **Perfil de Color:** El perfil asegura que lo que ves en tu monitor calibrado sea lo más parecido posible al resultado impreso. Perfiles como **FOGRA39** o **FOGRA29** son comunes en Europa, pero pueden variar según la máquina y el tipo de papel (estucado, no estucado, etc.).

> **La Regla de Oro:** Habla siempre con tu imprenta *antes* de empezar. Ellos te dirán exactamente qué modo y perfil de color utilizar. Esta simple conversación te ahorrará innumerables problemas.

### 2. Dejar Sangre (Bleed): El Margen de Seguridad

Este es uno de los errores más comunes y fáciles de evitar.

* **¿Qué es?** Es un área extra de tu diseño (imagen o color de fondo) que se extiende más allá de los bordes de corte finales del documento.
* **¿Por qué es crucial?** Las guillotinas que cortan el papel tienen una mínima tolerancia de movimiento. Sin sangre, cualquier pequeña desviación en el corte dejará un antiestético filete blanco en los bordes de tu diseño.
* **¿Cuánta sangre dejar?**
    * **Impresión estándar (tarjetas, folletos):** Mínimo **3 mm** por cada lado.
    * **Gran formato (vallas, carteles grandes):** Mínimo **1 cm** por cada lado, o más según el tamaño.

### 3. Tintas Planas (Spot Colors) y Muestras

Para colores especiales como Pantone, metálicos o fluorescentes, se usan tintas planas.

* **Nomenclatura es Clave:** Al crear una tinta plana, lo más importante no es el color que ves en pantalla, sino el **nombre de la muestra**. Debe ser el código exacto (ej. `PANTONE 432 C`). La imprenta usará este nombre como la instrucción para mezclar la tinta correcta.
* **Limpia tus Muestras:** Antes de enviar el archivo, elimina todas las muestras de color que no estés utilizando. Esto crea un fichero más limpio y evita confusiones al impresor.

### 4. Efectos y Acabados Especiales (Barniz, Stamping, Troquel)

Para aplicar un barniz, un estampado metálico (stamping) o un corte especial (troquel), debes prepararlo de forma técnica y clara.

1.  **Crea una Tinta Plana:** Genera una nueva muestra de tinta plana. Ponle un nombre descriptivo (`BARNIZ UV`, `STAMPING ORO`, `TROQUEL`). Asígnale un color muy llamativo y que no uses en el diseño (ej. 100% Magenta) para que sea fácil de identificar visualmente.
2.  **Usa una Capa Separada:** Coloca todos los elementos del acabado en una capa superior, por encima de tu diseño. Nómbrala de forma clara (`CAPA BARNIZ`). Esto permite al impresor aislar y trabajar con el efecto fácilmente.
3.  **Activa la Sobreimpresión (Overprint):** ¡Este paso es CRÍTICO! Debes seleccionar el objeto del efecto y activar el atributo de "Sobreimprimir" (en relleno si es una mancha, o en trazo si es una línea como un troquel).
    * **¿Por qué?** Si no lo haces, el objeto del efecto "vaciará" el diseño que tiene debajo (knockout), dejando un hueco blanco en la impresión final. Al sobreimprimir, te aseguras de que el efecto se aplique **encima** del diseño ya impreso.

### 5. Textos a Curvas (Crear Contornos)

Una vez que el diseño está aprobado y no habrá más cambios de texto, es una práctica de seguridad fundamental.

* **El Problema:** Si envías un archivo con texto editable, corres el riesgo de que la imprenta no tenga la tipografía que usaste, la reemplace por otra y arruine la composición. También pueden surgir problemas de licencias que impidan incrustar la fuente en el PDF.
* **La Solución:** Convierte todo el texto a curvas o contornos. Esto transforma las letras en formas vectoriales, eliminando cualquier dependencia del archivo de la fuente.
* **Consejo Pro:** Guarda siempre dos versiones de tu archivo: una con el texto editable (`_EDITABLE.ai`) y otra con el texto trazado para enviar a imprenta (`_PRINT.pdf`).

### 6. Exporta en PDF/X: El Estándar Profesional

Olvídate de los preajustes genéricos como "Impresión de alta calidad". La forma más segura y profesional de enviar un archivo a imprenta es usando un estándar PDF/X.

* **¿Qué es PDF/X?** Es un formato estandarizado (ISO) específicamente diseñado para el intercambio de archivos de impresión. Es un "contenedor sellado" que se asegura de que todo lo necesario (imágenes, fuentes incrustadas, perfiles de color, marcas de corte) esté incluido y configurado correctamente.
* **Ventajas:** Optimiza las imágenes a la resolución correcta, aplana transparencias de forma segura y elimina datos innecesarios, creando un fichero ligero, fiable y listo para imprimir sin sorpresas.

---

**En resumen:** una buena comunicación con la imprenta y seguir esta checklist técnica son la garantía para que el resultado final sea exactamente como lo imaginaste.