## 5.2. Landing Page, Services & Applications Implementation

### 5.2.1. Sprint 1

#### 5.2.1.1. Sprint Planning 1

En esta sección se documenta la reunión de planificación del Sprint 1, en la que el equipo CodeBrokers definió el objetivo del sprint, seleccionó las historias de usuario a comprometer desde el Product Backlog y acordó la velocidad esperada. El Sprint 1 concentra la totalidad del épico EP-01 (Landing Page) junto con la historia técnica TS-01 (configuración del entorno y despliegue), por tratarse del primer incremento entregable del producto VitaLink y de la superficie que valida la propuesta de valor frente a los segmentos objetivo.

\begingroup
\centering
\small
\setlength{\tabcolsep}{6pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.28\textwidth}|p{0.67\textwidth}|}
\hline
\textbf{Campo} & \textbf{Detalle} \\
\hline
\endfirsthead

\hline
\textbf{Campo} & \textbf{Detalle} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

\textbf{Sprint \#} & Sprint 1 \\
\hline
\textbf{Date} & 2026-08-24 \\
\hline
\textbf{Time} & 19:00 PM (GMT-5) \\
\hline
\textbf{Location} & Reunión remota vía Discord \\
\hline
\textbf{Prepared By} & Benigno Montero, Harold Fauskorp \\
\hline
\textbf{Attendees (to planning meeting)} & Osorio Ramírez, Eduardo Jesús; Said Conde, Yazid; Tello Quispe, Luis German; Rodriguez Gonzales, Leonel German; Salon Puerta, Merly; Benigno Montero, Harold Fauskorp \\
\hline
\textbf{Sprint 0 Review Summary} & No aplica. El Sprint 1 es el primer sprint del proyecto, por lo que no existe un sprint previo del cual derivar una revisión. El punto de partida es el Product Backlog priorizado en la sección 3.3 y el diseño definido en el Capítulo IV. \\
\hline
\textbf{Sprint 0 Retrospective Summary} & No aplica. Al no existir un sprint previo, el equipo acordó como acuerdos iniciales de trabajo: usar GitFlow con ramas \texttt{feat/<descripción>} por entregable, aplicar Conventional Commits, y exigir al menos una revisión de par antes de integrar a \texttt{develop}. \\
\hline
\textbf{Sprint 1 Goal} & \textbf{Our focus is on} publicar la Landing Page de VitaLink con una propuesta de valor diferenciada para los dos segmentos objetivo: familias con adultos mayores a cargo y profesionales de la salud. \newline\newline \textbf{We believe it delivers} a los visitantes de ambos segmentos la comprensión del servicio, de sus planes de suscripción y de sus garantías de seguridad de datos, sin necesidad de contactar previamente al equipo. \newline\newline \textbf{This will be confirmed when} un visitante accede a la URL pública, identifica el titular correspondiente a su segmento, revisa los planes disponibles y la sección de seguridad, y ejecuta la acción de conversión asociada a su perfil. \\
\hline
\textbf{Sprint 1 Velocity} & 17 Story Points \\
\hline
\textbf{Sum of Story Points} & 17 Story Points \\
\end{longtable}
\endgroup

Table: Sprint Planning 1

La velocidad comprometida de 17 Story Points corresponde a los 14 Story Points del épico EP-01 más los 3 Story Points de la historia técnica TS-01, y equivale a aproximadamente el 21 % de los 82 Story Points del Product Backlog completo. Al ser el primer sprint, esta cifra no proviene de una velocidad histórica, sino de una estimación por capacidad: seis integrantes con una disponibilidad estimada de 8 horas semanales durante el periodo del sprint, comprendido entre el 24/08/2026 y el 15/09/2026.

#### 5.2.1.2. Aspect Leaders and Collaborators

Los aspectos considerados en el Sprint 1 corresponden a las agrupaciones funcionales de la Landing Page derivadas de la arquitectura de información definida en la sección 4.2, junto con el aspecto transversal de configuración y despliegue. Para cada aspecto se designó un líder (L), responsable de su implementación y de la coherencia de la sección con el Style Guideline de la sección 4.1, y uno o más colaboradores (C), encargados de la revisión de los Pull Requests y del apoyo en la integración. La distribución guarda correspondencia directa con la asignación de work-items de la sección 5.2.1.3.

Los aspectos del Sprint 1 son: **A1.** Entorno y Despliegue, **A2.** Navegación y Hero, **A3.** Ecosistema y Flujo Clínico, **A4.** Protocolo de Alertas, **A5.** Planes y Precios, **A6.** Seguridad y Conversión, y **A7.** Footer y Equipo.

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.26\textwidth}|p{0.17\textwidth}|c|c|c|c|c|c|c|}
\hline
\textbf{Team Member (Last Name, First Name)} & \textbf{GitHub Username} & \textbf{A1} & \textbf{A2} & \textbf{A3} & \textbf{A4} & \textbf{A5} & \textbf{A6} & \textbf{A7} \\
\hline
\endfirsthead

\hline
\textbf{Team Member (Last Name, First Name)} & \textbf{GitHub Username} & \textbf{A1} & \textbf{A2} & \textbf{A3} & \textbf{A4} & \textbf{A5} & \textbf{A6} & \textbf{A7} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

Benigno Montero, Harold Fauskorp & harold-11 & L & C & L & C & --- & --- & C \\
\hline
Osorio Ramírez, Eduardo Jesús & Iron819 & C & L & C & --- & --- & --- & --- \\
\hline
Rodriguez Gonzales, Leonel German & leokiss15 & --- & C & C & L & C & --- & --- \\
\hline
Salon Puerta, Merly & MerlySalonP & --- & --- & --- & C & L & C & --- \\
\hline
Said Conde, Yazid & BL4Z3K4D & C & C & --- & --- & --- & C & L \\
\hline
Tello Quispe, Luis German & luistello1739-web & --- & --- & --- & --- & C & L & C \\
\end{longtable}
\endgroup

Table: Leadership-and-Collaboration Matrix (LACX) del Sprint 1

#### 5.2.1.3. Sprint Backlog 1

El objetivo principal del Sprint 1 es entregar la primera versión desplegada de la Landing Page de VitaLink, cubriendo las seis historias de usuario del épico EP-01 y la historia técnica TS-01 correspondiente a la configuración del repositorio y del entorno de publicación. En esta sección se descomponen dichas historias en work-items ejecutables. La gestión del Sprint Backlog se realiza en Jira, dentro del tablero Scrum del proyecto `VTL` (CodeBrokers), en el sprint denominado **Sprint 1 - Landing Page**, con fechas del 24/08/2026 al 15/09/2026.

**URL del Sprint Backlog en Jira:** \href{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1/backlog}{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1/backlog}

\includegraphics[width=0.9\linewidth]{assets/521-sprint-backlog-jira.png}

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.05\textwidth}|p{0.15\textwidth}|p{0.05\textwidth}|p{0.16\textwidth}|p{0.30\textwidth}|p{0.05\textwidth}|p{0.13\textwidth}|p{0.05\textwidth}|}
\hline
\textbf{User Story Id} & \textbf{User Story Title} & \textbf{Work-Item Id} & \textbf{Work-Item Title} & \textbf{Description} & \textbf{Est. (h)} & \textbf{Assigned To} & \textbf{Status} \\
\hline
\endfirsthead

\hline
\textbf{User Story Id} & \textbf{User Story Title} & \textbf{Work-Item Id} & \textbf{Work-Item Title} & \textbf{Description} & \textbf{Est. (h)} & \textbf{Assigned To} & \textbf{Status} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

US-01 & Propuesta de valor segmentada en Landing Page & WI-01 & Sección Hero con titulares segmentados & Maquetar el bloque principal con los titulares diferenciados para el segmento familiar y para el segmento de profesionales de la salud, acompañados de imagen de apoyo e indicadores de respaldo del servicio. & 3 & Osorio Ramírez, Eduardo Jesús & Done \\
\hline
US-01 & Propuesta de valor segmentada en Landing Page & WI-02 & Barra de navegación principal & Implementar la barra de navegación fija con anclajes a las secciones del sitio y el menú desplegable para la vista móvil. & 3 & Osorio Ramírez, Eduardo Jesús & Done \\
\hline
US-02 & Explicación del funcionamiento del sistema & WI-03 & Sección de ecosistema conectado para familias & Maquetar la sección que expone los cuatro pilares del servicio dirigidos al segmento familiar, explicando el funcionamiento del monitoreo de forma secuencial. & 3 & Benigno Montero, Harold Fauskorp & Done \\
\hline
US-02 & Explicación del funcionamiento del sistema & WI-04 & Sección de flujo clínico integrado & Maquetar la sección que describe el flujo clínico dirigido al profesional de la salud, desde la captura de datos hasta la intervención registrada. & 3 & Benigno Montero, Harold Fauskorp & Done \\
\hline
US-02 & Explicación del funcionamiento del sistema & WI-05 & Sección de protocolo de alerta inteligente & Implementar la sección que detalla el protocolo de escalamiento de alertas, con los niveles de urgencia y sus destinatarios. & 3 & Rodriguez Gonzales, Leonel German & Done \\
\hline
US-03 & Visualización de Planes y Suscripciones & WI-06 & Estructura y diseño de la sección de planes & Construir la estructura y el diseño base de la sección de tarifas, con el conmutador entre la vista familiar y la vista institucional. & 3 & Salon Puerta, Merly & Done \\
\hline
US-03 & Visualización de Planes y Suscripciones & WI-07 & Planes institucionales y familiares & Implementar las tarjetas de suscripción para ambos perfiles con sus precios, características incluidas y llamada a la acción por plan. & 3 & Salon Puerta, Merly & Done \\
\hline
US-04 & Sección de privacidad y seguridad de datos & WI-08 & Grid de seguridad y cumplimiento normativo & Maquetar la sección de seguridad de grado médico con cifrado de extremo a extremo, cumplimiento HIPAA y GDPR, y control de acceso por roles. & 3 & Tello Quispe, Luis German & Done \\
\hline
US-05 & Interfaz de captura de leads (Botones de acción) & WI-09 & Botón de conversión en el encabezado & Incorporar el botón de acción principal en la barra de navegación, con comportamiento fijo al desplazarse y anclaje a la sección de conversión. & 2 & Said Conde, Yazid & Done \\
\hline
US-05 & Interfaz de captura de leads (Botones de acción) & WI-10 & Sección de llamada a la acción final & Implementar la sección de cierre con los botones diferenciados de registro para familias y de incorporación para proveedores de salud. & 2 & Tello Quispe, Luis German & Done \\
\hline
US-06 & Mockups visuales del producto & WI-11 & Mockups ilustrativos del producto & Incorporar las imágenes del panel clínico en escritorio y de la notificación de alerta en dispositivo móvil, empleando datos claramente ficticios. & 3 & Osorio Ramírez, Eduardo Jesús & Done \\
\hline
TS-01 & Configuración del entorno y despliegue de la Landing Page & WI-12 & Estructura base del repositorio y hoja de estilos & Crear el repositorio de la Landing Page con la estructura para HTML, CSS y JS, e incorporar el reset de estilos y las variables del Style Guideline (4.1). & 3 & Said Conde, Yazid & Done \\
\hline
TS-01 & Configuración del entorno y despliegue de la Landing Page & WI-13 & Footer institucional y sección de equipo & Maquetar el pie de página con los enlaces legales y la sección de presentación del equipo de desarrollo. & 3 & Said Conde, Yazid & Done \\
\hline
TS-01 & Configuración del entorno y despliegue de la Landing Page & WI-14 & Despliegue en GitHub Pages y verificación & Configurar la publicación de la rama \texttt{main} en GitHub Pages, verificar la accesibilidad de la URL pública y la correcta visualización en los puntos de quiebre definidos. & 3 & Benigno Montero, Harold Fauskorp & Done \\
\end{longtable}
\endgroup

Table: Sprint Backlog 1

El esfuerzo total estimado para el Sprint 1 asciende a **40 horas**, distribuidas entre los seis integrantes del equipo, correspondientes a los 17 Story Points comprometidos.

#### 5.2.1.4. Development Evidence for Sprint Review

Durante el Sprint 1 el equipo CodeBrokers implementó la totalidad de la Landing Page de VitaLink en el repositorio `upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page`. El trabajo se organizó en ramas de característica integradas a `develop` mediante Pull Request revisado por un par, y consolidadas finalmente en `main`, rama que alimenta el despliegue en GitHub Pages. La tabla siguiente recoge los commits integrados en `main` durante el periodo del sprint, obtenidos directamente del historial del repositorio.

**Repositorio:** \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page}{upc-pre-202620-1asi0730-16712-CodeBrokers-Landing\_Page}

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.17\textwidth}|p{0.22\textwidth}|p{0.08\textwidth}|p{0.33\textwidth}|p{0.12\textwidth}|}
\hline
\textbf{Repository} & \textbf{Branch} & \textbf{Commit Id} & \textbf{Commit Message} & \textbf{Committed on} \\
\hline
\endfirsthead

\hline
\textbf{Repository} & \textbf{Branch} & \textbf{Commit Id} & \textbf{Commit Message} & \textbf{Committed on} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

CodeBrokers-Landing\_Page & main & 96150d0 & chore: initial commit. & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & main & 84f823d & feat: add the logo. & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/navbar-hero & 37348ae & feat: add navigation bar and hero section & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/navbar-hero & 9a747fc & feat: add hero image & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & develop & c15fe12 & Merge pull request \#1 from feat/navbar-hero & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & fix/remove-css-comment & d84c61d & fix: remove css comment & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & fix/remove-css-comment & b0513c7 & fix: remove css comment & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & develop & c56a4f2 & Merge pull request \#2 from fix/remove-css-comment & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/family-and-clinical-sections & aaab1b8 & feat(sections): add family ecosystem, monitoring, and clinical workflow sections & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/family-and-clinical-sections & 8c97a40 & merge: resolve conflicts with develop & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & develop & 30983be & Merge pull request \#3 from feat/family-and-clinical-sections & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/alert-protocol-and-pricing & 2774130 & feat(sections): add intelligent alert protocol and pricing plans & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/alert-protocol-and-pricing & 336b815 & feat(sections): add intelligent alert protocol and pricing plans & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/alert-protocol-and-pricing & dfae28e & feat(sections): add intelligent alert protocol and pricing plans & 10/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/alert-protocol-and-pricing & a624b41 & feat(sections): add intelligent alert protocol and pricing plans & 11/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/alert-protocol-and-pricing & e908fb8 & feat(sections): add intelligent alert protocol and pricing plans & 11/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/alert-protocol-and-pricing & 9cde198 & feat(sections): add intelligent alert protocol and pricing plans & 11/09/2026 \\
\hline
CodeBrokers-Landing\_Page & develop & f95559f & Merge pull request \#4 from feat/alert-protocol-and-pricing & 11/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/pricing-tiers-and-testimonials & 7f184c0 & feat: structure for plans and pricing added & 13/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/pricing-tiers-and-testimonials & d36b8ad & feat: design for plans and pricing added & 13/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/pricing-tiers-and-testimonials & 3a1c8ed & feat: add institutional and patient pricing tiers & 13/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/pricing-tiers-and-testimonials & 8011e43 & Removal of closing tags to prevent bugs & 13/09/2026 \\
\hline
CodeBrokers-Landing\_Page & develop & 786e2c6 & Merge pull request \#7 from feat/pricing-tiers-and-testimonials & 13/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feat/testimonials-security-and-cta & a1b9cde & feat(sections): add testimonials cards, security compliance grid, and final CTA section & 13/09/2026 \\
\hline
CodeBrokers-Landing\_Page & feature/team-members & caceaa9 & feat(footer): add the footer and restructure design. & 15/09/2026 \\
\hline
CodeBrokers-Landing\_Page & develop & 6b0d1ee & Merge pull request \#8 from feature/team-members & 15/09/2026 \\
\hline
CodeBrokers-Landing\_Page & main & 74acdf0 & Merge pull request \#9 from develop & 15/09/2026 \\
\end{longtable}
\endgroup

Table: Development Evidence del Sprint 1

**Resumen de la actividad de desarrollo**

| Métrica | Valor |
| :--- | :--- |
| Commits integrados en `main` | 27 |
| Ramas de característica creadas | 6 |
| Pull Requests integrados | 6 |
| Periodo cubierto | 10/09/2026 – 15/09/2026 |
| Integrantes con contribuciones registradas | 6 de 6 |
| Commit de cierre del incremento | 74acdf0 (15/09/2026) |

Table: Resumen de la actividad de desarrollo del Sprint 1

De forma paralela, el equipo desarrolló los Capítulos I al IV del informe en el repositorio `upc-pre-202620-1asi0730-16712-CodeBrokers-report-`, cuyo historial registra 82 commits adicionales en el periodo del 28/08/2026 al 15/09/2026, distribuidos en 19 ramas de característica.

#### 5.2.1.5. Execution Evidence for Sprint Review

Al cierre del Sprint 1 la Landing Page de VitaLink se encuentra implementada y desplegada en su totalidad. El incremento entregado comprende una página estática de navegación continua, construida en HTML5, CSS3 y JavaScript, con contenido diferenciado para los dos segmentos objetivo y comportamiento adaptativo verificado en los puntos de quiebre definidos en la sección 4.1.

Las vistas implementadas y verificadas en este Sprint son las siguientes:

- **Hero y barra de navegación.** Presenta la propuesta de valor con los titulares diferenciados por segmento y los indicadores de respaldo del servicio. La barra de navegación permanece fija durante el desplazamiento y colapsa en menú desplegable en la vista móvil.
- **Ecosistema conectado y flujo clínico.** Explica el funcionamiento del servicio mediante los cuatro pilares dirigidos al segmento familiar y el flujo clínico integrado dirigido al profesional de la salud.
- **Protocolo de alerta inteligente.** Detalla los niveles de urgencia de las alertas y sus destinatarios dentro de la red de cuidado.
- **Planes y suscripciones.** Muestra las tarjetas de suscripción para el perfil familiar y para el perfil institucional, con sus precios y características incluidas.
- **Testimonios y seguridad de datos.** Reúne los testimonios de usuarios y la sección de seguridad de grado médico, con cifrado de extremo a extremo, cumplimiento HIPAA y GDPR, y control de acceso por roles.
- **Llamada a la acción y footer.** Cierra la página con los botones de conversión diferenciados por segmento, el pie de página con los enlaces legales y la presentación del equipo de desarrollo.

**URL de la Landing Page desplegada:** \href{https://1asi0730-2620-16712-grupo2-codebrokers.github.io/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page/}{https://1asi0730-2620-16712-grupo2-codebrokers.github.io/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing\_Page/}

\includegraphics[width=0.8\linewidth]{assets/525-execution-hero.png}

\includegraphics[width=0.8\linewidth]{assets/525-execution-planes.png}

\includegraphics[width=0.8\linewidth]{assets/525-execution-seguridad.png}

#### 5.2.1.6. Services Documentation Evidence for Sprint Review

**No aplica para el Sprint 1.**

El alcance comprometido en el Sprint 1 corresponde al épico EP-01 (Landing Page) y a la historia técnica TS-01, cuyo resultado es una página estática implementada en HTML5, CSS3 y JavaScript. Este incremento no consume ni expone servicios web, por lo que no existen endpoints que documentar en esta etapa.

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

Durante este Sprint el equipo completó la implementación de la Landing Page y llevó a cabo su publicación mediante **GitHub Pages**, aprovechando su integración directa con el repositorio y la disponibilidad de HTTPS sin configuración adicional de infraestructura.

Las actividades realizadas fueron las siguientes:

1. Se creó la organización de GitHub del equipo: \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers}{1ASI0730-2620-16712-grupo2-CodeBrokers}, y dentro de ella el repositorio de la Landing Page.
2. Se cargó el código fuente de la Landing Page, incorporando los archivos `index.html`, `styles.css`, `script.js` y el directorio `assets/` con los recursos gráficos del sitio.
3. Se integraron las seis ramas de característica a `develop` mediante Pull Request revisado, y se consolidó el incremento en `main` mediante el Pull Request \#9 (commit `74acdf0`, 15/09/2026).
4. Se habilitó GitHub Pages desde **Settings > Pages**, configurando la rama `main` como fuente de despliegue y la carpeta raíz del repositorio como directorio de publicación.
5. Se etiquetó el incremento como **v1.0.0**, siguiendo la política de versionado semántico establecida en la sección 5.1.2, y se publicó el Release correspondiente en GitHub.
6. Se validó la disponibilidad de la publicación accediendo a la URL pública y verificando la correcta visualización en escritorio y en dispositivo móvil.

**Landing Page desplegada:** \href{https://1asi0730-2620-16712-grupo2-codebrokers.github.io/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page/}{https://1asi0730-2620-16712-grupo2-codebrokers.github.io/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing\_Page/}

**Evidencia del despliegue:**

\includegraphics[width=0.8\linewidth]{assets/vista-page.png}

\includegraphics[width=0.8\linewidth]{assets/527-deployment-landing-publicada.png}

#### 5.2.1.8. Team Collaboration Insights during Sprint

En esta sección se presenta la participación de cada integrante en el repositorio de la Landing Page durante el Sprint 1. Los seis miembros del equipo registraron commits y Pull Requests, cubriendo en conjunto la totalidad de las secciones comprometidas. La organización del trabajo siguió la asignación de aspectos definida en la sección 5.2.1.2, de modo que cada integrante lideró al menos una sección del sitio y colaboró en la revisión de las restantes.

\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.26\textwidth}|p{0.18\textwidth}|p{0.48\textwidth}|}
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{Contribución principal en el Sprint 1} \\
\hline
\endfirsthead

\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{Contribución principal en el Sprint 1} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

Said Conde, Yazid & BL4Z3K4D & Estructura base del repositorio, logotipo, footer institucional y sección de equipo de desarrollo. \\
\hline
Osorio Ramírez, Eduardo Jesús & Iron819 & Barra de navegación, sección Hero, imagen principal y mockups ilustrativos del producto. \\
\hline
Benigno Montero, Harold Fauskorp & harold-11 & Sección de ecosistema conectado para familias, flujo clínico integrado y despliegue en GitHub Pages. \\
\hline
Rodriguez Gonzales, Leonel German & leokiss15 & Sección de protocolo de alerta inteligente y apoyo en la estructura de planes. \\
\hline
Salon Puerta, Merly & MerlySalonP & Estructura y diseño de la sección de planes, tarifas institucionales y familiares. \\
\hline
Tello Quispe, Luis German & luistello1739-web & Testimonios, grid de seguridad y cumplimiento normativo, y sección de llamada a la acción final. \\
\end{longtable}
\endgroup

Table: Contribuciones por integrante durante el Sprint 1

**Capturas de Insights del repositorio:**

\includegraphics[width=0.8\linewidth]{assets/insigh.png}

\includegraphics[width=0.8\linewidth]{assets/528-insights-commits.png}


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




