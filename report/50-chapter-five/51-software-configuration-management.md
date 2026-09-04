# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

### 5.1.1. Software Development Environment Configuration

Para la gestión del proyecto y del Product Backlog se empleará **Trello** como tablero visual para la planificación de Sprints, organización del backlog y seguimiento de las tareas asignadas a los integrantes del equipo. Asimismo, se utilizará **GitHub Issues** para registrar incidencias y mantener la trazabilidad de actividades relacionadas directamente con los repositorios del proyecto.

Durante el levantamiento y gestión de requisitos se utilizará **Gherkin** para la definición de criterios de aceptación de las User Stories y Technical Stories mediante la estructura Given-When-Then. La documentación relacionada con los requisitos será almacenada dentro del repositorio del Project Report y gestionada colaborativamente mediante GitHub.

Para el Product UX/UI Design se utilizará **Figma** como herramienta principal para la elaboración de Wireframes, Mock-ups y Prototypes correspondientes a VitaLink. Para la creación de diagramas adicionales y UML se empleará **Lucidchart**, mientras que **Structurizr** será utilizado para la elaboración de los diagramas de arquitectura basados en C4 Model.

Para el diseño y modelado de la base de datos se empleará **MySQL Workbench**, permitiendo representar las tablas, columnas, claves primarias, claves foráneas, restricciones y relaciones necesarias para la persistencia de los datos de VitaLink.

Como entornos de desarrollo integrado se utilizará principalmente **Visual Studio Code** para el desarrollo de la Landing Page y Frontend Web Applications, mientras que **IntelliJ IDEA** será utilizado para el desarrollo y las pruebas de los RESTful Web Services implementados en Java.

Para el desarrollo de la Landing Page se utilizarán **HTML5, CSS3 y JavaScript**, permitiendo construir una interfaz responsive orientada a comunicar la propuesta de valor de VitaLink y facilitar el acceso de los diferentes segmentos objetivo a la plataforma.

Para el desarrollo de las Frontend Web Applications se utilizará **Node.js** en su versión LTS junto con **NPM** como administrador de paquetes. La aplicación será implementada utilizando **Angular Framework** y **TypeScript**, junto con HTML5 y CSS3 para la estructura y presentación de las interfaces. El lenguaje visual estará basado en Material Design y se utilizará **Angular Material** como biblioteca principal de componentes de interfaz.

Para el desarrollo de los RESTful Web Services se utilizará **Java** junto con **Spring Boot Framework** y **Spring Data JPA**. Estos servicios permitirán implementar la lógica de negocio asociada al monitoreo de información biométrica, gestión de alertas, historial de pacientes, triaje, red familiar y agendamiento asistido de citas. Para las pruebas unitarias y de integración del backend se utilizará **JUnit**.

Para el almacenamiento de la información se utilizará **MySQL** como sistema de gestión de base de datos relacional. Asimismo, se utilizará **Postman** para realizar pruebas sobre los endpoints implementados y mantener colecciones de solicitudes correspondientes a los RESTful Web Services.

Para la documentación de los servicios se utilizará **OpenAPI Specification mediante Swagger**, permitiendo visualizar y documentar los endpoints de la API, sus métodos HTTP, parámetros, requests y responses.

Para el control de versiones y trabajo colaborativo se utilizarán **Git** y **GitHub**. Los repositorios permitirán gestionar el código fuente y la documentación del proyecto mediante branches, commits y Pull Requests. Además, se utilizará **GitHub Actions** para procesos de integración y despliegue continuo, junto con **GitHub Secrets** para el manejo seguro de variables y credenciales utilizadas durante estos procesos.

Finalmente, la documentación del proyecto será elaborada mediante archivos **Markdown** almacenados en el repositorio público del Project Report. Cuando sea necesario publicar documentación estática adicional, se podrá utilizar **MkDocs** junto con **GitHub Pages**.


### 5.1.2. Source Code Management

Para el seguimiento de modificaciones y el trabajo colaborativo durante el desarrollo de VitaLink se utilizarán **Git** como sistema de control de versiones y **GitHub** como plataforma para el almacenamiento y gestión de los repositorios del proyecto.

Los repositorios serán administrados dentro de la organización **TilinesGroup**. Cada producto de software contará con su propio repositorio, permitiendo mantener separados los diferentes componentes de la solución y facilitando su desarrollo, mantenimiento y despliegue.

| Solución | Nombre del repositorio | Enlace |
|----------|-------------------------|--------|
| Landing Page | Pendiente | Pendiente |
| Frontend Web Application | Pendiente | Pendiente |
| Backend - RESTful Web Services | Pendiente | Pendiente |

En el caso del repositorio correspondiente a los **RESTful Web Services**, además del código fuente del backend, se almacenarán los archivos correspondientes a las pruebas unitarias, pruebas de integración y pruebas de aceptación necesarias para comprobar el correcto funcionamiento de los servicios implementados.

#### GitFlow Workflow

Para organizar el desarrollo colaborativo se utilizará **GitFlow Workflow**, permitiendo separar el código estable de las funcionalidades que todavía se encuentran en desarrollo.

La rama `main` contendrá las versiones estables del proyecto correspondientes a entregas o releases aprobadas. La rama `develop` será utilizada como rama principal de integración durante el desarrollo, donde se consolidarán las funcionalidades previamente desarrolladas y revisadas.

Cada nueva funcionalidad, sección o mejora será desarrollada mediante una rama independiente `feature/*`, creada a partir de `develop`. Una vez finalizados y revisados los cambios, la rama será integrada nuevamente a `develop` mediante un Pull Request.

Para la preparación de versiones estables se utilizarán ramas `release/*`, mientras que las ramas `hotfix/*` serán utilizadas para realizar correcciones urgentes sobre versiones que ya hayan sido integradas en `main`.

La estructura general del flujo será:

`main` → versiones estables  
`develop` → integración de avances  
`feature/*` → nuevas funcionalidades  
`release/*` → preparación de versiones  
`hotfix/*` → correcciones urgentes

#### Branch Naming Convention

Para mantener una nomenclatura uniforme, las ramas utilizarán nombres descriptivos y `kebab-case`.

Las ramas de funcionalidades seguirán la estructura:

`feature/<short-description>`

Ejemplos:

`feature/alert-management`

`feature/patient-history`

`feature/appointment-scheduling`

Las ramas destinadas a preparar nuevas versiones seguirán la estructura:

`release/<version>`

Ejemplo:

`release/1.0.0`

Las ramas destinadas a correcciones urgentes seguirán la estructura:

`hotfix/<version>`

Ejemplo:

`hotfix/1.0.1`

#### Semantic Versioning

Para identificar las versiones liberadas de VitaLink se utilizará **Semantic Versioning**, siguiendo la estructura:

`MAJOR.MINOR.PATCH`

Por ejemplo:

`v1.0.0`

El valor `MAJOR` será incrementado cuando se introduzcan cambios importantes que generen incompatibilidad con versiones anteriores. `MINOR` será utilizado cuando se incorporen nuevas funcionalidades compatibles con la versión existente y `PATCH` cuando se realicen correcciones de errores que no alteren la compatibilidad del producto.

Ejemplos:

`v1.0.0` - Primera versión estable de VitaLink.

`v1.1.0` - Incorporación de nuevas funcionalidades.

`v1.1.1` - Corrección de errores sobre la versión anterior.

#### Conventional Commits

Los mensajes utilizados en los commits seguirán la especificación **Conventional Commits**, permitiendo mantener un historial de cambios ordenado, comprensible y trazable.

La estructura general utilizada será:

`<type>(<scope>): <description>`

Entre los tipos de commits que se utilizarán se encuentran:

| Tipo | Descripción |
|------|-------------|
| `feat` | Incorporación de una nueva funcionalidad. |
| `fix` | Corrección de un error. |
| `docs` | Cambios relacionados con documentación. |
| `style` | Cambios de formato que no modifican el comportamiento del código. |
| `refactor` | Reestructuración del código sin modificar su funcionalidad. |
| `test` | Incorporación o modificación de pruebas. |
| `chore` | Tareas de mantenimiento o configuración. |

Ejemplos:

`feat(alerts): add critical alert management`

`feat(appointments): add appointment confirmation`

`fix(auth): correct user authentication`

`test(triage): add triage service unit tests`

`docs(report): add source code management section`

#### Pull Requests

La integración de cambios entre ramas se realizará mediante **Pull Requests** en GitHub. Este mecanismo permitirá revisar las modificaciones antes de incorporarlas a las ramas principales y mantener evidencia de los aportes realizados por los integrantes del equipo.

Las ramas `feature/*` serán integradas hacia `develop` una vez que los cambios hayan sido revisados y aprobados. Posteriormente, cuando se alcance una versión estable del producto, los cambios correspondientes serán integrados hacia `main` mediante el flujo de release establecido.

De esta manera, VitaLink mantendrá un proceso organizado de control de versiones, facilitando la colaboración entre los integrantes, la trazabilidad de cambios y la estabilidad de los diferentes productos que forman parte de la solución.



### 5.1.3. Source Code Style Guide & Conventions


En cuanto a las convenciones y guías de estilo, para el desarrollo de VitaLink se adoptarán reglas que permitan mantener uniformidad, legibilidad y facilidad de mantenimiento en el código fuente.

Para **HTML, CSS y JavaScript** se seguirán buenas prácticas de desarrollo web, priorizando una estructura ordenada, correcta indentación y el uso de nombres descriptivos en inglés para clases, identificadores, variables y funciones.

En el desarrollo del frontend con **Angular y TypeScript** se utilizarán las convenciones recomendadas por Angular y Google TypeScript Style Guide. Se empleará nomenclatura en inglés, nombres significativos para componentes, servicios, clases, interfaces, variables y métodos, además de una organización modular que facilite la reutilización y mantenimiento del código.

Para el backend desarrollado con **Java y Spring Boot** se seguirá Google Java Style Guide y las convenciones recomendadas para Spring Boot. Se utilizarán nombres descriptivos en inglés, una estructura clara de paquetes y una separación adecuada entre controladores, servicios, repositorios y entidades.

Los criterios de aceptación de las User Stories y Technical Stories serán redactados utilizando **Gherkin**, siguiendo la estructura `Given-When-Then`, con escenarios claros y verificables.

Asimismo, se mantendrán convenciones consistentes para el control de versiones. Los mensajes de commits seguirán **Conventional Commits**, mientras que el flujo de ramas se organizará mediante **GitFlow**, utilizando ramas `feature`, `release` y `hotfix`. Las versiones liberadas del software seguirán **Semantic Versioning**.

Estas convenciones permitirán mantener una estructura de código uniforme entre los diferentes componentes de VitaLink y facilitarán el trabajo colaborativo durante el desarrollo del proyecto.


### 5.1.4. Software Deployment Configuration

El despliegue de VitaLink se realizará utilizando servicios Cloud que permitan publicar y actualizar los diferentes productos digitales de la solución a partir de sus respectivos repositorios de código fuente.

La configuración de despliegue se organizará de manera independiente para la Landing Page, la Frontend Web Application y los RESTful Web Services, permitiendo que cada componente pueda mantenerse y actualizarse sin afectar directamente a los demás.

#### Landing Page

La Landing Page de VitaLink será desplegada utilizando **Cloudflare Pages**. Esta plataforma permitirá conectar el repositorio correspondiente con el servicio de despliegue para generar una versión pública del sitio.

El proceso general de despliegue será el siguiente:

1. Mantener el código fuente de la Landing Page en su repositorio de GitHub.
2. Conectar el repositorio con Cloudflare Pages.
3. Seleccionar la rama correspondiente a la versión que será publicada.
4. Configurar los parámetros necesarios para el proceso de publicación.
5. Ejecutar el despliegue.
6. Verificar el correcto funcionamiento de la Landing Page mediante la URL pública generada.

De esta manera, los cambios incorporados al repositorio podrán reflejarse posteriormente en nuevas versiones publicadas de la Landing Page.

#### Frontend Web Application

La Frontend Web Application de VitaLink será desplegada utilizando **Netlify**, aprovechando su integración con GitHub para facilitar la publicación y actualización de la aplicación desarrollada con Angular.

El proceso general será:

1. Mantener el proyecto Angular dentro de su repositorio correspondiente.
2. Conectar el repositorio de GitHub con Netlify.
3. Seleccionar la rama destinada al despliegue.
4. Configurar el proceso de instalación de dependencias y generación del build de producción.
5. Ejecutar el despliegue de la aplicación.
6. Verificar mediante la URL pública que las vistas y funcionalidades se ejecuten correctamente.

Netlify permitirá mantener disponible la aplicación web para los diferentes usuarios de VitaLink y facilitar la publicación de nuevas versiones conforme avance el desarrollo.

#### RESTful Web Services

Los RESTful Web Services de VitaLink serán desplegados utilizando **Azure Web App Service**. El backend será desarrollado mediante Java y Spring Boot y será publicado desde el repositorio correspondiente.

El proceso general de despliegue será:

1. Mantener el código fuente de los RESTful Web Services en GitHub.
2. Configurar el proyecto Spring Boot y sus dependencias necesarias para producción.
3. Crear y configurar el recurso correspondiente en Azure Web App Service.
4. Configurar las variables de entorno y credenciales necesarias para la ejecución del servicio.
5. Vincular el repositorio con el proceso de despliegue.
6. Publicar la aplicación.
7. Comprobar mediante la URL pública que los endpoints se encuentren disponibles y respondan correctamente.

Las credenciales y demás información sensible utilizada durante el despliegue no serán almacenadas directamente en el código fuente, sino que serán administradas mediante variables de entorno y mecanismos seguros de configuración.

#### Deployment Workflow

De manera general, el flujo de despliegue de los productos de VitaLink seguirá la siguiente estructura:

`GitHub Repository → Build / Configuration → Cloud Platform → Public Deployment`

La distribución de las plataformas será:

| Producto digital | Plataforma de despliegue |
|------------------|--------------------------|
| Landing Page |  |
| Frontend Web Application | |
| RESTful Web Services |  |

Esta estrategia permitirá mantener separados los procesos de despliegue de cada componente de VitaLink y facilitará la actualización progresiva de la solución durante los diferentes Sprints.


