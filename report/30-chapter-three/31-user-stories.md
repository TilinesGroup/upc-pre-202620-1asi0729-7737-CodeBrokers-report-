# 3. Capítulo III: Requirements Specification

## 3.1. User Stories

VitaLink construye sus historias de usuario a partir del análisis de las 6 entrevistas ya registradas (3 familiares + 3 adultos mayores, más las entrevistas del segmento clínico — ver [22-entrevistas.md](../20-chapter-two/22-entrevistas.md)) y de los dos segmentos objetivo definidos para la plataforma: **Profesionales de Salud** y **Familiares / Adultos Mayores**. Las historias se agrupan en Epics y se documentan en tres bloques: Landing Page, Aplicación Web (Frontend), y API RESTful (Backend), cada una con ID, título, descripción y criterios de aceptación verificables en formato Gherkin (**Given–When–Then**).

### Epics

| ID | Epic | Descripción |
|----|------|-------------|
| **EP-01** | Captación y Confianza (Landing Page) | Comunicar la propuesta de valor de VitaLink a ambos segmentos y convertir visitantes en usuarios registrados. |
| **EP-02** | Monitoreo Clínico y Gestión de Alertas | Dar a los profesionales de salud una vista operativa de sus pacientes y del ciclo de vida de cada alerta. |
| **EP-03** | Acompañamiento Familiar y Autocuidado | Permitir que familiares y adultos mayores sigan el estado de salud y actúen ante una alerta. |
| **EP-04** | Plataforma de Datos y Alertas (API) | Sostener con datos confiables y trazables el flujo Sentir → Analizar → Actuar entre wearables, backend e IA. |

> Los términos técnicos citados en esta sección (*Biometric Telemetry*, *Vital Signs Baseline*, *Family Caregiver*, *Clinical Health Record*) siguen el glosario definido en [2.5. Ubiquitous Language](../20-chapter-two/25-ubiquitous-language.md).

---

### User Stories — Landing Page (EP-01)

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

**US-04 · Unirme como proveedor de salud**
*Como* profesional de salud, *quiero* un botón específico para "unirme como proveedor de salud", *para* iniciar mi registro directamente.
```gherkin
Given un profesional de salud decidido a afiliarse
When hace clic en "Unirme como proveedor"
Then inicia el flujo de registro institucional diferenciado del registro de familiares
```

**US-05 · Ver un ejemplo visual de una alerta**
*Como* profesional de salud, *quiero* ver un ejemplo visual simple de cómo se ve una alerta, *para* entender rápido cómo funciona el seguimiento.
```gherkin
Given un profesional de salud en la sección "Protocolo de Alerta Inteligente"
When observa el mockup ilustrativo incluido en esa sección
Then identifica visualmente el nivel de urgencia, el paciente y la acción disponible sin leer documentación adicional
```

**US-06 · Entender el beneficio sin llamadas constantes**
*Como* familiar, *quiero* entender en segundos cómo la app me ayuda a saber del estado de mi padre/madre sin llamarlo constantemente, *para* decidir si me interesa registrarme.
```gherkin
Given un familiar que ingresa por primera vez a la landing page
When la sección Hero termina de cargar
Then el familiar identifica de inmediato el beneficio de monitoreo remoto sin necesidad de llamadas frecuentes
```

**US-07 · Confiar en quién ve los datos de salud**
*Como* familiar, *quiero* ver una sección clara de privacidad que explique quién puede ver los datos de salud de mi familiar, *para* confiar en registrar su información.
```gherkin
Given un familiar evaluando si registrar a su adulto mayor
When revisa la sección de privacidad de la landing page
Then encuentra una explicación en lenguaje simple de qué roles (familiar, médico) acceden a qué datos
```

**US-08 · Conocer cómo funciona antes de crear cuenta**
*Como* familiar, *quiero* un botón para "conocer cómo funciona" antes de crear una cuenta, *para* entender el proceso sin comprometerme aún.
```gherkin
Given un familiar indeciso sobre registrarse
When hace clic en "Conocer cómo funciona"
Then accede a la explicación del flujo Sentir → Analizar → Actuar sin que se le solicite ningún dato personal
```

**US-09 · Entender la app sin tecnicismos**
*Como* adulto mayor o su cuidador, *quiero* ver un mensaje simple (sin tecnicismos) que explique qué hace la app, *para* entender rápido si me sirve.
```gherkin
Given un adulto mayor o cuidador con baja familiaridad tecnológica
When lee el mensaje principal de la landing page
Then el texto evita jerga médica o técnica y comunica el beneficio en una sola idea
```

**US-10 · Ver qué esperar antes de registrarse**
*Como* visitante, *quiero* ver un ejemplo visual de cómo se ve una alerta o el dashboard, *para* saber qué esperar antes de registrarme.
```gherkin
Given un visitante familiar en la landing page
When llega a la sección que ilustra el dashboard
Then visualiza una captura representativa del panel familiar antes de crear una cuenta
```

---

### User Stories — Aplicación Web: Profesionales de Salud (EP-02)

**US-11 · Resumen inicial de alertas pendientes**
*Como* médico, *quiero* ver un resumen inicial con la cantidad de pacientes con alertas pendientes, *para* priorizar mi atención al iniciar el día.
```gherkin
Given un médico que inicia sesión en el dashboard
When la vista principal termina de cargar
Then observa un contador de alertas pendientes agrupado por nivel de urgencia
```

**US-12 · Nivel de urgencia visual**
*Como* médico, *quiero* ver el nivel de urgencia de cada alerta de forma visual (color/etiqueta), *para* decidir rápido qué revisar primero.
```gherkin
Given una lista de alertas en el dashboard médico
When el médico observa cada fila de la lista
Then cada alerta muestra un color y una etiqueta de urgencia sin necesidad de abrir el detalle
```

**US-13 · Acceder al detalle de un paciente**
*Como* médico, *quiero* acceder al detalle de un paciente desde el resumen, *para* revisar contexto sin buscar en varias pantallas.
```gherkin
Given una alerta listada en el resumen del dashboard
When el médico hace clic sobre esa alerta
Then se abre el detalle del paciente asociado sin salir del flujo de revisión de alertas
```

**US-14 · Historial ordenado por fecha**
*Como* médico, *quiero* ver el historial de registros de un paciente ordenado por fecha, *para* entender su evolución sin papeles dispersos.
```gherkin
Given el detalle de un paciente
When el médico abre la pestaña de historial
Then los registros se listan en orden cronológico descendente
```

**US-15 · Marcar una alerta como revisada o atendida**
*Como* médico, *quiero* marcar una alerta como "en revisión" o "atendida", *para* que otros sepan el estado del caso.
```gherkin
Given una alerta en estado "pendiente"
When el médico selecciona la acción "Marcar en revisión" o "Marcar atendida"
Then el estado de la alerta cambia visiblemente para todos los usuarios con acceso, sin eliminar el registro original
```

**US-16 · Agregar una observación breve**
*Como* médico, *quiero* agregar una observación breve al atender una alerta, *para* dejar registro rápido de lo ocurrido.
```gherkin
Given una alerta que el médico acaba de atender
When ingresa un texto breve en el campo de observaciones y confirma
Then la observación queda asociada a la alerta y visible en el historial del paciente
```

**US-17 · Evitar revisiones duplicadas**
*Como* médico, *quiero* ver si un caso ya fue revisado por otra persona, *para* evitar duplicar esfuerzos.
```gherkin
Given una alerta que ya fue marcada "en revisión" por otro profesional
When el médico abre esa alerta
Then el sistema muestra quién la está revisando y desde cuándo, antes de permitir una nueva acción
```

---

### User Stories — Aplicación Web: Familiares y Adultos Mayores (EP-03)

**US-18 · Estado general al abrir la app**
*Como* familiar y adulto mayor, *quiero* ver un estado general simple ("todo bien" / "necesita atención") al abrir la app, *para* saber de inmediato si debo actuar.
```gherkin
Given un familiar o adulto mayor que abre la aplicación
When la pantalla principal termina de cargar
Then observa un indicador de estado general, sin necesidad de interpretar datos crudos
```

**US-19 · Recibir una alerta comprensible**
*Como* familiar y adulto mayor, *quiero* recibir una alerta que indique qué pasó, qué tan grave es y si ya alguien está atendiendo la situación, *para* decidir si debo intervenir.
```gherkin
Given un evento fuera de rango detectado
When se genera la alerta correspondiente
Then el destinatario recibe una notificación con la causa, el nivel de gravedad y el estado de atención actual
```

**US-20 · Confirmar atención con un solo botón**
*Como* familiar y adulto mayor, *quiero* confirmar con un solo botón que ya contacté o atendí a mi familiar, *para* que el resto de la familia sepa que el caso está cubierto.
```gherkin
Given una alerta activa
When se presiona "Ya atendí este caso"
Then la alerta se marca como atendida por esa persona y es visible para el resto de la red familiar autorizada
```

**US-21 · Historial simple sin preguntar directamente**
*Como* familiar y adulto mayor, *quiero* ver un historial simple de días anteriores, *para* revisar el bienestar de mi familiar sin tener que preguntarle directamente.
```gherkin
Given un usuario en la vista de historial
When selecciona un rango de días anteriores
Then visualiza un resumen simplificado del estado diario, sin necesidad de interpretar valores clínicos
```

**US-22 · Ver el dato que originó una alerta**
*Como* familiar y adulto mayor, *quiero* ver el dato específico que originó una alerta (ej. presión alta), *para* entender la gravedad real sin depender solo de una descripción genérica.
```gherkin
Given una alerta abierta
When se revisa su detalle
Then se encuentra el valor medido, el rango normal esperado y la desviación detectada
```

**US-23 · Evitar duplicar esfuerzos entre familiares**
*Como* familiar y adulto mayor, *quiero* saber si otro miembro de la familia ya revisó o atendió una alerta, *para* no duplicar esfuerzos ni generar confusión.
```gherkin
Given una alerta ya atendida por otro familiar autorizado
When otro familiar la abre
Then el sistema indica claramente quién la atendió y en qué momento
```

**US-24 · Mantener actualizada la red familiar**
*Como* familiar y adulto mayor, *quiero* actualizar mis datos de contacto y ver quiénes más forman parte de la red familiar autorizada, *para* mantener la información al día.
```gherkin
Given un usuario en la sección de configuración de su perfil
When edita su número de contacto o revisa la lista de familiares autorizados
Then los cambios se guardan y son visibles para el resto de la red familiar
```

**US-25 · Modo de uso extremadamente simple**
*Como* familiar y adulto mayor, *quiero* un modo de uso extremadamente simple (botones grandes, pocos pasos), *para* poder usarlo sin depender siempre de ayuda.
```gherkin
Given un adulto mayor operando la aplicación por sí mismo
When accede a cualquier función principal
Then la completa en un máximo de dos pasos, con botones de tamaño ampliado y texto mínimo
```

**US-26 · Pedir ayuda rápido en una urgencia**
*Como* familiar y adulto mayor, *quiero* poder avisar rápido que necesito ayuda sin tener que explicar mucho, *para* pedir asistencia en momentos de urgencia.
```gherkin
Given un adulto mayor en una situación de urgencia
When presiona el botón de ayuda rápida
Then se notifica de inmediato a su red familiar autorizada sin exigir texto adicional
```

---

### Technical Stories — API RESTful (EP-04)

Las historias técnicas exponen, como endpoints RESTful, la capa **Analizar** del flujo Sentir → Analizar → Actuar. Consolidan las necesidades de datos de ambos segmentos sobre un mismo backend, evitando endpoints duplicados por segmento.

**TS-01 · Ingesta de Telemetría Biométrica**
`POST /api/v1/events`
*Como* sistema, *quiero* registrar un evento o Telemetría Biométrica capturada y generar automáticamente una alerta cuando el valor esté fuera de rango, *para* iniciar el flujo de atención sin depender de revisión manual.
```gherkin
Given un payload JSON con datos de un evento o signo vital de un paciente o adulto mayor
When el endpoint POST /api/v1/events recibe la solicitud
Then persiste el evento y, si el valor se desvía de su Línea Base de Signos Vitales, crea automáticamente una alerta con un nivel de prioridad asignado
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
*Como* sistema, *quiero* almacenar y exponer el Historial Clínico Digital de un paciente (registros, alertas, acciones), *para* permitir consultas posteriores desde el frontend médico y familiar.
```gherkin
Given un paciente con eventos, alertas y acciones registradas
When se solicita GET /api/v1/patients/{id}/history
Then la respuesta retorna el historial completo ordenado cronológicamente
```

**TS-04 · Transición de estado de una alerta**
`PATCH /api/v1/alerts/{id}`
*Como* sistema, *quiero* cambiar el estado de una alerta (pendiente/en revisión/atendida/cerrada) sin eliminarla, registrando quién la atendió y cuándo, *para* conservar el historial completo y mantener trazabilidad.
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
Given una alerta recién creada
When el servicio de notificaciones procesa los destinatarios asociados
Then el familiar recibe un mensaje orientado a la acción inmediata y el médico recibe el detalle clínico correspondiente
```

**TS-11 · Control de acceso a datos de salud (RBAC)**
`GET /api/v1/patients/{id}/access-log`
*Como* sistema, *quiero* registrar el nivel de acceso de cada usuario a los datos de salud del adulto mayor, *para* cumplir con las expectativas de privacidad expresadas por los entrevistados.
```gherkin
Given un usuario con rol "familiar secundario" que consulta datos de salud
When el sistema autoriza o deniega el acceso según su rol
Then la decisión y el usuario quedan registrados en el access-log del paciente
```
