
# Prompt Engeenering

---

## Indice

- [Prompt Engeenering](#prompt-engeenering)
  - [Indice](#indice)
  - [Teoria de prompts](#teoria-de-prompts)
    - [Bases](#bases)
  - [Tecnicas](#tecnicas)
  - [Formatos de prompt estandar](#formatos-de-prompt-estandar)
    - [Prompt de texto](#prompt-de-texto)
    - [Generador de prompts](#generador-de-prompts)
    - [Prompt de imagen](#prompt-de-imagen)
    - [Prompt de musica](#prompt-de-musica)
    - [Prompt de video](#prompt-de-video)
  - [Diseccionando prompts](#diseccionando-prompts)
    - [Personalizacion o rol](#personalizacion-o-rol)
    - [Contexto](#contexto)
    - [Tarea o accion concreta](#tarea-o-accion-concreta)
    - [Formato](#formato)
    - [Ejemplos](#ejemplos)
    - [Tono](#tono)

---

## Teoria de prompts

### Bases

- Claridad y especifidad: Un buen prompt debe ser lo mas claro y específico posible.

- Contexto y roles: Darle un rol al modelo y proporcionarle el contexto adecuado puede mejorar drásticamente la calidad de la respuesta. El modelo se ajustará a la personalidad que le asignes.

- Mostrar ejemplos: Los ejemplos son una de las herramientas más poderosas para guiar al modelo. Puedes mostrarle cómo quieres que sea la respuesta, tanto en estilo como en formato.

- Dividir tareas: Si la solicitud es muy elaborada, lo mejor es  dividirla en pasos mas pequeños.

- Usar restricciones: Si necesitas que la respuesta cumpla con ciertos requisitos, es fundamental que lo especifiques en el prompt. Esto incluye límites de palabras, tipo de contenido o formato

- Chain-of-Thought Esta técnica pide al modelo que muestre su "proceso de pensamiento" paso a paso antes de dar la respuesta final. Es especialmente útil para resolver problemas complejos.

- Self-Consistency: Le pides al modelo que genere varias respuestas a la misma pregunta (usando Chain- of thought) Luego, comparas las respuestas y eliges la que aparece con mayor frecuencia.

- Retrieval-Augmented Generation Permites al modelo acceder a una base de conocimientos externa (como documentos, bases de datos o la web) para generar una respuesta.

- FFine-Tuning (Ajuste fino) Si necesitas que el modelo se adapte a un estilo, tono o tipo de tarea muy específico, puedes ajustar el modelo con tus propios datos. A diferencia de un prompt, el ajuste fino modifica el comportamiento del modelo de forma permanente.

- Role Prompting: Creas un "persona" completa con una personalidad, un conjunto de habilidades e incluso limitaciones.

## Tecnicas

- Zero-Shot: Simplemente le das la instrucción y esperas que el modelo entienda la tarea y la complete correctamente.

- Few-Shot: Le das al modelo un pequeño número de ejemplos (generalmente entre 1 y 5) que le muestran cómo quieres que responda.

- Tree of Thoughts: Le pides al modelo que genere varias "ideas" o "hipótesis" para resolver un problema, las evalúe y luego elija la mejor.

- ReAct: sta técnica combina el razonamiento del modelo (Reason) con la capacidad de interactuar con herramientas externas (Act).

El modelo no solo piensa, sino que también decide qué herramientas usar (por ejemplo, una calculadora, una API de búsqueda, o un buscador web) para obtener la información que necesita.

- ReAct:  El modelo no solo piensa en la respueta tambien debe pensar en qué herramientas usar para obtener la información que necesita y como usarlas.

- Self-Ask:  Le pides al modelo que se haga preguntas a sí mismo y las responda antes de dar la respuesta final.

- Least-to-Most: Consiste en dividir el problema en subproblemas más sencillos, resolverlos uno a uno y usar cada  solución de cada subproblema como parte del prompt para el siguiente.

## Formatos de prompt estandar

### Prompt de texto

[Rol] [Contexto] [Tarea] [Formato] [Ejemplo] [Tono]

Ejemplo:
"Actúa como un profesor de historia especializado en la Segunda Guerra Mundial. Tu tarea es explicar la Batalla de Stalingrado, enfocándote en las estrategias y el impacto humano del invierno. La explicación debe ser concisa y clara, usando un lenguaje apto para un estudiante de preparatoria. La respuesta debe estar estructurada en una lista numerada de no más de cinco puntos clave."

Variantes comunes:

- Clasificación: Clasifica el siguiente texto como [categoría 1], [categoría 2] o [categoría 3]. Texto: [texto].

- Emociones: Clasifica el siguiente texto con la emoción que expresa: [lista de emociones]. Texto: [texto].

- Generación de texto: Escribe un artículo sobre [tema] con un tono [tono] y un mínimo de [cantidad] palabras.

- Traducción: Traduce el siguiente texto de [idioma de origen] a [idioma de destino]. Texto: [texto].

- Preguntas y respuestas: Usando la siguiente información, responde la pregunta [pregunta]. Información: [texto de contexto].

- Extracción de información: Extrae/Encuentra esta [informacion], en el seiguiente texto: [texto].

### Generador de prompts

[Rol] [Meta/Objetivo] [Ejemplos] [Elementos clave] [Solicita el prompt final]

Ejemplo:
"Actúa como un experto en ingeniería de prompts. Tu tarea es crear un prompt ideal para un modelo de lenguaje. El prompt que generes debe ser claro, conciso y seguir la estructura de un prompt ideal, que incluye: instrucción, contexto, rol y formato de salida. Aquí tienes un ejemplo de un buen prompt: 'Actúa como un profesor de historia. Tu tarea es explicar la Revolución Francesa a un estudiante de 10 años, usando analogías sencillas y sin jerga académica.' Ahora, crea un prompt para la tarea de [tarea]."

### Prompt de imagen

[Sujeto] [Acción] [Ambiente/Entorno] [Estilo visual] [Camara/Plano] [Iluminacion] + [Calidad]

- Camara/Plano (opcional): El tipo de encuadre de la imagen.

Ejemplo:
"Un viejo mago sabio, leyendo un antiguo tomo lleno de runas brillantes, en el rincón polvoriento de una biblioteca mágica. Pintura al óleo, estilo clásico renacentista [Estilo visual]. Un plano detalle de las manos del mago y el libro. Iluminación de una única vela parpadeante que proyecta sombras dramáticas. El resultado debe ser de alta resolución y detalle"

### Prompt de musica

[Género/Estilo] [Instrumentación] [Tono/Emoción] [Tempo/Ritmo] [Estructura] [Referencias]

- Estructura (opcional): Definir secciones como "intro", "verso", "coro", "puente" y "outro".

- Referencias (opcional): Artistas o canciones que sirvan como inspiración.

Ejemplo:
"Una pieza orquestal épica y cinematográfica, con cuerdas dramáticas y metales triunfantes. Ideal para una escena de batalla en una película, con un ritmo que comienza lento pero se va volviendo mas dinamico, toma como base la musica de Hans Zimmer"

### Prompt de video

[Sujeto principal] [Acción] [Ambiente/Entorno] [Estilo visual] [Camara/Plano] [Iluminacion] [Atmosfera/Emocion] [Calidad]

Ejemplo:
"Un astronauta, flotando sin esfuerzo, dentro de una nave espacial futurista y minimalista. Fotografía de ciencia ficción, hiperrealista. Un plano medio que hace un lento zoom hacia su rostro. Iluminación fría y suave que proviene de las consolas de control, creando una atmósfera de silencio sereno y de asombro. El video debe tener una calidad 4K"

## Diseccionando prompts

Si bien el uso o desuso de palabras puede parecernos trivial, para el modelo no lo es, cada una refleja una accion sutil pero diferente, esto puede darnos variaciones pequeñas o grandes segun el contexto.

### Personalizacion o rol

Se basa en definir un rol para que tome, usualmente profesiones, carpintero, programador, psicologo, ingeniero, etc.

"Actúa como / Actúa de", "Imagina que eres", "Responde como", "Asume el papel de", "Eres", "Experto en", "Analista de", "Mentor/Coach", "Consultor de"

### Contexto

- Para establecer la situación o el escenario:

"En este escenario", "Considera la siguiente situación", "El objetivo de esta tarea es", "Estamos trabajando en", "El trasfondo de esta solicitud es"

- Para establecer el público objetivo

"La audiencia es", "Dirígete a", "Ten en cuenta que el lector/público no tiene conocimientos de", "El tono debe ser adecuado para"

- Para establecer restricciones o limitaciones

"La respuesta debe ser", "La respuesta tiene que incluir/excluir", "No uses", "El límite de palabras es", "Evita", "Mantén un tono", "Estructura la respuesta en", "Cíñete a"

### Tarea o accion concreta

- Escribir o generar texto

"Escribe", "Genera", "Crea", "Redacta", "Desarrolla"

- Analizar o resumir información

"Analiza", "Resume", "Identifica", "Explica", "Compara"

- Restructurar o mejorar

"Reformula", "Corrige", "Mejora", "Reescribe", "Expande"

- Clasificar o categorizar

"Clasifica", "Categoriza", "Organiza"

### Formato

- Organizar en listas

"En una lista con viñetas", "En una lista numerada", "Como una lista de pros y contras", "En una lista con solo los puntos clave"

- Estructurar en tablas o cuadros

"En una tabla con las columnas", "Usa una tabla con encabezados", "Como un cuadro comparativo"

- Escribir párrafos o secciones

"En un solo párrafo", "En varios párrafos", "En secciones", "Divide la respuesta en las siguientes secciones"

- Formatos creativos o técnicos

"Como un guion de diálogo", "Como un poema/haiku", "En formato de código", "En formato de correo electrónico"

### Ejemplos

- Mostrar el formato y el estilo deseado

"Aquí tienes un ejemplo de cómo me gustaría la respuesta", "Sigue este formato para tu respuesta", "Mira este ejemplo de lo que estoy buscando", "Basado en el siguiente ejemplo, genera una respuesta similar"

- Idea de complejidad o nivel de detalle

"El ejemplo muestra el nivel de detalle que busco", "Fíjate en cómo el siguiente ejemplo aborda el tema"

- Demostrar un patrón o una relación entre datos

1. Input: [texto o dato]
2. Output: [respuesta deseada]
3. Correlacion: [A → B]
4. Ejemplo de transformación:

- Ejemplo de uso:

    Eres un corrector de estilo. Vas a corregir el tono de algunas oraciones para que suenen más formales. Corrige la siguiente oración. Mira este ejemplo de transformación:

    1. "Estaré esperando tus comentarios para ver qué onda con esto."
    2. "Aguardo sus comentarios para continuar con el proceso."

    Ahora, corrige la siguiente oración:
    "Necesitamos apurarnos para acabar el proyecto, se nos acaba el tiempo."

### Tono

- Tono Profesional / Formal

"En un tono profesional", "Adopta un tono formal y objetivo", "Utiliza un lenguaje académico y técnico", "Con un enfoque corporativo", "Mantén un tono serio y respetuoso"

- Tono Casual / Amigable

"Usa un tono conversacional y relajado", "Con un lenguaje sencillo y amigable", "Mantén un tono casual, como si hablaras con un amigo", "Sé informal y cercano", "Con un toque de humor, si es apropiado"

- Tono Empático / Sensible

"Demuestra empatía y comprensión", "Con un tono de apoyo y consolación", "Sé sensible y compasivo en tu respuesta", "Con un lenguaje que transmita calidez", "Utiliza un tono cuidadoso y considerado"

- Tono Informativo / Neutro

"Mantén un tono neutro y objetivo", "Sé conciso y directo en la información", "Utiliza un tono puramente informativo", "Evita opiniones personales y juicios", "Con un enfoque periodístico, basado en hechos"

- Tono Persuasivo / Motivacional

"Utiliza un tono persuasivo y convincente", "Con un lenguaje que inspire y motive", "Redacta de forma que animes a la acción", "Sé entusiasta y optimista", "Con un enfoque de marketing, orientado a la venta"

- Tono Creativo / Descriptivo

"Adopta un tono creativo y poético", "Usa un lenguaje vívido y descriptivo", "Con un enfoque narrativo, como si contaras una historia", "Permítete ser imaginativo y original", "Transmite una atmósfera o emoción a través de tus palabras"
