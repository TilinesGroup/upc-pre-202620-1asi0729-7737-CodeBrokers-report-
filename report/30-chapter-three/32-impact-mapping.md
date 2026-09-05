## 3.2. Impact Mapping

El Impact Mapping de VitaLink parte de los objetivos de negocio del piloto (**WHY**), identifica a los actores que pueden ayudar o impedir alcanzarlos (**WHO**), define el cambio de comportamiento que se espera de cada uno (**HOW**) y lo conecta con los entregables concretos del producto (**WHAT**). Los actores se construyen a partir del análisis de las 6 entrevistas ya registradas ([2.2.3. Análisis de entrevistas](../20-chapter-two/22-entrevistas.md)) y los entregables referencian directamente los Epics y Stories definidos en [3.1. User Stories](31-user-stories.md).

> **Nota de consistencia:** las tres personas descritas en esta sección se basan en los hallazgos de las entrevistas ya registradas y quedan disponibles para reutilizarse en [2.3.1. User Personas](../20-chapter-two/23-needfinding.md) cuando esa sección se complete, evitando definir personas contradictorias entre capítulos.

### User Personas (WHO)

**Persona 1 — Dra. Jimena, Profesional de Salud**
* **Rol:** Médica tratante en centro de salud, con alta carga de pacientes.
* **Contexto actual:** Usa el sistema institucional y papeles dispersos; solo conoce el estado de un paciente en la consulta presencial.
* **Frustración clave:** *"No cuento con seguimiento remoto ni información en tiempo real; me entero de las complicaciones recién en la siguiente cita o ante una emergencia grave."*
* **Objetivo:** Visualizar de un vistazo qué casos son urgentes, sin que eso le tome tiempo adicional a su jornada.

**Persona 2 — Samir, Familiar Cuidador**
* **Rol:** Hijo y soporte principal del cuidado de su madre adulta mayor, coordina con hermanos.
* **Contexto actual:** Llama 2-3 veces al día para verificar que todo esté bien; se entera de los problemas por terceros o por su propia madre, cuando el problema ya ocurrió.
* **Frustración clave:** *"Priorizo que la plataforma garantice la privacidad y protección de los datos de mi madre"* — junto con la culpa y fatiga de coordinar todo manualmente con sus hermanos.
* **Objetivo:** Saber de inmediato si todo está en orden y registrar que ya atendió una situación con un solo botón.

**Persona 3 — Doña Rosa, Adulta Mayor**
* **Rol:** Adulta mayor monitoreada, con baja familiaridad tecnológica.
* **Contexto actual:** Su bienestar hoy se verifica solo mediante llamadas telefónicas esporádicas de su familia.
* **Frustración clave:** Necesita poder pedir ayuda en una urgencia sin depender de que alguien la llame primero, y le preocupa quién puede ver sus datos de salud.
* **Objetivo:** Mantener su independencia el mayor tiempo posible, con una forma simple de avisar cuando algo no está bien.

---

### Business Goal 1 (WHY): Validar la reducción del tiempo de respuesta familiar

> **SMART:** Lograr que el **70%** de los familiares que completen el registro en el piloto confirmen al menos una alerta dentro de las **2 semanas** posteriores a su registro, para validar que VitaLink reduce el tiempo de respuesta ante una situación de riesgo del adulto mayor frente al método actual (llamadas esporádicas).

| WHO (Actor) | HOW (Impact) | WHAT (Deliverables) |
|---|---|---|
| Samir (Familiar Cuidador) | Deja de depender de llamadas esporádicas y revisa la app al recibir una notificación, confirmando la atención en un solo paso | US-06, US-18, US-19, US-20, US-23, TS-10 |
| Doña Rosa (Adulta Mayor) | Registra (o permite que su cuidador registre) sus datos de forma consistente, generando telemetría suficiente para detectar anomalías reales | US-25, US-26, TS-01, TS-09 |
| Sistema VitaLink | Notifica con la causa, gravedad y estado de atención de cada alerta sin intervención manual | TS-02, TS-10 |

---

### Business Goal 2 (WHY): Validar el canal de afiliación de proveedores de salud

> **SMART:** Afiliar a **5 proveedores de salud** (clínicas o médicos independientes) a la red de VitaLink dentro de los primeros **3 meses** del piloto, para validar la viabilidad del canal de adquisición B2B (ver [2.1.2. Estrategia 3](../20-chapter-two/21-competidores.md)).

| WHO (Actor) | HOW (Impact) | WHAT (Deliverables) |
|---|---|---|
| Dra. Jimena (Profesional de Salud) | Se registra como proveedor a través de la landing page | US-04, TS-06 |
| Sistema VitaLink | Vincula al proveedor con los pacientes que lo seleccionan, sin gestión manual de la asociación | TS-06 |

---

### Business Goal 3 (WHY): Validar la confianza en el manejo de datos de salud

> **SMART:** Lograr que el **90%** de los familiares encuestados califiquen con **4 o 5 (sobre 5)** su confianza en el manejo de los datos de salud de su adulto mayor durante el **primer mes** de uso del piloto, respondiendo directamente al hallazgo de entrevistas donde el 100% de los profesionales y el 66% de los familiares exigió transparencia sobre quién accede a la información (ver [2.2.3. Análisis de entrevistas](../20-chapter-two/22-entrevistas.md)).

| WHO (Actor) | HOW (Impact) | WHAT (Deliverables) |
|---|---|---|
| Samir (Familiar Cuidador) | Revisa la sección de privacidad antes de registrar a su madre y entiende quién ve cada dato | US-02, US-07, TS-11 |
| Dra. Jimena (Profesional de Salud) | Confía en registrar información de pacientes porque el acceso queda auditado por rol | US-02, TS-11 |
| Sistema VitaLink | Registra y expone el nivel de acceso (RBAC) de cada usuario a los datos de salud, sin excepciones silenciosas | TS-11 |

---

### Trazabilidad Goals → Epics

| Business Goal | Epics relacionados (3.1) |
|---|---|
| G1. Reducción del tiempo de respuesta familiar | EP-01, EP-03, EP-04 |
| G2. Afiliación de proveedores de salud | EP-01, EP-02, EP-04 |
| G3. Confianza en el manejo de datos | EP-01, EP-02, EP-03, EP-04 |
