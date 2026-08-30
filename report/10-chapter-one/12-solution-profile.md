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

* **Hypothesis Statement 1**
  * **We believe we will achieve** a 30% increase in monthly platform retention
  * **If** primary family caregivers
  * **Attain** continuous peace of mind regarding the daily vital signs and health stability of their elderly relatives
  * **With** an interactive real-time dashboard displaying simulated IoT telemetry metrics (heart rate, SpO2, and fall detection).

* **Hypothesis Statement 2**
  * **We believe we will achieve** a 50% reduction in the average time required to coordinate an urgent medical consultation
  * **If** family caregivers
  * **Attain** immediate medical appointment booking without the need to manually search or contact multiple healthcare providers
  * **With** an intelligent auto-scheduling feature that suggests and reserves optimal slots in nearby affiliated medical centers.

* **Hypothesis Statement 3**
  * **We believe we will achieve** a 40% growth in affiliated clinic partnerships and healthcare network expansion
  * **If** healthcare providers and clinic reception staff
  * **Attain** pre-triaged patient admissions and instant access to chronological biometric history before patient arrival
  * **With** a centralized patient health record and triage export module.

* **Hypothesis Statement 4**
  * **We believe we will achieve** a 75% confirmation rate on emergency health alerts within the first 5 minutes
  * **If** designated family tutors
  * **Attain** immediate awareness of abnormal physiological thresholds or detected emergency incidents
  * **With** an automated external notification integration using SMS and emergency messaging services.

* **Hypothesis Statement 5**
  * **We believe we will achieve** a 35% adoption rate among low-income households without private healthcare coverage
  * **If** uninsured elderly patients and their caregivers
  * **Attain** access to low-cost preventive consultations and direct referral to community health networks
  * **With** an integrated social-rate care module coordinated alongside verified community healthcare organizations.


#### 1.2.2.4. Lean UX Canvas

