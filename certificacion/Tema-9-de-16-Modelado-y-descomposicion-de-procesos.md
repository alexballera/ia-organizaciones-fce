# Modelado y descomposición de procesos

- **Del objetivo a las piezas** — Para automatizar o mejorar un proceso con inteligencia artificial, primero hay que desarmarlo en sus componentes básicos.
- **Lo invisible** — Los procesos reales rara vez siguen el manual a rajatabla.
- **La granularidad justa** — Modelar un proceso requiere encontrar el equilibrio justo entre un mapa demasiado general y uno exageradamente detallado.

## Del objetivo a las piezas

Para automatizar o mejorar un proceso con inteligencia artificial, primero hay que desarmarlo en sus componentes básicos.

Un objetivo no es una actividad y una tarea no es una decisión. En una cooperativa agropecuaria, el objetivo de "liquidar las ventas de granos de los asociados" no es una sola acción. Al desglosarlo, aparecen tareas concretas como la descarga de cartas de porte y el cotejo de pesajes.

También surgen decisiones clave, como determinar si la calidad del grano entregado requiere aplicar un descuento según la tolerancia de la normativa. Los actores (el recepcionista del acopio y el analista de administración) usan recursos específicos como las planillas de excel y el sistema de gestión. Sin este mapa de piezas, es imposible saber qué parte delegar a un modelo de lenguaje y qué decisión debe seguir bajo estricto control humano.

Para operar con inteligencia artificial sin cometer errores costosos, debemos entender que un proceso no es una masa homogénea de trabajo. En una consultora que realiza estudios de mercado para empresas de consumo masivo, el objetivo general de entregar un reporte sectorial se compone de elementos con naturalezas totalmente distintas.

### Desglosando las piezas del proceso

- **Tareas:** Son actividades procedimentales, como descargar las bases de datos de precios de los competidores o unificar los formatos de las planillas.
- **Decisiones:** Implican evaluar alternativas bajo ciertos criterios, por ejemplo, determinar si un desvío de precios en un canal de venta es una anomalía de carga o un cambio real de estrategia comercial.
- **Actores:** Los analistas junior que recopilan la información y los directores de cuenta que validan las conclusiones.
- **Recursos:** Las bases de datos externas y el software de análisis.
- **Dependencias:** No se puede redactar el análisis de tendencias sin la consolidación de datos previa.

Cuando una organización decide incorporar inteligencia artificial, el error más común es intentar automatizar el objetivo completo en lugar de intervenir las piezas correctas. Un modelo de lenguaje puede ser excelente para redactar el borrador inicial de las conclusiones basados en los datos ya procesados (tarea), o para proponer hipótesis de por qué bajaron las ventas en una región (recurso de apoyo para una decisión). Sin embargo, la decisión final de validar si esa hipótesis es correcta para el cliente sigue siendo responsabilidad del director de cuenta, el actor humano.

### Ampliación y ejemplo

Descomponer un proceso permite distinguir actividades repetibles, decisiones que requieren criterios, responsables, herramientas y relaciones de dependencia. Para cada paso es útil registrar qué lo inicia, qué información recibe, qué transformación realiza, qué resultado produce y quién lo valida. Con ese mapa se pueden localizar tareas candidatas para asistencia automatizada sin confundirlas con el objetivo final ni transferir automáticamente la responsabilidad de una decisión.

Por ejemplo, para gestionar la devolución de un producto, el objetivo es resolver el caso del cliente. Entre las piezas pueden aparecer recibir el reclamo, identificar la compra, comprobar el plazo de devolución, verificar el estado del producto, decidir si corresponde una excepción y comunicar la resolución. La IA puede ayudar a extraer los datos de la solicitud o preparar un borrador de respuesta; la decisión sobre una excepción puede seguir a cargo del responsable definido por la política. El desglose hace visibles tanto las oportunidades como los límites de la automatización.

## Lo invisible en los procesos

Los procesos reales rara vez siguen el manual de procedimientos a rajatabla. Siempre existen caminos informales por donde entra la información y lugares clave donde se pierde. En el área de recursos humanos de una empresa de servicios, por ejemplo, el proceso oficial de selección puede dictar que todos los currículums deben cargarse en una plataforma centralizada.

Sin embargo, en el día a día ocurre algo muy distinto. Muchos gerentes envían candidatos directamente por mensajes de WhatsApp al selector, creando un canal paralelo invisible. Además, surgen excepciones no escritas, como el adelanto de entrevistas para perfiles muy demandados. Estos desvíos y los cuellos de botella reales (como la demora del gerente en dar feedback sobre un candidato) suelen estar ocultos para la dirección.

Si decides entrenar una herramienta de inteligencia artificial ignorando esta informalidad, el sistema fallará. La IA procesará datos incompletos o rechazará candidatos válidos simplemente porque la realidad de la oficina no coincide con el procedimiento oficial del manual.

### Ampliación y ejemplo

Para descubrir el proceso real, no alcanza con leer el procedimiento escrito. Conviene contrastarlo con entrevistas a quienes ejecutan y reciben el trabajo, observar una muestra de casos y revisar los registros disponibles. Las excepciones, los pasos que se repiten, las esperas, los datos que se corrigen fuera del sistema y los canales alternativos pueden revelar diferencias importantes entre el proceso diseñado y el proceso cotidiano. El objetivo no es legitimar toda práctica informal, sino entenderla antes de cambiarla.

Por ejemplo, el procedimiento de compras puede indicar que todas las solicitudes se ingresan en una plataforma, pero los equipos avisan por mensajería cuando necesitan reponer un insumo de manera urgente. Si ese aviso informal no se registra luego en el sistema, una IA que pronostique la demanda solo con los pedidos oficiales subestimará el consumo. Mapear ambas vías permite decidir si se deben integrar, formalizar o tratar como excepciones, además de establecer cómo se protegerán los datos personales que aparezcan en esos canales.

## La granularidad justa

Modelar un proceso requiere encontrar el equilibrio justo entre un mapa demasiado general y uno exageradamente detallado. Un organigrama de alto nivel no sirve para intervenir porque no muestra cómo viajan los datos. Por otro lado, registrar cada clic del mouse o cada movimiento del teclado resulta impracticable y paraliza el análisis.

El modelo es útil cuando permite identificar los puntos exactos de intervención de la inteligencia artificial. En una fintech que procesa solicitudes de microcréditos, por ejemplo, describir el paso como "evaluar riesgo crediticio" es una definición muy vaga. Por el contrario, describirlo como "escribir la fórmula en la celda B14 de la planilla" es demasiado fino.

La granularidad justa consiste en definir el paso en un nivel intermedio de procesamiento de información. En este caso, el paso correcto sería "extracción de datos del recibo de sueldo presentado por el cliente". Este nivel de detalle te permite ver con claridad que puedes automatizar esa lectura de texto específica con un modelo de lenguaje, sin perderte en los detalles físicos del software.

### Ampliación y ejemplo

Un paso está descrito con suficiente granularidad cuando se entiende qué información entra, qué resultado se espera y cómo se puede comprobar si el paso se realizó bien. Una descripción demasiado general oculta actividades diferentes y no permite asignar responsabilidades ni medir errores. Una descripción excesivamente minuciosa hace que el mapa sea costoso de mantener y distrae del análisis del trabajo y de los datos.

Por ejemplo, en el procesamiento de facturas, “administrar cuentas por pagar” es demasiado amplio para decidir qué automatizar. “Hacer clic en el botón de carga” describe una acción de interfaz que puede cambiar cuando se actualiza el software. “Extraer de cada factura el proveedor, la fecha, el importe y el número de documento, y marcar los campos ilegibles” define una unidad más útil: tiene una entrada identificable, un resultado verificable y una excepción que puede derivarse a revisión humana. Ese nivel permite probar una herramienta y medir la precisión campo por campo.
