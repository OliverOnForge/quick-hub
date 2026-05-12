
# Guía de Repaso: Diseño Profesional en Gran Formato

Este documento resume los puntos más importantes para abordar proyectos de diseño en gran formato, basándose en la relación fundamental entre **resolución, distancia de visualización y escala de trabajo**.

## 1\. Conceptos Fundamentales

### ¿Qué es el Gran Formato?

Se considera "gran formato" a cualquier diseño cuyas dimensiones superan el tamaño estándar de la impresión offset (aproximadamente **70 x 100 cm**). La impresión se realiza en máquinas especializadas llamadas **plotters** o impresoras de gigantografía.

**Ejemplos comunes:**

  * Vallas publicitarias (Billboards)
  * Lonas para edificios
  * MUPIS (Mobiliario Urbano como Punto de Información) en paradas de autobús o metro.
  * Vinilos decorativos para locales y stands.
  * Banners y Roll-ups.
  * Rotulación de vehículos.

### El Principio Clave: La Distancia de Visualización

La regla más importante en el diseño de gran formato es:

> A mayor distancia de visualización, menor es la resolución (píxeles por pulgada) que necesita tu diseño.

Un ojo humano no puede distinguir los píxeles individuales de una valla publicitaria que está a 50 metros, por lo que usar una resolución altísima (como 300 ppp) es innecesario, ineficiente y puede colapsar tu ordenador.

### Vectorial vs. Mapa de Bits

  * **Vectorial**: Compuesto por fórmulas matemáticas. Ideal para logos, textos y formas. **Se puede escalar infinitamente sin perder calidad**.
  * **Mapa de Bits (Raster)**: Compuesto por píxeles. Ideal para fotografías e imágenes complejas. **Pierde calidad al escalarse** y es el origen del "problema" de la resolución.

Si tu diseño es **100% vectorial**, no tienes que preocuparte por la resolución. El problema surge cuando incluyes imágenes de mapa de bits.

## 2\. El Flujo de Trabajo Profesional

El método más eficiente y versátil para crear diseños de gran formato que incluyan fotografías es el siguiente:

1.  **Preparar la Imagen (Photoshop)**: Ajusta el tamaño, la resolución y el color de tu imagen o fondo en un software de edición de mapa de bits como Photoshop. Guarda el archivo en formato `.PSD`.
2.  **Maquetar el Diseño (Illustrator)**: Crea tu documento final en un software vectorial como Illustrator. Coloca (no incrustes) el archivo `.PSD` que preparaste. Añade textos, logos y otros elementos vectoriales.
3.  **Exportar para Imprenta (PDF)**: Exporta tu diseño final en formato **PDF/X-4:2008**, que es un estándar de alta calidad para la impresión profesional.

## 3\. La Tabla de Resolución: Tu Herramienta Esencial

Esta tabla es la clave para decidir qué resolución usar según la distancia y la escala de trabajo.

| Distancia de Visualización | Resolución (Escala Real 1:1) | Resolución (Escala 1:10)\* |
| :--- | :---: | :---: |
| **Corta (0 - 1 metro)** | 200 - 300 ppp | No aplica |
| **Media (1 - 5 metros)**<br>*Ej: MUPIS, Roll-ups* | 75 - 150 ppp | 750 - 1500 ppp |
| **Larga (+15 metros)**<br>*Ej: Vallas, Lonas* | 20 - 50 ppp | **300 - 500 ppp** |

> **\*¿Por qué la resolución es más alta a escala 1:10?**
> Porque estás creando un archivo 10 veces más pequeño. La imprenta lo ampliará 10 veces para imprimirlo, y en ese proceso, la resolución se dividirá entre 10. Por ejemplo, un archivo a **400 ppp** a escala 1:10 se convertirá en un archivo de **40 ppp** a tamaño real (1:1), lo cual es perfecto para una valla.

## 4\. Técnicas y Configuraciones Clave

### Trabajo a Escala (1:10)

Debes trabajar a escala cuando las dimensiones de tu diseño superan el límite del software.

  * **Límite de Adobe Illustrator:** `577 cm`.
  * **¿Cómo funciona?** Simplemente divide todas tus medidas entre 10.
      * **Ejemplo:** Una valla de `800 cm x 300 cm` se diseña en una mesa de trabajo de `80 cm x 30 cm`.
      * La **sangre** también se escala. 4 cm de sangre a tamaño real se convierten en `0.4 cm` en tu documento a escala.

### Ajuste de Resolución en Illustrator (¡El Truco\!)

Por defecto, Illustrator no permite resoluciones personalizadas como 110 o 400 ppp. Para configurarla correctamente:

1.  Ve al menú `Efecto` \> `Ajustes de efectos de rasterizado de documento...`
2.  En la sección `Resolución`, selecciona la opción `Otra`.
3.  Introduce manualmente los píxeles por pulgada (ppp) que necesitas según la tabla.

### Preparación del Archivo en Photoshop

  * **Dimensiones:** El tamaño final del documento debe incluir la sangre.
      * *Ejemplo Mupi (escala 1:1):* Diseño de 120x175cm + 2cm de sangre por lado = Documento de `124 x 179 cm`.
  * **Resolución:** La que indica la tabla para la distancia de visualización.
  * **Modo de Color:** Siempre **CMYK**.

### Consejo de Composición: Adapta tus Recursos

No coloques el texto "encima" de los elementos importantes de una foto. Esto crea un conflicto visual.

> **Práctica profesional:** Edita y adapta la imagen de fondo para que **genere un espacio natural** donde el texto pueda respirar y tener máxima legibilidad. Utiliza herramientas como **"Rellenar según contenido"** en Photoshop para extender fondos de manera inteligente.

## 5\. Resumen de Ejemplos Prácticos

#### Caso 1: MUPI (Visualización a corta distancia, 1-5 metros)

  * **Medidas Reales:** 120 x 175 cm (+ 2 cm de sangre).
  * **Escala de Trabajo:** **1:1 (Real)**, ya que cabe en Illustrator.
  * **Resolución Seleccionada:** **110 ppp**.
  * **Workflow:**
    1.  **Photoshop:** Crear documento de 124x179 cm a 110 ppp en CMYK.
    2.  **Illustrator:** Crear documento de 120x175 cm con 2 cm de sangre. Ajustar resolución interna a 110 ppp. Colocar el PSD y maquetar.
    3.  **Exportar:** PDF/X-4.

#### Caso 2: Valla Publicitaria (Visualización a larga distancia, +15 metros)

  * **Medidas Reales:** 800 x 300 cm (+ 4 cm de sangre).
  * **Escala de Trabajo:** **1:10**, porque supera el límite de Illustrator.
  * **Resolución Seleccionada:** **400 ppp**.
  * **Workflow:**
    1.  **Photoshop:** Crear documento a escala de 80.8 x 30.8 cm (80x30 + 0.4 de sangre por lado) a 400 ppp en CMYK.
    2.  **Illustrator:** Crear documento de 80x30 cm con 0.4 cm de sangre. Ajustar resolución interna a 400 ppp. Colocar el PSD y maquetar.
    3.  **Exportar:** PDF/X-4.

## 6\. Consejo Final: La Comunicación es Clave

> **Habla siempre con la imprenta antes de empezar a diseñar.**
> Pregúntales por sus especificaciones técnicas: perfiles de color, cantidad de sangre requerida y cualquier otra particularidad de sus máquinas. Esto te ahorrará tiempo, dinero y evitará sorpresas desagradables.