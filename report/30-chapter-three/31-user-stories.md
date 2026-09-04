# 3. Capítulo III: Requirements Specification

## 3.1. User Stories

VitaLink construye sus historias de usuario a partir del análisis de entrevistas (ver [22-entrevistas.md](../20-chapter-two/22-entrevistas.md)) y de los dos segmentos objetivo definidos para la plataforma: **Profesionales de Salud** (médicos independientes y clínicas afiliadas) y **Familiares / Adultos Mayores** (el núcleo familiar que monitorea, y el propio adulto mayor cuando puede operar la aplicación por sí mismo). Las historias se agrupan en Epics y se documentan en tres bloques: historias de Landing Page, historias de Aplicación Web (Frontend), e historias técnicas de API RESTful (Backend), cada una con ID, título, descripción y criterios de aceptación verificables en formato Gherkin (**Given–When–Then**).

### Epics

| ID | Epic | Descripción |
|----|------|-------------|
| **EP-01** | Captación y Confianza (Landing Page) | Comunicar la propuesta de valor de VitaLink a ambos segmentos y convertir visitantes en usuarios registrados. |
| **EP-02** | Monitoreo Clínico y Gestión de Alertas | Dar a los profesionales de salud una vista operativa de sus pacientes y del ciclo de vida de cada alerta. |
| **EP-03** | Acompañamiento Familiar y Autocuidado | Permitir que familiares y adultos mayores (o su cuidador) sigan el estado de salud y actúen ante una alerta. |
| **EP-04** | Plataforma de Datos y Alertas (API) | Sostener con datos confiables y trazables el flujo Sentir → Analizar → Actuar entre wearables, backend e IA, incluyendo la evaluación de triaje, el agendamiento asistido de citas y el escalamiento de emergencia. |

> Los términos técnicos citados en esta sección (*Biometric Telemetry*, *Critical Alert*, *Vital Signs Baseline*, *Triage Assessment*, *Emergency Escalation*, *Assisted Appointment Scheduling*, *Clinical Health Record*, *Fall Incident*) siguen el glosario definido en [2.5. Ubiquitous Language](../20-chapter-two/25-ubiquitous-language.md), para mantener un vocabulario consistente entre negocio, entrevistas y las historias técnicas de este capítulo.

---

### User Stories — Landing Page (EP-01)

Ambos segmentos comparten una misma landing page con un selector de perfil (ver [4.2.5. Navigation Systems](../40-chapter-four/42-information-architecture.md)), por lo que sus historias se documentan juntas.

**US-01 · Entender la propuesta de valor en segundos**
*Como* visitante médico, *quiero* entender en segundos qué problema resuelve VitaLink, *para* decidir si me interesa conocer más.
```gherkin
Given un visitante médico que ingresa por primera vez a la landing page
When la sección Hero termina de cargar
Then el visitante ve, sin necesidad de hacer scroll, el nombre de VitaLink y una frase que resume el problema que resuelve
```

**US-02 · Confiar antes de registrar datos de pacientes**
*Como* profesional de salud, *quiero* ver una sección de privacidad/seguridad de datos, *para* confiar en registrar información de mis pacientes.
```gherkin
Given un profesional de salud navegando la landing page
When llega a la sección "Seguridad de grado médico"
Then visualiza referencias explícitas a cifrado E2E, cumplimiento HIPAA & GDPR y control de acceso (RBAC)
```

**US-03 · Solicitar información antes de registrarse**
*Como* profesional de salud, *quiero* un botón claro para "solicitar información" antes de registrarme, *para* evaluar la herramienta sin compromiso.
```gherkin
Given un profesional de salud interesado pero no convencido de registrarse
When hace clic en el botón "Solicitar información técnica"
Then se despliega un formulario de contacto que no exige crear una cuenta
```

**US-04 · Ver respaldo institucional**
*Como* profesional de salud, *quiero* ver quiénes respaldan la plataforma (clínicas/instituciones), *para* confiar en su legitimidad.
```gherkin
Given un profesional de salud en la landing page
When revisa la sección de respaldo institucional
Then encuentra logos o nombres de clínicas y médicos independientes afiliados a la red de VitaLink
```

**US-05 · Resolver dudas sin contactar a alguien**
*Como* profesional de salud, *quiero* una sección de preguntas frecuentes, *para* resolver dudas sin tener que contactar a alguien.
```gherkin
Given un profesional de salud con dudas comunes sobre la plataforma
When abre la sección de Preguntas Frecuentes (#faq)
Then encuentra respuestas agrupadas por tema, incluyendo afiliación, seguridad y facturación
```

**US-06 · Unirme como proveedor de salud**
*Como* profesional de salud, *quiero* un botón específico para "unirme como proveedor de salud", *para* iniciar mi registro directamente.
```gherkin
Given un profesional de salud decidido a afiliarse
When hace clic en "Unirme como proveedor"
Then inicia el flujo de registro institucional diferenciado del registro de familiares
```

**US-07 · Ver un ejemplo visual de una alerta**
*Como* profesional de salud, *quiero* ver un ejemplo visual simple de cómo se ve una alerta, *para* entender rápido cómo funciona el seguimiento.
```gherkin
Given un profesional de salud en la sección "Protocolo de Alerta Inteligente"
When observa el mockup ilustrativo incluido en esa sección
Then identifica visualmente el nivel de urgencia, el paciente y la acción disponible sin leer documentación adicional
```

**US-08 · Entender el beneficio sin llamadas constantes**
*Como* familiar, *quiero* entender en segundos cómo la app me ayuda a saber del estado de mi padre/madre sin llamarlo constantemente, *para* decidir si me interesa registrarme.
```gherkin
Given un familiar que ingresa por primera vez a la landing page
When la sección Hero termina de cargar
Then el familiar identifica de inmediato el beneficio de monitoreo remoto sin necesidad de llamadas frecuentes
```

**US-09 · Confiar en quién ve los datos de salud**
*Como* familiar, *quiero* ver una sección clara de privacidad que explique quién puede ver los datos de salud de mi familiar, *para* confiar en registrar su información.
```gherkin
Given un familiar evaluando si registrar a su adulto mayor
When revisa la sección de privacidad de la landing page
Then encuentra una explicación en lenguaje simple de qué roles (familiar, médico) acceden a qué datos
```

**US-10 · Conocer cómo funciona antes de crear cuenta**
*Como* familiar, *quiero* un botón para "conocer cómo funciona" antes de crear una cuenta, *para* entender el proceso sin comprometerme aún.
```gherkin
Given un familiar indeciso sobre registrarse
When hace clic en "Conocer cómo funciona"
Then accede a la explicación del flujo Sentir → Analizar → Actuar sin que se le solicite ningún dato personal
```

**US-11 · Confiar en que el sistema no depende de un aviso manual**
*Como* familiar con parientes en el extranjero o en otra ciudad, *quiero* ver que la plataforma no depende de que alguien "se acuerde de avisarme", *para* confiar en que es más segura que el método actual.
```gherkin
Given un familiar que vive lejos del adulto mayor
When lee la sección "Flujo clínico integrado"
Then comprende que las alertas se generan automáticamente a partir de datos y no de un tercero que decide avisar o no
```

**US-12 · Entender la app sin tecnicismos**
*Como* adulto mayor o su cuidador, *quiero* ver un mensaje simple (sin tecnicismos) que explique qué hace la app, *para* entender rápido si me sirve.
```gherkin
Given un adulto mayor o cuidador con baja familiaridad tecnológica
When lee el mensaje principal de la landing page
Then el texto evita jerga médica o técnica y comunica el beneficio en una sola idea
```

**US-13 · Ver qué esperar antes de registrarse**
*Como* visitante, *quiero* ver un ejemplo visual de cómo se ve una alerta o el dashboard, *para* saber qué esperar antes de registrarme.
```gherkin
Given un visitante familiar en la landing page
When llega a la sección que ilustra el dashboard
Then visualiza una captura representativa del panel familiar antes de crear una cuenta
```

**US-14 · Resolver dudas sobre el modo asistido**
*Como* familiar, *quiero* una sección de preguntas frecuentes sobre qué pasa si mi familiar no puede usar la app solo, *para* saber si aplica a mi caso (ej. modo asistido/cuidador).
```gherkin
Given un familiar cuyo adulto mayor no puede operar un smartphone
When busca en la sección FAQ el término "modo asistido"
Then encuentra una respuesta que explica cómo un cuidador puede registrar datos en su nombre
```

---

### User Stories — Aplicación Web: Profesionales de Salud (EP-02)

**US-15 · Resumen inicial de alertas pendientes**
*Como* médico, *quiero* ver un resumen inicial con la cantidad de pacientes con alertas pendientes, *para* priorizar mi atención al iniciar el día.
```gherkin
Given un médico que inicia sesión en el dashboard
When la vista principal termina de cargar
Then observa un contador de alertas pendientes agrupado por nivel de urgencia
```

**US-16 · Nivel de urgencia visual**
*Como* médico, *quiero* ver el nivel de urgencia de cada alerta de forma visual (color/etiqueta), *para* decidir rápido qué revisar primero.
```gherkin
Given una lista de alertas en el dashboard médico
When el médico observa cada fila de la lista
Then cada alerta muestra un color y una etiqueta de urgencia (ej. crítica, moderada, informativa) sin necesidad de abrir el detalle
```

**US-17 · Acceder al detalle de un paciente**
*Como* médico, *quiero* acceder al detalle de un paciente desde el resumen, *para* revisar contexto sin buscar en varias pantallas.
```gherkin
Given una alerta listada en el resumen del dashboard
When el médico hace clic sobre esa alerta
Then se abre el detalle del paciente asociado sin salir del flujo de revisión de alertas
```

**US-18 · Historial ordenado por fecha**
*Como* médico, *quiero* ver el historial de registros de un paciente ordenado por fecha, *para* entender su evolución sin papeles dispersos.
```gherkin
Given el detalle de un paciente
When el médico abre la pestaña de historial
Then los registros de signos vitales, alertas y acciones se listan en orden cronológico descendente
```

**US-19 · Marcar una alerta como revisada o atendida**
*Como* médico, *quiero* marcar una alerta como "en revisión" o "atendida", *para* que otros sepan el estado del caso.
```gherkin
Given una alerta en estado "pendiente"
When el médico selecciona la acción "Marcar en revisión" o "Marcar atendida"
Then el estado de la alerta cambia visiblemente para todos los usuarios con acceso, sin eliminar el registro original
```

**US-20 · Agregar una observación breve**
*Como* médico, *quiero* agregar una observación breve al atender una alerta, *para* dejar registro rápido de lo ocurrido.
```gherkin
Given una alerta que el médico acaba de atender
When ingresa un texto breve en el campo de observaciones y confirma
Then la observación queda asociada a la alerta y visible en el historial del paciente
```

**US-21 · Evitar revisiones duplicadas**
*Como* médico, *quiero* ver si un caso ya fue revisado por otra persona, *para* evitar duplicar esfuerzos.
```gherkin
Given una alerta que ya fue marcada "en revisión" por otro profesional
When el médico abre esa alerta
Then el sistema muestra quién la está revisando y desde cuándo, antes de permitir una nueva acción
```

**US-33 · Recibir y confirmar una cita derivada por triaje**
*Como* proveedor de salud, *quiero* recibir y confirmar solicitudes de citas pre-agendadas por el sistema ante una Alerta Crítica, *para* atender casos derivados sin gestionar yo mismo la búsqueda de cupo.
```gherkin
Given una cita pre-agendada por el motor de Agendamiento Asistido en la agenda del proveedor
When el proveedor revisa la solicitud y presiona "Confirmar disponibilidad"
Then la cita queda validada por la clínica y el familiar recibe la confirmación final
```

---

### User Stories — Aplicación Web: Familiares y Adultos Mayores (EP-03)

**US-22 · Estado general al abrir la app**
*Como* familiar, *quiero* ver un estado general simple ("todo bien" / "necesita atención") al abrir la app, *para* saber de inmediato si debo actuar.
```gherkin
Given un familiar que abre la aplicación
When la pantalla principal termina de cargar
Then observa un indicador de estado general de su adulto mayor, sin necesidad de interpretar datos crudos
```

**US-23 · Recibir una alerta comprensible**
*Como* familiar, *quiero* recibir una alerta que indique qué pasó, qué tan grave es y si ya alguien está atendiendo la situación, *para* decidir si debo intervenir.
```gherkin
Given un evento fuera de rango detectado en el adulto mayor
When se genera la alerta correspondiente
Then el familiar recibe una notificación con la causa, el nivel de gravedad y el estado de atención actual
```

**US-24 · Confirmar atención con un solo botón**
*Como* familiar, *quiero* confirmar con un solo botón que ya contacté o atendí a mi familiar, *para* que el resto de la familia sepa que el caso está cubierto.
```gherkin
Given una alerta activa recibida por el familiar
When el familiar presiona "Ya atendí este caso"
Then la alerta se marca como atendida por ese familiar y es visible para el resto de la red familiar autorizada
```

**US-25 · Historial simple sin preguntar directamente**
*Como* familiar, *quiero* ver un historial simple de días anteriores, *para* revisar el bienestar de mi familiar sin tener que preguntarle directamente.
```gherkin
Given un familiar en la vista de historial
When selecciona un rango de días anteriores
Then visualiza un resumen simplificado del estado diario, sin necesidad de interpretar valores clínicos
```

**US-26 · Ver el dato que originó una alerta**
*Como* familiar, *quiero* ver el dato específico que originó una alerta (ej. presión alta), *para* entender la gravedad real sin depender solo de una descripción genérica.
```gherkin
Given una alerta abierta por el familiar
When revisa el detalle de la alerta
Then encuentra el valor medido, el rango normal esperado y la desviación detectada
```

**US-27 · Evitar duplicar esfuerzos entre familiares**
*Como* familiar, *quiero* saber si otro miembro de la familia ya revisó o atendió una alerta, *para* no duplicar esfuerzos ni generar confusión.
```gherkin
Given una alerta ya atendida por otro familiar autorizado
When el familiar actual la abre
Then el sistema indica claramente quién la atendió y en qué momento
```

**US-28 · Mantener actualizada la red familiar**
*Como* familiar, *quiero* actualizar mis datos de contacto y ver quiénes más forman parte de la red familiar autorizada, *para* mantener la información al día.
```gherkin
Given un familiar en la sección de configuración de su perfil
When edita su número de contacto o revisa la lista de familiares autorizados
Then los cambios se guardan y son visibles para el resto de la red familiar
```

**US-32 · Confirmar una cita pre-agendada ante una alerta crítica**
*Como* familiar, *quiero* confirmar con un solo clic una cita médica pre-agendada automáticamente cuando ocurre una Alerta Crítica, *para* asegurar atención rápida sin tener que buscar disponibilidad yo mismo.
```gherkin
Given una Alerta Crítica que activó el Agendamiento Asistido de Citas y encontró un cupo disponible
When el familiar recibe el SMS de confirmación y presiona "Confirmar cita"
Then la cita queda confirmada para el adulto mayor y el proveedor de salud recibe la notificación de confirmación
```

**US-29 · Modo de uso extremadamente simple para el adulto mayor**
*Como* adulto mayor, *quiero* un modo de uso extremadamente simple (botones grandes, pocos pasos), *para* poder usarlo sin depender siempre de ayuda.
```gherkin
Given un adulto mayor operando la aplicación por sí mismo
When accede a cualquier función principal
Then la completa en un máximo de dos pasos, con botones de tamaño ampliado y texto mínimo
```

**US-30 · Pedir ayuda rápido en una urgencia**
*Como* adulto mayor, *quiero* poder avisar rápido que necesito ayuda sin tener que explicar mucho, *para* pedir asistencia en momentos de urgencia.
```gherkin
Given un adulto mayor en una situación de urgencia
When presiona el botón de ayuda rápida
Then se notifica de inmediato a su red familiar autorizada sin exigir texto adicional
```

**US-31 · Registrar datos en nombre del adulto mayor (modo asistido)**
*Como* cuidador de un adulto mayor, *quiero* poder operar el registro de datos en su lugar, *para* casos donde el adulto mayor no puede usar la tecnología por sí mismo.
```gherkin
Given un cuidador autorizado en modo asistido
When registra un evento o dato de salud en nombre del adulto mayor
Then el registro queda guardado indicando explícitamente que fue capturado por un cuidador y no por el propio adulto mayor
```

---

### Technical Stories — API RESTful (EP-04)

Las historias técnicas exponen, como endpoints RESTful, la capa **Analizar** del flujo Sentir → Analizar → Actuar. Consolidan las necesidades de datos de ambos segmentos (médicos y familiares) sobre un mismo backend, evitando endpoints duplicados por segmento.

**TS-01 · Ingesta de Telemetría Biométrica**
`POST /api/v1/events`
*Como* sistema, *quiero* registrar la Telemetría Biométrica de un wearable simulado y generar automáticamente una alerta cuando se detecte una Anomalía Fisiológica respecto a la Línea Base de Signos Vitales del paciente, *para* iniciar el flujo de atención sin depender de revisión manual.
```gherkin
Given un payload JSON con Telemetría Biométrica (frecuencia cardíaca, SpO2, acelerometría) de un paciente o adulto mayor
When el endpoint POST /api/v1/events recibe la solicitud
Then persiste el evento y, si el valor se desvía de su Línea Base de Signos Vitales, crea automáticamente una alerta con prioridad calculada; si el patrón corresponde a un Incidente de Caída o a una Anomalía Fisiológica aguda, la alerta se marca como Alerta Crítica
```

**TS-02 · Listado de alertas**
`GET /api/v1/alerts`
*Como* sistema, *quiero* exponer un listado de alertas filtrable por estado y prioridad, *para* alimentar el dashboard médico y familiar.
```gherkin
Given alertas existentes con distintos estados y prioridades
When se solicita GET /api/v1/alerts con filtros de estado y/o prioridad
Then la respuesta retorna únicamente las alertas que cumplen los filtros, ordenadas por prioridad
```

**TS-03 · Historial Clínico Digital de paciente o adulto mayor**
`GET /api/v1/patients/{id}/history`
*Como* sistema, *quiero* almacenar y exponer el Historial Clínico Digital de un paciente (telemetría, alertas, acciones), *para* permitir consultas posteriores desde el frontend médico y familiar.
```gherkin
Given un paciente con eventos, alertas y acciones registradas
When se solicita GET /api/v1/patients/{id}/history
Then la respuesta retorna el historial completo ordenado cronológicamente
```

**TS-04 · Transición de estado de una alerta**
`PATCH /api/v1/alerts/{id}`
*Como* sistema, *quiero* cambiar el estado de una alerta (pendiente/en revisión/atendida/cerrada) sin eliminarla, *para* conservar el historial completo y trazar quién y cuándo hizo el cambio.
```gherkin
Given una alerta en estado "pendiente"
When se solicita PATCH /api/v1/alerts/{id} con un nuevo estado válido
Then el estado se actualiza, se registra el usuario y la fecha del cambio, y el registro original se conserva
```

**TS-05 · Observaciones sobre una alerta**
`POST /api/v1/alerts/{id}/notes`
*Como* sistema, *quiero* registrar observaciones breves asociadas a una alerta, *para* dejar trazabilidad de lo ocurrido durante su atención.
```gherkin
Given una alerta existente
When se solicita POST /api/v1/alerts/{id}/notes con un texto de observación
Then la observación se asocia a la alerta y queda disponible en el historial del paciente
```

**TS-06 · Asociación paciente–proveedor de salud**
`POST /api/v1/patients/{id}/provider`
*Como* sistema, *quiero* asociar a cada paciente un proveedor de salud (si existe), *para* vincular la información clínica correspondiente.
```gherkin
Given un paciente sin proveedor de salud asociado
When se solicita POST /api/v1/patients/{id}/provider con el ID de un proveedor válido
Then el paciente queda vinculado a ese proveedor para futuras consultas y notificaciones
```

**TS-07 · Validación de datos mínimos**
`POST /api/v1/patients`
*Como* sistema, *quiero* validar que los datos básicos de un paciente estén completos antes de activar su seguimiento, *para* asegurar información mínima confiable.
```gherkin
Given una solicitud de registro de un nuevo paciente
When falta un dato obligatorio (ej. fecha de nacimiento o contacto de emergencia)
Then el endpoint rechaza la creación y responde con el listado de campos faltantes
```

**TS-08 · Red familiar con roles**
`POST /api/v1/elders/{id}/caregivers`
*Como* sistema, *quiero* permitir múltiples familiares autorizados por adulto mayor con roles diferenciados (principal/secundario), *para* reflejar cómo se distribuyen realmente las responsabilidades de cuidado.
```gherkin
Given un adulto mayor con un familiar principal ya registrado
When se solicita POST /api/v1/elders/{id}/caregivers con un nuevo familiar y rol "secundario"
Then el nuevo familiar queda autorizado con permisos correspondientes a su rol, sin reemplazar al familiar principal
```

**TS-09 · Registro en modo asistido**
`POST /api/v1/events` (variante con `capturedBy`)
*Como* sistema, *quiero* registrar un modo "asistido" donde un cuidador ingresa datos en nombre del adulto mayor, *para* cubrir los casos donde el usuario final no puede operar la tecnología directamente.
```gherkin
Given un cuidador autorizado en modo asistido
When registra un evento indicando el campo capturedBy=caregiver
Then el evento se guarda distinguiendo que el origen del dato fue el cuidador y no el propio adulto mayor
```

**TS-10 · Notificaciones diferenciadas por rol**
`POST /api/v1/notifications`
*Como* sistema, *quiero* enviar notificaciones diferenciadas según el destinatario (familiar vs. médico), *para* que cada uno reciba solo la información relevante a su rol.
```gherkin
Given una alerta crítica recién creada
When el servicio de notificaciones procesa los destinatarios asociados
Then el familiar recibe un mensaje orientado a la acción inmediata y el médico recibe el detalle clínico correspondiente
```

**TS-11 · Control de acceso a datos de salud (RBAC)**
`GET /api/v1/patients/{id}/access-log`
*Como* sistema, *quiero* registrar el nivel de acceso de cada usuario a los datos de salud del adulto mayor, *para* cumplir con las expectativas de privacidad expresadas por los entrevistados y con el esquema RBAC definido en [4.2.2. Labeling Systems](../40-chapter-four/42-information-architecture.md).
```gherkin
Given un usuario con rol "familiar secundario" que consulta datos de salud
When el sistema autoriza o deniega el acceso según su rol
Then la decisión y el usuario quedan registrados en el access-log del paciente
```

**TS-12 · Evaluación de Triaje**
`POST /api/v1/triage`
*Como* sistema, *quiero* calcular una Evaluación de Triaje a partir de la Telemetría Biométrica anómala y, de corresponder, de un Incidente de Caída, *para* clasificar de forma objetiva el nivel de severidad antes de decidir una acción.
```gherkin
Given una Anomalía Fisiológica detectada para un paciente
When se solicita POST /api/v1/triage con el identificador del evento
Then el sistema retorna un nivel de severidad (leve, moderado, crítico) que determina si corresponde una Alerta Crítica y un Agendamiento Asistido de Citas
```

**TS-13 · Agendamiento Asistido de Citas**
`POST /api/v1/appointments/auto-schedule`
*Como* sistema, *quiero* localizar un cupo médico disponible en un proveedor de salud cercano y pre-agendar una cita ante una Alerta Crítica, *para* reducir el tiempo entre la detección del riesgo y la atención efectiva.
```gherkin
Given una Alerta Crítica con Evaluación de Triaje de severidad alta
When el motor de Agendamiento Asistido de Citas localiza un cupo disponible en un Proveedor de Salud afiliado
Then el sistema pre-agenda la cita en estado "pendiente de confirmación" y dispara el aviso al familiar (ver TS-10) para su confirmación (ver US-32)
```

**TS-14 · Confirmación de cita pre-agendada**
`PATCH /api/v1/appointments/{id}/confirm`
*Como* sistema, *quiero* permitir que el familiar o el proveedor de salud confirmen una cita pre-agendada, *para* formalizar el Agendamiento Asistido antes de la atención.
```gherkin
Given una cita en estado "pendiente de confirmación"
When el familiar o el proveedor solicitan PATCH /api/v1/appointments/{id}/confirm
Then la cita cambia a estado "confirmada" y ambas partes quedan notificadas
```

**TS-15 · Escalamiento de Emergencia**
`POST /api/v1/alerts/{id}/escalate`
*Como* sistema, *quiero* escalar una Alerta Crítica a contactos secundarios o servicios de emergencia cuando el Cuidador Familiar principal no confirma su recepción dentro de un plazo definido, *para* evitar que una situación crítica quede sin respuesta.
```gherkin
Given una Alerta Crítica sin confirmación de recepción por parte del Cuidador Familiar principal durante 5 minutos
When el temporizador de la política de Escalamiento de Emergencia se cumple
Then el sistema notifica automáticamente a los contactos secundarios registrados y registra el escalamiento en el Historial Clínico Digital del paciente
```
