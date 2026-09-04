## 3.3. Product Backlog.

El Product Backlog consolida las historias definidas en [3.1. User Stories](31-user-stories.md), estimadas en Story Points (escala de Fibonacci: 1/2/3/5/8) y priorizadas según el valor de negocio que aportan a los tres Business Goals definidos en [3.2. Impact Mapping](32-impact-mapping.md):

* **G1** — Reducción del tiempo de respuesta familiar (70% de familiares confirman una alerta en 2 semanas).
* **G2** — Afiliación de proveedores de salud (5 proveedores en 3 meses).
* **G3** — Confianza en el manejo de datos de salud (90% califica 4-5/5 en el primer mes).

La prioridad usa la escala **MoSCoW**: **Must** (bloquea directamente el ciclo de validación de al menos un Business Goal en esta primera entrega), **Should** (soporta el objetivo pero no es indispensable para medirlo) y **Could** (aporta valor pero puede entregarse después sin invalidar la medición del piloto).

### 3.3.1. Tabla de Backlog

| ID | Historia | Epic | Story Points | Prioridad | Responde a |
|---|---|---|---|---|---|
| US-01 | Entender la propuesta de valor en segundos (médico) | EP-01 | 1 | Must | G2 |
| US-02 | Confiar antes de registrar datos de pacientes | EP-01 | 1 | Must | G3 |
| US-03 | Solicitar información antes de registrarse | EP-01 | 2 | Should | G2 |
| US-04 | Ver respaldo institucional | EP-01 | 1 | Should | G2 |
| US-05 | Resolver dudas sin contactar a alguien (FAQ médico) | EP-01 | 1 | Should | G2 |
| US-06 | Unirme como proveedor de salud | EP-01 | 2 | Must | G2 |
| US-07 | Ver un ejemplo visual de una alerta | EP-01 | 2 | Should | G2 |
| US-08 | Entender el beneficio sin llamadas constantes | EP-01 | 1 | Must | G1 |
| US-09 | Confiar en quién ve los datos de salud | EP-01 | 1 | Must | G3 |
| US-10 | Conocer cómo funciona antes de crear cuenta | EP-01 | 2 | Should | G1 |
| US-11 | Confiar en que el sistema no depende de un aviso manual | EP-01 | 1 | Must | G1 |
| US-12 | Entender la app sin tecnicismos | EP-01 | 1 | Should | G1 |
| US-13 | Ver qué esperar antes de registrarse | EP-01 | 2 | Should | G1 |
| US-14 | Resolver dudas sobre el modo asistido | EP-01 | 1 | Should | G1 |
| US-15 | Resumen inicial de alertas pendientes | EP-02 | 3 | Must | G1 |
| US-16 | Nivel de urgencia visual | EP-02 | 2 | Must | G1 |
| US-17 | Acceder al detalle de un paciente | EP-02 | 2 | Should | G1 |
| US-18 | Historial ordenado por fecha | EP-02 | 3 | Should | G3 |
| US-19 | Marcar una alerta como revisada o atendida | EP-02 | 3 | Must | G1 |
| US-20 | Agregar una observación breve | EP-02 | 2 | Should | G3 |
| US-21 | Evitar revisiones duplicadas | EP-02 | 2 | Should | G1 |
| US-33 | Recibir y confirmar una cita derivada por triaje | EP-02 | 3 | Could | G2 |
| US-22 | Estado general al abrir la app | EP-03 | 2 | Must | G1 |
| US-23 | Recibir una alerta comprensible | EP-03 | 3 | Must | G1 |
| US-24 | Confirmar atención con un solo botón | EP-03 | 2 | Must | G1 |
| US-25 | Historial simple sin preguntar directamente | EP-03 | 3 | Should | G3 |
| US-26 | Ver el dato que originó una alerta | EP-03 | 2 | Should | G3 |
| US-27 | Evitar duplicar esfuerzos entre familiares | EP-03 | 2 | Must | G1 |
| US-28 | Mantener actualizada la red familiar | EP-03 | 3 | Should | G1 |
| US-29 | Modo de uso extremadamente simple para el adulto mayor | EP-03 | 5 | Should | G1 |
| US-30 | Pedir ayuda rápido en una urgencia | EP-03 | 2 | Must | G1 |
| US-31 | Registrar datos en nombre del adulto mayor (modo asistido) | EP-03 | 3 | Should | G1 |
| US-32 | Confirmar una cita pre-agendada ante una alerta crítica | EP-03 | 3 | Could | G2 |
| TS-01 | Ingesta de Telemetría Biométrica | EP-04 | 5 | Must | G1 |
| TS-02 | Listado de alertas | EP-04 | 3 | Must | G1 |
| TS-03 | Historial Clínico Digital de paciente o adulto mayor | EP-04 | 3 | Should | G3 |
| TS-04 | Transición de estado de una alerta | EP-04 | 3 | Must | G1 |
| TS-05 | Observaciones sobre una alerta | EP-04 | 2 | Should | G3 |
| TS-06 | Asociación paciente–proveedor de salud | EP-04 | 2 | Should | G2 |
| TS-07 | Validación de datos mínimos | EP-04 | 2 | Should | G3 |
| TS-08 | Red familiar con roles | EP-04 | 3 | Should | G1 |
| TS-09 | Registro en modo asistido | EP-04 | 2 | Should | G1 |
| TS-10 | Notificaciones diferenciadas por rol | EP-04 | 5 | Must | G1 |
| TS-11 | Control de acceso a datos de salud (RBAC) | EP-04 | 5 | Must | G3 |
| TS-12 | Evaluación de Triaje | EP-04 | 8 | Could | G2 |
| TS-13 | Agendamiento Asistido de Citas | EP-04 | 8 | Could | G2 |
| TS-14 | Confirmación de cita pre-agendada | EP-04 | 2 | Could | G2 |
| TS-15 | Escalamiento de Emergencia | EP-04 | 5 | Must | G1 |

**Total del backlog:** 48 historias · 128 Story Points.

### 3.3.2. Criterio de priorización

Los ítems **Could** (US-32, US-33, TS-12, TS-13, TS-14) concentran el flujo de Agendamiento Asistido de Citas, que sirve a **G2** — un objetivo con ventana de validación de 3 meses, más amplia que la de G1 y G3 (2 y 4 semanas respectivamente). Al mismo tiempo son los ítems de mayor esfuerzo del backlog (8 puntos cada uno los dos motores principales), por lo que priorizarlos después de asegurar el ciclo Sentir → Analizar → Actuar básico (Must) reduce el riesgo de la primera entrega sin invalidar la medición de ningún Business Goal.

Los ítems **Must** cubren, de manera mínima, un ciclo completo y demostrable: un familiar y un médico entienden la propuesta de valor (US-01, US-08), el sistema captura telemetría y genera una alerta (TS-01), la muestra priorizada (TS-02), el familiar la confirma en un clic (US-24) o el médico la marca atendida (US-19), y si nadie responde el sistema escala (TS-15) — todo bajo un control de acceso auditable (TS-11).

### 3.3.3. Tablero público del Backlog

> **[PENDIENTE — acción manual del equipo, no delegable a este borrador]**
>
> La rúbrica pide una **URL pública** y una **captura** del backlog. Esta tabla (3.3.1) está lista para copiarse/pegarse en un tablero público; recomendado usar **GitHub Projects** ya que el equipo ya trabaja con la organización `TilinesGroup` (cero herramientas nuevas que aprender):
>
> 1. En la organización de GitHub, ir a **Projects → New project → Board**.
> 2. Crear una columna por estado (`Backlog`, `Sprint actual`, `En progreso`, `Hecho`) y una vista de tabla con columnas `Story Points` y `Prioridad`.
> 3. Cargar las 48 filas de 3.3.1 (se puede pegar como CSV/tabla directamente en la vista de tabla de Projects).
> 4. Poner el proyecto en visibilidad **pública**, copiar la URL y pegarla aquí.
> 5. Tomar una captura de pantalla del tablero completo y guardarla en `assets/product-backlog.png`, luego referenciarla con:
>    `\includegraphics[width=0.9\linewidth]{assets/product-backlog.png}`
>
> URL pública del backlog: `[completar]`
