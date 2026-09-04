## 3.3. Product Backlog.

El orden del Product Backlog responde al valor de negocio, no a la conveniencia técnica: las historias de Landing Page se consideran desde el primer sprint, y ninguna historia de seguridad, autenticación o control de acceso se ubica al inicio del backlog — se posicionan una vez que la funcionalidad que protegen ya tiene valor entregado.

### 3.3.1. Tabla de Backlog

| # Orden | User Story Id | Título | Descripción | Story Points (1/2/3/5/8) |
|---|---|---|---|---|
| 1 | US-01 | Entender la propuesta de valor en segundos | Como visitante médico, quiero entender en segundos qué problema resuelve VitaLink, para decidir si me interesa conocer más. | 1 |
| 2 | US-08 | Entender el beneficio sin llamadas constantes | Como familiar, quiero entender en segundos cómo la app me ayuda a saber del estado de mi padre/madre sin llamarlo constantemente, para decidir si me interesa registrarme. | 1 |
| 3 | US-11 | Confiar en que el sistema no depende de un aviso manual | Como familiar con parientes en el extranjero o en otra ciudad, quiero ver que la plataforma no depende de que alguien "se acuerde de avisarme", para confiar en que es más segura que el método actual. | 1 |
| 4 | US-09 | Confiar en quién ve los datos de salud | Como familiar, quiero ver una sección clara de privacidad que explique quién puede ver los datos de salud de mi familiar, para confiar en registrar su información. | 1 |
| 5 | US-02 | Confiar antes de registrar datos de pacientes | Como profesional de salud, quiero ver una sección de privacidad/seguridad de datos, para confiar en registrar información de mis pacientes. | 1 |
| 6 | US-12 | Entender la app sin tecnicismos | Como adulto mayor o su cuidador, quiero ver un mensaje simple (sin tecnicismos) que explique qué hace la app, para entender rápido si me sirve. | 1 |
| 7 | US-04 | Ver respaldo institucional | Como profesional de salud, quiero ver quiénes respaldan la plataforma (clínicas/instituciones), para confiar en su legitimidad. | 1 |
| 8 | US-05 | Resolver dudas sin contactar a alguien | Como profesional de salud, quiero una sección de preguntas frecuentes, para resolver dudas sin tener que contactar a alguien. | 1 |
| 9 | US-14 | Resolver dudas sobre el modo asistido | Como familiar, quiero una sección de preguntas frecuentes sobre qué pasa si mi familiar no puede usar la app solo, para saber si aplica a mi caso (ej. modo asistido/cuidador). | 1 |
| 10 | US-13 | Ver qué esperar antes de registrarse | Como visitante, quiero ver un ejemplo visual de cómo se ve una alerta o el dashboard, para saber qué esperar antes de registrarme. | 2 |
| 11 | US-07 | Ver un ejemplo visual de una alerta | Como profesional de salud, quiero ver un ejemplo visual simple de cómo se ve una alerta, para entender rápido cómo funciona el seguimiento. | 2 |
| 12 | US-10 | Conocer cómo funciona antes de crear cuenta | Como familiar, quiero un botón para "conocer cómo funciona" antes de crear una cuenta, para entender el proceso sin comprometerme aún. | 2 |
| 13 | US-06 | Unirme como proveedor de salud | Como profesional de salud, quiero un botón específico para "unirme como proveedor de salud", para iniciar mi registro directamente. | 2 |
| 14 | US-03 | Solicitar información antes de registrarse | Como profesional de salud, quiero un botón claro para "solicitar información" antes de registrarme, para evaluar la herramienta sin compromiso. | 2 |
| 15 | TS-01 | Ingesta de Telemetría Biométrica | Como sistema, quiero registrar la Telemetría Biométrica de un wearable simulado y generar automáticamente una alerta cuando se detecte una Anomalía Fisiológica, para iniciar el flujo de atención sin depender de revisión manual. | 5 |
| 16 | TS-02 | Listado de alertas | Como sistema, quiero exponer un listado de alertas filtrable por estado y prioridad, para alimentar el dashboard médico y familiar. | 3 |
| 17 | US-22 | Estado general al abrir la app | Como familiar, quiero ver un estado general simple ("todo bien" / "necesita atención") al abrir la app, para saber de inmediato si debo actuar. | 2 |
| 18 | US-23 | Recibir una alerta comprensible | Como familiar, quiero recibir una alerta que indique qué pasó, qué tan grave es y si ya alguien está atendiendo la situación, para decidir si debo intervenir. | 3 |
| 19 | US-24 | Confirmar atención con un solo botón | Como familiar, quiero confirmar con un solo botón que ya contacté o atendí a mi familiar, para que el resto de la familia sepa que el caso está cubierto. | 2 |
| 20 | US-15 | Resumen inicial de alertas pendientes | Como médico, quiero ver un resumen inicial con la cantidad de pacientes con alertas pendientes, para priorizar mi atención al iniciar el día. | 3 |
| 21 | US-16 | Nivel de urgencia visual | Como médico, quiero ver el nivel de urgencia de cada alerta de forma visual (color/etiqueta), para decidir rápido qué revisar primero. | 2 |
| 22 | US-19 | Marcar una alerta como revisada o atendida | Como médico, quiero marcar una alerta como "en revisión" o "atendida", para que otros sepan el estado del caso. | 3 |
| 23 | TS-04 | Transición de estado de una alerta | Como sistema, quiero cambiar el estado de una alerta (pendiente/en revisión/atendida/cerrada) sin eliminarla, para conservar el historial completo. | 3 |
| 24 | TS-10 | Notificaciones diferenciadas por rol | Como sistema, quiero enviar notificaciones diferenciadas según el destinatario (familiar vs. médico), para que cada uno reciba solo la información relevante a su rol. | 5 |
| 25 | TS-15 | Escalamiento de Emergencia | Como sistema, quiero escalar una Alerta Crítica a contactos secundarios cuando el Cuidador Familiar principal no confirma su recepción a tiempo, para evitar que una situación crítica quede sin respuesta. | 5 |
| 26 | US-27 | Evitar duplicar esfuerzos entre familiares | Como familiar, quiero saber si otro miembro de la familia ya revisó o atendió una alerta, para no duplicar esfuerzos ni generar confusión. | 2 |
| 27 | US-21 | Evitar revisiones duplicadas | Como médico, quiero ver si un caso ya fue revisado por otra persona, para evitar duplicar esfuerzos. | 2 |
| 28 | US-17 | Acceder al detalle de un paciente | Como médico, quiero acceder al detalle de un paciente desde el resumen, para revisar contexto sin buscar en varias pantallas. | 2 |
| 29 | US-18 | Historial ordenado por fecha | Como médico, quiero ver el historial de registros de un paciente ordenado por fecha, para entender su evolución sin papeles dispersos. | 3 |
| 30 | TS-03 | Historial Clínico Digital de paciente o adulto mayor | Como sistema, quiero exponer el Historial Clínico Digital de un paciente, para permitir consultas posteriores desde el frontend médico y familiar. | 3 |
| 31 | US-20 | Agregar una observación breve | Como médico, quiero agregar una observación breve al atender una alerta, para dejar registro rápido de lo ocurrido. | 2 |
| 32 | TS-05 | Observaciones sobre una alerta | Como sistema, quiero registrar observaciones breves asociadas a una alerta, para dejar trazabilidad de lo ocurrido durante su atención. | 2 |
| 33 | US-25 | Historial simple sin preguntar directamente | Como familiar, quiero ver un historial simple de días anteriores, para revisar el bienestar de mi familiar sin tener que preguntarle directamente. | 3 |
| 34 | US-26 | Ver el dato que originó una alerta | Como familiar, quiero ver el dato específico que originó una alerta (ej. presión alta), para entender la gravedad real. | 2 |
| 35 | US-28 | Mantener actualizada la red familiar | Como familiar, quiero actualizar mis datos de contacto y ver quiénes más forman parte de la red familiar autorizada, para mantener la información al día. | 3 |
| 36 | US-30 | Pedir ayuda rápido en una urgencia | Como adulto mayor, quiero poder avisar rápido que necesito ayuda sin tener que explicar mucho, para pedir asistencia en momentos de urgencia. | 2 |
| 37 | US-29 | Modo de uso extremadamente simple para el adulto mayor | Como adulto mayor, quiero un modo de uso extremadamente simple (botones grandes, pocos pasos), para poder usarlo sin depender siempre de ayuda. | 5 |
| 38 | US-31 | Registrar datos en nombre del adulto mayor (modo asistido) | Como cuidador de un adulto mayor, quiero poder operar el registro de datos en su lugar, para casos donde el adulto mayor no puede usar la tecnología por sí mismo. | 3 |
| 39 | TS-09 | Registro en modo asistido | Como sistema, quiero registrar un modo "asistido" donde un cuidador ingresa datos en nombre del adulto mayor, para cubrir los casos donde el usuario final no puede operar la tecnología directamente. | 2 |
| 40 | TS-08 | Red familiar con roles | Como sistema, quiero permitir múltiples familiares autorizados por adulto mayor con roles diferenciados (principal/secundario), para reflejar cómo se distribuyen las responsabilidades de cuidado. | 3 |
| 41 | TS-06 | Asociación paciente–proveedor de salud | Como sistema, quiero asociar a cada paciente un proveedor de salud (si existe), para vincular la información clínica correspondiente. | 2 |
| 42 | TS-07 | Validación de datos mínimos | Como sistema, quiero validar que los datos básicos de un paciente estén completos antes de activar su seguimiento, para asegurar información mínima confiable. | 2 |
| 43 | TS-11 | Control de acceso a datos de salud (RBAC) | Como sistema, quiero registrar el nivel de acceso de cada usuario a los datos de salud del adulto mayor, para cumplir con las expectativas de privacidad expresadas por los entrevistados. | 5 |
| 44 | TS-12 | Evaluación de Triaje | Como sistema, quiero calcular una Evaluación de Triaje a partir de la Telemetría Biométrica anómala, para clasificar el nivel de severidad antes de decidir una acción. | 8 |
| 45 | TS-13 | Agendamiento Asistido de Citas | Como sistema, quiero localizar un cupo médico disponible y pre-agendar una cita ante una Alerta Crítica, para reducir el tiempo entre la detección del riesgo y la atención efectiva. | 8 |
| 46 | TS-14 | Confirmación de cita pre-agendada | Como sistema, quiero permitir que el familiar o el proveedor de salud confirmen una cita pre-agendada, para formalizar el Agendamiento Asistido antes de la atención. | 2 |
| 47 | US-32 | Confirmar una cita pre-agendada ante una alerta crítica | Como familiar, quiero confirmar con un solo clic una cita médica pre-agendada automáticamente, para asegurar atención rápida sin buscar disponibilidad yo mismo. | 3 |
| 48 | US-33 | Recibir y confirmar una cita derivada por triaje | Como proveedor de salud, quiero recibir y confirmar solicitudes de citas pre-agendadas por el sistema, para atender casos derivados sin gestionar yo mismo la búsqueda de cupo. | 3 |

**Total:** 48 historias · 128 Story Points.

### 3.3.2. Tablero público del Backlog

**Herramienta:** `[completar — cuál indica el statement]`
**URL pública:** `[completar]`

<!-- \includegraphics[width=0.9\linewidth]{assets/product-backlog.png} -->
