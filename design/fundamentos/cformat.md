
## Guía Práctica de Modos de Color para Diseñadores: RGB vs. CMYK

Todo proyecto de diseño comienza con una pregunta fundamental que define todas nuestras decisiones técnicas posteriores: **"¿Esto se va a imprimir o se va a ver en una pantalla?"**. La respuesta a esta pregunta determina el modo de color que debemos usar, un pilar esencial para garantizar la fidelidad y consistencia de nuestro trabajo.

---

### Los Dos Universos del Color

Existen dos grandes modos de color, cada uno diseñado para un medio específico. Entender su naturaleza es clave para evitar sorpresas desagradables.

#### Modo RGB: El Mundo de la Luz (Pantallas)
El modo RGB es el lenguaje de las pantallas. Desde un smartphone hasta un televisor, todos los dispositivos que emiten luz utilizan este sistema.

* **Qué significa:** **R**ed (Rojo), **G**reen (Verde), **B**lue (Azul).
* **Cómo funciona (Color Aditivo):** Se basa en la **adición de luz**. El punto de partida es el negro absoluto (ausencia total de luz). A medida que se añaden y combinan luces roja, verde y azul, se crean los diferentes colores.
    * `Negro = 0% de luz`
    * `Blanco = 100% de luz roja + verde + azul`
* **Casos de Uso:** Diseño web, aplicaciones móviles, gráficos para redes sociales, vídeo, presentaciones digitales. En resumen, **todo lo que será visualizado en una pantalla.**

#### Modo CMYK: El Mundo del Pigmento (Impresión)
El modo CMYK es el lenguaje de las tintas y la impresión física.

* **Qué significa:** **C**yan (Cian), **M**agenta, **Y**ellow (Amarillo), **K**ey (Negro).
* **Cómo funciona (Color Sustractivo):** Se basa en la **sustracción de luz**. El punto de partida es el blanco del papel. A medida que se añaden tintas, estas absorben (sustraen) ciertas ondas de luz y reflejan otras, creando los colores que vemos.
    * `Blanco = 0% de tinta (el papel)`
    * `Negro "teórico"`: La mezcla de C+M+Y produce un marrón oscuro, no un negro puro. Por eso se añade la cuarta tinta, el **Negro (K)**, para lograr profundidad y contraste.
* **Casos de Uso:** Tarjetas de visita, folletos, revistas, packaging, etiquetas, cartelería, ropa. En resumen, **todo lo que vaya a ser impreso sobre un soporte físico.**

---

### La Regla de Oro: El Flujo de Trabajo Correcto

Si un proyecto tiene componentes tanto para impresión como para pantalla (por ejemplo, una campaña con carteles y posts para Instagram), existe una regla fundamental para mantener la consistencia del color:

> **Comienza siempre en el modo de color más pequeño, es decir, CMYK.**

El espectro o **gama de colores (gamut)** que se puede reproducir con tintas (CMYK) es significativamente más reducido que el que se puede mostrar con luz (RGB). Es fácil y seguro convertir colores de CMYK a RGB, ya que todos los colores de impresión caben dentro del espectro de pantalla.

El proceso inverso es peligroso y es la causa principal de la "decepción del color".

### El Peligro de la Conversión: Por Qué los Colores Vivos se "Apagan"

Cuando diseñas en RGB usando colores muy brillantes y saturados (verdes fosforitos, azules eléctricos, naranjas vibrantes) y luego conviertes el archivo a CMYK para imprimir, te encontrarás con una desagradable sorpresa:

**RGB → CMYK = Pérdida drástica de viveza y brillo.**

Los colores se verán "apagados" o sucios. Esto no es un error del programa, es una limitación física. Simplemente, **no existe una mezcla de tintas capaz de replicar la intensidad de un color generado por luz pura.**

* **Conversión Segura (CMYK a RGB):** El cambio es mínimo. Los colores se mantienen fieles, a veces ganando un poco de brillo.
* **Conversión Peligrosa (RGB a CMYK):** El cambio es notorio y decepcionante. Los colores se apagan para ajustarse a lo que la imprenta puede reproducir.

### HSB: La Herramienta Intuitiva para Elegir Colores

Dentro de los programas de diseño, existe un tercer modelo de color que no es un modo de salida, sino una herramienta de trabajo para los diseñadores: **HSB**.

* **H (Hue/Tono):** El color puro en el círculo cromático (rojo, verde, azul...).
* **S (Saturation/Saturación):** La intensidad del color (de gris a un color muy vivo).
* **B (Brightness/Brillo):** La cantidad de luz u oscuridad del color (de negro al color puro).

Trabajar con HSB es mucho más intuitivo para buscar y refinar colores, ya que se alinea con cómo pensamos naturalmente sobre ellos, en lugar de intentar adivinar porcentajes de RGB o CMYK.

### Tip Práctico para la Exportación Web

Cuando exportes imágenes para uso digital (web, redes sociales), los programas de diseño como Illustrator o Photoshop tienen opciones como "Exportar para pantallas" o "Guardar para web". Por defecto, estas funciones ya están configuradas para convertir tu archivo al perfil de color estándar de internet, **sRGB**, y optimizarlo para que se vea de manera consistente en la mayoría de los dispositivos. No necesitas hacer ajustes complejos; el software se encarga de ello.