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

\begingroup
\centering
\small
\setlength{\tabcolsep}{6pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.45\textwidth}|p{0.40\textwidth}|}
\hline
\textbf{Métrica} & \textbf{Valor} \\
\hline
\endfirsthead

\hline
\textbf{Métrica} & \textbf{Valor} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

Commits integrados en \texttt{main} & 27 \\
\hline
Ramas de característica creadas & 6 \\
\hline
Pull Requests integrados & 6 \\
\hline
Periodo cubierto & 10/09/2026 – 15/09/2026 \\
\hline
Integrantes con contribuciones registradas & 6 de 6 \\
\hline
Commit de cierre del incremento & \texttt{74acdf0} (15/09/2026) \\
\end{longtable}
\endgroup

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

\begingroup
\centering
\small
\setlength{\tabcolsep}{6pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.20\textwidth}|p{0.55\textwidth}|p{0.18\textwidth}|}
\hline
\textbf{Bounded Context} & \textbf{Endpoints previstos} & \textbf{Sprint de implementación} \\
\hline
\endfirsthead

\hline
\textbf{Bounded Context} & \textbf{Endpoints previstos} & \textbf{Sprint de implementación} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

Profiles & \texttt{/api/v1/older-adults}, \texttt{/api/v1/care-providers}, \texttt{/api/v1/family-caregivers} & Sprint 2 \\
\hline
Monitoring & \texttt{/api/v1/health-records}, \texttt{/api/v1/record-types} & Sprint 2 \\
\hline
Alerting & \texttt{/api/v1/alerts}, \texttt{/api/v1/alerts/\{id\}/status} & Sprint 2 \\
\hline
Care Assignment & \texttt{/api/v1/assignments} & Sprint 3 \\
\hline
Notification & \texttt{/api/v1/notifications} & Sprint 3 \\
\end{longtable}
\endgroup

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

El Sprint 2 tuvo como propósito construir la primera versión funcional de la Frontend Web Application de VitaLink. El alcance se concentró en las experiencias de profesionales de la salud y familiares cuidadores, empleando Vue 3 y un servicio REST simulado para representar la información de pacientes, alertas, registros de salud e intervenciones. El equipo seleccionó once elementos del Product Backlog y acordó integrarlos mediante ramas de característica y Pull Requests hacia `develop`.

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
\textbf{Sprint \#} & Sprint 2 \\
\hline
\textbf{Date} & 2026-10-02 \\
\hline
\textbf{Time} & 19:00 (GMT-5) \\
\hline
\textbf{Location} & Reunión remota vía Discord \\
\hline
\textbf{Prepared By} & Benigno Montero, Harold Fauskorp \\
\hline
\textbf{Attendees (to planning meeting)} & Osorio Ramírez, Eduardo Jesús; Said Conde, Yazid; Tello Quispe, Luis German; Rodriguez Gonzales, Leonel German; Salon Puerta, Merly; Benigno Montero, Harold Fauskorp \\
\hline
\textbf{Sprint 1 Review Summary} & El Sprint 1 concluyó con la Landing Page de VitaLink implementada y publicada. El Product Backlog, los diseños de las aplicaciones web y la arquitectura de software quedaron preparados como base para iniciar el primer incremento de la Frontend Web Application. \\
\hline
\textbf{Sprint 1 Retrospective Summary} & El equipo acordó reducir las integraciones de último momento, mantener una rama por elemento del backlog, revisar cada Pull Request antes del merge y conservar trazabilidad entre Jira, los commits y las evidencias del informe. \\
\hline
\textbf{Sprint 2 Goal} & \textbf{Our focus is on} implementar la primera versión navegable de la aplicación web para profesionales de la salud y familiares cuidadores. \newline\newline \textbf{We believe it delivers} acceso centralizado a alertas, detalle e historial de pacientes, seguimiento familiar y preferencias de comunicación. \newline\newline \textbf{This will be confirmed when} los usuarios puedan cambiar de rol, navegar entre las vistas comprometidas, consultar los datos expuestos por el servicio REST simulado y utilizar la interfaz en inglés o español con soporte básico de accesibilidad. \\
\hline
\textbf{Sprint 2 Velocity} & 37 Story Points \\
\hline
\textbf{Sum of Story Points} & 37 Story Points \\
\end{longtable}
\endgroup

Table: Sprint Planning 2

El sprint se ejecutó del 2 al 5 de octubre de 2026. Los 37 Story Points comprometidos alcanzaron el estado **Finalizado** al cierre, incluyendo dos historias técnicas transversales y nueve historias de usuario distribuidas entre los perfiles profesional y familiar.


#### 5.2.2.2. Aspect Leaders and Collaborators

Los aspectos se organizaron según las capacidades funcionales y transversales del incremento: **A1.** Fundamentos y capa compartida, **A2.** Alertas y detalle profesional, **A3.** Historial y revisiones, **A4.** Panel y seguimiento familiar, **A5.** Pacientes asignados y preferencias, y **A6.** Internacionalización y accesibilidad. La letra L identifica al líder del aspecto y la letra C a quienes colaboraron en su implementación o revisión.

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.28\textwidth}|p{0.17\textwidth}|c|c|c|c|c|c|}
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{A1} & \textbf{A2} & \textbf{A3} & \textbf{A4} & \textbf{A5} & \textbf{A6} \\
\hline
\endfirsthead
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{A1} & \textbf{A2} & \textbf{A3} & \textbf{A4} & \textbf{A5} & \textbf{A6} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Benigno Montero, Harold Fauskorp & harold-11 & L & L & C & --- & --- & C \\
\hline
Said Conde, Yazid & BL4Z3K4D & C & C & --- & --- & --- & --- \\
\hline
Salon Puerta, Merly & MerlySalonP & --- & C & L & --- & --- & --- \\
\hline
Osorio Ramírez, Eduardo Jesús & Iron819 & --- & --- & --- & L & C & --- \\
\hline
Tello Quispe, Luis German & luistello1739-web & --- & --- & --- & C & L & C \\
\hline
Rodriguez Gonzales, Leonel German & leokiss15 & C & --- & C & --- & C & L \\
\end{longtable}
\endgroup

Table: Leadership-and-Collaboration Matrix (LACX) del Sprint 2


#### 5.2.2.3. Sprint Backlog 2

El Sprint Backlog 2 reúne once actividades asociadas a los épicos de Frontend Web Application. La planificación y el control de estados se realizaron en Jira, en el sprint **Sprint 2 - Frontend** del proyecto VTL. La captura siguiente registra las once actividades en estado finalizado; la tabla posterior transcribe su contenido para mantener el artefacto legible y trazable dentro del informe.

**URL del Sprint Backlog en Jira:** \href{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1/backlog}{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1/backlog}

\includegraphics[width=0.92\linewidth]{assets/522-sprint2-completed-items.png}

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.25}

\begin{longtable}{|p{0.07\textwidth}|p{0.23\textwidth}|p{0.07\textwidth}|p{0.30\textwidth}|p{0.06\textwidth}|p{0.15\textwidth}|p{0.07\textwidth}|}
\hline
\textbf{Story Id} & \textbf{Story Title} & \textbf{Work Item} & \textbf{Description} & \textbf{Est. (SP)} & \textbf{Assigned To} & \textbf{Status} \\
\hline
\endfirsthead
\hline
\textbf{Story Id} & \textbf{Story Title} & \textbf{Work Item} & \textbf{Description} & \textbf{Est. (SP)} & \textbf{Assigned To} & \textbf{Status} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
TS-02 & Configuración base de la Frontend Web Application & VTL-66 & Configurar Vue, Vite, PrimeVue, Router, Pinia, Axios, i18n, variables de entorno y la capa compartida. & 3 & Benigno Montero, Harold Fauskorp & Done \\
\hline
US-07 & Resumen inicial de alertas pendientes & VTL-36 & Presentar el resumen profesional con alertas pendientes y sus datos principales. & 5 & Benigno Montero, Harold Fauskorp & Done \\
\hline
US-08 & Nivel de urgencia visual en cada alerta & VTL-38 & Mostrar y ordenar alertas según prioridad alta, media o baja. & 3 & Said Conde, Yazid & Done \\
\hline
US-09 & Acceso al detalle de paciente desde el resumen & VTL-39 & Permitir la navegación desde una alerta hacia el detalle del paciente relacionado. & 3 & Said Conde, Yazid & Done \\
\hline
US-13 & Visibilidad de revisión previa por otro profesional & VTL-44 & Presentar el historial de intervenciones y la revisión profesional asociada a la alerta. & 2 & Salon Puerta, Merly & Done \\
\hline
US-10 & Historial de registros del paciente ordenado por fecha & VTL-48 & Consultar y filtrar registros de salud ordenados desde el más reciente. & 5 & Salon Puerta, Merly & Done \\
\hline
US-21 & Panel visual del estado general & VTL-50 & Mostrar al familiar las últimas mediciones y alertas abiertas del adulto mayor. & 3 & Osorio Ramírez, Eduardo Jesús & Done \\
\hline
US-23 & Visualización de información centralizada & VTL-52 & Centralizar mediciones y casos que requieren seguimiento en la vista familiar. & 2 & Osorio Ramírez, Eduardo Jesús & Done \\
\hline
US-28 & Búsqueda y selección de pacientes asignados & VTL-59 & Permitir al profesional buscar y abrir los pacientes bajo su responsabilidad. & 3 & Tello Quispe, Luis German & Done \\
\hline
US-33 & Preferencias de idioma y notificaciones & VTL-64 & Configurar idioma y canales de notificación guardados en el navegador. & 3 & Tello Quispe, Luis German & Done \\
\hline
TS-05 & Internacionalización y accesibilidad de la Web Application & VTL-69 & Incorporar locales en\_US y es\_419, atributos ARIA, estados accesibles y soporte de navegación por teclado. & 5 & Rodriguez Gonzales, Leonel German & Done \\
\end{longtable}
\endgroup

Table: Sprint Backlog 2

El esfuerzo total comprometido y completado fue de **37 Story Points**. La trazabilidad se conserva mediante las claves VTL de Jira, las ramas de característica y los commits incluidos en la sección siguiente.


#### 5.2.2.4. Development Evidence for Sprint Review

La Frontend Web Application se implementó en el repositorio público `upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application`. El equipo creó una rama por capacidad, integró once Pull Requests en `develop` y posteriormente consolidó el incremento en `main` mediante el Pull Request \#12. El historial de `main` contiene 24 commits del Sprint 2; la tabla siguiente recoge los commits funcionales que identifican cada aporte y el commit de integración de la entrega.

**Repositorio:** \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application}{upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application}

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.25}

\begin{longtable}{|p{0.19\textwidth}|p{0.24\textwidth}|p{0.08\textwidth}|p{0.35\textwidth}|p{0.09\textwidth}|}
\hline
\textbf{Repository} & \textbf{Branch} & \textbf{Commit Id} & \textbf{Commit Message} & \textbf{Date} \\
\hline
\endfirsthead
\hline
\textbf{Repository} & \textbf{Branch} & \textbf{Commit Id} & \textbf{Commit Message} & \textbf{Date} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Frontend Application & feature/frontend-foundation & 0060569 & chore(frontend): configure Vue application foundation & 04/10/2026 \\
\hline
Frontend Application & feature/frontend-foundation & a4c53b4 & fix(frontend): align foundation and add shared layer & 05/10/2026 \\
\hline
Frontend Application & feature/pending-alerts-summary & b13b231 & feat(alerting): add pending alerts overview & 05/10/2026 \\
\hline
Frontend Application & feature/alert-priority & 02f8398 & feat(alerting): display and sort alert priorities & 05/10/2026 \\
\hline
Frontend Application & feature/patient-detail & 5111528 & feat(elder-care): open patient details from alerts & 05/10/2026 \\
\hline
Frontend Application & feature/review-visibility & 1af0de3 & feat(care-coordination): show previous professional reviews & 04/10/2026 \\
\hline
Frontend Application & feature/patient-health-history & f48f212 & feat(preventive-monitoring): add ordered patient history & 04/10/2026 \\
\hline
Frontend Application & feature/family-overview & 59823ce & feat(elder-care): add family care overview & 05/10/2026 \\
\hline
Frontend Application & feature/family-case-follow-up & 901ea93 & feat(care-coordination): add family case follow-up & 05/10/2026 \\
\hline
Frontend Application & feature/assigned-patient-search & 753b4bb & feat(elder-care): add assigned patient search & 05/10/2026 \\
\hline
Frontend Application & feature/notification-preferences & 3df9516 & feat(notification): add language and notification preferences & 05/10/2026 \\
\hline
Frontend Application & feature/i18n-accessibility & b7c5007 & feat(shared): strengthen i18n and accessibility support & 05/10/2026 \\
\hline
Frontend Application & main & 630720e & Merge pull request \#12 from develop & 05/10/2026 \\
\end{longtable}
\endgroup

Table: Development Evidence del Sprint 2

La revisión final confirmó que las diez primeras ramas de característica ya estaban contenidas en `develop` y que `feature/i18n-accessibility` fue integrada mediante el Pull Request \#11 antes de consolidar `develop` en `main`.

El incremento se publicó como el release estable **v0.2.11 — TB1**, asociado a `main`: \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application/releases/tag/v0.2.11}{VitaLink Frontend v0.2.11 — TB1}.


#### 5.2.2.5. Execution Evidence for Sprint Review

La aplicación se ejecutó localmente con Vite 7.3.6 y consumió el servicio REST simulado mediante Axios. La verificación de producción se realizó con `npm run build`: Vite transformó 264 módulos y generó correctamente el directorio `dist` en 1.74 segundos, sin errores de compilación.

Las principales capacidades verificadas fueron las siguientes:

- **Resumen profesional de cuidado.** Presenta contadores de alertas, filtros por estado y prioridad, y navegación hacia el paciente relacionado.
- **Detalle e historial del paciente.** Muestra alertas, prioridad, estado, fecha, historial de intervenciones y registros clínicos ordenados por fecha.
- **Panel familiar.** Permite seleccionar al adulto mayor, consultar sus últimas mediciones y revisar casos pendientes o en seguimiento.
- **Pacientes asignados.** Permite buscar y seleccionar pacientes bajo responsabilidad del profesional.
- **Preferencias e internacionalización.** Conserva idioma y preferencias de notificación en el navegador, con soporte para English (`en_US`) y Latin American Spanish (`es_419`).
- **Accesibilidad.** Incorpora atributos ARIA, foco visible, navegación por teclado, estados de carga y vacío anunciables, y etiquetas de idioma equivalentes para el navegador.

**Resumen profesional de alertas:**

\includegraphics[width=0.92\linewidth]{assets/522-sprint2-professional-dashboard.png}

**Detalle del familiar: últimas mediciones y casos para seguir:**

\includegraphics[width=0.92\linewidth]{assets/522-sprint2-patient-detail.png}

**Panel del familiar cuidador:**

\includegraphics[width=0.92\linewidth]{assets/522-sprint2-family-dashboard.png}

**Selector de idioma y vista en inglés:**

\includegraphics[width=0.82\linewidth]{assets/522-sprint2-preferences.png}


#### 5.2.2.6. Services Documentation Evidence for Sprint Review

El alcance del TB1 corresponde a la primera Frontend Web Application; los Web Services propios en ASP.NET Core se implementarán en un sprint posterior. Para permitir la ejecución integrada del frontend, el equipo configuró un servicio REST local mediante JSON Server 0.17.4. El archivo `server/routes.json` expone los recursos bajo el prefijo `/api/v1`, mientras `server/db.json` conserva la información empleada por las vistas.

\begingroup
\centering
\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.16\textwidth}|p{0.30\textwidth}|p{0.45\textwidth}|}
\hline
\textbf{Method} & \textbf{Endpoint} & \textbf{Uso en la aplicación} \\
\hline
\endfirsthead
\hline
\textbf{Method} & \textbf{Endpoint} & \textbf{Uso en la aplicación} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
GET & /api/v1/patients & Lista, búsqueda, selección y detalle de pacientes. \\
\hline
GET & /api/v1/patients/:id & Consulta individual del paciente seleccionado. \\
\hline
GET & /api/v1/alerts & Alertas de cuidado, prioridad, estado y asociación con pacientes. \\
\hline
GET & /api/v1/records & Historial de mediciones y registros de salud. \\
\hline
GET & /api/v1/interventions & Revisiones e intervenciones asociadas a las alertas. \\
\end{longtable}
\endgroup

Table: Recursos del servicio REST simulado del Sprint 2

El servicio se inicia desde el directorio `server` mediante `sh start.sh`, cuyo comando ejecuta `npx json-server --watch db.json --routes routes.json`. Esta evidencia no reemplaza la documentación OpenAPI requerida para los Web Services definitivos; documenta únicamente el contrato simulado utilizado por el frontend durante el Sprint 2.


#### 5.2.2.7. Software Deployment Evidence for Sprint Review

El incremento se consolidó en la rama `main` mediante el commit `630720e` y se etiquetó con la versión semántica `v0.2.11`. La publicación del release estable permite identificar de forma inmutable el código correspondiente al TB1 y descargar sus artefactos fuente desde GitHub.

\begingroup
\centering
\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.27\textwidth}|p{0.64\textwidth}|}
\hline
\textbf{Elemento} & \textbf{Evidencia} \\
\hline
\endfirsthead
\hline
\textbf{Elemento} & \textbf{Evidencia} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Repositorio & \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application}{Frontend Web Application} \\
\hline
Rama de entrega & `main`, commit `630720e` \\
\hline
Release & \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application/releases/tag/v0.2.11}{v0.2.11 — TB1} \\
\hline
Validación de build & `npm run build`: 264 módulos transformados; compilación completada en 1.74 s. \\
\hline
Frontend desplegado & \href{https://vitalink-opal.vercel.app}{https://vitalink-opal.vercel.app} (Vercel, rama \texttt{main}) \\
\hline
Servicio REST simulado desplegado & \href{https://vitalink-api-m3uk.onrender.com/api/v1}{https://vitalink-api-m3uk.onrender.com/api/v1} (JSON Server en Render) \\
\end{longtable}
\endgroup

Table: Evidencias de release y despliegue del Sprint 2

La aplicación está preparada para consumir una URL configurable mediante `VITE_API_BASE_URL`. Para la publicación, el frontend se despliega como sitio estático generado por Vite y el JSON Server se publica en un servicio capaz de ejecutar procesos Node.js. Las dos URL públicas deben reemplazar los campos pendientes de la tabla antes de exportar la versión final del informe TB1.


#### 5.2.2.8. Team Collaboration Insights during Sprint

La colaboración se evidenció mediante ramas individuales, once Pull Requests hacia `develop`, una integración de `develop` a `main` y un release estable. Los seis integrantes registraron aportes identificables en el historial. La autoría de commits y la asignación en Jira no siempre coinciden de forma individual, debido a revisiones, integración y apoyo cruzado entre responsables; por ello, la evaluación considera tanto el liderazgo funcional como la evidencia registrada en GitHub.

\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.26\textwidth}|p{0.18\textwidth}|p{0.48\textwidth}|}
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{Contribución principal en el Sprint 2} \\
\hline
\endfirsthead
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{Contribución principal en el Sprint 2} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Benigno Montero, Harold Fauskorp & harold-11 & Capa compartida, resumen y prioridad de alertas, detalle de pacientes, integración de ramas, verificación y release del incremento. \\
\hline
Said Conde, Yazid & BL4Z3K4D & Inicialización del repositorio y configuración base de la aplicación Vue. \\
\hline
Salon Puerta, Merly & MerlySalonP & Visibilidad de revisiones profesionales e historial de salud ordenado por fecha. \\
\hline
Osorio Ramírez, Eduardo Jesús & Iron819 & Panel de estado general para familiares y seguimiento centralizado de casos. \\
\hline
Tello Quispe, Luis German & luistello1739-web & Búsqueda de pacientes asignados y preferencias de idioma y notificaciones. \\
\hline
Rodriguez Gonzales, Leonel German & leokiss15 & Internacionalización, accesibilidad, documentación técnica y revisión final de la experiencia compartida. \\
\end{longtable}
\endgroup

Table: Contribuciones por integrante durante el Sprint 2

**Captura de Insights del repositorio:**

\includegraphics[width=0.82\linewidth]{assets/522-sprint2-github-insights.png}

La analítica de GitHub confirma contribuciones de los seis integrantes durante octubre de 2026. Esta evidencia complementa la tabla anterior al mostrar la cantidad de commits y el volumen de líneas agregadas y eliminadas asociado a cada cuenta del equipo.

**Evolución del trabajo pendiente:**

\includegraphics[width=0.92\linewidth]{assets/522-sprint2-burndown.png}

La gráfica registra el cierre de los 37 Story Points al finalizar el sprint. También evidencia que la actualización de estados se concentró al final del periodo, en lugar de reflejar una reducción progresiva diaria. Como acción de mejora, el equipo acordó actualizar Jira al completar cada actividad y no únicamente durante el cierre, de modo que el siguiente burndown represente con mayor fidelidad el avance real y facilite la detección temprana de bloqueos.


### 5.2.3. Sprint 3

#### 5.2.3.1. Sprint Planning 3

El Sprint 3 tiene como propósito construir y desplegar la primera versión de los RESTful Web Services de VitaLink, desarrollados con ASP.NET Core, Entity Framework Core y C# sobre PostgreSQL, e integrar la Web Application con dichos servicios en reemplazo del servicio REST simulado del Sprint 2. El alcance incluye la persistencia de pacientes, registros de salud y alertas, el ciclo de atención de alertas, el inicio de sesión con navegación por rol, la documentación OpenAPI vía Swagger y la integración con un servicio externo de terceros para el envío de notificaciones por correo.

El sprint se desarrolla del 25 de octubre al 9 de noviembre de 2026, según el sprint **Sprint 3 - Web Services** registrado en Jira. Al tratarse del penúltimo sprint, el equipo comprometió aproximadamente la mitad del Product Backlog pendiente: 53 de los 106 Story Points restantes. La selección consideró el avance del sílabo del curso hasta la entrega del AV2; por ello, el endurecimiento de la seguridad (TS-04) y las pruebas unitarias y de integración de los Web Services se programaron para el Sprint 4, ya que sus temas (Web Services Security - Part 2 y Best Practices) se desarrollan entre las semanas 13 y 16.

\begingroup
\centering
\small
\setlength{\tabcolsep}{6pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.28\textwidth}|p{0.65\textwidth}|}
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
\textbf{Sprint \#} & Sprint 3 \\
\hline
\textbf{Date} & 2026-10-25 \\
\hline
\textbf{Time} & 21:15 -- 21:57 (GMT-5) \\
\hline
\textbf{Location} & Reunión remota vía Microsoft Teams \\
\hline
\textbf{Prepared By} & Benigno Montero, Harold Fauskorp \\
\hline
\textbf{Attendees (to planning meeting)} & Benigno Montero, Harold Fauskorp; Osorio Ramírez, Eduardo Jesús; Tello Quispe, Luis German; Salon Puerta, Merly; Said Conde, Yazid. No asistió: Rodriguez Gonzales, Leonel German. \\
\hline
\textbf{Sprint 2 Review Summary} & El Sprint 2 concluyó con los 37 Story Points comprometidos en estado finalizado. Se desplegó la primera versión de la Frontend Web Application, desarrollada con Vue 3 y PrimeVue, con las vistas para profesionales de la salud y familiares cuidadores, internacionalización en inglés y español y soporte de accesibilidad, consumiendo un servicio REST simulado. \\
\hline
\textbf{Sprint 2 Retrospective Summary} & El equipo identificó que los estados de Jira se actualizaron al cierre del sprint, por lo que el burndown no reflejó el avance real. Se acordó mover cada tarea el mismo día en que cambia de estado, mantener una rama por elemento del backlog y revisar cada Pull Request por otro integrante antes de integrarlo en \texttt{develop}. \\
\hline
\textbf{Sprint 3 Goal} & \textbf{Our focus is on} que profesionales de la salud y familiares cuidadores trabajen con datos reales persistidos mediante la API RESTful de VitaLink. \newline\newline \textbf{We believe it delivers} alertas, historial de salud y asociación paciente-proveedor confiables, además de avisos por correo ante eventos críticos. \newline\newline \textbf{This will be confirmed when} un profesional de la salud consulta en la Web Application desplegada una alerta generada por la API a partir de un registro de salud, la marca como en revisión o atendida, y el familiar recibe el correo de aviso del servicio externo. \\
\hline
\textbf{Sprint 3 Velocity} & 53 Story Points \\
\hline
\textbf{Sum of Story Points} & 53 Story Points \\
\end{longtable}
\endgroup

Table: Sprint Planning 3

La reunión se realizó el 25 de octubre de 2026 en Microsoft Teams, con la asistencia de cinco de los seis integrantes. Las capturas siguientes registran el inicio (21:15) y el cierre (21:57) de la reunión con los participantes visibles.

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-planning-start.png}

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-planning-end.png}

Durante el Sprint Planning, el equipo revisó la descomposición de cada elemento del backlog en tareas, acordó los responsables y estimó en horas cada tarea, con un máximo de 8 horas por tarea; ninguna tarea superó ese límite, por lo que no fue necesario dividirlas. Además, se programaron cuatro reuniones de seguimiento del sprint en Microsoft Teams, registradas con capturas de inicio y cierre en las que se identifican los participantes.

\begingroup
\centering
\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.04\textwidth}|p{0.25\textwidth}|p{0.22\textwidth}|p{0.40\textwidth}|}
\hline
\textbf{\#} & \textbf{Reunión} & \textbf{Fecha y hora} & \textbf{Objetivo} \\
\hline
\endfirsthead
\hline
\textbf{\#} & \textbf{Reunión} & \textbf{Fecha y hora} & \textbf{Objetivo} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
1 & Sprint Planning 3 & 2026-10-25, 21:15--21:57 & Definir el Sprint Goal, el alcance, los responsables y la estimación en horas de las tareas. \\
\hline
2 & Revisión del backend base & 2026-10-29, 21:00--21:20 & Presentar la base de la API y acordar cómo cada integrante construye su módulo sobre ella. \\
\hline
3 & Revisión de mitad de sprint & 2026-10-31, 21:00--21:20 & Revisar el tablero, las dependencias entre tareas y los Pull Requests pendientes. \\
\hline
4 & Sprint Review y Sprint Retrospective 3 & 2026-11-09, 21:00--22:00 & Demostrar el incremento desplegado, verificar el Sprint Goal y acordar mejoras para el Sprint 4. \\
\end{longtable}
\endgroup

Table: Reuniones del Sprint 3

La agenda de cada reunión se presenta a continuación.

\begingroup
\centering
\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.22\textwidth}|p{0.13\textwidth}|p{0.57\textwidth}|}
\hline
\textbf{Reunión} & \textbf{Hora} & \textbf{Tema} \\
\hline
\endfirsthead
\hline
\textbf{Reunión} & \textbf{Hora} & \textbf{Tema} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Sprint Planning 3 & 21:15--21:17 & Captura de inicio con asistentes y apertura. \\
\cline{2-3}
(2026-10-25) & 21:17--21:24 & Resumen del Sprint Review y de la Sprint Retrospective del Sprint 2. \\
\cline{2-3}
 & 21:24--21:31 & Sprint Goal 3 y alcance: 12 elementos del backlog y 53 Story Points. \\
\cline{2-3}
 & 21:31--21:35 & Responsables y Leadership-and-Collaboration Matrix (LACX). \\
\cline{2-3}
 & 21:35--21:48 & Estimación en horas de las tareas T-1 a T-30 (máximo 8 horas por tarea). \\
\cline{2-3}
 & 21:48--21:53 & Acuerdos técnicos: repositorio de Web Services en C\# y .NET 10, documentación OpenAPI de los endpoints, PostgreSQL, ramas \texttt{feature/}, Pull Requests revisados por otro integrante e internacionalización de la API con inglés por defecto. \\
\cline{2-3}
 & 21:53--21:57 & Dudas, cierre y captura final. \\
\hline
Revisión del backend base & 21:00--21:02 & Captura de inicio con asistentes. \\
\cline{2-3}
(2026-10-29) & 21:02--21:10 & Demostración de la estructura inicial de la API (T-1): proyecto ASP.NET Core con carpetas por bounded context, convención de rutas \texttt{/api/v1} en kebab-case, referencia de API con Scalar, política CORS por entorno y endpoint de health check. Se acordó que la persistencia con Entity Framework Core y PostgreSQL se integraría en los dos días siguientes. \\
\cline{2-3}
 & 21:10--21:15 & Inicio de cada módulo sobre esa estructura, empezando por el modelo de dominio mientras se completa la persistencia, con prioridad para los modelos de los que dependen otras tareas: Alert (T-8), HealthRecord (T-18) y Patient (T-27). \\
\cline{2-3}
 & 21:15--21:18 & Avance de las tareas que no dependen del código: proveedor de correo (T-13), base de datos en la nube (T-22) y configuración de Swagger (T-25). \\
\cline{2-3}
 & 21:18--21:20 & Bloqueos, cierre y captura final. \\
\hline
Revisión de mitad de sprint & 21:00--21:02 & Captura de inicio con asistentes. \\
\cline{2-3}
(2026-10-31) & 21:02--21:10 & Repaso del tablero de Jira por integrante y actualización de estados. \\
\cline{2-3}
 & 21:10--21:15 & Dependencias críticas: HealthRecord (T-18) hacia la generación de alertas (T-9); modelo Alert (T-8) hacia el cambio de estado (T-16), las transiciones de atención (T-11) y la observación (T-30); alerta creada (T-9) hacia el correo al familiar (T-15); API desplegada (T-23) hacia las integraciones de la Web Application. \\
\cline{2-3}
 & 21:15--21:18 & Pull Requests pendientes de revisión y asignación de revisores. \\
\cline{2-3}
 & 21:18--21:20 & Plan de la segunda semana: integración de los módulos con la persistencia ya disponible (migración inicial), manejo de errores e internacionalización compartidos, integración con la Web Application y despliegue final. Cierre y captura final. \\
\hline
Sprint Review y & 21:00--21:05 & Captura de inicio con asistentes. \\
\cline{2-3}
Sprint Retrospective 3 & 21:05--21:40 & Sprint Review: demostración por integrante en la Web Application y los Web Services desplegados. \\
\cline{2-3}
(2026-11-09) & 21:40--21:45 & Verificación del cumplimiento del Sprint Goal. \\
\cline{2-3}
 & 21:45--21:57 & Sprint Retrospective: aciertos, oportunidades de mejora y acciones para el Sprint 4. \\
\cline{2-3}
 & 21:57--22:00 & Acuerdos, cierre y captura final. \\
\end{longtable}
\endgroup

Table: Agenda de las reuniones del Sprint 3


#### 5.2.3.2. Aspect Leaders and Collaborators

Los aspectos del Sprint 3 se organizaron según los bloques funcionales de los Web Services y su integración con la Web Application: **A1.** Base de la API e inicio de sesión, **A2.** Generación de alertas, **A3.** Historial de salud, **A4.** Pacientes y estados de alertas, **A5.** Atención de alertas y notificaciones externas, y **A6.** Despliegue y documentación de servicios. La letra L identifica al líder del aspecto, es decir, al integrante responsable de sus elementos del backlog; la letra C identifica a quienes colaboran porque su trabajo depende de ese aspecto o lo complementa.

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.28\textwidth}|p{0.17\textwidth}|c|c|c|c|c|c|}
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{A1} & \textbf{A2} & \textbf{A3} & \textbf{A4} & \textbf{A5} & \textbf{A6} \\
\hline
\endfirsthead
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{A1} & \textbf{A2} & \textbf{A3} & \textbf{A4} & \textbf{A5} & \textbf{A6} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Benigno Montero, Harold Fauskorp & harold-11 & L & --- & --- & C & --- & C \\
\hline
Said Conde, Yazid & BL4Z3K4D & --- & L & C & --- & C & --- \\
\hline
Salon Puerta, Merly & MerlySalonP & --- & C & L & --- & --- & --- \\
\hline
Osorio Ramírez, Eduardo Jesús & Iron819 & --- & C & --- & C & L & --- \\
\hline
Tello Quispe, Luis German & luistello1739-web & --- & C & --- & L & C & --- \\
\hline
Rodriguez Gonzales, Leonel German & leokiss15 & C & --- & --- & --- & --- & L \\
\end{longtable}
\endgroup

Table: Leadership-and-Collaboration Matrix (LACX) del Sprint 3

Las colaboraciones responden a dependencias entre tareas. En A2, Merly provee el modelo de registros de salud que se evalúa para generar alertas, Luis implementa el cambio de estado sobre el modelo de alerta y Eduardo envía el correo cuando se crea una alerta. En A3, Yazid consume los registros de salud para la evaluación de alertas. En A4, Harold valida el perfil del paciente y Eduardo reutiliza el cambio de estado para las transiciones de atención. En A5, Luis provee el cambio de estado y Yazid registra la observación asociada a la atención. Finalmente, Leonel documenta en Swagger el esquema de autenticación de A1 y Harold provee la base de la API que se despliega en A6.


#### 5.2.3.3. Sprint Backlog 3

El Sprint Backlog 3 reúne doce elementos del Product Backlog orientados a la primera versión de los Web Services y a su integración con la Web Application. La planificación y el control de estados se realizan en Jira, en el sprint **Sprint 3 - Web Services** del proyecto VTL, con el flujo To-do, In Process, To Review y Done (Por hacer, En curso, En revisión y Finalizado). La captura siguiente muestra el tablero al inicio del sprint; las tablas posteriores transcriben su contenido con el estado registrado al cierre del sprint (9 de noviembre de 2026). Los elementos marcados como \textit{Retirado (Sprint 4)} se trasladaron al sprint \textbf{Sprint 4 - Web Services 2}, según se explica en la Sprint Retrospective 3 (sección 5.2.3.8). El registro de cambios de alcance de Jira muestra que US-25, US-12 y TS-06 se retiraron del sprint el 8 de noviembre y US-20 el 9 de noviembre, antes de su cierre.

**URL pública del Sprint Backlog en Jira:** \nolinkurl{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1}

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-board.png}

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.25}

\begin{longtable}{|p{0.08\textwidth}|p{0.08\textwidth}|p{0.38\textwidth}|p{0.06\textwidth}|p{0.20\textwidth}|p{0.07\textwidth}|}
\hline
\textbf{Story Id} & \textbf{Jira Key} & \textbf{Story Title} & \textbf{SP} & \textbf{Assigned To} & \textbf{Status} \\
\hline
\endfirsthead
\hline
\textbf{Story Id} & \textbf{Jira Key} & \textbf{Story Title} & \textbf{SP} & \textbf{Assigned To} & \textbf{Status} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
TS-03 & VTL-67 & Configuración base del Backend RESTful API y persistencia & 5 & Benigno Montero, Harold Fauskorp & Done \\
\hline
US-25 & VTL-56 & Inicio y cierre de sesión con navegación por rol & 3 & Benigno Montero, Harold Fauskorp & Retirado (Sprint 4) \\
\hline
US-20 & VTL-45 & Validación de datos básicos del paciente & 3 & Benigno Montero, Harold Fauskorp & Retirado (Sprint 4) \\
\hline
US-14 & VTL-35 & Generación automática de alerta desde un evento & 8 & Said Conde, Yazid & Done \\
\hline
US-12 & VTL-42 & Observación breve al atender una alerta & 2 & Said Conde, Yazid & Retirado (Sprint 4) \\
\hline
US-16 & VTL-47 & Almacenamiento del historial del paciente & 8 & Salon Puerta, Merly & Done \\
\hline
TS-08 & VTL-72 & Integración confiable de notificaciones externas & 5 & Osorio Ramírez, Eduardo Jesús & Done \\
\hline
US-11 & VTL-41 & Marcar alerta como en revisión o atendida & 3 & Osorio Ramírez, Eduardo Jesús & Done \\
\hline
US-18 & VTL-40 & Cambio de estado de alerta sin eliminar & 5 & Tello Quispe, Luis German & Done \\
\hline
US-19 & VTL-46 & Asociación de paciente con proveedor de salud & 3 & Tello Quispe, Luis German & Done \\
\hline
TS-07 & VTL-71 & Integración continua y despliegue de la Web Application & 5 & Rodriguez Gonzales, Leonel German & Done \\
\hline
TS-06 & VTL-70 & Documentación y verificación de contratos de servicios & 3 & Rodriguez Gonzales, Leonel German & Retirado (Sprint 4) \\
\hline
\multicolumn{3}{|r|}{\textbf{Total comprometido}} & \textbf{53} & \multicolumn{2}{l|}{} \\
\hline
\multicolumn{3}{|r|}{\textbf{Completado (Done)}} & \textbf{42} & \multicolumn{2}{l|}{} \\
\hline
\multicolumn{3}{|r|}{\textbf{Trasladado al Sprint 4}} & \textbf{11} & \multicolumn{2}{l|}{} \\
\end{longtable}
\endgroup

Table: Elementos del Product Backlog incluidos en el Sprint 3

La tabla siguiente presenta la descomposición de cada elemento en tareas, según la estructura de control de estado del sprint. Cada tarea está asignada al mismo integrante responsable de su elemento del backlog. La tarea T-4 se completó en el Sprint 3, pero se movió en Jira junto con su historia US-25, ya que una historia solo se cierra cuando todas sus tareas están terminadas.

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.25}

\begin{longtable}{|p{0.06\textwidth}|p{0.13\textwidth}|p{0.08\textwidth}|p{0.17\textwidth}|p{0.24\textwidth}|p{0.06\textwidth}|p{0.11\textwidth}|p{0.05\textwidth}|}
\hline
\textbf{Story Id} & \textbf{Story Title} & \textbf{Task Id} & \textbf{Task Title} & \textbf{Task Description} & \textbf{Est. (Hours)} & \textbf{Assigned To} & \textbf{Status} \\
\hline
\endfirsthead
\hline
\textbf{Story Id} & \textbf{Story Title} & \textbf{Task Id} & \textbf{Task Title} & \textbf{Task Description} & \textbf{Est. (Hours)} & \textbf{Assigned To} & \textbf{Status} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
TS-03 & Configuración base del Backend RESTful API y persistencia & T-1 (VTL-73) & Crear la solución ASP.NET Core por bounded contexts & Solución en .NET 10 con capas Domain, Application, Infrastructure e Interfaces, prefijo \texttt{/api/v1}, CORS por entorno y endpoint de salud. & 5 & Benigno Montero, Harold & Done \\
\hline
TS-03 & Configuración base del Backend RESTful API y persistencia & T-2 (VTL-74) & Configurar Entity Framework Core con PostgreSQL & DbContext, convenciones de nombres, Unit of Work, repositorio base y migración inicial sin credenciales en el repositorio. & 6 & Benigno Montero, Harold & Done \\
\hline
TS-03 & Configuración base del Backend RESTful API y persistencia & T-3 (VTL-75) & Manejo uniforme de errores e internacionalización de la API & Middleware de excepciones con ProblemDetails y mensajes localizados en\_US (por defecto) y es\_419 según el encabezado Accept-Language. & 5 & Benigno Montero, Harold & Done \\
\hline
US-25 & Inicio y cierre de sesión con navegación por rol & T-4 (VTL-76) & Usuarios, roles, hash de contraseñas y usuarios semilla & Modelo User y Role en el bounded context IAM, contraseñas con BCrypt y usuarios semilla por rol. & 4 & Benigno Montero, Harold & Done \\
\hline
US-25 & Inicio y cierre de sesión con navegación por rol & T-5 (VTL-77) & Emisión y validación de JWT con autorización por rol & Tokens con expiración, emisor y audiencia, middleware de autenticación y políticas de autorización por rol. & 6 & Benigno Montero, Harold & Retirado (Sprint 4) \\
\hline
US-25 & Inicio y cierre de sesión con navegación por rol & T-6 (VTL-78) & Endpoints de inicio y cierre de sesión & \texttt{POST /api/v1/authentication/sign-in} y \texttt{sign-out}, respuesta segura ante credenciales inválidas y protección de endpoints. & 4 & Benigno Montero, Harold & Retirado (Sprint 4) \\
\hline
US-25 & Inicio y cierre de sesión con navegación por rol & T-7 (VTL-79) & Integrar inicio y cierre de sesión en la Web Application & Vista de inicio de sesión, store de sesión, interceptor de Axios, guards por rol y conexión de los CTA de la Landing Page. & 5 & Benigno Montero, Harold & Retirado (Sprint 4) \\
\hline
US-14 & Generación automática de alerta desde un evento & T-8 (VTL-80) & Modelar el agregado Alert y su persistencia & Agregado Alert y MonitoringRule en el bounded context Alerts con configuración Fluent API y migración. & 6 & Said Conde, Yazid & Done \\
\hline
US-14 & Generación automática de alerta desde un evento & T-9 (VTL-81) & Generación automática de alertas por umbral & \texttt{POST /api/v1/alerts} que evalúa un registro de salud y crea una única alerta PENDING de forma idempotente y transaccional. & 8 & Said Conde, Yazid & Done \\
\hline
US-14 & Generación automática de alerta desde un evento & T-10 (VTL-82) & Endpoints de consulta de alertas & \texttt{GET /api/v1/alerts} con filtros por estado y paciente, y \texttt{GET /api/v1/alerts/\{id\}}. & 5 & Said Conde, Yazid & Done \\
\hline
US-11 & Marcar alerta como en revisión o atendida & T-11 (VTL-83) & Transiciones a en revisión y atendida & Transiciones PENDING, IN\_REVIEW y ATTENDED con actor y fecha sobre el endpoint de estado de US-18. & 4 & Osorio Ramírez, Eduardo & Done \\
\hline
US-11 & Marcar alerta como en revisión o atendida & T-12 (VTL-84) & Integrar el resumen y el cambio de estado de alertas en la Web Application & Reemplazo del servicio simulado de alertas por la API real, con manejo de conflictos y errores de red. & 5 & Osorio Ramírez, Eduardo & Done \\
\hline
TS-08 & Integración confiable de notificaciones externas & T-13 (VTL-85) & Seleccionar y configurar el proveedor externo de correo & Elección del servicio de terceros, creación de la cuenta, verificación del remitente y registro de la clave como secreto. & 4 & Osorio Ramírez, Eduardo & Done \\
\hline
TS-08 & Integración confiable de notificaciones externas & T-14 (VTL-86) & Adaptador del servicio externo de notificaciones & Interfaz de envío y adaptador en el bounded context Notifications con clave idempotente, registro de intentos y reintentos limitados. & 8 & Osorio Ramírez, Eduardo & Done \\
\hline
TS-08 & Integración confiable de notificaciones externas & T-15 (VTL-87) & Enviar correo al familiar al generarse una alerta & Envío del correo ante una alerta creada, con plantilla en inglés y español según la preferencia del familiar. & 5 & Osorio Ramírez, Eduardo & Done \\
\hline
US-18 & Cambio de estado de alerta sin eliminar & T-16 (VTL-88) & Cambio de estado con historial y control de concurrencia & \texttt{PATCH /api/v1/alerts/\{id\}/status} con validación de transiciones, auditoría, cierre sin eliminación y control de concurrencia. & 7 & Tello Quispe, Luis & Done \\
\hline
US-18 & Cambio de estado de alerta sin eliminar & T-17 (VTL-89) & Integrar el estado de las alertas en la vista familiar & Consulta del estado actual y del historial de cambios de las alertas desde la vista familiar. & 4 & Tello Quispe, Luis & Done \\
\hline
US-16 & Almacenamiento del historial del paciente & T-18 (VTL-90) & Modelar HealthRecord y su persistencia & HealthRecord y catálogo de tipos de registro en el bounded context Health Records con configuración Fluent API y migración. & 6 & Salon Puerta, Merly & Done \\
\hline
US-16 & Almacenamiento del historial del paciente & T-19 (VTL-91) & Endpoints de registro y consulta del historial de salud & \texttt{POST} y \texttt{GET /api/v1/older-adults/\{id\}/health-records} con filtros por fecha y tipo y orden descendente. & 7 & Salon Puerta, Merly & Done \\
\hline
US-16 & Almacenamiento del historial del paciente & T-20 (VTL-92) & Validar los registros de salud según su tipo & Reglas de validación por tipo de registro con mensajes localizados en\_US y es\_419, sin persistencia parcial. & 4 & Salon Puerta, Merly & Done \\
\hline
US-16 & Almacenamiento del historial del paciente & T-21 (VTL-93) & Integrar el historial del paciente en la Web Application & Reemplazo del servicio simulado del historial de registros por la API real. & 5 & Salon Puerta, Merly & Done \\
\hline
TS-07 & Integración continua y despliegue de la Web Application & T-22 (VTL-94) & Desplegar la base de datos PostgreSQL en la nube & Instancia administrada de PostgreSQL con acceso seguro y cadenas de conexión por entorno. & 5 & Rodriguez Gonzales, Leonel & Done \\
\hline
TS-07 & Integración continua y despliegue de la Web Application & T-23 (VTL-95) & Desplegar los Web Services con GitHub Actions & Pipeline que compila y despliega la API en la nube al integrar en \texttt{main}, aplicando migraciones con variables protegidas. & 7 & Rodriguez Gonzales, Leonel & Done \\
\hline
TS-07 & Integración continua y despliegue de la Web Application & T-24 (VTL-96) & Actualizar el despliegue de la Web Application y la Landing Page & URL de la API por entorno en la Web Application, nuevos despliegues y verificación de los CTA de la Landing Page. & 4 & Rodriguez Gonzales, Leonel & Done \\
\hline
TS-06 & Documentación y verificación de contratos de servicios & T-25 (VTL-97) & Configurar Swagger/OpenAPI con ejemplos y esquema JWT & Swagger mediante Swashbuckle con comentarios XML, ejemplos sin datos personales reales y esquema de seguridad Bearer. & 5 & Rodriguez Gonzales, Leonel & Retirado (Sprint 4) \\
\hline
TS-06 & Documentación y verificación de contratos de servicios & T-26 (VTL-98) & Verificar los contratos y publicar la documentación desplegada & Prueba de los contratos con datos de muestra desde Swagger desplegado y validación de la especificación OpenAPI. & 4 & Rodriguez Gonzales, Leonel & Retirado (Sprint 4) \\
\hline
US-19 & Asociación de paciente con proveedor de salud & T-27 (VTL-99) & Asociación entre paciente y proveedor de salud & Modelo OlderAdult y CareProvider y \texttt{PUT /api/v1/older-adults/\{id\}/care-provider} idempotente. & 7 & Tello Quispe, Luis & Done \\
\hline
US-20 & Validación de datos básicos del paciente & T-28 (VTL-100) & Creación y actualización validada del perfil del paciente & \texttt{POST} y \texttt{PUT /api/v1/older-adults} con validaciones de identificación y de activación del seguimiento. & 5 & Benigno Montero, Harold & Retirado (Sprint 4) \\
\hline
US-20 & Validación de datos básicos del paciente & T-29 (VTL-101) & Integrar la búsqueda y el detalle de pacientes en la Web Application & Reemplazo del servicio simulado de pacientes asignados y del detalle de paciente por la API real. & 4 & Benigno Montero, Harold & Retirado (Sprint 4) \\
\hline
US-12 & Observación breve al atender una alerta & T-30 (VTL-102) & Observación breve al atender una alerta & Registro de una observación opcional de 1 a 1000 caracteres asociada a la atención y su captura en la Web Application. & 5 & Said Conde, Yazid & Retirado (Sprint 4) \\
\end{longtable}
\endgroup

Table: Sprint Backlog 3

El esfuerzo total comprometido fue de **53 Story Points** y **159 horas** estimadas. Al cierre, ocho elementos (**42 Story Points**) quedaron en estado Done, junto con 22 de las 30 tareas (**121 horas** estimadas). Los cuatro elementos restantes (**11 Story Points**, 38 horas pendientes) se trasladaron al Sprint 4: US-25 (inicio de sesión con JWT), US-20 (validación del perfil del paciente), US-12 (observación al atender una alerta) y TS-06 (documentación publicada de los contratos). La historia US-25 concentraba 19 horas en cuatro tareas frente a sus 3 Story Points, lo que evidenció una subestimación de su complejidad en el Product Backlog; esta diferencia se analizó en la Sprint Retrospective 3. La trazabilidad se conserva mediante las claves VTL de Jira, las ramas de característica y los commits que se registrarán en la sección siguiente.


#### 5.2.3.4. Development Evidence for Sprint Review

Durante el Sprint 3 se construyó la primera versión de los RESTful Web Services de VitaLink en el repositorio `upc-pre-202620-1asi0730-16712-CodeBrokers-web-services`, con ASP.NET Core sobre .NET 10, Entity Framework Core y PostgreSQL. La solución se organizó por bounded contexts (Shared, IAM, Alerting, Preventive Monitoring, Elder Care y Notification), cada uno con sus capas Domain, Application, Infrastructure e Interfaces. Los principales avances fueron los siguientes:

- **Base de la API (TS-03).** Prefijo `/api/v1` con rutas en kebab-case, CORS por entorno, endpoint de salud que verifica la base de datos, `AppDbContext` con convención de nombres en snake\_case, Unit of Work, repositorio base, patrón Result, manejo global de errores con ProblemDetails y mensajes localizados en inglés (`en-US`, por defecto) y español (`es-419`) según el encabezado `Accept-Language`.
- **Identidad (base de US-25).** Agregado `User` con roles, contraseñas cifradas con BCrypt, migración de la tabla `iam.users` y usuarios de demostración por rol (T-4).
- **Alertas (US-14).** Agregado `Alert` con transiciones de estado, consulta paginada con filtros y generación automática e idempotente de alertas a partir de la evaluación de un registro de salud contra las reglas de monitoreo activas.
- **Historial de salud (US-16).** Agregado `HealthRecord`, catálogo de ocho tipos de registro, validación del valor y la nota según el tipo, reglas de monitoreo (`MonitoringRule`) con umbrales mínimo y máximo y severidad, y servicio de evaluación de riesgo que aplica la severidad más alta.
- **Estado de alertas (US-18 y US-11).** Cambio de estado sin eliminación (`PENDING`, `IN_REVIEW`, `ATTENDED`), historial de cambios con actor y fecha, y control de concurrencia optimista mediante la columna `xmin` de PostgreSQL.
- **Asociación paciente-proveedor (US-19).** Modelo `OlderAdult` y `CareProvider` y asociación idempotente con claves foráneas.
- **Notificaciones externas (TS-08).** Agregado `Notification` con estados de entrega y reintentos, adaptador del proveedor Resend y envío automático del correo al familiar cuando se genera una alerta.
- **Integración continua y despliegue (TS-07).** Dockerfile, workflow de compilación para Pull Requests y workflow de despliegue continuo hacia Azure.

En la Frontend Web Application se reemplazó el servicio REST simulado por la API real en las funcionalidades de alertas: resumen y cambio de estado de alertas para el profesional (T-12), historial de salud del paciente (T-21) y estado de las alertas en el panel familiar (T-17). La Landing Page no requirió cambios en este sprint: sus llamadas a la acción ya dirigían a la Web Application desplegada.

Cada integrante trabajó en una rama `feature/` y lo integró en `develop` mediante Pull Requests revisados por otro integrante. En Web Services se integraron 22 Pull Requests (\#1 al \#22) y el incremento se consolidó en `main` con el Pull Request \#23; en la Frontend Web Application se integraron los Pull Requests \#13, \#14, \#16 y \#17, y el incremento se consolidó en `main` con el Pull Request \#18. Las tablas siguientes recogen los commits que identifican cada aporte.

**Repositorio de Web Services:** \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-web-services}{upc-pre-202620-1asi0730-16712-CodeBrokers-web-services}

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.25}

\begin{longtable}{|p{0.13\textwidth}|p{0.25\textwidth}|p{0.08\textwidth}|p{0.39\textwidth}|p{0.09\textwidth}|}
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
Web Services & main & 40ab24f & Initial commit & 29/10/2026 \\
\hline
Web Services & feature/backend-foundation & 67b645d & feat(shared): add api version route prefix convention & 29/10/2026 \\
\hline
Web Services & feature/backend-foundation & 41949fb & chore(config): add scalar api reference & 29/10/2026 \\
\hline
Web Services & feature/backend-foundation & 5e34eac & feat(shared): add health check endpoint & 29/10/2026 \\
\hline
Web Services & feature/backend-foundation & e9ff69d & feat(shared): add app db context & 30/10/2026 \\
\hline
Web Services & feature/backend-foundation & 90b9cc5 & feat(shared): implement base repository and unit of work & 30/10/2026 \\
\hline
Web Services & feature/backend-foundation & 1013c38 & feat(shared): add initial migration & 31/10/2026 \\
\hline
Web Services & feature/backend-foundation & 6d382eb & feat(shared): verify database availability in health check & 31/10/2026 \\
\hline
Web Services & feature/backend-foundation & 6f3b0b4 & feat(shared): add result pattern for operation outcomes & 02/11/2026 \\
\hline
Web Services & feature/backend-foundation & ae5c2fd & feat(shared): add global exception handler with problem details & 03/11/2026 \\
\hline
Web Services & feature/backend-foundation & 7b53d56 & feat(shared): localize problem details and validation messages & 04/11/2026 \\
\hline
Web Services & feature/role-based-sign-in & 71869d7 & feat(iam): add password hasher port with bcrypt implementation & 04/11/2026 \\
\hline
Web Services & feature/role-based-sign-in & 0dff94c & feat(iam): add user aggregate & 04/11/2026 \\
\hline
Web Services & feature/role-based-sign-in & cb23d59 & feat(iam): add user entity configuration and migration & 04/11/2026 \\
\hline
Web Services & feature/role-based-sign-in & 1cec826 & feat(iam): seed demo users per role in development & 04/11/2026 \\
\hline
Web Services & feature/alert-generation & a5ac003 & feat(alerting): add alert id value object & 31/10/2026 \\
\hline
Web Services & feature/alert-generation & e3d9e79 & feat(alerting): add alert aggregate base structure & 31/10/2026 \\
\hline
Web Services & feature/alert-generation & 2265273 & feat(alerting): add alert status transitions & 01/11/2026 \\
\hline
Web Services & feature/alert-generation & 8842c4b & feat(alerting): add alert entity framework configuration & 02/11/2026 \\
\hline
Web Services & feature/alert-generation & 9256c2c & feat(alerting): add alerts persistence migration & 02/11/2026 \\
\hline
Web Services & feature/alert-generation & ad9dd25 & feat(alerting): add paginated alert query endpoints & 02/11/2026 \\
\hline
Web Services & feature/alert-generation & be0d28c & feat(alerting): add create alert endpoint & 05/11/2026 \\
\hline
Web Services & feature/alert-generation & 91807a9 & feat(alerting): validate health record before raising alert & 05/11/2026 \\
\hline
Web Services & feature/alert-generation & ce3ca42 & feat(monitoring): implement monitoring context facade & 05/11/2026 \\
\hline
Web Services & feature/alert-generation & 97f66a6 & feat(alerting): generate alerts from health record evaluation & 06/11/2026 \\
\hline
Web Services & feature/alert-observation & 5b4a642 & feat(alerting): record observations for attended alerts & 06/11/2026 \\
\hline
Web Services & feature/external-notifications & f205416 & feat(notification): add notification aggregate with delivery and retry rules & 30/10/2026 \\
\hline
Web Services & feature/external-notifications & 676d7f5 & feat(notification): add resend email sender adapter & 30/10/2026 \\
\hline
Web Services & feature/external-notifications & a418421 & feat(notification): register email sender services & 30/10/2026 \\
\hline
Web Services & feature/external-notifications & b2db259 & feat(notification): add notification entity configuration & 02/11/2026 \\
\hline
Web Services & feature/external-notifications & 053b188 & feat(notification): add notifications table migration & 02/11/2026 \\
\hline
Web Services & feature/external-notifications & cbcbc29 & feat(notification): add send alert notification command & 04/11/2026 \\
\hline
Web Services & feature/external-notifications & 86b4a62 & feat(notification): add send alert notification command service & 04/11/2026 \\
\hline
Web Services & feature/external-notifications & e719327 & feat(notification): add notifications controller & 04/11/2026 \\
\hline
Web Services & feature/t15-alert-email & c374084 & feat(notification): add alert raised email notifier & 07/11/2026 \\
\hline
Web Services & feature/t15-alert-email & 8be6bdb & feat(notification): notify family caregiver when an alert is created & 07/11/2026 \\
\hline
Web Services & feature/t15-alert-email & e77ba3a & feat(notification): register alert email notification & 07/11/2026 \\
\hline
Web Services & feature/alert-status-change & b02bbcc & feat(alerting): add optimistic concurrency control & 05/11/2026 \\
\hline
Web Services & feature/alert-status-change & abdfef0 & feat(alerting): implement alert status command service & 05/11/2026 \\
\hline
Web Services & feature/alert-status-change & 0fe76d9 & feat(alerting): add localized alert status endpoint & 05/11/2026 \\
\hline
Web Services & feature/alert-status-change & f850e2b & fix(alerting): map optimistic concurrency to PostgreSQL xmin & 05/11/2026 \\
\hline
Web Services & feature/alert-status-change & 7fd8012 & feat(alerting): expose concurrency version in alert responses & 05/11/2026 \\
\hline
Web Services & feature/alert-status-change & ed41f3b & feat(alerting): expose alert status change history endpoint & 05/11/2026 \\
\hline
Web Services & feature/alert-status-change & ce93ab0 & refactor(alerting): group status endpoints under alert status route & 05/11/2026 \\
\hline
Web Services & feature/alert-status-change & 3fa71fc & fix(alerting): localize status validation messages & 05/11/2026 \\
\hline
Web Services & feature/care-provider-association & bda0c0f & feat(elder-care): add core value objects & 04/11/2026 \\
\hline
Web Services & feature/care-provider-association & 8e8c86a & feat(elder-care): add care provider aggregate and repository contract & 04/11/2026 \\
\hline
Web Services & feature/care-provider-association & 939aa89 & feat(elder-care): add older adult EF Core configuration & 04/11/2026 \\
\hline
Web Services & feature/care-provider-association & 5812704 & fix(elder-care): make care provider association idempotent & 04/11/2026 \\
\hline
Web Services & feature/care-provider-association & ed3ad72 & feat(elder-care): implement older adult command service & 04/11/2026 \\
\hline
Web Services & feature/care-provider-association & a7d28d5 & feat(elder-care): expose care provider association endpoint & 05/11/2026 \\
\hline
Web Services & feature/care-provider-association & 5a455e6 & feat(elder-care): add database migration and fix owned value object mappings & 05/11/2026 \\
\hline
Web Services & feature/care-provider-association & 4973e9d & fix(elder-care): align namespaces, localize REST errors and enforce foreign keys & 06/11/2026 \\
\hline
Web Services & feature/patient-health-history & f529bce & feat(monitoring): add health record aggregate root & 04/11/2026 \\
\hline
Web Services & feature/patient-health-history & 4588a46 & feat(monitoring): add record type entity configuration and seed data & 04/11/2026 \\
\hline
Web Services & feature/patient-health-history & c5eb1c0 & feat(monitoring): add health record repository & 04/11/2026 \\
\hline
Web Services & feature/patient-health-history & b3af816 & feat(monitoring): add risk evaluation domain service & 05/11/2026 \\
\hline
Web Services & feature/patient-health-history & c211e58 & feat(monitoring): add monitoring rule aggregate root & 05/11/2026 \\
\hline
Web Services & feature/patient-health-history & ee735ae & feat(monitoring): add monitoring rules migration & 05/11/2026 \\
\hline
Web Services & feature/patient-health-history & 3bf6c8f & feat(monitoring): add monitoring rules controller & 05/11/2026 \\
\hline
Web Services & feature/patient-health-history & a122be3 & feat(monitoring): add health records migration & 05/11/2026 \\
\hline
Web Services & feature/health-record-endpoints & 8f172f9 & feat(monitoring): add health record history query & 06/11/2026 \\
\hline
Web Services & feature/health-record-endpoints & 4d4ff66 & feat(monitoring): add health record command service & 06/11/2026 \\
\hline
Web Services & feature/health-record-endpoints & 3fec922 & feat(monitoring): add health records controller & 06/11/2026 \\
\hline
Web Services & feature/health-record-endpoints & 1d7a87c & feat(monitoring): validate health record value and note by type & 06/11/2026 \\
\hline
Web Services & feature/health-record-endpoints & 115c770 & feat(monitoring): add unit validation and update command model & 06/11/2026 \\
\hline
Web Services & feature/monitoring-rule-fixes & 719a773 & refactor(monitoring): align monitoring rule model with the database schema & 06/11/2026 \\
\hline
Web Services & feature/monitoring-rule-fixes & 15da666 & fix(monitoring): migrate monitoring\_rules to severity, min/max values and unique active rule & 06/11/2026 \\
\hline
Web Services & feature/monitoring-rule-fixes & 8f4abd3 & feat(monitoring): evaluate health records against active rules by highest severity & 06/11/2026 \\
\hline
Web Services & feature/health-record-endpoints & 5e45c1f & chore(monitoring): remove unused Swashbuckle package & 07/11/2026 \\
\hline
Web Services & feature/continuous-deployment & a728915 & build(docker): add dockerfile for building and running the api & 01/11/2026 \\
\hline
Web Services & feature/continuous-deployment & 6f7bbd5 & ci: add backend build workflow for pull requests & 01/11/2026 \\
\hline
Web Services & feature/continuous-deployment & 10494b3 & Enable OpenAPI and Scalar for Azure deployment & 03/11/2026 \\
\hline
Web Services & feature/continuous-deployment & be677bb & Configure automated Docker deployment & 03/11/2026 \\
\hline
Web Services & feature/continuous-deployment & fb14db3 & test: verify continuous deployment & 03/11/2026 \\
\hline
Web Services & feature/continuous-deployment & 95f496b & docs: document continuous deployment & 03/11/2026 \\
\hline
Web Services & feature/continuous-deployment & 2cd8b31 & docs: update continuous deployment branch to develop & 06/11/2026 \\
\hline
Web Services & main & a55873f & Merge pull request \#23 from develop & 09/11/2026 \\
\end{longtable}
\endgroup

Table: Development Evidence del Sprint 3 — Web Services

**Repositorio de la Frontend Web Application:** \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application}{upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application}

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.25}

\begin{longtable}{|p{0.13\textwidth}|p{0.25\textwidth}|p{0.08\textwidth}|p{0.39\textwidth}|p{0.09\textwidth}|}
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
Frontend Application & feature/alert-status-ui & ac1a9b3 & chore(alerting): add backend API base URL & 06/11/2026 \\
\hline
Frontend Application & feature/alert-status-ui & 03f03cc & feat(alerting): add alert API client & 06/11/2026 \\
\hline
Frontend Application & feature/alert-status-ui & 5f90c77 & feat(alerting): load alerts and status history from the backend & 06/11/2026 \\
\hline
Frontend Application & feature/alert-status-ui & 32d3449 & feat(alerting): add alert status change action to the workspace store & 06/11/2026 \\
\hline
Frontend Application & feature/alert-status-ui & 6e9f41e & feat(alerting): add start review and mark attended actions & 06/11/2026 \\
\hline
Frontend Application & feature/alert-status-ui & 743b604 & feat(alerting): add status action and error translations & 06/11/2026 \\
\hline
Frontend Application & feature/alert-status-ui & de82fca & fix(alerting): use a generic message for status change conflicts & 07/11/2026 \\
\hline
Frontend Application & feature/readme-backend-dev & 95ab8ee & docs(readme): translate README to English and document backend setup & 07/11/2026 \\
\hline
Frontend Application & feature/t21-patient-history-fix & b8c634a & fix(monitoring): load patient history from health record endpoints & 08/11/2026 \\
\hline
Frontend Application & feature/t17-family-alert-status & bd74fa1 & feat(elder-care): show all alert statuses in family dashboard & 08/11/2026 \\
\hline
Frontend Application & feature/t17-family-alert-status & 5755116 & fix(elder-care): correct family alert counter markup & 08/11/2026 \\
\hline
Frontend Application & main & a0dbf43 & Merge pull request \#18 from develop & 09/11/2026 \\
\end{longtable}
\endgroup

Table: Development Evidence del Sprint 3 — Frontend Web Application

La Landing Page no registra commits en el Sprint 3. Las historias trasladadas al Sprint 4 también tienen avance en el repositorio: la base de identidad de US-25 (T-4) ya está integrada en `develop` y el endpoint de observación de US-12 se integró en el Pull Request \#20, pero su captura en la Web Application y la verificación de sus criterios de aceptación quedaron pendientes.


#### 5.2.3.5. Execution Evidence for Sprint Review

Al cierre del Sprint 3, los Web Services están desplegados en Azure y responden con datos persistidos en PostgreSQL, y la Web Application desplegada en Vercel consume la API real en el flujo de alertas. El recorrido verificado en el Sprint Review fue el siguiente:

1. Se registra un registro de salud fuera de umbral para un adulto mayor (`POST /api/v1/older-adults/{id}/health-records`) y se solicita su evaluación (`POST /api/v1/alerts`). La API compara el valor con las reglas de monitoreo activas y crea una única alerta `PENDING` con la severidad de la regla incumplida.
2. Al crearse la alerta, el bounded context Notification envía el correo de aviso al familiar mediante Resend y registra la notificación con su estado de entrega.
3. El profesional de la salud consulta el resumen de alertas en la Web Application, abre la alerta y la marca como en revisión y luego como atendida. Cada cambio queda en el historial de estados con su actor y fecha; si otra persona modificó la alerta antes, la API responde con un conflicto y la vista muestra un mensaje genérico.
4. El profesional revisa el historial de salud del paciente, cargado desde la API y ordenado del más reciente al más antiguo.
5. El familiar cuidador consulta en su panel el estado actualizado de las alertas de su familiar (pendiente, en revisión o atendida).

En este incremento, la Web Application registra los cambios de estado con un profesional de demostración y asocia los pacientes del frontend con identificadores de demostración del backend. Los pacientes asignados y su detalle todavía se leen del servicio REST simulado hasta completar US-20.

**URL de la Web Application:** \href{https://vitalink-opal.vercel.app}{https://vitalink-opal.vercel.app}

**Resumen de alertas del profesional con datos de la API (filtro: pendientes):**

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-professional-alerts.png}

**Detalle del paciente con el historial de intervenciones de una alerta (pendiente, en revisión y atendida):**

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-alert-status.png}

**Historial de salud del paciente cargado desde la API:**

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-patient-history.png}

**Seguimiento del caso en el panel familiar: el familiar ve la alerta de Carmen Morales atendida y el historial de cambios registrado por el profesional:**

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-family-alerts.png}

**Correo de aviso recibido por el familiar al generarse una alerta de severidad alta:**

\includegraphics[width=0.7\linewidth]{assets/523-sprint3-alert-email.png}

<!-- PENDIENTE: reemplazar por el enlace del video de navegación del Sprint 3 en Microsoft Stream.
**Video de navegación del Sprint 3:** \href{URL}{Ver video de navegación del Sprint 3}
-->


#### 5.2.3.6. Services Documentation Evidence for Sprint Review

La especificación OpenAPI de los Web Services se genera con el soporte nativo de ASP.NET Core (`Microsoft.AspNetCore.OpenApi`, commit `41949fb`) a partir de los controladores, sus atributos `ProducesResponseType` y sus comentarios XML. En este sprint la especificación se visualizó y probó con **Scalar**, una interfaz interactiva que lee el mismo documento OpenAPI y permite enviar solicitudes con datos de muestra. El enunciado del curso establece Swagger como interfaz de documentación; durante el sprint se agregó el paquete Swashbuckle, pero no llegó a configurarse y se retiró por no usarse (commit `5e45c1f`). La configuración de Swagger UI sobre esta especificación, con ejemplos y el esquema de seguridad Bearer, forma parte de TS-06 en el Sprint 4. Los errores se devuelven como ProblemDetails con el título localizado según `Accept-Language`.

La especificación y la interfaz interactiva solo se publican en el entorno de desarrollo. El commit `10494b3` las habilitó también para el despliegue, pero ese cambio se perdió al resolver un conflicto de merge en `Program.cs`, por lo que en la API desplegada las rutas `/openapi/v1.json` y `/scalar` responden con 404. Su publicación en el entorno desplegado se completa en el Sprint 4 con TS-06.

\begingroup
\centering
\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.27\textwidth}|p{0.64\textwidth}|}
\hline
\textbf{Elemento} & \textbf{Evidencia} \\
\hline
\endfirsthead
\hline
\textbf{Elemento} & \textbf{Evidencia} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Repositorio & \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-web-services}{upc-pre-202620-1asi0730-16712-CodeBrokers-web-services} \\
\hline
Especificación OpenAPI (local) & \nolinkurl{http://localhost:5270/openapi/v1.json} \\
\hline
Interfaz interactiva Scalar (local) & \nolinkurl{http://localhost:5270/scalar} \\
\hline
URL base de la API desplegada & \nolinkurl{https://vitalink-api-dev-h4gdanfjc5ezbqep.canadacentral-01.azurewebsites.net/api/v1} \\
\hline
Commits de documentación & \texttt{41949fb} (OpenAPI y Scalar), \texttt{10494b3} (OpenAPI y Scalar para el despliegue, perdido en un merge), \texttt{1202af3} (documentación del endpoint de creación de alertas), \texttt{9b1a1d9} (validación del registro de salud), \texttt{5e45c1f} (retiro de Swashbuckle), \texttt{6c734d7}, \texttt{399ebc2} y \texttt{0fffdcf} (guía de instalación, persistencia y manejo de errores en el README) y \texttt{95f496b} (documentación del despliegue continuo) \\
\end{longtable}
\endgroup

Table: Documentación de los Web Services del Sprint 3

La tabla siguiente resume los endpoints implementados en el sprint. Todas las rutas usan el prefijo `/api/v1`, reciben y devuelven JSON, y responden 400 con ProblemDetails cuando un identificador o un campo del cuerpo no es válido.

\begingroup
\centering
\scriptsize
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.25}

\begin{longtable}{|p{0.06\textwidth}|p{0.29\textwidth}|p{0.27\textwidth}|p{0.31\textwidth}|}
\hline
\textbf{Verbo} & \textbf{Sintaxis de llamada} & \textbf{Parámetros} & \textbf{Response} \\
\hline
\endfirsthead
\hline
\textbf{Verbo} & \textbf{Sintaxis de llamada} & \textbf{Parámetros} & \textbf{Response} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
GET & \texttt{/api/v1/health} & Ninguno. & 200 con \texttt{status}, \texttt{database} y \texttt{timestamp}; confirma que la API y la base de datos están disponibles. \\
\hline
POST & \texttt{/api/v1/older-adults/\{olderAdultId\}/health-records} & Ruta: \texttt{olderAdultId}. Cuerpo: \texttt{recordTypeCode}, \texttt{measurementValue}, \texttt{unit}, \texttt{note}, \texttt{source} (\texttt{OLDER\_ADULT}, \texttt{FAMILY\_CAREGIVER} o \texttt{CARE\_PROVIDER}) y \texttt{recordedBy}. & 201 con el registro creado. 400 si el tipo, el valor o la nota no cumplen la validación de su tipo; no se guarda nada parcialmente. \\
\hline
GET & \texttt{/api/v1/older-adults/\{olderAdultId\}/health-records} & Ruta: \texttt{olderAdultId}. Consulta opcional: \texttt{from}, \texttt{to} (fechas) y \texttt{type}. & 200 con la lista de registros del paciente en orden descendente por fecha. \\
\hline
POST & \texttt{/api/v1/monitoring-rules} & Cuerpo: \texttt{olderAdultId}, \texttt{recordTypeCode}, \texttt{minThreshold}, \texttt{maxThreshold} y \texttt{severity} (\texttt{HIGH}, \texttt{MEDIUM} o \texttt{LOW}). & 201 con la regla creada. 409 si ya existe una regla activa para ese paciente, tipo de registro y severidad. \\
\hline
GET & \texttt{/api/v1/monitoring-rules/older-adult/\{olderAdultId\}} & Ruta: \texttt{olderAdultId}. & 200 con las reglas del paciente, sus umbrales, severidad y estado. \\
\hline
POST & \texttt{/api/v1/alerts} & Cuerpo: \texttt{healthRecordId}. & 201 con \texttt{healthRecordId} y la alerta creada cuando el valor está fuera de umbral; 200 con \texttt{alert: null} si está dentro de límites, o con la alerta existente si el registro ya fue evaluado (idempotencia). 404 si el registro no existe. \\
\hline
GET & \texttt{/api/v1/alerts} & Consulta opcional: \texttt{status}, \texttt{olderAdultId}, \texttt{page} (1 por defecto) y \texttt{pageSize} (20 por defecto). & 200 con \texttt{items}, \texttt{page}, \texttt{pageSize}, \texttt{totalItems} y \texttt{totalPages}. \\
\hline
GET & \texttt{/api/v1/alerts/pending} & Consulta opcional: \texttt{olderAdultId}, \texttt{page} y \texttt{pageSize}. & 200 con la página de alertas en estado \texttt{PENDING}. \\
\hline
GET & \texttt{/api/v1/alerts/\{id\}} & Ruta: \texttt{id}. & 200 con la alerta: paciente, registro y regla de origen, severidad, estado, fechas y \texttt{version}. 404 si no existe. \\
\hline
PATCH & \texttt{/api/v1/alerts/\{alertId\}/status} & Ruta: \texttt{alertId}. Cuerpo: \texttt{status}, \texttt{changedBy} y \texttt{version}. & 200 con el nuevo estado. 409 si la transición no es válida o si \texttt{version} no coincide con la versión actual (otra persona modificó la alerta). 404 si no existe. \\
\hline
GET & \texttt{/api/v1/alerts/\{alertId\}/status/history} & Ruta: \texttt{alertId}. & 200 con los cambios de estado de la alerta, su actor y su fecha. \\
\hline
POST & \texttt{/api/v1/alerts/\{alertId\}/observation} & Ruta: \texttt{alertId}. Cuerpo: \texttt{text} (opcional) y \texttt{createdBy}. & 201 con la observación; 204 si se atiende sin observación. 409 si la alerta no está atendida o ya tiene observación. Pendiente de integración en la Web Application (US-12, Sprint 4). \\
\hline
GET & \texttt{/api/v1/alerts/\{alertId\}/observation} & Ruta: \texttt{alertId}. & 200 con la observación; 404 si la alerta no tiene observación. \\
\hline
PATCH & \texttt{/api/v1/older-adults/\{id\}/care-provider} & Ruta: \texttt{id}. Cuerpo: \texttt{careProviderId}. & 200 al asociar el proveedor de salud; repetir la misma asociación no la duplica. 404 si el paciente o el proveedor no existen; 409 si la asociación entra en conflicto con una existente. \\
\hline
POST & \texttt{/api/v1/notifications} & Cuerpo: \texttt{alertId}, \texttt{recipientId}, \texttt{recipientEmail}, \texttt{olderAdultName} y \texttt{severity}. & 201 con la notificación y su estado de entrega. 409 si ya se notificó esa alerta a ese destinatario; 503 si el proveedor de correo no está disponible. \\
\hline
GET & \texttt{/api/v1/notifications/\{id\}} & Ruta: \texttt{id}. & 200 con la notificación; 404 si no existe. \\
\hline
GET & \texttt{/api/v1/notifications} & Consulta obligatoria: \texttt{recipientId}. & 200 con las notificaciones del destinatario; 400 si falta \texttt{recipientId}. \\
\end{longtable}
\endgroup

Table: Endpoints de los Web Services implementados en el Sprint 3

**Ejemplos de interacción con datos de muestra.** Las respuestas siguientes se obtuvieron de la API desplegada el 9 de noviembre de 2026. Los identificadores corresponden a datos de demostración y no a personas reales.

`GET /api/v1/health`

```json
{ "status": "Healthy", "database": "Up", "timestamp": "2026-11-10T00:26:01.1670612Z" }
```

`GET /api/v1/older-adults/00000000-0000-4000-8000-000000000104/health-records` (primer elemento)

```json
{
  "id": "f21f3184-bbd7-4162-8409-3a8db0273736",
  "olderAdultId": "00000000-0000-4000-8000-000000000104",
  "recordTypeCode": "HEART_RATE",
  "measurementValue": 130.00,
  "note": "Frecuencia cardiaca elevada en reposo",
  "source": "OLDER_ADULT",
  "recordedAt": "2026-11-09T07:15:54.7846+00:00"
}
```

El paciente tiene una regla activa de frecuencia cardiaca con máximo de 100 y severidad `HIGH`. Al evaluar este registro, la API generó la alerta siguiente (`GET /api/v1/alerts?pageSize=1`):

```json
{
  "items": [{
    "id": "17b35586-dbf6-48b4-ae9a-32ef3492aeae",
    "olderAdultId": "00000000-0000-4000-8000-000000000104",
    "healthRecordId": "f21f3184-bbd7-4162-8409-3a8db0273736",
    "monitoringRuleId": "3580b847-519c-4ecb-9bc1-7eab5d0f77b9",
    "assignedProviderId": null,
    "severity": "HIGH",
    "status": "PENDING",
    "raisedAt": "2026-11-09T07:15:55.025207+00:00",
    "lastStatusChangeAt": "2026-11-09T07:15:55.025207+00:00",
    "version": 83077
  }],
  "page": 1, "pageSize": 1, "totalItems": 21, "totalPages": 21
}
```

El campo `version` es el que la Web Application envía en `PATCH /status` para detectar cambios concurrentes. Una consulta sin un parámetro obligatorio devuelve un error localizado; por ejemplo, `GET /api/v1/notifications` sin `recipientId`, con `Accept-Language: es-419`, responde 400 con el título *"La solicitud contiene valores no válidos."*

**Interfaz de Scalar en el entorno local (`http://localhost:5270/scalar`), con los endpoints agrupados por controlador:**

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-scalar-overview.png}

<!-- PENDIENTE: captura de una prueba con datos de muestra desde Scalar.
**Prueba de POST /api/v1/alerts con datos de muestra desde Scalar:**

\includegraphics[width=0.92\linewidth]{assets/523-sprint3-scalar-create-alert.png}
-->


#### 5.2.3.7. Software Deployment Evidence for Sprint Review

En el Sprint 3 se desplegó por primera vez el backend de VitaLink y se actualizó la Web Application para consumirlo. Las actividades fueron: creación de los recursos en Microsoft Azure (App Service y Azure Database for PostgreSQL), contenedorización de la API con Docker, automatización del despliegue con GitHub Actions y Docker Hub, configuración de secretos y variables de entorno, configuración del proveedor de correo y actualización del despliegue de la Web Application en Vercel.

**Entorno local de desarrollo.** Antes del despliegue, cada integrante ejecuta la API contra una base de datos PostgreSQL 16 local. El repositorio incluye un `docker-compose.yml` que levanta el contenedor `vitalink-postgres` con un volumen persistente y el puerto expuesto solo en `127.0.0.1`. Las credenciales se definen en un archivo `.env` creado a partir de `.env.example`, que no se sube al repositorio, y la cadena de conexión se guarda con `dotnet user-secrets`. Así, los seis integrantes trabajan con la misma versión del motor sin instalarlo en su equipo y sin exponer contraseñas en el código (commit `bf0de1e`). El puerto local se define en `.env`; en la captura se usa el 5433 porque el 5432 estaba ocupado.

\includegraphics[width=0.85\linewidth]{assets/523-sprint3-docker-local-db.png}

La captura muestra el contenedor `vitalink-postgres` (imagen `postgres:16`) en ejecución en Docker Desktop.

**Base de datos (T-22).** Se creó el servidor flexible `vitalink-postgres-dev` de Azure Database for PostgreSQL, en el grupo de recursos `rg-vitalink-dev` (suscripción Azure for Students, región Canada Central). La cadena de conexión se configura en la variable de entorno `ConnectionStrings__DefaultConnection` del App Service y no se incluye en el repositorio. Al iniciar, la API aplica las migraciones pendientes (`InitialCreate`, `AddAlerts`, `AddNotifications`, `AddUsers`, `AddHealthRecords`, `AddMonitoringRules`, entre otras), de modo que el esquema de cada bounded context queda creado sin pasos manuales.

**Web Services (T-23).** El despliegue sigue estos pasos:

1. El `Dockerfile` compila la solución con la imagen `dotnet/sdk:10.0` y la ejecuta con `dotnet/aspnet:10.0` en el puerto 8080. La imagen Docker empaqueta la API junto con el runtime de .NET 10 en un único artefacto, que se ejecuta igual en cualquier entorno: el App Service corre ese contenedor sin instalar .NET en el servidor, y cada imagen se etiqueta con el SHA de su commit, lo que permite saber qué versión está desplegada y volver a una anterior si es necesario.
2. El workflow `ci.yml` compila la solución en cada Pull Request hacia `develop`, de modo que un cambio que no compila no se integra.
3. Al integrar en `develop`, el workflow `cd.yml` se autentica en Docker Hub con secretos de GitHub Actions, construye la imagen y la publica como `leorg15/vitalink-api` con las etiquetas `dev` y el SHA del commit.
4. Docker Hub notifica al App Service `vitalink-api-dev` (plan `ASP-rgvitalinkdev-9ad2`, Canada Central) mediante un webhook, y Azure descarga la nueva imagen y reinicia la aplicación.

El equipo eligió `develop` como rama de despliegue del entorno de desarrollo para verificar cada Pull Request integrado en la nube; la rama `main` recibe el incremento estable al cierre del sprint (Pull Request \#23).

**Web Application y Landing Page (T-24).** La Web Application se despliega en Vercel desde `main`. La variable `VITE_BACKEND_API_BASE_URL` de `.env.production` apunta a la API de Azure, y el CORS del backend se configura por entorno (`Cors:AllowedOrigins`): en Azure admite el origen de Vercel y, en desarrollo, `localhost`. La Landing Page se mantiene publicada en GitHub Pages y sus llamadas a la acción dirigen a la Web Application.

\begingroup
\centering
\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.27\textwidth}|p{0.64\textwidth}|}
\hline
\textbf{Producto} & \textbf{Evidencia de despliegue} \\
\hline
\endfirsthead
\hline
\textbf{Producto} & \textbf{Evidencia de despliegue} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Web Services & \nolinkurl{https://vitalink-api-dev-h4gdanfjc5ezbqep.canadacentral-01.azurewebsites.net/api/v1} (Azure App Service, imagen \texttt{leorg15/vitalink-api:dev}) \\
\hline
Verificación & \nolinkurl{https://vitalink-api-dev-h4gdanfjc5ezbqep.canadacentral-01.azurewebsites.net/api/v1/health} responde \texttt{\{"status":"Healthy","database":"Up"\}} \\
\hline
Base de datos & Azure Database for PostgreSQL; migraciones aplicadas al iniciar la API \\
\hline
Web Application & \href{https://vitalink-opal.vercel.app}{https://vitalink-opal.vercel.app} (Vercel, rama \texttt{main}, commit \texttt{a0dbf43}) \\
\hline
Landing Page & \href{https://1asi0730-2620-16712-grupo2-codebrokers.github.io/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page/}{GitHub Pages} (sin cambios en el Sprint 3) \\
\hline
Integración en \texttt{main} & Web Services: Pull Request \#23 (\texttt{a55873f}); Web Application: Pull Request \#18 (\texttt{a0dbf43}), ambos el 9 de noviembre de 2026 \\
\end{longtable}
\endgroup

Table: Productos desplegados al cierre del Sprint 3

La ejecución de pruebas automatizadas en el pipeline se incorpora en el Sprint 4, junto con las pruebas unitarias y de integración de los Web Services.

**Grupo de recursos `rg-vitalink-dev` en Azure, con el App Service, su plan y el servidor PostgreSQL:**

\includegraphics[width=0.95\linewidth]{assets/523-sprint3-azure-resources.png}

**Ejecuciones de los workflows de integración (CI) y despliegue (CD) en GitHub Actions:**

\includegraphics[width=0.95\linewidth]{assets/523-sprint3-actions-runs.png}

**Ejecución del despliegue continuo tras integrar el Pull Request \#22 en `develop`:**

\includegraphics[width=0.95\linewidth]{assets/523-sprint3-cd-workflow.png}

**Imagen `leorg15/vitalink-api` publicada en Docker Hub con las etiquetas `dev` y el SHA del commit:**

\includegraphics[width=0.95\linewidth]{assets/523-sprint3-dockerhub.png}

**Servicio externo de correo (TS-08)**

Para los avisos por correo de TS-08 se configuró **Resend** como proveedor externo (T-13, VTL-85). Se compararon tres servicios con API HTTP y plan gratuito. Se eligió Resend porque ofrece una API HTTP simple, consumible desde un adaptador con `IHttpClientFactory`, y un plan gratuito de 3 000 correos al mes y 100 al día, suficiente para el alcance académico. SendGrid se descartó porque retiró su plan gratuito en mayo de 2025, y Brevo porque requiere un dominio propio para entregar de forma confiable a buzones de Gmail.

\begingroup
\centering
\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.27\textwidth}|p{0.64\textwidth}|}
\hline
\textbf{Elemento} & \textbf{Evidencia} \\
\hline
\endfirsthead
\hline
\textbf{Elemento} & \textbf{Evidencia} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Proveedor & \href{https://resend.com}{Resend} (plan gratuito: 3 000 correos/mes, 100/día) \\
\hline
Integración & Puerto \texttt{IEmailSenderService} y adaptador \texttt{ResendEmailSenderService} (\texttt{POST https://api.resend.com/emails}) en el bounded context Notification \\
\hline
Remitente & \texttt{onboarding@resend.dev} (\texttt{Notification:Email:SenderAddress}), nombre \texttt{VitaLink} (\texttt{Notification:Email:SenderName}) \\
\hline
Credencial & \texttt{Notification:Email:ApiKey}, con permiso de solo envío; se configura con \texttt{dotnet user-secrets} o una variable de entorno y no se incluye en el repositorio \\
\hline
Modo sin credenciales & Sin clave de API se registra \texttt{LoggingEmailSenderService}, que solo escribe el mensaje en el log; el equipo desarrolla y prueba sin cuenta en el proveedor \\
\hline
Restricción & Sin dominio propio, Resend solo entrega al correo de la cuenta; la demostración del aviso al familiar usa ese destinatario \\
\hline
Pull request & \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-web-services/pull/2}{Web Services \#2} (T-14, VTL-86) \\
\end{longtable}
\endgroup

Table: Configuración del servicio externo de correo del Sprint 3

\includegraphics[width=0.8\linewidth]{assets/5237-resend-api-key.png}

La captura muestra la clave de API \texttt{vitalink-dev} creada en Resend para el desarrollo local, con su valor oculto.

Para el entorno desplegado se creó una segunda clave, \texttt{vitalink-azure}, con permiso de solo envío. Se configuró como variable de entorno del App Service (\texttt{Notification\_\_Email\_\_ApiKey}), de modo que la API desplegada envía los correos sin que la clave figure en el repositorio. El destinatario del aviso se define con la variable \texttt{Notification\_\_AlertRecipient\_\_Email} y debe corresponder a un usuario registrado con el rol de familiar cuidador; como Resend sin dominio propio solo entrega al correo de la cuenta, para la demostración se registró ese correo como familiar cuidador de prueba.

\includegraphics[width=0.8\linewidth]{assets/5237-resend-api-key-azure.png}

#### 5.2.3.8. Team Collaboration Insights during Sprint

La implementación del Sprint 3 se organizó por bounded context: cada integrante lideró un módulo de los Web Services en su propia rama `feature/` y lo integró en `develop` mediante Pull Requests revisados por otro integrante. El 29 de octubre se presentó la base de la API para que todos construyeran sus módulos sobre la misma estructura, y en la revisión de mitad de sprint se acordaron las dependencias entre módulos. Para reducir conflictos al integrar varias ramas, el equipo acordó tres reglas: el Pull Request que se fusiona después regenera su migración y verifica que solo modifique sus propias tablas; en los archivos compartidos (`SharedResource.resx` y `Program.cs`) se conservan las líneas de todos; y nadie fusiona su propio Pull Request.

En el repositorio de Web Services se registraron 201 commits de los seis integrantes entre el 25 de octubre y el 9 de noviembre de 2026, sin contar los commits de merge, y 17 commits en la Frontend Web Application.

\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.24\textwidth}|p{0.16\textwidth}|p{0.09\textwidth}|p{0.43\textwidth}|}
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{Commits} & \textbf{Contribución principal en el Sprint 3} \\
\hline
\endfirsthead
\hline
\textbf{Team Member} & \textbf{GitHub Username} & \textbf{Commits} & \textbf{Contribución principal en el Sprint 3} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Benigno Montero, Harold Fauskorp & harold-11 & WS: 44 \newline FE: 2 & Base de la API (TS-03), identidad de usuarios (T-4), corrección del modelo de reglas de monitoreo y evaluación por severidad, integración del historial del paciente en la Web Application y revisión e integración de Pull Requests. \\
\hline
Said Conde, Yazid & BL4Z3K4D & WS: 33 & Agregado Alert, consulta paginada de alertas, generación automática e idempotente de alertas a partir de los registros de salud (US-14) y endpoint de observación de US-12. \\
\hline
Salon Puerta, Merly & MerlySalonP & WS: 45 & Agregado HealthRecord y catálogo de tipos, reglas de monitoreo, validación por tipo y endpoints del historial de salud (US-16). \\
\hline
Osorio Ramírez, Eduardo Jesús & Iron819 & WS: 31 \newline FE: 13 & Bounded context Notification, adaptador de Resend y correo al familiar ante una alerta (TS-08); integración del resumen y del cambio de estado de alertas en la Web Application (US-11). \\
\hline
Tello Quispe, Luis German & luistello1739-web & WS: 39 \newline FE: 2 & Cambio de estado de alertas con historial y control de concurrencia (US-18), asociación paciente-proveedor (US-19) y estado de las alertas en el panel familiar (T-17). \\
\hline
Rodriguez Gonzales, Leonel German & leokiss15 & WS: 9 & Dockerfile, workflows de integración y despliegue continuo, base de datos PostgreSQL y App Service en Azure (TS-07). \\
\end{longtable}
\endgroup

Table: Contribuciones por integrante durante el Sprint 3

El número de commits refleja la forma de trabajo de cada integrante y no el esfuerzo: la infraestructura de despliegue de Leonel se configuró principalmente en Azure y Docker Hub, fuera del repositorio.

**Aplicación de GitFlow.** La captura siguiente muestra los 23 Pull Requests del repositorio de Web Services, todos cerrados. Cada rama `feature/` se integró en `develop` con la revisión aprobada de otro integrante (columna de revisiones 1/1) y la verificación del workflow de compilación; el incremento estable pasó de `develop` a `main` con el Pull Request \#23 (*Release Sprint 3*). El Pull Request \#17 se cerró sin integrarse.

\includegraphics[width=0.95\linewidth]{assets/523-sprint3-pull-requests.png}

**Evolución del trabajo pendiente.** La gráfica de Jira por Story Points muestra que el trabajo restante se mantuvo sin cambios durante la primera semana, mientras se construían los módulos en ramas separadas, y disminuyó entre el 5 y el 9 de noviembre, cuando se integraron y finalizaron las historias. Las caídas del 8 y 9 de noviembre incluyen el retiro de los cuatro elementos trasladados al Sprint 4.

\includegraphics[width=0.95\linewidth]{assets/523-sprint3-burndown.png}

\includegraphics[width=0.95\linewidth]{assets/523-sprint3-scope-changes.png}

\includegraphics[width=0.95\linewidth]{assets/523-sprint3-completed-items.png}

El informe del sprint registra los cambios de alcance y las ocho actividades completadas (42 Story Points). La gráfica por horas no se presenta porque las estimaciones en horas se registraron en este informe, pero no en el campo de estimación original de Jira.

**Insights del repositorio de Web Services (commits por integrante):**

\includegraphics[width=0.8\linewidth]{assets/523-sprint3-insights-web-services.png}

**Insights del repositorio de la Frontend Web Application:**

\includegraphics[width=0.8\linewidth]{assets/523-sprint3-insights-frontend.png}

GitHub calcula estos analíticos sobre la rama `main`, por lo que reflejan el incremento integrado con los Pull Requests de release de cada repositorio.

**Sprint Review 3.** En el Sprint Review del 9 de noviembre se demostró el incremento integrado en la rama `main` de ambos repositorios y desplegado en Azure:

- **Preventive Monitoring.** Registro y consulta del historial de salud por adulto mayor (`/older-adults/{id}/health-records`) y evaluación de cada registro contra las reglas de monitoreo activas, por orden de prioridad (US-16).
- **Alerting.** Generación automática e idempotente de una alerta cuando un registro queda fuera de umbral (US-14), consulta de alertas pendientes y del historial de estados, y cambio de estado a en revisión o atendida sin eliminar la alerta (US-11, US-18).
- **Elder Care.** Asociación de un paciente con su proveedor de salud mediante `PATCH /older-adults/{id}/care-provider` (US-19).
- **Notification.** Al generarse una alerta, el manejador `AlertRaisedEmailNotifier` envía el aviso por correo mediante Resend (TS-08).
- **Web Application.** El resumen de alertas, las acciones de iniciar revisión y marcar como atendida, el historial del paciente y el estado de las alertas en el panel familiar consumen la API desplegada (TS-03, TS-07).

Se completaron 42 de los 53 Story Points comprometidos (79 \%). Durante el sprint se retiraron cuatro elementos (11 Story Points), registrados en el informe de cambios de alcance de Jira, que pasan al Sprint 4.

El Sprint Goal se **cumplió**. Un profesional consulta en la Web Application desplegada una alerta generada por la API a partir de un registro de salud y cambia su estado, mientras el familiar consulta ese estado en su panel. La integración del aviso por correo se completó dentro del sprint; la entrega a un buzón real se confirmó el 10 de noviembre, después de reemplazar el destinatario de demostración, que Resend rechazaba, por el correo de un familiar cuidador.

**Sprint Retrospective 3.** El equipo analizó el sprint en tres partes:

\begingroup
\centering
\small
\setlength{\tabcolsep}{5pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.22\textwidth}|p{0.69\textwidth}|}
\hline
\textbf{Aspecto} & \textbf{Resumen} \\
\hline
\endfirsthead
\hline
\textbf{Aspecto} & \textbf{Resumen} \\
\hline
\endhead
\hline
\endfoot
\hline
\endlastfoot
Aciertos & Presentar la base de la API al inicio permitió que cada integrante construyera su bounded context en paralelo sobre las mismas convenciones. Las reglas de integración (migraciones, archivos compartidos y revisión por otro integrante) evitaron perder trabajo al fusionar ramas. El despliegue continuo desde \texttt{develop} permitió verificar cada integración en la nube. Se aplicó la mejora del Sprint 2 de mover las tareas en Jira el mismo día en que cambian de estado. \\
\hline
Oportunidades de mejora & La mayor parte de las integraciones se concentró en la segunda semana, como muestra el burndown. La cadena de dependencias (registro de salud, regla de monitoreo, evaluación, alerta y correo) hizo que varias historias esperaran a otras, y el modelo de reglas de monitoreo necesitó un Pull Request adicional de correcciones. Al resolver un conflicto de merge en \texttt{Program.cs} se perdió el cambio que publicaba la documentación OpenAPI en el despliegue. Las horas estimadas no se registraron en Jira, por lo que el burndown por horas quedó vacío. El aviso por correo se integró con un destinatario de demostración y su entrega real no se verificó hasta después de la Review. Además, el servicio REST simulado que aún provee los pacientes tarda en responder la primera vez, lo que puede mostrar un error al abrir la Web Application. \\
\hline
Ajuste de alcance & Cuatro elementos se retiraron del sprint (11 Story Points). US-25 concentraba 19 horas en cuatro tareas frente a sus 3 Story Points, lo que evidenció una subestimación en el Product Backlog; de ella se completó la base de identidad (T-4). US-20 depende de esa identidad, TS-06 de la configuración final de la API y, de US-12, el endpoint de observación ya está en \texttt{main}, pero falta su integración en la Web Application. El equipo priorizó cerrar el flujo de alertas antes que abrir historias que no alcanzarían el Definition of Done. \\
\hline
Hallazgos en el código & El aviso por correo se envía a un único destinatario configurado (\texttt{AlertRecipientOptions}) y no al familiar asociado al adulto mayor. El repositorio de Web Services aún no tiene pruebas automatizadas. La Web Application todavía obtiene pacientes del servicio REST simulado. Quedan ramas sin integrar ni cerrar (\texttt{feature/patient-health-history} en Web Services y \texttt{feature/t21-patient-history} en la Web Application). \\
\hline
Acciones para el Sprint 4 & (1) Re-estimar las historias retiradas antes del Sprint Planning 4 y planificarlas según sus dependencias. (2) Integrar cada tarea en \texttt{develop} en cuanto esté revisada, sin esperar a terminar toda la historia. (3) Incorporar las pruebas unitarias y de integración y ejecutarlas en el pipeline. (4) Reemplazar los servicios simulados restantes (pacientes) por la API. (5) Registrar en Jira la estimación original en horas de cada tarea al planificar. (6) Revisar en cada Pull Request que la resolución de conflictos no descarte cambios de otros integrantes. (7) Enviar el aviso por correo al familiar asociado al adulto mayor en lugar de un destinatario fijo. (8) Cerrar las ramas de característica ya integradas o abandonadas. \\
\end{longtable}
\endgroup

Table: Resumen de la Sprint Retrospective 3


<!-- Sprint 4: se completa para el TB2
### 5.2.4. Sprint 4

#### 5.2.4.1. Sprint Planning 4



#### 5.2.4.2. Aspect Leaders and Collaborators



#### 5.2.4.3. Sprint Backlog 4



#### 5.2.4.4. Development Evidence for Sprint Review



#### 5.2.4.5. Execution Evidence for Sprint Review



#### 5.2.4.6. Services Documentation Evidence for Sprint Review



#### 5.2.4.7. Software Deployment Evidence for Sprint Review



#### 5.2.4.8. Team Collaboration Insights during Sprint
-->
