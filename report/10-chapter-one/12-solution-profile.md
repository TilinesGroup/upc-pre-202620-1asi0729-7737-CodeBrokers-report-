## 1.2 Solution Profile

### 1.2.1 Antecedentes y problemática



### 1.2.2 Lean UX Process

#### 1.2.2.1. Lean UX Problem Statements
El estado actual del telemonitoreo y cuidado de adultos mayores se ha centrado principalmente en cuidadores familiares que gestionan registros manuales y en centros de salud que atienden emergencias de manera reactiva, generando demoras criticas y una atencion fragmentada ante complicaciones de salud.

Lo que los productos y servicios existentes no logran resolver es la falta de integracion en tiempo real entre el monitoreo continuo de signos vitales y la capacidad de agendar consultas medicas de forma inmediata.

Nuestra plataforma resuelve esta brecha mediante un servicio SaaS que procesa telemetria biometrica en tiempo real, evalua anomalias y pre-agenda de forma automatica citas preventivas o prioritarias con centros de salud asociados, derivando reportes de evolucion al instante tanto al cuidador como al especialista.

El enfoque inicial estara dirigido a cuidadores familiares a cargo de adultos mayores y a centros de salud locales o clinicas ambulatorias.

Sabremos que tenemos exito cuando se logre una reduccion del 50% en el tiempo necesario para coordinar una cita ante una anomalia, una tasa minima del 70% de aceptacion en las citas pre-agendadas y la afiliacion activa de al menos 15 centros de salud a la red.


#### 1.2.2.2. Lean UX Assumptions

###### Business Outcomes

1. *Creemos que nuestros clientes necesitan* una forma confiable, centralizada y en tiempo real de monitorear la salud de los adultos mayores para prevenir complicaciones medicas y actuar con rapidez ante emergencias.

2. *Estas necesidades se pueden resolver con* una plataforma web SaaS integrada a telemetria IoT simulada que procesa signos vitales y un sistema inteligente de pre-agendamiento asistido para derivacion clinica inmediata.

3. *Mis clientes iniciales seran* cuidadores familiares a cargo de adultos mayores con patologias cronicas y centros de salud o clinicas de atencion ambulatoria.

4. *El valor #1 que un cliente quiere es* la tranquilidad de detectar anomalias a tiempo y asegurar una atencion medica rapida y efectiva sin esperas burocraticas.

5. *Beneficios adicionales* consolidacion de la historia clinica en la nube, alertas criticas multicanal, reduccion del estres del cuidador y acceso a consultas a tarifa social para pacientes sin seguro medico.

6. *Voy a adquirir clientes a traves de* convenios directos con policlinicos locales, alianzas estrategicas con organizaciones no gubernamentales comunitarias, campanas digitales orientadas a familias y programas de recomendacion.

7. *Mi competencia es* servicios tradicionales de cuidadores particulares a domicilio, aplicaciones basicas de recordatorio de medicinas y plataformas genericas de reserva de citas medicas.

8. *Hare dinero a traves de* planes de suscripcion mensual por niveles (B2C) para familias y membresias o comisiones por citas efectivas (B2B) cobradas a centros medicos aliados.

9. *Los venceremos porque* integramos el sensado continuo de parametros vitales con un actuador inteligente que pre-agenda citas y alerta al instante, evitando que el usuario deba buscar especialistas por su cuenta en momentos de crisis.

10. *Mayor riesgo de producto* desconfianza de los usuarios en la precision del sistema de alertas o dificultades en la adopcion de la plataforma web por parte de personas de edad avanzada o cuidadores con baja alfabetizacion digital.

11. *Lo resolveremos con* diseno centrado en accesibilidad (a11y), interfaces de alto contraste, flujos asistidos de un solo clic, soporte guiado y videos explicativos breves durante el onboarding.

12. *Otra suposicion critica* los centros de salud asociados mantendran actualizada su disponibilidad de cupos en el sistema y los cuidadores validaran activamente las citas sugeridas por el actuador ante alertas criticas.

###### User Outcomes

- **Quien es el Usuario?**  
  Cuidadores principales (familiares directos o tutores) responsables del bienestar diario de adultos mayores, y personal de recepcion o profesionales medicos pertenecientes a las clinicas y centros de salud afiliados.

- **Que problemas tiene nuestro producto que debe resolver?**  
  La falta de control continuo sobre las variables fisiologicas del adulto mayor, la demora en la deteccion de sintomas de riesgo y los tramites engorrosos o demoras prolongadas para conseguir una consulta medica oportuna.

- **Que caracteristicas son importantes?**  
  Panel de control de telemetria en tiempo real (IoT simulada), notificaciones de emergencia inmediatas, pre-agendamiento automatizado de citas medicas segun cercania y disponibilidad, ficha de triaje clinico exportable y canal de consultas a costo social.

- **Donde encaja nuestro producto en su vida?**  
  En el acompanamiento preventivo cotidiano en el hogar y como canal prioritario de comunicacion entre la familia y la red medica ante cualquier alteracion de salud.

- **Cuando y como es usado?**  
  Funciona de manera continua en segundo plano procesando lecturas biometricas; el cuidador lo consulta diariamente para verificar historiales y de manera reactiva inmediata cuando recibe una notificacion de riesgo para confirmar una cita medica en un clic.

- **Como debe verse y comportarse el producto?**  
  Debe ser visualmente limpio, directo, predecible y con apego estricto a estandares de accesibilidad web: tipografia grande y legible, contrastes definidos, estados de alerta claros mediante codigo de colores y navegacion sin pasos superfluos.

#### 1.2.2.3. Lean UX Hypothesis Statements

* **Declaracion de Hipotesis 1**
  * **Creemos que lograremos** un incremento del 30% en la retencion mensual de la plataforma
  * **Si** los cuidadores familiares principales
  * **Obtienen** tranquilidad continua respecto a los signos vitales diarios y la estabilidad de salud de sus familiares de la tercera edad
  * **Con** un panel interactivo en tiempo real que visualiza metricas de telemetria IoT simulada (frecuencia cardiaca, SpO2 y deteccion de caidas).

* **Declaracion de Hipotesis 2**
  * **Creemos que lograremos** una reduccion del 50% en el tiempo promedio requerido para coordinar una consulta medica de urgencia
  * **Si** los cuidadores familiares
  * **Obtienen** el agendamiento inmediato de citas medicas sin necesidad de buscar o contactar manualmente a multiples proveedores de salud
  * **Con** una funcionalidad de auto-agendamiento inteligente que sugiere y reserva cupos optimos en centros medicos afiliados cercanos.

* **Declaracion de Hipotesis 3**
  * **Creemos que lograremos** un crecimiento del 40% en convenios con clinicas afiliadas y expansion de la red de salud
  * **Si** los proveedores de salud y el personal de recepcion clinica
  * **Obtienen** admisiones de pacientes pre-triados y acceso instantaneo al historial biometrico cronologico antes de la llegada del paciente
  * **Con** un modulo centralizado de historial de salud del paciente y exportacion de triaje.

* **Declaracion de Hipotesis 4**
  * **Creemos que lograremos** una tasa de confirmacion del 75% en alertas de emergencia dentro de los primeros 5 minutos
  * **Si** los tutores familiares designados
  * **Obtienen** conocimiento inmediato de umbrales fisiologicos fuera de rango o incidentes criticos detectados
  * **Con** una integracion de notificaciones externas automatizadas mediante SMS y servicios de mensajeria de emergencia.

* **Declaracion de Hipotesis 5**
  * **Creemos que lograremos** una tasa de adopcion del 35% en hogares de bajos recursos sin cobertura de seguro medico privado
  * **Si** los adultos mayores sin seguro y sus cuidadores
  * **Obtienen** acceso a consultas preventivas a bajo costo y derivacion directa hacia redes comunitarias de salud
  * **Con** un modulo integrado de atencion a tarifa social coordinado junto a organizaciones comunitarias de salud.
  * **We believe we will achieve** a 35% adoption rate among low-income households without private healthcare coverage
  * **If** uninsured elderly patients and their caregivers
  * **Attain** access to low-cost preventive consultations and direct referral to community health networks
  * **With** an integrated social-rate care module coordinated alongside verified community healthcare organizations.


#### 1.2.2.4. Lean UX Canvas

#### 1.2.2.4. Lean UX Canvas

| 1. Business Problem | 2. Business Outcomes | 3. Users |
|  :---               | :---                 | :---     |
| El cuidado de adultos mayores depende de registros manuales y respuestas reactivas ante emergencias de salud, generando demoras criticas y desconexion entre el monitoreo diario del hogar y los centros de atencion medica. | - Reduccion del 50% en el tiempo para coordinar una cita ante anomalias.<br>- Tasa minima del 70% de aceptacion en citas pre-agendadas.<br>- Afiliacion de al menos 15 centros de salud a la red.<br>- Incremento del 30% en la retencion mensual de familias suscriptoras. | - Cuidadores familiares principales (hijos, tutores).<br>- Adultos mayores con enfermedades cronicas.<br>- Centros de salud y profesionales medicos independientes. |

| 4. User Outcomes & Benefits | 5. Solutions | 6. Hypotheses |
| :--- | :--- | :--- |
| - Deteccion temprana de anomalias biometricas y tranquilidad familiar continua.<br>- Atencion medica rapida sin busqueda manual de proveedores en crisis.<br>- Historial clinico y triaje previo disponible para el medico antes de la consulta.<br>- Acceso a consultas a tarifa social para adultos mayores sin seguro. | - Plataforma SaaS con tablero de telemetria IoT simulada en tiempo real.<br>- Sistema inteligente de triaje y pre-agendamiento automatico de consultas.<br>- Historial biometrico centralizado y ficha de triaje exportable.<br>- Modulo de atencion a tarifa social conectado con policlinicos y ONGs.<br>- Notificaciones automatizadas via SMS y mensajeria de emergencia. | - Creemos que el monitoreo IoT en tiempo real lograra un 30% mas de retencion mensual al brindar tranquilidad continua a los cuidadores.<br>- Creemos que el auto-agendamiento inteligente reducira en 50% el tiempo de coordinacion de citas de urgencia.<br>- Creemos que el historial y triaje previo aumentara un 40% los convenios con clinicas.<br>- Creemos que las alertas SMS lograran un 75% de confirmacion en los primeros 5 minutos.<br>- Creemos que la tarifa social lograra un 35% de adopcion en hogares sin seguro privado. |

| 7. What is the most important thing we need to learn first? | 8. What is the least amount of work we need to do to learn the next most important thing? |
| :--- | :--- |
| - Validar si los cuidadores familiares aceptan y confian en el auto-agendamiento ante una anomalia detectada.<br>- Confirmar la disposicion de las clinicas para publicar y gestionar sus cupos de atencion dentro del SaaS.<br>- Identificar el rango de precio mensual aceptable para los planes familiares de suscripcion. | - Desplegar la Landing Page con la propuesta de valor y medir el interes de registro de cuidadores y clinicas.<br>- Probar prototipos interactivos en Figma con cuidadores para validar el flujo de confirmacion de citas en un clic.<br>- Ejecutar simulaciones del flujo de datos IoT y pre-agendamiento en el MVP inicial. |