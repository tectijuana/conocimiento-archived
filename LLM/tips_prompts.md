| #Principio | Principio de Instrucción para Prompts |
|------------|---------------------------------------|
| 1          | No es necesario ser cortés con LLM por lo que no es necesario añadir frases como "por favor", "si no te importa", "gracias", "me gustaría", etc., y ser directo al punto. |
| 2          | Integrar la audiencia prevista en el prompt, por ejemplo, la audiencia es un experto en el campo. |
| 3          | Desglosar tareas complejas en una secuencia de prompts más simples en una conversación interactiva. |
| 4          | Emplear directivas afirmativas como 'haz', mientras se evita el lenguaje negativo como 'no hagas'. |
| 5          | Cuando necesites aclarar o profundizar en la comprensión de un tema, idea o cualquier pieza de información, utiliza los siguientes prompts: o Explicar [inserta tema específico] en términos simples. o Explícame como si tuviera 11 años. o Explícame como si fuera un principiante en [campo]. o Escribe el [ensayo/texto/párrafo] usando un inglés simple como si estuvieras explicando algo a un niño de 5 años. |
| 6          | Añade "Voy a intentar x cosa para una mejor solución". |
| 7          | Implementar el uso del prompt de ejemplo impulsado (Usar "Ejemplo de prompt"). |
| 8          | Cuando formatees tu prompt, comienza con '###Instruction###', seguido por '###Example###' si es relevante. Posteriormente, preguntas, contexto, y datos de entrada. Usa una o más líneas '###Question###' si es relevante. Subsecuentemente, preguntas, contexto, y datos de entrada. |
| 9          | Incorporar a los siguientes frases: "Tus tareas" y "DEBES" y "DEBES HACER". |
| 10         | Incorporar las siguientes frases: "Serás penalizado". |
| 11         | Usa la frase "Responder a una pregunta en un estilo humano". |
| 12         | Utiliza palabras guía como "paso a paso". |
| 13         | Al añadir tu prompt la siguiente frase "Asegúrate que tu respuesta es imparcial y no se basa en estereotipos". |
| 14         | Permitir al modelo elegir detalles y requisitos precisos desde ti preguntando preguntas que él tiene derecho a saber. |
| 15         | Para indagar acerca de un tema o artículo específico o para examinar y probar tu entendimiento, puedes usar la frase: "Enséñame la [teoría/norma/regla] de [tema] y no incluyas una respuesta al final, pero dime si obtuve la respuesta correcta cuando responda". |
| 16         | Asignar un rol a los modelos de lenguaje grandes. |
| 17         | Utiliza Delimitadores. |
| 18         | Repite una palabra o frase específica múltiples veces dentro de un prompt. |
| 19         | Combinar Cadena-de-Pensamiento (CoT) con el flujo de estilo de pensamiento. |
| 20         | Utiliza prompts de salida, los cuales concluyen tu prompt con el comienzo del resultado deseado. Utiliza resultados de salida terminando tu prompt con la parte inicial de la respuesta deseada. |
| 21         | Para escribir un ensayo/texto/párrafo/artículo o cualquier tipo de texto que deba ser detallado: "Escribe un ensayo/texto detallado [tema] en [tema] basado en toda la información necesaria". |
| 22         | Para corregir/cambiar el texto específico sin cambiar su estilo: "Intenta revisar cada oración enviada por los usuarios. Deberías intentar mejorar la gramática y el vocabulario del usuario y asegúrate de que suena natural. No deberías cambiar el estilo de escritura, como cambiar un párrafo casual a uno formal". |
| 23         | Cuando tengas una tarea compleja de codificación que pueda ser en diferentes archivos: "Desde ahora en adelante y cada vez que generes código que abarque más de un archivo, genera un [lenguaje de programación] script que se pueda ejecutar automáticamente para ejecutar