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

El sprint se desarrolla del 25 de octubre al 8 de noviembre de 2026, según el sprint **Sprint 3 - Web Services** registrado en Jira. Al tratarse del penúltimo sprint, el equipo comprometió aproximadamente la mitad del Product Backlog pendiente: 53 de los 106 Story Points restantes. La selección consideró el avance del sílabo del curso hasta la entrega del AV2; por ello, el endurecimiento de la seguridad (TS-04) y las pruebas unitarias y de integración de los Web Services se programaron para el Sprint 4, ya que sus temas (Web Services Security - Part 2 y Best Practices) se desarrollan entre las semanas 13 y 16.

<!-- PENDIENTE: completar Time y Attendees con los datos reales de la reunión del 25/10 (captura de inicio y cierre en Microsoft Teams). -->

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
\textbf{Time} & \textit{Por completar tras la reunión} \\
\hline
\textbf{Location} & Reunión remota vía Microsoft Teams \\
\hline
\textbf{Prepared By} & Benigno Montero, Harold Fauskorp \\
\hline
\textbf{Attendees (to planning meeting)} & \textit{Por completar tras la reunión} \\
\hline
\textbf{Sprint 2 Review Summary} & El Sprint 2 concluyó con los 37 Story Points comprometidos en estado finalizado. Se desplegó la primera versión de la Frontend Web Application, desarrollada con Vue 3 y PrimeVue, con las vistas para profesionales de la salud y familiares cuidadores, internacionalización en inglés y español y soporte de accesibilidad, consumiendo un servicio REST simulado. \\
\hline
\textbf{Sprint 2 Retrospective Summary} & El equipo identificó que los estados de Jira se actualizaron al cierre del sprint, por lo que el burndown no reflejó el avance real. Se acordó mover cada tarea el mismo día en que cambia de estado, mantener una rama por elemento del backlog y revisar cada Pull Request por otro integrante antes de integrarlo en \texttt{develop}. \\
\hline
\textbf{Sprint 3 Goal} & \textbf{Our focus is on} que profesionales de la salud y familiares cuidadores trabajen con datos reales persistidos mediante la API RESTful de VitaLink, con acceso por rol. \newline\newline \textbf{We believe it delivers} alertas, historial de salud y asociación paciente-proveedor confiables, además de avisos por correo ante eventos críticos. \newline\newline \textbf{This will be confirmed when} un usuario inicia sesión en la Web Application desplegada, consulta una alerta generada por la API, la atiende con una observación y el familiar recibe el correo de aviso del servicio externo. \\
\hline
\textbf{Sprint 3 Velocity} & 53 Story Points \\
\hline
\textbf{Sum of Story Points} & 53 Story Points \\
\end{longtable}
\endgroup

Table: Sprint Planning 3

Durante el Sprint Planning, el equipo revisó la descomposición de cada elemento del backlog en tareas, acordó los responsables y estimó en horas cada tarea, con un máximo de 8 horas por tarea; las tareas que superaron ese límite se dividieron en la misma reunión. Además, se programaron cuatro reuniones de seguimiento del sprint en Microsoft Teams, registradas con capturas de inicio y cierre en las que se identifican los participantes.

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
1 & Sprint Planning 3 & 2026-10-25, 21:00--22:00 & Definir el Sprint Goal, el alcance, los responsables y la estimación en horas de las tareas. \\
\hline
2 & Revisión del backend base & 2026-10-29, 21:00--21:20 & Presentar la base de la API y acordar cómo cada integrante construye su módulo sobre ella. \\
\hline
3 & Revisión de mitad de sprint & 2026-10-31, 21:00--21:20 & Revisar el tablero, las dependencias entre tareas y los Pull Requests pendientes. \\
\hline
4 & Sprint Review y Sprint Retrospective 3 & 2026-11-07, 21:00--22:00 & Demostrar el incremento desplegado, verificar el Sprint Goal y acordar mejoras para el Sprint 4. \\
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
Sprint Planning 3 & 21:00--21:05 & Captura de inicio con asistentes y apertura. \\
\cline{2-3}
(2026-10-25) & 21:05--21:15 & Resumen del Sprint Review y de la Sprint Retrospective del Sprint 2. \\
\cline{2-3}
 & 21:15--21:25 & Sprint Goal 3 y alcance: 12 elementos del backlog y 53 Story Points; elementos que se trasladan al Sprint 4 y motivo. \\
\cline{2-3}
 & 21:25--21:30 & Responsables y Leadership-and-Collaboration Matrix (LACX). \\
\cline{2-3}
 & 21:30--21:50 & Estimación en horas de las tareas T-1 a T-30 (máximo 8 horas por tarea). \\
\cline{2-3}
 & 21:50--21:55 & Acuerdos técnicos: repositorio de Web Services en C\# y .NET 10, Swagger mediante Swashbuckle, PostgreSQL, ramas \texttt{feature/}, Pull Requests revisados por otro integrante e internacionalización de la API con inglés por defecto. \\
\cline{2-3}
 & 21:55--22:00 & Dudas, cierre y captura final. \\
\hline
Revisión del backend base & 21:00--21:02 & Captura de inicio con asistentes. \\
\cline{2-3}
(2026-10-29) & 21:02--21:10 & Demostración de la base de la API: solución ASP.NET Core por bounded contexts, Entity Framework Core con PostgreSQL, migración inicial, manejo de errores e internacionalización (T-1 a T-3). \\
\cline{2-3}
 & 21:10--21:15 & Construcción de cada módulo sobre la base, con prioridad para los modelos de los que dependen otras tareas: Alert (T-8), HealthRecord (T-18) y Patient (T-27). \\
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
 & 21:18--21:20 & Plan de la segunda semana: inicio de sesión (T-4 a T-7), integración y despliegue final. Cierre y captura final. \\
\hline
Sprint Review y & 21:00--21:05 & Captura de inicio con asistentes. \\
\cline{2-3}
Sprint Retrospective 3 & 21:05--21:40 & Sprint Review: demostración por integrante en la Web Application y los Web Services desplegados. \\
\cline{2-3}
(2026-11-07) & 21:40--21:45 & Verificación del cumplimiento del Sprint Goal. \\
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

El Sprint Backlog 3 reúne doce elementos del Product Backlog orientados a la primera versión de los Web Services y a su integración con la Web Application. La planificación y el control de estados se realizan en Jira, en el sprint **Sprint 3 - Web Services** del proyecto VTL, con el flujo To-do, In Process, To Review y Done (Por hacer, En curso, En revisión y Finalizado). La captura del tablero se presenta a continuación y las tablas posteriores transcriben su contenido para mantener el artefacto legible y trazable dentro del informe.

**URL pública del Sprint Backlog en Jira:** \nolinkurl{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1}

<!-- PENDIENTE: insertar la captura del tablero del Sprint 3 tomada después del Sprint Planning (assets/523-sprint3-board.png). -->

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
TS-03 & VTL-67 & Configuración base del Backend RESTful API y persistencia & 5 & Benigno Montero, Harold Fauskorp & To-do \\
\hline
US-25 & VTL-56 & Inicio y cierre de sesión con navegación por rol & 3 & Benigno Montero, Harold Fauskorp & To-do \\
\hline
US-20 & VTL-45 & Validación de datos básicos del paciente & 3 & Benigno Montero, Harold Fauskorp & To-do \\
\hline
US-14 & VTL-35 & Generación automática de alerta desde un evento & 8 & Said Conde, Yazid & To-do \\
\hline
US-12 & VTL-42 & Observación breve al atender una alerta & 2 & Said Conde, Yazid & To-do \\
\hline
US-16 & VTL-47 & Almacenamiento del historial del paciente & 8 & Salon Puerta, Merly & To-do \\
\hline
TS-08 & VTL-72 & Integración confiable de notificaciones externas & 5 & Osorio Ramírez, Eduardo Jesús & To-do \\
\hline
US-11 & VTL-41 & Marcar alerta como en revisión o atendida & 3 & Osorio Ramírez, Eduardo Jesús & To-do \\
\hline
US-18 & VTL-40 & Cambio de estado de alerta sin eliminar & 5 & Tello Quispe, Luis German & To-do \\
\hline
US-19 & VTL-46 & Asociación de paciente con proveedor de salud & 3 & Tello Quispe, Luis German & To-do \\
\hline
TS-07 & VTL-71 & Integración continua y despliegue de la Web Application & 5 & Rodriguez Gonzales, Leonel German & To-do \\
\hline
TS-06 & VTL-70 & Documentación y verificación de contratos de servicios & 3 & Rodriguez Gonzales, Leonel German & To-do \\
\hline
\multicolumn{3}{|r|}{\textbf{Total}} & \textbf{53} & \multicolumn{2}{l|}{} \\
\end{longtable}
\endgroup

Table: Elementos del Product Backlog incluidos en el Sprint 3

La tabla siguiente presenta la descomposición de cada elemento en tareas, según la estructura de control de estado del sprint. Cada tarea está asignada al mismo integrante responsable de su elemento del backlog.

<!-- PENDIENTE: completar la columna Estimation (Hours) con las horas acordadas en el Sprint Planning del 25/10 y registrar las tareas que se hayan dividido por superar 8 horas. -->

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
TS-03 & Configuración base del Backend RESTful API y persistencia & T-1 (VTL-73) & Crear la solución ASP.NET Core por bounded contexts & Solución en .NET 10 con capas Domain, Application, Infrastructure e Interfaces, prefijo \texttt{/api/v1}, CORS por entorno y endpoint de salud. & --- & Benigno Montero, Harold & To-do \\
\hline
TS-03 & Configuración base del Backend RESTful API y persistencia & T-2 (VTL-74) & Configurar Entity Framework Core con PostgreSQL & DbContext, convenciones de nombres, Unit of Work, repositorio base y migración inicial sin credenciales en el repositorio. & --- & Benigno Montero, Harold & To-do \\
\hline
TS-03 & Configuración base del Backend RESTful API y persistencia & T-3 (VTL-75) & Manejo uniforme de errores e internacionalización de la API & Middleware de excepciones con ProblemDetails y mensajes localizados en\_US (por defecto) y es\_419 según el encabezado Accept-Language. & --- & Benigno Montero, Harold & To-do \\
\hline
US-25 & Inicio y cierre de sesión con navegación por rol & T-4 (VTL-76) & Usuarios, roles, hash de contraseñas y usuarios semilla & Modelo User y Role en el bounded context IAM, contraseñas con BCrypt y usuarios semilla por rol. & --- & Benigno Montero, Harold & To-do \\
\hline
US-25 & Inicio y cierre de sesión con navegación por rol & T-5 (VTL-77) & Emisión y validación de JWT con autorización por rol & Tokens con expiración, emisor y audiencia, middleware de autenticación y políticas de autorización por rol. & --- & Benigno Montero, Harold & To-do \\
\hline
US-25 & Inicio y cierre de sesión con navegación por rol & T-6 (VTL-78) & Endpoints de inicio y cierre de sesión & \texttt{POST /api/v1/authentication/sign-in} y \texttt{sign-out}, respuesta segura ante credenciales inválidas y protección de endpoints. & --- & Benigno Montero, Harold & To-do \\
\hline
US-25 & Inicio y cierre de sesión con navegación por rol & T-7 (VTL-79) & Integrar inicio y cierre de sesión en la Web Application & Vista de inicio de sesión, store de sesión, interceptor de Axios, guards por rol y conexión de los CTA de la Landing Page. & --- & Benigno Montero, Harold & To-do \\
\hline
US-14 & Generación automática de alerta desde un evento & T-8 (VTL-80) & Modelar el agregado Alert y su persistencia & Agregado Alert y MonitoringRule en el bounded context Alerts con configuración Fluent API y migración. & --- & Said Conde, Yazid & To-do \\
\hline
US-14 & Generación automática de alerta desde un evento & T-9 (VTL-81) & Generación automática de alertas por umbral & \texttt{POST /api/v1/alerts} que evalúa un registro de salud y crea una única alerta PENDING de forma idempotente y transaccional. & --- & Said Conde, Yazid & To-do \\
\hline
US-14 & Generación automática de alerta desde un evento & T-10 (VTL-82) & Endpoints de consulta de alertas & \texttt{GET /api/v1/alerts} con filtros por estado y paciente, y \texttt{GET /api/v1/alerts/\{id\}}. & --- & Said Conde, Yazid & To-do \\
\hline
US-11 & Marcar alerta como en revisión o atendida & T-11 (VTL-83) & Transiciones a en revisión y atendida & Transiciones PENDING, IN\_REVIEW y ATTENDED con actor y fecha sobre el endpoint de estado de US-18. & --- & Osorio Ramírez, Eduardo & To-do \\
\hline
US-11 & Marcar alerta como en revisión o atendida & T-12 (VTL-84) & Integrar el resumen y el cambio de estado de alertas en la Web Application & Reemplazo del servicio simulado de alertas por la API real, con manejo de conflictos y errores de red. & --- & Osorio Ramírez, Eduardo & To-do \\
\hline
TS-08 & Integración confiable de notificaciones externas & T-13 (VTL-85) & Seleccionar y configurar el proveedor externo de correo & Elección del servicio de terceros, creación de la cuenta, verificación del remitente y registro de la clave como secreto. & --- & Osorio Ramírez, Eduardo & To-do \\
\hline
TS-08 & Integración confiable de notificaciones externas & T-14 (VTL-86) & Adaptador del servicio externo de notificaciones & Interfaz de envío y adaptador en el bounded context Notifications con clave idempotente, registro de intentos y reintentos limitados. & --- & Osorio Ramírez, Eduardo & To-do \\
\hline
TS-08 & Integración confiable de notificaciones externas & T-15 (VTL-87) & Enviar correo al familiar al generarse una alerta & Envío del correo ante una alerta creada, con plantilla en inglés y español según la preferencia del familiar. & --- & Osorio Ramírez, Eduardo & To-do \\
\hline
US-18 & Cambio de estado de alerta sin eliminar & T-16 (VTL-88) & Cambio de estado con historial y control de concurrencia & \texttt{PATCH /api/v1/alerts/\{id\}/status} con validación de transiciones, auditoría, cierre sin eliminación y control de concurrencia. & --- & Tello Quispe, Luis & To-do \\
\hline
US-18 & Cambio de estado de alerta sin eliminar & T-17 (VTL-89) & Integrar el estado de las alertas en la vista familiar & Consulta del estado actual y del historial de cambios de las alertas desde la vista familiar. & --- & Tello Quispe, Luis & To-do \\
\hline
US-16 & Almacenamiento del historial del paciente & T-18 (VTL-90) & Modelar HealthRecord y su persistencia & HealthRecord y catálogo de tipos de registro en el bounded context Health Records con configuración Fluent API y migración. & --- & Salon Puerta, Merly & To-do \\
\hline
US-16 & Almacenamiento del historial del paciente & T-19 (VTL-91) & Endpoints de registro y consulta del historial de salud & \texttt{POST} y \texttt{GET /api/v1/older-adults/\{id\}/health-records} con filtros por fecha y tipo y orden descendente. & --- & Salon Puerta, Merly & To-do \\
\hline
US-16 & Almacenamiento del historial del paciente & T-20 (VTL-92) & Validar los registros de salud según su tipo & Reglas de validación por tipo de registro con mensajes localizados en\_US y es\_419, sin persistencia parcial. & --- & Salon Puerta, Merly & To-do \\
\hline
US-16 & Almacenamiento del historial del paciente & T-21 (VTL-93) & Integrar el historial del paciente en la Web Application & Reemplazo del servicio simulado del historial de registros por la API real. & --- & Salon Puerta, Merly & To-do \\
\hline
TS-07 & Integración continua y despliegue de la Web Application & T-22 (VTL-94) & Desplegar la base de datos PostgreSQL en la nube & Instancia administrada de PostgreSQL con acceso seguro y cadenas de conexión por entorno. & --- & Rodriguez Gonzales, Leonel & To-do \\
\hline
TS-07 & Integración continua y despliegue de la Web Application & T-23 (VTL-95) & Desplegar los Web Services con GitHub Actions & Pipeline que compila y despliega la API en la nube al integrar en \texttt{main}, aplicando migraciones con variables protegidas. & --- & Rodriguez Gonzales, Leonel & To-do \\
\hline
TS-07 & Integración continua y despliegue de la Web Application & T-24 (VTL-96) & Actualizar el despliegue de la Web Application y la Landing Page & URL de la API por entorno en la Web Application, nuevos despliegues y verificación de los CTA de la Landing Page. & --- & Rodriguez Gonzales, Leonel & To-do \\
\hline
TS-06 & Documentación y verificación de contratos de servicios & T-25 (VTL-97) & Configurar Swagger/OpenAPI con ejemplos y esquema JWT & Swagger mediante Swashbuckle con comentarios XML, ejemplos sin datos personales reales y esquema de seguridad Bearer. & --- & Rodriguez Gonzales, Leonel & To-do \\
\hline
TS-06 & Documentación y verificación de contratos de servicios & T-26 (VTL-98) & Verificar los contratos y publicar la documentación desplegada & Prueba de los contratos con datos de muestra desde Swagger desplegado y validación de la especificación OpenAPI. & --- & Rodriguez Gonzales, Leonel & To-do \\
\hline
US-19 & Asociación de paciente con proveedor de salud & T-27 (VTL-99) & Asociación entre paciente y proveedor de salud & Modelo OlderAdult y CareProvider y \texttt{PUT /api/v1/older-adults/\{id\}/care-provider} idempotente. & --- & Tello Quispe, Luis & To-do \\
\hline
US-20 & Validación de datos básicos del paciente & T-28 (VTL-100) & Creación y actualización validada del perfil del paciente & \texttt{POST} y \texttt{PUT /api/v1/older-adults} con validaciones de identificación y de activación del seguimiento. & --- & Benigno Montero, Harold & To-do \\
\hline
US-20 & Validación de datos básicos del paciente & T-29 (VTL-101) & Integrar la búsqueda y el detalle de pacientes en la Web Application & Reemplazo del servicio simulado de pacientes asignados y del detalle de paciente por la API real. & --- & Benigno Montero, Harold & To-do \\
\hline
US-12 & Observación breve al atender una alerta & T-30 (VTL-102) & Observación breve al atender una alerta & Registro de una observación opcional de 1 a 1000 caracteres asociada a la atención y su captura en la Web Application. & --- & Said Conde, Yazid & To-do \\
\end{longtable}
\endgroup

Table: Sprint Backlog 3

El esfuerzo total comprometido es de **53 Story Points**. La trazabilidad se conserva mediante las claves VTL de Jira, las ramas de característica y los commits que se registrarán en la sección siguiente.


#### 5.2.3.4. Development Evidence for Sprint Review

<!-- PENDIENTE (cierre del sprint): introducción con los avances de implementación y tabla de commits por repositorio (Web Services, Frontend Web Application y Landing Page) con Repository, Branch, Commit Id, Commit Message, Commit Message Body y Committed on (Date). -->


#### 5.2.3.5. Execution Evidence for Sprint Review

<!-- PENDIENTE (cierre del sprint): resumen de lo alcanzado, capturas de las vistas integradas con la API (inicio de sesión, alertas, historial y pacientes) y URL completa del video de navegación del sprint. -->


#### 5.2.3.6. Services Documentation Evidence for Sprint Review

<!-- PENDIENTE (cierre del sprint): introducción, tabla de endpoints documentados con OpenAPI (verbo HTTP, sintaxis de llamada, parámetros, ejemplo y explicación del response, URL de la documentación desplegada), capturas de Swagger con datos de muestra, URL del repositorio de Web Services e ids de los commits de documentación. -->


#### 5.2.3.7. Software Deployment Evidence for Sprint Review

<!-- PENDIENTE (cierre del sprint): pasos y capturas del despliegue de la base de datos PostgreSQL, los Web Services (pipeline de GitHub Actions), la Web Application y la Landing Page; URLs públicas de cada producto. Indicar que la ejecución de pruebas en el pipeline se incorpora en el Sprint 4. -->


#### 5.2.3.8. Team Collaboration Insights during Sprint

<!-- PENDIENTE (cierre del sprint): explicación de las actividades de implementación y capturas de los analíticos de colaboración y commits en GitHub de cada repositorio, evidenciando la participación de los seis integrantes. -->


### 5.2.4. Sprint 4

#### 5.2.4.1. Sprint Planning 4



#### 5.2.4.2. Aspect Leaders and Collaborrators



#### 5.2.4.3. Sprint Backlog 4



#### 5.2.4.4. Development Evidence for Sprint Review



#### 5.2.4.5. Execution Evidence for Sprint Review



#### 5.2.4.6. Services Documentation Evidence for Sprint Review



#### 5.2.4.7. Software Deployment Evidence for Sprint Review



#### 5.2.4.8. Team Collaboration Insights during Sprint




