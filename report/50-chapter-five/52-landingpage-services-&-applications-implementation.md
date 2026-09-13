## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. Sprint Planning 1

En esta sección se documenta la reunión de planificación del Sprint 1, en la que el equipo CodeBrokers definió el objetivo del sprint, seleccionó las historias de usuario a comprometer desde el Product Backlog y acordó la velocidad esperada. El Sprint 1 concentra la totalidad del épico EP-01 (Landing Page), por tratarse del primer incremento entregable del producto VitaLink y de la superficie que valida la propuesta de valor frente a los segmentos objetivo.

| Campo | Detalle |
| :--- | :--- |
| **Sprint #** | Sprint 1 |
| **Date** | 2026-08-24 |
| **Time** | 19:00 PM (GMT-5) |
| **Location** | Reunión remota vía Discord |
| **Prepared By** | Benigno Montero, Harold Fauskorp |
| **Attendees (to planning meeting)** | Osorio Ramírez, Eduardo Jesús; Said Conde, Yazid; Tello Quispe, Luis German; Rodriguez Gonzales, Leonel German; Salon Puerta, Merly; Benigno Montero, Harold Fauskorp |
| **Sprint 0 Review Summary** | No aplica. El Sprint 1 es el primer sprint del proyecto, por lo que no existe un sprint previo del cual derivar una revisión. El punto de partida es el Product Backlog priorizado en la sección 3.3 y el diseño definido en el Capítulo IV. |
| **Sprint 0 Retrospective Summary** | No aplica. Al no existir un sprint previo, el equipo acordó como acuerdos iniciales de trabajo: usar GitFlow con ramas `feature/<número>-<descripción>` por entregable, aplicar Conventional Commits, y exigir al menos una revisión de par antes de integrar a `develop`. |
| **Sprint 1 Goal** | Publicar una Landing Page desplegada que comunique con claridad la propuesta de valor de VitaLink al segmento de profesionales de la salud y habilite las acciones de conversión (solicitar información y unirse como proveedor de salud), transmitiendo confianza mediante evidencia de respaldo institucional y una sección explícita de privacidad y seguridad de datos. <br><br> **Via** Implementación de la Landing Page en HTML5, CSS3 y JavaScript, siguiendo el Style Guideline de la sección 4.1 y la arquitectura de información de la sección 4.2, desplegada en un servicio de hosting estático. <br><br> **The Success Metrics Are** Las 7 historias de usuario comprometidas alcanzan sus criterios de aceptación, la Landing Page se encuentra accesible mediante una URL pública y todas las ramas de trabajo se integran a `develop` mediante Pull Request revisado. |
| **Sprint 1 Velocity** | 16 Story Points |
| **Sum of Story Points** | 16 Story Points |

Table: Sprint Planning 1

La velocidad comprometida de 16 Story Points corresponde al total del épico EP-01 y equivale a aproximadamente el 22 % de los 74 Story Points del Product Backlog completo. Al ser el primer sprint, esta cifra no proviene de una velocidad histórica, sino de una estimación por capacidad: seis integrantes con una disponibilidad estimada de 8 horas semanales durante el periodo del sprint.

#### 5.2.1.2. Aspect Leaders and Collaborrators



#### 5.2.1.3. Sprint Backlog 1

En esta sección se descomponen las historias de usuario comprometidas para el Sprint 1 en work-items ejecutables. La gestión del Sprint Backlog se realiza en Jira, dentro del tablero Scrum del proyecto `VTL` (CodeBrokers), en el sprint denominado **Sprint 1 - Landing Page**, con fechas del 24/08/2026 al 17/09/2026.

**URL del Sprint Backlog en Jira:** \href{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1/backlog}{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1/backlog}

| User Story Id | User Story Title | Work-Item Id | Work-Item Title | Description | Estimation (hours) | Assigned To | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| US-01 | Propuesta de valor clara en Landing Page | WI-01 | Estructura base del proyecto de la Landing Page | Crear el repositorio de la Landing Page con la estructura de carpetas para HTML, CSS y JS, e incorporar el reset de estilos y las variables del Style Guideline (4.1). | 4 | Benigno Montero, Harold Fauskorp | Done |
| US-01 | Propuesta de valor clara en Landing Page | WI-02 | Implementación de la sección Hero | Maquetar el bloque principal con titular, subtitular e imagen de apoyo, expresando el problema que resuelve VitaLink en menos de diez segundos de lectura. | 4 | Osorio Ramírez, Eduardo Jesús | Done |
| US-02 | Sección de privacidad y seguridad de datos | WI-03 | Sección de privacidad y seguridad | Maquetar la sección dedicada al tratamiento de datos clínicos, con los tres pilares de seguridad y el enlace a la política de privacidad completa. | 3 | Salon Puerta, Merly | Done |
| US-03 | Botón para solicitar información | WI-04 | Formulario de solicitud de información | Implementar el formulario con los campos nombre, correo y especialidad, incluyendo validación en el cliente y mensaje de confirmación tras el envío. | 5 | Said Conde, Yazid | Done |
| US-03 | Botón para solicitar información | WI-05 | Botón de llamada a la acción en el encabezado | Incorporar el botón "Solicitar información" en el encabezado con comportamiento fijo al desplazarse y anclaje al formulario. | 2 | Said Conde, Yazid | Done |
| US-04 | Respaldo de clínicas e instituciones | WI-06 | Franja de respaldo institucional | Maquetar la franja de logotipos de clínicas e instituciones aliadas y el testimonio de un profesional de la salud. | 3 | Rodriguez Gonzales, Leonel German | Done |
| US-05 | Sección de preguntas frecuentes | WI-07 | Componente acordeón de preguntas frecuentes | Implementar en JavaScript el comportamiento de expansión y contracción de cada pregunta, garantizando la navegación por teclado. | 4 | Tello Quispe, Luis German | Done |
| US-05 | Sección de preguntas frecuentes | WI-08 | Redacción del contenido de preguntas frecuentes | Redactar las preguntas y respuestas sobre costos, privacidad y funcionamiento básico, alineadas al Ubiquitous Language (2.5). | 2 | Tello Quispe, Luis German | Done |
| US-06 | Botón para unirse como proveedor de salud | WI-09 | Botón de registro para proveedores de salud | Incorporar el botón "Unirme como proveedor de salud" en el encabezado y enlazarlo al flujo de registro médico. | 3 | Rodriguez Gonzales, Leonel German | Done |
| US-07 | Ejemplo visual de una alerta | WI-10 | Mockup ilustrativo del panel de alertas | Maquetar el ejemplo visual de una alerta dentro del panel médico, empleando datos claramente ficticios y los colores de urgencia definidos en 4.1. | 4 | Osorio Ramírez, Eduardo Jesús | Done |
| — | Tarea transversal del sprint | WI-11 | Despliegue de la Landing Page | Configurar el despliegue continuo de la Landing Page en el servicio de hosting estático y verificar la accesibilidad de la URL pública. | 3 | Benigno Montero, Harold Fauskorp | Done |
| — | Tarea transversal del sprint | WI-12 | Revisión de responsividad y verificación cruzada | Verificar la correcta visualización en los puntos de quiebre definidos y revisar el cumplimiento de los criterios de aceptación de las siete historias comprometidas. | 3 | Salon Puerta, Merly | Done |

Table: Sprint Backlog 1

El esfuerzo total estimado para el Sprint 1 asciende a **40 horas**, distribuidas entre los seis integrantes del equipo, correspondientes a los 16 Story Points comprometidos.

#### 5.2.1.4. Development Evidence for Sprint Review

Durante el Sprint 1 el equipo CodeBrokers concentró su trabajo en el repositorio de documentación del proyecto, donde se elaboraron los Capítulos I al IV y los artefactos de diseño que sustentan la implementación de la Landing Page. La tabla siguiente recoge la evidencia de los commits realizados en el periodo del sprint (24/08/2026 – 17/09/2026), obtenida directamente del historial del repositorio.

**Repositorio:** \href{https://github.com/CodeBrokers-web-app-1ASI0730-2620-16712/upc-pre-202620-1asi0730-16712-CodeBrokers-report-}{upc-pre-202620-1asi0730-16712-CodeBrokers-report-}

| Repository | Branch | Commit Id | Commit Message | Commit Message Body | Committed on (Date) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 626a1c2 | Initial commit | — | 28/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 80a4829 | chore(repo): initialize folder structure and base files for chapters | — | 28/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 16ffe11 | build(config): set up pandoc configuration files and pdf engine | — | 28/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/startup-profile | 739290f | docs: add startup description and team members table. | — | 29/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/solution-profile | 808000a | docs: add backgrounds and problems, using  5W & 2H. | — | 29/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/target-segments | 9892ffb | docs: add target segments. | — | 29/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/bibliography | 77769e0 | docs: add bibliography and references. | — | 29/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 3fe5050 | Expand Lean UX section in solution profile - eduardo | Added Lean UX assumptions, user outcomes, features, and risks for VitaLink. | 30/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 1cefaf4 | Add problem statements for elderly care solutions - eduardo | Added two problem statements regarding preventive monitoring and communication for elderly care. | 30/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 64a41b8 | feat(frontmatter): complete report frontmatter section | — | 30/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 2b5a08c | Update risk and assumptions in solution profile darle enter a la parte de abajo xd | Added assumptions regarding user adoption and integration of monitoring tools. | 30/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 666ccf1 | Add assumptions regarding app adoption and usability | — | 30/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 0141897 | fix(11): update team members table and fix typos | — | 30/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 27c9617 | Rename VitaLink to SeniorCare in solution profile | — | 30/08/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/11-startup-profile | d1f24b3 | docs: update team member table | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/11-startup-profile | 090c970 | Docs: update update team member table | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/11-startup-profile | 23918aa | Docs: update update team member table | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/11-startup-profile | a4ae9fc | docs: update update team member table | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/11-startup-profile | 0231e67 | docs: update update team member table | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 2355d07 | Add Lean UX hypothesis statements for health platform | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/lean-ux | cd30969 | docs: add the lean ux canva. | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/entrevistas | c4fe552 | docs: add the interviews design. | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | cf1d8a3 | foto para la presentacion de integrantes | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 57424bf | Add member profile for Eduardo Osorio Ramírez | Updated member profile details for Eduardo Osorio Ramírez, including student code, career, description, and contributions to the team. | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 26ea45f | Change profile image in startup profile | Updated the profile image in the startup profile. | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 9eb436f | Update project name from VitaLink to SeniorCare | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 8462642 | Update references from VitaLink to SeniorCare | — | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/lean-ux-hypotheses | 2a6743a | docs: update Lean UX hypothesis statements | Add hypothesis statements based on the defined feature assumptions. | 01/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 45a4b43 | Add user stories for landing page and functionalities | Added detailed user stories for the landing page, frontend, and backend functionalities, including acceptance criteria for each story. | 02/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/entrevistas | 720d226 | docs: add the interview analysis. | — | 02/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 41f32ad | Update 11-startup-profile.md | — | 02/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/entrevistas | 355ac3c | docs: add the interview analysis. | — | 02/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/entrevistas | f5775f0 | docs: add the interview analysis. | — | 02/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | e2a44af | Add impact mapping table for SeniorCare project | Added an impact mapping table for the SeniorCare project, detailing business objectives, actors, impacts, and deliverables. | 02/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 07cc24a | Add product backlog table to chapter three | Added a detailed product backlog table with user stories and descriptions for the VitaLink project. | 02/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/team-member-profile | e861601 | docs: add Leonel team member profile | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/team-member-profile | 5f65445 | Add files via upload | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/team-member-profile | 6eee590 | docs: add Leonel team member profile | Updated image file extension from .jpg to .jpeg in startup profile. | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/team-member-profile | 64e2966 | docs: fix team member profile | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/team-member-profile | d94a4f3 | docs: fix team member profile | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/entrevistas | 90e9e6b | docs: add the interview register. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/entrevistas | c62a264 | docs: fix the name of target objects. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/style-guidelines | 334c445 | docs: add the style guidelines. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/style-guidelines | 3be8051 | docs: add the general style guidelines. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/style-guidelines | 6d5dcbb | docs: add the general style guidelines. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/style-guidelines | ccfd051 | docs: add the web style guidelines. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/style-guidelines | be15397 | docs: add the logo of vitalink. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/style-guidelines | 2373da0 | docs: add the colors of vitalink. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | ce351e0 | feat(12): Add member profile Luis Tello | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 5a7a8e2 | feat(21): add all the points regarding the competitors | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feautre/42-information-arquitecure | 7dfbdc3 | docs: add the organization systems. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feautre/42-information-arquitecure | ac27cb4 | docs: add the labeling systems. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feautre/42-information-arquitecure | dbb2464 | docs: add the seo tags and meta tags. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feautre/42-information-arquitecure | 759c1ea | docs: add the searching systems & navigation systems. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/entrevistas | 741804a | docs: add the interview record. | — | 03/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | b094d66 | Rename SeniorCare to VitaLink in startup profile | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | e036566 | Rename SeniorCare to VitaLink in solution profile | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 14a63a2 | Update references from SeniorCare to VitaLink | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/12-solution-profile | af06cb4 | docs: fix the lean ux canva design. | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/12-solution-profile | 7d76d33 | docs: fix the lean ux canva design. | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/needfinding | cb6ab27 | feat: item 2.3.1 completo | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/needfinding | 2ee831c | feat: item 2.3.2 completo | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/needfinding | 2bc59d4 | feat: item 2.3.3 completo | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/needfinding | b17836e | feat: item 2.3.4 completo | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/needfinding | 56d6006 | feat: Needfinding, imagenes agregadas y enlazadas | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/needfinding | 2e773cb | refactor: se refactorizo el formato de escritura de la tabla | — | 05/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 74fe811 | refactor(32): convert table from latex to markdown | — | 06/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/needfinding | da6202d | docs: fix the organized of images. | — | 06/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | e040acc | fix(33): update table structure and prioritize landing page stories | — | 06/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/needfinding | 7133b41 | Fix: Se corrigió la tabla del User task Matrix | — | 06/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 44e5ea0 | refactor(31): convert user stories table from latex to markdown and add missing frontend epics | — | 06/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 9ab9490 | feat(43): complete landing page UI design wireframes and mockups | — | 06/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/25-ubiquitous-language | bc253c5 | Expand Ubiquitous Language with key term definitions | Added definitions for key terms in the Ubiquitous Language section to clarify concepts related to elder care. | 06/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | ebc23b4 | feat(11): Add member profile Harold Benigno | — | 10/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 31048ec | feat(11): Add Harold Benigno to cover page | — | 10/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | c3bba66 | docs: add the We applications UX/UI Design. | — | 10/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | develop | 9eb0b5f | docs: add the web applications protyping. | — | 10/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/46-domain-driven-software-architecture | 1330e84 | feat(4.6): C4 model de VitaLink en Structurizr DSL | — | 12/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/471-class-diagrams | f18a779 | feat(4.7): diagramas de clases por bounded context en PlantUML | — | 12/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/48-database-design | fb83f96 | feat(4.8): diseno de base de datos normalizado en PostgreSQL | — | 12/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/45-web-applications-prototyping | 41a39ab | feat(45): add web applications prototyping section | — | 13/09/2026 |
| upc-pre-202620-1asi0730-16712-CodeBrokers-report- | feature/45-web-applications-prototyping | 7d046f6 | fix(45): limitar el alcance del prototipo a Desktop Web Browser | — | 13/09/2026 |

Table: Development Evidence del Sprint 1

**Resumen del sprint**

| Métrica | Valor |
| :--- | :--- |
| Commits totales (excluyendo merges) | 82 |
| Ramas de característica creadas | 19 |
| Pull Requests integrados | 17 |
| Periodo cubierto | 28/08/2026 – 13/09/2026 |
| Integrantes con contribuciones registradas | 6 de 6 |
| Identidades de Git distintas detectadas | 8 (dos integrantes commitearon con dos cuentas) |

Table: Resumen de la actividad de desarrollo del Sprint 1

Los commits marcados con la rama `develop` corresponden a contribuciones cuya rama de origen no pudo determinarse de forma unívoca en el historial, por haberse integrado mediante merges de consolidación entre `develop` y `main` en lugar de merges individuales de rama de característica. Esta situación se corrigió a partir del 12/09/2026, fecha desde la cual cada sección del informe se desarrolla en su propia rama `feature/<n>-<descripción>` con un Pull Request independiente.

#### 5.2.1.5. Execution Evidence for Sprint Review



#### 5.2.1.6. Services Documentation Evidence for Sprint Review

**No aplica para el Sprint 1.**

El alcance comprometido en el Sprint 1 corresponde íntegramente al épico EP-01 (Landing Page), cuyas siete historias de usuario se resuelven con una página estática implementada en HTML5, CSS3 y JavaScript. Este incremento no consume ni expone servicios web, por lo que no existen endpoints que documentar en esta etapa.

La documentación de servicios mediante **OpenAPI/Swagger** se incorporará a partir del Sprint 2, cuando comience la implementación de los servicios RESTful en ASP.NET Core correspondientes a los épicos EP-02 (Frontend) y EP-03 (Backend). El contrato de dichos servicios se derivará de los bounded contexts y agregados definidos en la sección 4.6 y del esquema de base de datos especificado en la sección 4.8. La siguiente tabla anticipa la cobertura prevista:

| Bounded Context | Endpoints previstos | Sprint de implementación |
| :--- | :--- | :--- |
| Profiles | `/api/v1/older-adults`, `/api/v1/care-providers`, `/api/v1/family-caregivers` | Sprint 2 |
| Monitoring | `/api/v1/health-records`, `/api/v1/record-types` | Sprint 2 |
| Alerting | `/api/v1/alerts`, `/api/v1/alerts/{id}/status` | Sprint 2 |
| Care Assignment | `/api/v1/assignments` | Sprint 3 |
| Notification | `/api/v1/notifications` | Sprint 3 |

Table: Cobertura prevista de documentación de servicios

#### 5.2.1.7. Software Deployment Evidence for Sprint Review



#### 5.2.1.8. Team Collaboration Insights during Sprint



### 5.2.2. Sprint 2

#### 5.2.2.1. Sprint Planning 2



#### 5.2.2.2. Aspect Leaders and Collaborrators



#### 5.2.2.3. Sprint Backlog 2



#### 5.2.2.4. Development Evidence for Sprint Review



#### 5.2.2.5. Execution Evidence for Sprint Review



#### 5.2.2.6. Services Documentation Evidence for Sprint Review



#### 5.2.2.7. Software Deployment Evidence for Sprint Review



#### 5.2.2.8. Team Collaboration Insights during Sprint



### 5.2.3. Sprint 3

#### 5.2.3.1. Sprint Planning 3



#### 5.2.3.2. Aspect Leaders and Collaborrators



#### 5.2.3.3. Sprint Backlog 3



#### 5.2.3.4. Development Evidence for Sprint Review



#### 5.2.3.5. Execution Evidence for Sprint Review



#### 5.2.3.6. Services Documentation Evidence for Sprint Review



#### 5.2.3.7. Software Deployment Evidence for Sprint Review



#### 5.2.3.8. Team Collaboration Insights during Sprint



### 5.2.4. Sprint 4

#### 5.2.4.1. Sprint Planning 4



#### 5.2.4.2. Aspect Leaders and Collaborrators



#### 5.2.4.3. Sprint Backlog 4



#### 5.2.4.4. Development Evidence for Sprint Review



#### 5.2.4.5. Execution Evidence for Sprint Review



#### 5.2.4.6. Services Documentation Evidence for Sprint Review



#### 5.2.4.7. Software Deployment Evidence for Sprint Review



#### 5.2.4.8. Team Collaboration Insights during Sprint




