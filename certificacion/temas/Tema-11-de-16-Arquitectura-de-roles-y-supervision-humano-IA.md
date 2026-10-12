# Arquitectura de roles y supervisión humano-IA

- **El reparto** — Para optimizar un proceso en una consultora que trabaja por proyectos, el trabajo se divide entre distintos actores según sus fortalezas.
- **La posición del humano no es binaria** — La interacción entre el humano y la IA no es de todo o nada, sino que se organiza en cuatro esquemas de supervisión.
- **Responsabilidad con dueño** — La delegación de tareas operativas en la IA no desplaza la responsabilidad profesional.

## El reparto

Para optimizar un proceso en una consultora que trabaja por proyectos, el trabajo se divide entre distintos actores según sus fortalezas. Las herramientas determinísticas, como un software de planillas, se encargan de tareas estructuradas con tolerancia cero al error, por ejemplo, calcular el desvío presupuestario de las horas facturadas. La IA generativa se utiliza para redactar el primer borrador del informe de avance del proyecto, un proceso de alto volumen pero con flexibilidad en la redacción. Por último, el consultor humano asume las tareas de baja estructura, alta ambigüedad y que requieren empatía, como la reunión con el cliente para explicar los desvíos y acordar los pasos a seguir. El reparto eficiente evita usar IA para cálculos exactos o humanos para transcripciones repetitivas, balanceando el costo, la velocidad y la sensibilidad del resultado.

Para dominar el reparto de tareas en una organización, no basta con saber que la IA redacta y Excel calcula. El diseño organizativo requiere evaluar criterios cruzados antes de asignar un nodo del proceso a un actor, especialmente en un entorno como una PyME familiar en crecimiento que busca profesionalizar su relación con proveedores.

Tomemos el caso de una empresa distribuidora de alimentos. El proceso de evaluación anual de proveedores combina datos duros de entregas con datos blandos de negociación:

- **Herramientas determinísticas:** El análisis de cumplimiento de plazos (on-time delivery) es una tarea estructurada, repetitiva y de tolerancia cero al error. Se asigna a una planilla parametrizada que cruce las fechas de las órdenes de compra con los remitos de recepción. El costo es bajo y el resultado es exacto.
- **IA generativa:** La redacción de la carta de reclamo o felicitación presenta mayor ambigüedad. La IA puede tomar la planilla de desvíos y redactar borradores adaptados al tono histórico de la relación familiar (formal pero cercano), procesando un volumen de cincuenta proveedores en segundos.
- **El profesional humano:** El criterio de reversibilidad y empatía exige que el responsable de compras revise, ajuste el tono y despache. Un error con un proveedor clave de harina puede romper una relación comercial de treinta años. La IA es excelente para estructurar ideas, pero pésima para evaluar el costo político de un adjetivo fuera de lugar.

### Ampliación y ejemplo

El reparto de tareas no se define solo por el tipo de herramienta, sino también por las características del trabajo. Para decidir quién o qué sistema debe realizar cada paso, se pueden considerar la estructura de la tarea, la tolerancia al error, la necesidad de interpretar lenguaje, el impacto de una equivocación, la posibilidad de revertirla y el costo de revisar el resultado. Una misma etapa puede combinar actores: una herramienta calcula, la IA explica patrones y una persona decide qué acción tomar.

Por ejemplo, en una consultora que prepara informes mensuales, un sistema determinístico puede sumar horas y comparar el presupuesto con lo ejecutado; la IA puede convertir las variaciones en un borrador narrativo y señalar datos que parecen inconsistentes; y el gerente de proyecto puede confirmar las causas, decidir qué comunicar y acordar medidas con el cliente. Así se aprovecha cada capacidad sin pedirle al modelo que invente explicaciones ni delegar decisiones sensibles por conveniencia.

Una asignación también debe indicar entradas, salidas y límites. Si la IA recibe una tabla, conviene especificar qué columnas puede usar, qué hacer ante valores ausentes y qué resultados requieren validación humana. Así, el reparto se vuelve un diseño operativo comprobable y no una regla simplista como “la IA redacta y la planilla calcula”.

## La posición del humano no es binaria

La interacción entre el humano y la IA no es de todo o nada, sino que se organiza en cuatro esquemas de supervisión que se adaptan según el nivel de riesgo y el impacto financiero del proceso:

- **In the loop (Humano activo):** La IA propone y el humano aprueba cada paso de forma individual. Es el esquema ideal para procesos críticos donde no hay margen de error, como la carga y autorización de órdenes de pago a proveedores clave en una distribuidora.
- **On the loop (Humano por excepción):** La IA ejecuta el proceso de forma continua y el humano interviene únicamente cuando el sistema detecta una anomalía o requiere una excepción, como en el control automático de stock de materias primas.
- **Over the loop (Humano auditor):** El profesional no revisa transacciones en tiempo real. En su lugar, realiza auditorías retrospectivas y periódicas sobre las métricas generales del sistema para validar que la IA esté clasificando de forma correcta, por ejemplo, los gastos de caja chica.
- **Out of the loop (Autonomía total):** La IA opera de manera autónoma, reservado exclusivamente para decisiones de bajísimo riesgo y alta reversibilidad, como definir el orden visual de los productos en un catálogo web.

Diseñar correctamente esta posición evita que tu equipo administrativo sufra un cuello de botella por revisiones constantes, sin perder jamás el control de la operación.

### Ampliación y ejemplo

Estos esquemas representan distintos grados de participación humana, no una escala en la que siempre convenga avanzar hacia más autonomía. La elección depende del daño posible, de cuán fácil sea detectar un error antes de que afecte a alguien, de si la decisión se puede revertir y de la capacidad real de supervisión. También puede cambiar con el tiempo: una tarea podría empezar con aprobación de cada caso y pasar a revisión por excepción solo después de demostrar un desempeño estable y contar con mecanismos para detenerla.

Por ejemplo, para ordenar productos en una tienda en línea, se puede permitir que la IA proponga cambios y que una persona apruebe cada modificación (in the loop) durante una prueba inicial. Cuando el equipo comprueba que los cambios respetan reglas comerciales, puede habilitar ajustes automáticos dentro de límites definidos y alertas para resultados atípicos (on the loop). Una auditoría periódica puede revisar métricas como ventas, disponibilidad y reclamos. Aunque el riesgo parezca bajo, los cambios deben poder revertirse y quedar registrados.

En una operación de pagos, en cambio, la autorización de cada transferencia puede requerir aprobación humana, mientras que la detección de importes inusuales puede automatizarse para priorizar la revisión. No es necesario aplicar el mismo nivel de supervisión a todas las tareas de un proceso: se puede supervisar con mayor intensidad el paso que genera el mayor riesgo y automatizar los pasos rutinarios de menor impacto.

## Responsabilidad con dueño

La delegación de tareas operativas en la IA no desplaza la responsabilidad profesional. Cuando incorporamos herramientas digitales en una organización, es vital comprender que delegar la ejecución técnica no exime de responsabilidad al profesional que firma o autoriza el trabajo.

Imaginemos que en el área de administración y finanzas de nuestra PyME utilizamos un asistente de IA para elaborar el informe de flujo de fondos (cash flow) para presentar ante el directorio. La IA se encarga de consolidar las planillas de ingresos y egresos enviadas por las sucursales y redactar las conclusiones. Si la IA comete una inconsistencia grave, por ejemplo, interpretar un cobro extraordinario único como un ingreso operativo recurrente, distorsionará la proyección de liquidez de los próximos meses.

Ante el directorio, el responsable de esa distorsión es el analista que presentó el informe, no la tecnología. La IA operó como un procesador de datos de alta velocidad, pero la validación de las premisas financieras y la verificación de consistencia corresponden exclusivamente al juicio crítico del profesional.

### Ampliación y ejemplo

Para que la responsabilidad no quede difusa, cada etapa debe tener una persona o un rol responsable de revisar y aprobar el resultado, además de saber qué parte produjo la herramienta. La supervisión no consiste en aceptar todo lo que devuelve la IA ni en comprobar cada palabra sin criterio: debe enfocarse en los datos de origen, los supuestos utilizados, los cálculos relevantes, las excepciones y las consecuencias de la decisión. Cuando el resultado no puede verificarse con la información disponible, debe quedar pendiente de revisión en vez de presentarse como confirmado.

Por ejemplo, antes de presentar una proyección de caja, el analista puede cotejar los totales del informe con las planillas originales, comprobar que los ingresos extraordinarios estén identificados por separado y revisar los supuestos de fechas de cobro y pago. Otra persona puede validar los movimientos de mayor impacto. El informe puede conservar un registro de las fuentes, los cambios realizados y las verificaciones, de modo que sea posible explicar cómo se llegó a las cifras.

La organización también debe definir quién puede aprobar el uso del sistema, quién atiende los errores, cómo se documentan las correcciones y cuándo se suspende la automatización. Estas medidas hacen posible aprender de los fallos y mantener trazabilidad; no sustituyen las obligaciones profesionales, regulatorias o legales que correspondan en cada contexto.
