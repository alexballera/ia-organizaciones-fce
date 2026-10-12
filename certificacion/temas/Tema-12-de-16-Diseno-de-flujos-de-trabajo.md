# Diseño de flujos de trabajo

- **La secuencia: el mapa del recorrido** — La secuencia es la estructura que define el camino de los datos de un extremo al otro del proceso.
- **Los controles: salvaguardas del proceso** — Un flujo de trabajo sin controles es una automatización esperando su incidente, ya que la inteligencia artificial puede cometer errores de lectura o interpretación.
- **Sin pasos mágicos: consistencia y depuración** — Un flujo de trabajo falla cuando se asume que un nodo recibirá información que nadie le envió realmente, lo que se conoce como un paso mágico.

## La secuencia: el mapa del recorrido

La secuencia es la estructura que define el camino de los datos de un extremo al otro del proceso. Para armarla se utiliza un lienzo conceptual de nodos y conexiones, sin necesidad de programar código. Todo comienza con un disparador, que es el evento que activa el flujo. A partir de allí, los datos avanzan a través de condiciones y bifurcaciones que determinan qué camino seguir. Por ejemplo, en el área de administración y finanzas de una empresa mediana, la recepción de una factura digital en un correo electrónico específico actúa como disparador. El sistema de inteligencia artificial extrae los datos clave y, mediante una bifurcación condicional, verifica el monto: si el total es menor a quinientos mil pesos, el flujo dirige el documento a registro automático; si supera ese límite, la secuencia desvía el caso hacia una carpeta de revisión manual.

Imagina que estás en una PyME familiar en crecimiento que distribuye alimentos y decide automatizar la gestión de reclamos de clientes por mercadería fallada o faltante. Para que esto funcione sin código, debemos mapear tres elementos clave en nuestro lienzo conceptual: el disparador, las condiciones y las bifurcaciones.

- **El disparador:** Es el evento inicial. En este caso, ocurre cuando un cliente envía un mensaje de WhatsApp con la foto del remito firmado y el detalle del problema.
- **La extracción:** La inteligencia artificial procesa el mensaje y la imagen, convirtiendo esos datos desestructurados en información clara: número de cliente, artículo y cantidad.
- **Las condiciones y bifurcaciones:** El flujo no es lineal, es un árbol de decisiones. La primera bifurcación valida la identidad: ¿existe el cliente en la base de datos? Si no existe, el flujo deriva el caso a soporte manual. Si existe, pasa a la siguiente condición sobre el monto: si el reclamo es menor a cincuenta mil pesos, se genera una nota de crédito automática; si supera ese monto, se desvía para la validación de un supervisor.

Este diseño visual te permite ver exactamente dónde actúa la tecnología y dónde interviene el criterio humano.

### Ampliación y ejemplo

Diseñar una secuencia implica especificar qué inicia el flujo, qué datos recibe cada etapa, qué transformación realiza y cuál es el resultado que entrega al siguiente paso. Una secuencia clara contempla tanto el camino normal como las alternativas: información incompleta, documentos ilegibles, datos que no coinciden y servicios que no están disponibles. Si no se define qué ocurre en esas situaciones, el flujo puede detenerse sin aviso o continuar con datos incorrectos.

Por ejemplo, en el reclamo por mercadería faltante, la secuencia puede ser: recibir el mensaje, identificar al cliente, extraer el número de remito y los productos reclamados, contrastarlos con la entrega registrada, decidir si la diferencia está dentro de los criterios aprobados y, por último, generar una respuesta o derivar el caso. Si la imagen del remito no permite leer el número, el flujo debe pedir una nueva imagen o enviar el caso a una persona, en lugar de inventar o inferir el dato.

Cada bifurcación debe basarse en una condición observable y definida. “Reclamo de bajo riesgo” es ambiguo si no se explica cómo se determina; “importe menor al límite aprobado y coincidencia entre cliente y remito” puede verificarse. Para evaluar el diseño, se puede recorrer el diagrama con casos normales y excepcionales y comprobar que cada uno tenga una salida prevista.

## Los controles: salvaguardas del proceso

Un flujo de trabajo sin controles es una automatización esperando su incidente. En el diseño de flujos, la inteligencia artificial procesa grandes volúmenes de datos con rapidez, pero carece de sentido común. Por eso, un diseño profesional requiere establecer paradas obligatorias para la supervisión humana, la gestión de excepciones y el cierre formal.

Imagina que estás en una cooperativa agropecuaria que implementa un flujo asistido por IA para gestionar las solicitudes de prórroga en los plazos de pago de insumos que hacen los productores asociados. La IA recibe los correos, analiza el historial crediticio del productor, revisa las condiciones climáticas de su zona y redacta una propuesta de nuevo plan de pagos.

Para que este proceso sea seguro, diseñamos cuatro tipos de controles clave:

- **Aprobación obligatoria:** La IA no envía la propuesta directamente. El documento queda en el panel de control de un analista de créditos, quien debe validar y firmar digitalmente la propuesta antes de que sea despachada.
- **Escalamiento de lo anómalo:** Si el sistema detecta que la solicitud excede el 70% del cupo de crédito histórico o hay inconsistencias en las firmas, el flujo se detiene de inmediato y el caso se deriva a la gerencia de finanzas.
- **Registro y cierre:** Cada vez que el analista aprueba o modifica la propuesta, el sistema registra quién realizó el cambio y a qué hora. El cierre del flujo ocurre únicamente cuando el productor firma la conformidad y el sistema contable se actualiza automáticamente.

Para entender la verdadera profundidad de una secuencia, analicemos un caso de negocio donde el diseño teórico falló al enfrentarse a la realidad operativa.

Imagina que estás en una PyME dedicada a la distribución de alimentos que implementa un flujo automatizado para el análisis de presupuestos de proveedores de fletes. El disparador ocurre cuando un transportista envía una propuesta tarifaria en PDF por correo electrónico. La IA lee el documento, extrae el costo por kilómetro y actualiza una planilla comparativa. La condición establecida es simple: si la tarifa propuesta es menor o igual al promedio actual del mercado, el flujo envía un correo automático de aceptación del presupuesto. Si es mayor, se desvía a una carpeta de negociación.

El problema surgió cuando un proveedor extranjero envió sus tarifas en dólares estadounidenses, mientras que la base de datos de la PyME estaba expresada en pesos. Al no tener una condición que validara la moneda de origen, la IA interpretó un valor de 2 dólares por kilómetro como si fueran 2 pesos. El sistema consideró que la tarifa era extraordinariamente baja, cumplió la condición y envió automáticamente el correo de aceptación, comprometiendo comercialmente a la empresa bajo condiciones erróneas.

Para solucionar este fallo, se rediseñó la secuencia agregando nodos de control de datos y bifurcaciones de seguridad antes del procesamiento de la condición de negocio. La primera bifurcación nueva analiza la variable de la moneda: si detecta dólares, el flujo activa un nodo intermedio que consulta el tipo de cambio oficial del día en una base de datos financiera y realiza la conversión a pesos antes de pasar a la etapa de comparación.

### Ampliación y ejemplo

Los controles son puntos de verificación que reducen la probabilidad o el impacto de un error. Pueden actuar antes de procesar (validar que el archivo sea del tipo esperado), durante el flujo (detener un valor fuera de rango) o antes de cerrar una operación (pedir aprobación). También deben existir controles de excepción, trazabilidad y recuperación: el sistema debe registrar qué ocurrió y permitir corregir o revertir acciones cuando sea posible.

En el ejemplo de las tarifas de flete, además de verificar la moneda, se puede comprobar que la tarifa incluya unidad de medida, vigencia, ruta y costos adicionales. Si falta la moneda o no se puede obtener un tipo de cambio confiable, el flujo no debería aceptar la oferta ni asumir una equivalencia; debe dejarla pendiente y solicitar revisión. La aprobación humana se reserva para las condiciones comerciales definidas por la empresa, mientras que el registro conserva el documento recibido, los datos extraídos y la decisión tomada.

Un cuarto control útil es la validación de datos antes de ejecutar la regla de negocio: por ejemplo, comprobar que el importe sea numérico, la moneda pertenezca a una lista admitida y la fecha de vigencia no haya vencido. Los controles deben probarse con casos límite y errores intencionales, no solo con ejemplos ideales. También conviene monitorear cuántos casos se derivan a revisión, cuántas alertas son falsas y cuántas operaciones deben corregirse, para ajustar el flujo sin eliminar salvaguardas necesarias.

## Sin pasos mágicos: consistencia y depuración

Un paso mágico ocurre cuando diseñamos un proceso asumiendo que un nodo tiene información o capacidades que en realidad nadie le entregó en el paso anterior. Es el equivalente a pedirle a un colaborador que prepare un informe financiero sin darle acceso al sistema contable. Para evitar esto, cada transferencia de datos en un flujo de trabajo que integra IA debe ser explícita.

Imagina una empresa mediana que importa y exporta componentes electrónicos y decide optimizar el proceso de atención de reclamos de aduana mediante un flujo automatizado. En el diseño inicial, el equipo plantea que la IA redactará una carta de descargo formal en formato PDF dirigida al organismo aduanero explicando los motivos de la demora en la presentación de una declaración de importación.

Sin embargo, este diseño contiene un paso mágico flagrante: el flujo le pide a la IA que redacte la carta de descargo, pero en ninguna de las etapas previas se le ha provisto al sistema el número de despacho de importación, la fecha de ingreso de la mercadería ni el código de la infracción notificada.

Para que el proceso funcione sin interrupciones, el diseño debe modificarse agregando un paso de transferencia explícita de datos:

1. La IA primero debe recibir el PDF de la notificación de la aduana y extraer de allí los identificadores clave.
2. Luego, cruza esa información mediante una consulta al sistema de gestión interna para traer los datos del despacho.
3. Finalmente, con todos esos insumos cargados en su memoria de contexto, procede a la redacción del borrador.

### Ampliación y ejemplo

Para evitar pasos mágicos, cada nodo debe tener entradas identificables y una salida esperada. En la práctica, esto significa especificar qué campo produce cada etapa, de qué sistema proviene, en qué formato se transmite y qué ocurre si está vacío o no puede validarse. También es importante confirmar que el nodo siguiente tenga permiso y capacidad para acceder a esa información; mencionar un dato en una instrucción no equivale a proporcionarlo ni garantiza que el sistema pueda consultarlo.

Por ejemplo, un flujo que redacta una respuesta a un reclamo puede necesitar el identificador del cliente, el número de pedido, el producto, el motivo y la política de devolución aplicable. El nodo de extracción obtiene algunos campos del mensaje; una consulta al sistema de ventas recupera el pedido; otra consulta aporta la política vigente. Si el identificador no coincide con un registro, el flujo debe detenerse y pedir revisión. No debe completar los campos faltantes con una suposición presentada como un hecho.

La depuración consiste en recorrer el flujo paso a paso y revisar las entradas y salidas reales de cada nodo. Se puede probar con un caso completo, otro con un dato ausente, uno con formato inesperado y uno que active una bifurcación. Al observar en qué punto desaparece un campo, cambia su formato o deja de estar disponible, se puede corregir la transferencia concreta en lugar de modificar instrucciones generales a ciegas. Un registro de ejecución facilita repetir la prueba y confirmar que la corrección resolvió el problema.
