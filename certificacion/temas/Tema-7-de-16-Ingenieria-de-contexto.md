# Ingeniería de contexto

- **Seleccionar: El contexto mínimo suficiente** — Para que una inteligencia artificial resuelva bien una tarea, necesita contexto, pero más no siempre es mejor.
- **Empaquetar: Restricciones, formato y ejemplos** — Una vez seleccionado el contexto, hay que empaquetarlo de forma estructurada para que la IA entienda cómo procesarlo.
- **El contexto persistente** — Hay datos e instrucciones que no cambian en el día a día y que resulta ineficiente repetir en cada conversación con la IA.

## Seleccionar: El contexto mínimo suficiente

Para que una inteligencia artificial resuelva bien una tarea, necesita contexto, pero más no siempre es mejor. Subir decenas de reportes financieros completos o transcribir reuniones de horas suele generar ruido y contradicciones, lo que dispersa la atención de la IA. El secreto está en seleccionar el contexto mínimo suficiente. Por ejemplo, si en una PyME familiar en crecimiento se necesita que la IA redacte un correo para reclamar un pago atrasado a un cliente histórico, no sirve subir todo el historial de ventas del año. Alcanza con darle la fecha de vencimiento de la última factura, el monto adeudado y una breve indicación sobre el tono cordial que se quiere mantener para no dañar la relación comercial. Al recortar lo accesorio, la IA responde con mucha más precisión.

### Ampliación y ejemplo

Seleccionar contexto consiste en identificar qué datos permiten resolver la tarea y descartar los que no aportan a esa decisión. No significa entregar la menor cantidad posible de información a cualquier costo: si se omite una condición relevante, la respuesta puede resultar incompleta. Conviene definir primero el objetivo, listar los datos necesarios para alcanzarlo y comprobar que estén actualizados, sean comprensibles y no se contradigan entre sí.

Por ejemplo, si una empresa pide comparar el desempeño de dos sucursales durante el último trimestre, puede proporcionar las ventas de ese período, la cantidad de días que cada sucursal estuvo abierta y una nota sobre cierres excepcionales. Enviar todos los movimientos de los últimos cinco años aumentaría el volumen sin ayudar a esa comparación; omitir los días de cierre, en cambio, podría hacer que la IA interprete injustamente una diferencia de ventas. El contexto mínimo suficiente es el conjunto acotado que permite responder con fundamento.

## Empaquetar: Restricciones, formato y ejemplos

Una vez seleccionado el contexto mínimo suficiente, el siguiente paso es empaquetarlo de forma estructurada para que la IA entienda con precisión cómo procesarlo. No basta con subir un archivo y pedir un análisis libre. Necesitas establecer reglas de juego claras para que la herramienta no asuma patrones falsos o invente datos.

Un paquete de instrucciones profesional y efectivo debe estructurarse bajo tres pilares fundamentales:

- **Restricciones claras:** Establece límites estrictos sobre lo que la IA no debe hacer. Por ejemplo, prohibirle explícitamente que asuma o suponga información que no esté escrita de manera literal en los datos provistos.
- **Formato de salida:** Define con exactitud cómo quieres estructurar el resultado. Puede ser una tabla con columnas específicas, una lista de viñetas cortas, o un informe con títulos determinados.
- **Ejemplo del resultado (few-shot prompting):** Incluir un ejemplo real o ficticio de cómo debe verse la salida deseada es la forma más rápida y efectiva de alinear la respuesta de la IA con tu estándar de calidad.

Imagina que trabajas en el área de administración de una cadena de retail y necesitas procesar los reclamos de clientes en las sucursales para identificar fallas en los medios de pago. Al estructurar el contexto con restricciones, formato de salida rígido y un ejemplo de referencia, logras que la IA clasifique cientos de comentarios en segundos con un formato estandarizado, listo para copiar y pegar en tu planilla de control sin necesidad de editar nada de forma manual.

### Ampliación y ejemplo

Empaquetar el contexto es convertir una necesidad de trabajo en instrucciones que reduzcan la ambigüedad. Una tarea bien delimitada indica qué información puede usar el modelo, qué hacer cuando falten datos, qué decisiones no debe tomar y cómo debe presentar el resultado. El formato de salida también funciona como control: si se solicita una columna para la evidencia textual, será más fácil revisar por qué se asignó una categoría.

Por ejemplo, para clasificar reclamos sobre pagos, se puede pedir una tabla con las columnas `comentario`, `categoría`, `evidencia` y `requiere revisión`. Se indica que las categorías válidas son “terminal”, “tarjeta”, “transferencia” y “otro”; que no se infieran causas ausentes del comentario; y que los casos ambiguos se marquen para revisión. Un ejemplo de referencia podría mostrar que “me cobró dos veces” se clasifica como “tarjeta” solo si el comentario menciona ese medio; si no lo especifica, corresponde marcarlo como ambiguo. Así, la muestra enseña el criterio y no solo la apariencia de la respuesta.

## El contexto persistente

Hay datos e instrucciones que no cambian en el día a día y que resulta ineficiente repetir en cada conversación con la IA. Para esto sirve el contexto persistente: directrices que se configuran una sola vez en el perfil de la herramienta (a menudo llamadas instrucciones personalizadas) y que la IA aplica por defecto en todos los chats.

Para determinar qué información debe ser persistente y cuál pertenece al chat diario, aplicamos el criterio de estabilidad:

- **Información persistente:** La identidad de la organización, las normas de estilo y las restricciones regulatorias o de seguridad que nunca cambian.
- **Información del chat:** Los datos transaccionales de la semana, las planillas mensuales o las consultas específicas de un cliente.

Por ejemplo, una fintech que otorga microcréditos puede configurar su contexto persistente para que la IA adopte siempre el rol de un oficial de atención al cliente de servicios financieros, mantenga una redacción clara y, bajo ninguna circunstancia, brinde asesoramiento legal o de inversión directa.

De esta forma, cuando un analista abre un chat un lunes por la mañana para responder una duda sobre tasas de interés, no tiene que explicar todo desde cero. Simplemente introduce los datos de la consulta y la IA genera la respuesta respetando las directrices de la empresa de manera automática.

### Ampliación y ejemplo

La prueba práctica para decidir si una instrucción debe ser persistente es preguntar cuánto tiempo seguirá siendo válida y a cuántas tareas ayudará. Las pautas de tono, el público habitual, los límites de seguridad y las definiciones propias de la organización suelen mantenerse estables. En cambio, precios, saldos, fechas, nombres de clientes y políticas temporales deben proporcionarse en la conversación correspondiente, porque pueden cambiar y quedar obsoletos.

Por ejemplo, una organización puede guardar como instrucción persistente que las respuestas deben usar lenguaje claro, no prometer beneficios que no estén documentados y derivar las consultas sobre casos urgentes a una persona responsable. Para responder a una consulta puntual sobre una factura, el analista agrega el monto, la fecha y el estado actual de esa cuenta en el chat, en lugar de guardar esos datos transaccionales como una regla permanente. Las instrucciones persistentes también deben revisarse cuando cambia una política, un producto o una obligación regulatoria.
