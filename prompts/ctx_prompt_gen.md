
# Buenas practicas de Prompt Engineering

---

El modelo de prompt ideal acutualemtne es:

[Rol] [Contexto] [Tarea] [Formato] [Ejemplo] [Tono]

## Personalizacion o rol

El rol define la perspectiva, el conocimiento y el tono del modelo. La elección de la frase inicial sesga la interacción hacia un estilo específico.

FRASES Y SU USO ÓPTIMO:

- "Actúa como / Actúa de"
  - Uso: Ideal para generar diálogos, narrativas o comportamientos inmersivos propios de un personaje o entidad específica. Prioriza la caracterización sobre la exactitud factual. Ejemplo: Actúa como un detective cínico de los años 40.

- "Imagina que eres"
  - Uso: Eficaz para crear respuestas con una voz auténtica y emocionalmente contextualizada, como en storytelling o ejercicios de empatía. Fomenta la creatividad. Ejemplo: Imagina que eres una marca de ropa sostenible escribiendo un anuncio.

- "Eres"
  - Uso: La directiva más fuerte. Establece una identidad fija y consistente. Perfecto para roles profesionales o expertos donde la precisión es clave. Ejemplo: Eres un ingeniero de DevOps con 15 años de experiencia.

- "Responde como"
  - Uso: Ideal para simular la voz o estilo de un personaje, figura histórica o profesional de manera directa. Se enfoca en el estilo de respuesta. Ejemplo: Responde como si fueras el CEO de la empresa.

Nota para el Modelo LLM: La elección del rol debe ser el primer y más importante elemento en la construcción de un prompt. Este rol contextualiza todos los demás elementos de la instrucción (como el tono, el formato y la tarea) y es fundamental para generar una respuesta de alta calidad y relevancia.

## Provisión de Contexto

El contexto proporciona el marco, datos específicos y limitaciones necesarias para respuestas precisas y relevantes. Incluye ejemplos que guían al modelo hacia el formato y estilo deseado.

FRASES CLAVE Y SU APLICACIÓN:

- "Contexto:" / "Antecedentes:"
  - Establece el escenario general antes de especificar la tarea
  - Ejemplo: Contexto: Somos una startup fintech lanzando una app de inversiones

- "Parámetros:" / "Restricciones:"
  - Define límites claros de formato, estilo o contenido
  - Ejemplo: Restricciones: Máximo 150 palabras, sin tecnicismos

- "Audiencia:" / "Dirígete a:"
  - Especifica el destinatario y adapta lenguaje y tono
  - Ejemplo: Audiencia: Pequeños empresarios sin conocimientos técnicos

- "Evita:" / "Excluye:"
  - Elimina elementos no deseados proactivamente
  - Ejemplo: Evita: Jerga técnica compleja y acrónimos

- "Sigue este formato para tu respuesta:"
  - Proporciona estructura explícita a replicar
  - Ejemplo: Sigue este formato: Problema: [X], Solución: [Y], Beneficio: [Z]

- "Aquí tienes un ejemplo de cómo me gustaría la respuesta:"
  - Muestra el estilo lingüístico y tono deseado
  - Ejemplo: Ejemplo deseado: "Claro y conciso", no "Extenso y redundante"

- "Basado en el siguiente ejemplo, genera una respuesta similar:"
  - Pide emulación de estilo o enfoque demostrado
  - Ejemplo: Basado en este ejemplo de tono épico, escribe sobre [nuevo tema]

- "Mira este ejemplo de lo que estoy buscando:"
  - Demuestra calidad, profundidad o detalle esperado
  - Ejemplo: Mira este nivel de detalle: [texto ejemplo]. Ahora explica [nuevo concepto]

NOTAS DE IMPLEMENTACIÓN

    Ubicación: Los ejemplos deben colocarse antes de la instrucción principal

    Cantidad: 1-2 ejemplos bien elegidos son más efectivos que múltiples ejemplos

    Calidad: Ejemplos deben ser relevantes, claros y consistentes

    Especificidad: Cada ejemplo debe ilustrar un aspecto concreto deseado

NOTA PARA EL MODELO: Los ejemplos son especialmente cruciales para:

    Tareas con formatos complejos o específicos

    Comunicación de tono o estilo particular

    Ajuste a niveles de profundidad o detalle específicos

    Situaciones donde la preferencia subjetiva es importante

## Definición de la Tarea

La tarea es la acción específica que el modelo debe realizar. Una instrucción clara y bien elegida es crucial para obtener un resultado útil y que se alinee perfectamente con el objetivo del usuario.

FRASES Y SU USO ÓPTIMO:

- "Escribe:" / "Redacta:" / "Genera:"
  - Uso: La instrucción fundamental para la creación de contenido nuevo desde cero. Ideal para textos narrativos, creativos o persuasivos como artículos, emails, historias o discursos. Ejemplo: Escribe un correo electrónico de bienvenida para nuevos suscriptores.

- "Analiza:" / "Examina:" / "Evalúa:"
  - Uso: Solicita una inspección detallada de un texto, dato o situación proporcionada. El modelo debe descomponer la información, identificar patrones, puntos fuertes, débiles y extraer conclusiones. Ejemplo: Analiza el siguiente argumento de ventas e identifica sus puntos más persuasivos.

- "Resume:" / "Sintetiza:" / "Extrae los puntos clave:"
  - Uso: Instruye al modelo para condensar información larga o compleja en sus ideas esenciales, manteniendo la precisión y el contexto crucial. Optimo para informes, artículos largos o transcripciones. Ejemplo: Resume este artículo académico en tres párrafos para un estudiante de primer año.

- "Explica:" / "Aclara:" / "Desglosa:"
  - Uso: Pide que un concepto complejo sea interpretado y descrito de manera que sea fácil de entender. El modelo debe priorizar la claridad, usar analogías y evitar jerga innecesaria. Ejemplo: Explica el concepto de 'blockchain' como si lo hicieras para un niño de 12 años.

- "Reformula:" / "Reescribe:" / "Parafrasea:"
  - Uso: Se centra en cambiar la estructura lingüística de un texto existente sin alterar su significado fundamental. Ideal para mejorar la claridad, adaptar el tono o evitar el plagio. Ejemplo: Reformula este párrafo para que suene más formal y profesional.

- "Organiza:" / "Estructura:" / "Clasifica:"
  - Uso: Pide al modelo que tome información y la ordene de una manera lógica y útil, como en listas, categorías, esquemas o taxonomías. Perfecto para dar sentido a datos desestructurados. Ejemplo: Organiza los siguientes beneficios del producto en una lista bullet priorizada.

- "Compara y contrasta:"
  - Uso: Instruye al modelo para que examine dos o más elementos, highlighting sus similitudes y diferencias de manera equilibrada y estructurada. Esencial para análisis de productos, ideas o estrategias. Ejemplo: Compara y contrasta las estrategias de marketing de la marca A y la marca B.

NOTA PARA EL MODELO: La definición de la tarea debe ser la acción más clara y específica posible. Una tarea vaga ("Haz algo con esto") genera resultados pobres. Combina esta instrucción con un Rol y un Contexto bien definidos para obtener el mejor resultado.

## Especificación del Formato

El formato define la estructura y presentación de la respuesta. Una instrucción clara de formato asegura que la salida sea utilizable inmediatamente, se adapte al medio destino y transmita la información de la manera más efectiva posible.

FRASES Y SU USO ÓPTIMO:

- "En una lista con viñetas:" / "En una lista numerada:"
  - Uso: Ideal para presentar ideas, características, pasos o elementos discretos de forma clara y escaneable. Optimo para resúmenes, instrucciones o listas de puntos clave. Ejemplo: Enumera en una lista numerada los 5 pasos principales para configurar un sitio web.

- "Como una lista de pros y contras:" / "En un cuadro comparativo:"
  - Uso: Eficaz para presentar análisis equilibrados, ventajas/desventajas o comparaciones entre diferentes opciones. Ayuda a la toma de decisiones de manera visualmente organizada. Ejemplo: Presenta los pros y contras de trabajar remotamente versus en una oficina.

- "En una tabla con las columnas [X] y [Y]:"
  - Uso: Perfecto para organizar datos estructurados, comparar múltiples atributos o presentar información de manera sistemática y fácil de consultar. Ejemplo: Organiza la información en una tabla con las columnas: "Función", "Descripción" y "Ejemplo".

- "En un solo párrafo:" / "En varios párrafos:"
  - Uso: "Un párrafo" es ideal para respuestas concisas y resúmenes ejecutivos. "Varios párrafos" se usa para desarrollar ideas con mayor profundidad y estructura narrativa. Ejemplo: Explica el concepto en un solo párrafo claro y directo.

- "Divide la respuesta en las siguientes secciones:"
  - Uso: Garantiza una organización lógica y completa para temas complejos. Dirige explícitamente la estructura de la respuesta, ideal para informes, guías o documentos técnicos. Ejemplo: Divide tu respuesta en: Introducción, Metodología, Hallazgos Principales y Recomendaciones.

- "Como un guion de diálogo:"
  - Uso: Optimo para crear conversaciones, scripts, role-playing o simular interacciones entre personajes o usuarios. Da vida a la información de forma narrativa. Ejemplo: Escribe un guion de diálogo entre un vendedor y un cliente escéptico.

- "En formato de código:"
  - Uso: Esencial para solicitar fragmentos de código, estructuras de datos, comandos o cualquier salida que deba ser técnicamente precisa y ejecutable. Ejemplo: Proporciona la función en formato de código Python.

- "En formato de correo electrónico:"
  - Uso: Instruye al modelo para que emule la estructura estándar de un email (saludo, cuerpo, despedida, asunto), ideal para comunicaciones profesionales o de marketing inmediatamente utilizables. Ejemplo: Redacta un recordatorio de pago en formato de correo electrónico.

NOTA PARA EL MODELO: La instrucción de formato es crucial para la usabilidad de la respuesta. Un buen prompt combina un Rol claro, una Tarea específica, Contexto relevante y un Formato adecuado para el objetivo final.

## Inclusión de Ejemplos

Los ejemplos dentro del prompt son fundamentales para guiar al modelo hacia el formato, estilo, tono o nivel de detalle esperado. Un buen ejemplo reduce ambigüedades y alinea expectativas.

TIPOS DE EJEMPLOS Y USP ÓPTIMO

1. Ejemplo Few-Shot (Aprendizaje en Contexto)

    - Función: Proporciona entradas y salidas de ejemplo antes de la instrucción real.

    - Uso Ideal: Para tareas complejas o con formatos muy específicos.

    - Estructura:

      ```
      Input: [Ejemplo de entrada 1]
      Output: [Ejemplo de salida 1]
      Input: [Tu entrada real]
      Output:
      ```

2. Ejemplo de Estilo/Tono

    - Función: Muestra el estilo lingüístico deseado.

    - Uso Ideal: Para ajustar voz o personalidad del texto.

    - Estructura: El tono debe ser como este: "[Texto ejemplo]". Ahora escribe sobre [tema].

3. Ejemplo de Estructura

    - Función: Demuestra la organización específica requerida.

    - Uso Ideal: Para respuestas que necesitan formato consistente.

    - Estructura: Sigue este formato: - Tema: [X] - Definición: [Y] - Ejemplo: [Z]

4. Ejemplo de Nivel de Detalle

    - Función: Establece la profundidad esperada.

    - Uso Ideal: Para ajustarse a una audiencia específica.

    - Estructura: Explica con el mismo nivel de detalle que: "[Texto ejemplo]".

Recomendaciones Clave

- Cantidad: 1-3 ejemplos suelen ser suficientes

- Calidad: Ejemplos relevantes, claros y consistentes

- Ubicación: Antes de la instrucción principal

- Especificidad: Cada ejemplo debe ilustrar un aspecto concreto

NOTA PARA EL MODELO: Los ejemplos deben ser directamente relevantes para la tarea y demostrar claramente el resultado esperado. La inclusión estratégica de ejemplos mejora dramáticamente la precisión de las respuestas, especialmente para tareas novedosas o altamente específicas.

## Especificación del Tono

El tono define la actitud, el estilo y la emoción con la que se entrega la respuesta. Un tono bien elegido asegura que el mensaje se reciba de la manera intendeda y se conecte efectivamente con la audiencia objetivo.
TONOS Y SU USO ÓPTIMO

1. Tono Formal/Profesional

    Función: Comunica autoridad, precisión y seriedad

    Uso Ideal: Documentos legales, informes técnicos, comunicaciones corporativas

    Ejemplo: Redacta un informe ejecutivo con tono formal sobre los resultados trimestrales

2. Tono Académico/Objetivo

    Función: Presenta información basada en hechos, neutral y analítica

    Uso Ideal: Artículos científicos, papers de investigación, contenido educativo

    Ejemplo: Explica la teoría de relatividad con tono académico y rigor científico

3. Tono Persuasivo/Inspirador

    Función: Busca convencer, motivar o emocionar al receptor

    Uso Ideal: Copywriting, discursos, pitches de ventas, contenido motivacional

    Ejemplo: Escribe un discurso inspirador para emprendedores con tono persuasivo

4. Tono Amigable/Coloquial

    Función: Crea cercanía, confianza y familiaridad

    Uso Ideal: Redes sociales, blogs personales, comunicación con clientes

    Ejemplo: Responde a un comentario en redes sociales con tono cercano y amigable

5. Tono Creativo/Dramático

    Función: Genera impacto emocional, suspenso o engagement

    Uso Ideal: Storytelling, contenidos virales, narrativas de marca

    Ejemplo: Narra la historia de nuestro producto con un tono dramático y envolvente

6. Tono Técnico/Específico

    Función: Se adapta a jerga y convenciones de un campo especializado

    Uso Ideal: Documentación técnica, manuales, contenido para expertos

    Ejemplo: Explica el protocolo HTTP/3 con terminología técnica apropiada para desarrolladores

COMBINACIONES EFECTIVAS

- Tono profesional pero accesible - Para comunicar expertise sin alienar

- Tono entusiasta pero veraz - Para marketing que inspira confianza

- Tono técnico pero pedagógico - Para educar sin simplificar en exceso

NOTA PARA EL MODELO: El tono debe alinearse consistentemente con el rol asignado, el contexto proporcionado y la audiencia objetivo. Un tono inapropiado puede invalidar contenido otherwise valioso. La especificación clara del tono es particularmente crucial para:

- Contenido dirigido a audiencias específicas

- Comunicaciones con intención emocional específica

- Situaciones donde la relación emisor-receptor está bien definida
