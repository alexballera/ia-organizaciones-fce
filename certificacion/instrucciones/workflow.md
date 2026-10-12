# Flujo de gestión de trámites

## 1. Recepción y clasificación del correo

Entrada del mensaje e identificación inicial del tipo de trámite mediante un agente de IA.

Para este agente, un nombre semántico y claro puede ser **Clasificador de Correos Ciudadanos**.

Te propongo la siguiente estructura para su prompt:

**Misión:** Analizar el correo entrante del vecino para categorizar el tipo de trámite y extraer datos clave.

**Instrucción de clasificación:** Clasificar cada mensaje en una de estas tres rutas acordadas:

- **Aclaración de datos:** Direcciones incompletas o errores de tipeo en DNI/nombre.
- **Reclamo técnico o de terreno:** Situaciones que requieran evaluación del área de Catastro.
- **Trámite formal:** Exenciones impositivas, compromisos de obra o fijación de plazos legales.

**Salida esperada:** Devolver la categoría asignada, el motivo de la clasificación y los datos extraídos del vecino (nombre, DNI, dirección o referencia catastral).

 Clasificador de Correos Ciudadanos:

Herramienta (tool): Claude
Herramientas permitidas (allowed_tools): Claude
Objetivo (objective): Analizar y clasificar los correos entrantes de los vecinos para encauzarlos en el circuito correspondiente.
Límites (limits): No enviar respuestas automáticas directamente al vecino ni responder promesas de condonación de deudas o resoluciones legales.
Prompt:
"Eres el agente encargado de la recepción de atención ciudadana. Tu misión es analizar el correo entrante del vecino, categorizar el tipo de trámite y extraer los datos clave.
Clasifica el mensaje en una de estas rutas:

Aclaración de datos: Direcciones incompletas o errores de tipeo en DNI o nombre.
Reclamo técnico o de terreno: Situaciones que requieran evaluación del área de Catastro.
Trámite formal: Exenciones impositivas, compromisos de obra o fijación de plazos legales.
Salida esperada: Devuelve la categoría asignada, el motivo de la clasificación y los datos extraídos del vecino (nombre, DNI, dirección o referencia catastral)."

## 2. Validación de datos catastrales

Cotejo de la dirección, entrecalle o referencia catastral contra la base de datos, con apoyo de herramientas de geolocalización. Julieta revisa los casos en bloques fijos diarios.

## 3. Búsqueda y cita de normativa vigente

Para las solicitudes que requieren fundamentación o rechazo por falta de datos, una IA consulta la legislación actual para garantizar que no se utilicen ordenanzas derogadas.

## 4. Revisión en lotes (Julieta)

Julieta valida en dos momentos del día los borradores generados. Si es un pedido simple de aclaración de datos, le da el visto bueno y sale directo.

## 5. Derivación según el tipo de caso

- **Casos complejos de terreno:** Se envían en un paquete consolidado los jueves a las 17:00 hs al área de Catastro (Ana) para inspección.
- **Exenciones, plazos o compromisos legales:** Pasan obligatoriamente a la bandeja de Micaela Cortés para su firma final autorizada antes del envío.
