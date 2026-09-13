## 3.3. Product Backlog.

El Product Backlog de VitaLink reúne las 21 User Stories identificadas en la sección 3.1, ordenadas según el valor que aportan al negocio. El criterio de priorización fue el siguiente: primero las historias del sitio web estático, que son las que comunican la propuesta de valor y captan tanto a profesionales de salud como a familiares; a continuación el circuito que entrega el valor central del producto, es decir, detectar la situación de riesgo, notificar al profesional y registrar la atención; y finalmente el contexto clínico de respaldo. Las historias de habilitación técnica, redactadas como "Como sistema, quiero...", no encabezan el backlog: cada una se ubica inmediatamente antes de la historia de usuario que la necesita.

La gestión del Product Backlog se realiza en **Jira**, en el proyecto CodeBrokers (clave VTL) de la organización `codebrokers.atlassian.net`. Las historias están agrupadas en tres épicas —EP-01 Landing Page, EP-02 Frontend y EP-03 Backend— y cada una incluye su descripción, sus criterios de aceptación y su estimación en story points.

**URL del Product Backlog:** \href{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1/backlog}{https://codebrokers.atlassian.net/jira/software/projects/VTL/boards/1/backlog}

Las siete historias del épico EP-01 (Landing Page) se encuentran comprometidas en el Sprint 1, mientras que las catorce restantes permanecen en el backlog a la espera de su planificación en los sprints siguientes.

\begin{figure}[h!]
\centering
\includegraphics[width=\linewidth]{assets/33-product-backlog-jira-sprint1.png}
\caption{Historias comprometidas en el Sprint 1 (16 story points)}
\end{figure}

\begin{figure}[h!]
\centering
\includegraphics[width=\linewidth]{assets/33-product-backlog-jira-backlog.png}
\caption{Historias pendientes en el backlog (58 story points)}
\end{figure}

\begin{table}[h!]
\centering
\small
\begin{tabular}{|p{0.05\textwidth}|p{0.08\textwidth}|p{0.21\textwidth}|p{0.42\textwidth}|p{0.05\textwidth}|}
\hline
\textbf{\# Orden} & \textbf{User Story Id} & \textbf{Título} & \textbf{Descripción} & \textbf{Story Points} \\ \hline
1 & US-01 & Propuesta de valor clara en Landing Page & Como visitante médico, quiero entender en segundos qué problema resuelve VitaLink, para decidir si me interesa conocer más. & 2 \\ \hline
2 & US-03 & Botón para solicitar información & Como profesional de salud, quiero un botón claro para "solicitar información" antes de registrarme, para evaluar la herramienta sin compromiso. & 3 \\ \hline
3 & US-06 & Botón para unirse como proveedor de salud & Como profesional de salud, quiero un botón específico para "unirme como proveedor de salud", para iniciar mi registro directamente. & 2 \\ \hline
4 & US-02 & Sección de privacidad y seguridad de datos & Como profesional de salud, quiero ver una sección de privacidad/seguridad de datos, para confiar en registrar información de mis pacientes. & 2 \\ \hline
5 & US-07 & Ejemplo visual de una alerta & Como profesional de salud, quiero ver un ejemplo visual simple de cómo se ve una alerta, para entender rápido cómo funciona el seguimiento. & 2 \\ \hline
6 & US-04 & Respaldo de clínicas e instituciones & Como profesional de salud, quiero ver quiénes respaldan la plataforma (clínicas/instituciones), para confiar en su legitimidad. & 2 \\ \hline
7 & US-05 & Sección de preguntas frecuentes & Como profesional de salud, quiero ver una sección de preguntas frecuentes, para resolver dudas sin tener que contactar a alguien. & 3 \\ \hline
8 & US-15 & Generación automática de alerta desde un evento & Como sistema, quiero registrar un evento y generar automáticamente una alerta asociada, para iniciar el flujo de atención. & 8 \\ \hline
9 & US-08 & Resumen inicial de alertas pendientes & Como médico, quiero ver un resumen inicial con la cantidad de pacientes con alertas pendientes, para priorizar mi atención al iniciar el día. & 5 \\ \hline
10 & US-16 & Asignación de nivel de prioridad a alertas & Como sistema, quiero asignar un nivel de prioridad a cada alerta, para permitir su ordenamiento en el frontend. & 5 \\ \hline
11 & US-09 & Nivel de urgencia visual en cada alerta & Como médico, quiero ver el nivel de urgencia de cada alerta de forma visual (color/etiqueta), para decidir rápido qué revisar primero. & 3 \\ \hline
12 & US-10 & Acceso al detalle de paciente desde el resumen & Como médico, quiero acceder al detalle de un paciente desde el resumen, para revisar contexto sin buscar en varias pantallas. & 3 \\ \hline
13 & US-19 & Cambio de estado de alerta sin eliminar & Como sistema, quiero cambiar el estado de una alerta (pendiente/en revisión/atendida/cerrada) sin eliminarla, para conservar el historial completo. & 5 \\ \hline
14 & US-12 & Marcar alerta como en revisión o atendida & Como médico, quiero marcar una alerta como "en revisión" o "atendida", para que otros sepan el estado del caso. & 3 \\ \hline
15 & US-13 & Observación breve al atender una alerta & Como médico, quiero agregar una observación breve al atender una alerta, para dejar registro rápido de lo ocurrido. & 2 \\ \hline
16 & US-18 & Trazabilidad de atención de alertas & Como sistema, quiero registrar quién atendió una alerta y cuándo, para mantener trazabilidad de las acciones. & 3 \\ \hline
17 & US-14 & Visibilidad de revisión previa por otro profesional & Como médico, quiero ver si un caso ya fue revisado por otra persona, para evitar duplicar esfuerzos. & 2 \\ \hline
18 & US-21 & Validación de datos básicos del paciente & Como sistema, quiero validar que los datos básicos de un paciente estén completos antes de activar su seguimiento, para asegurar información mínima confiable. & 3 \\ \hline
19 & US-20 & Asociación de paciente con proveedor de salud & Como sistema, quiero asociar a cada paciente un proveedor de salud (si existe), para vincular la información clínica correspondiente. & 3 \\ \hline
20 & US-17 & Almacenamiento del historial del paciente & Como sistema, quiero almacenar el historial de un paciente (registros, alertas, acciones), para permitir consultas posteriores. & 8 \\ \hline
21 & US-11 & Historial de registros del paciente ordenado por fecha & Como médico, quiero ver el historial de registros de un paciente ordenado por fecha, para entender su evolución sin papeles dispersos. & 5 \\ \hline
\multicolumn{4}{|r|}{\textbf{Total}} & \textbf{74} \\ \hline
\end{tabular}
\caption{Product Backlog de VitaLink}
\end{table}
