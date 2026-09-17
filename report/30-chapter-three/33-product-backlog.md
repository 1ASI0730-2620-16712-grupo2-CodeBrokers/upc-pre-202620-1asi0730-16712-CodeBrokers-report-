## 3.3. Product Backlog.

<<<<<<< HEAD
\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.06\textwidth}|p{0.12\textwidth}|p{0.26\textwidth}|p{0.42\textwidth}|p{0.08\textwidth}|}
\hline
\textbf{\# Orden} & \textbf{User Story Id} & \textbf{Título} & \textbf{Descripción} & \textbf{Story Points} \\
\hline
\endfirsthead

\hline
\textbf{\# Orden} & \textbf{User Story Id} & \textbf{Título} & \textbf{Descripción} & \textbf{Story Points} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

1 & US-01 & Propuesta de valor segmentada en Landing Page & Como visitante, quiero entender en segundos qué problema resuelve VitaLink, para decidir si me interesa conocer más. & 2 \\
\hline
2 & US-02 & Explicación del funcionamiento del sistema & Como visitante, quiero entender cómo funciona la plataforma paso a paso, para evaluar su utilidad. & 2 \\
\hline
3 & US-03 & Visualización de Planes y Suscripciones & Como visitante, quiero conocer las opciones de planes y sus costos, para elegir el que mejor se adapte a mi necesidad. & 3 \\
\hline
4 & US-04 & Sección de privacidad y seguridad de datos & Como profesional de salud, quiero ver una sección de seguridad de datos, para confiar en registrar información clínica. & 2 \\
\hline
5 & US-05 & Interfaz de captura de leads (Botones de acción) & Como visitante, quiero botones claros para iniciar mi registro o pedir información, para comenzar a usar la plataforma. & 2 \\
\hline
6 & US-06 & Mockups visuales del producto & Como visitante, quiero ver ejemplos de la interfaz real, para entender rápidamente cómo se recibe la información. & 3 \\
\hline
7 & US-14 & Generación automática de alerta desde un evento & Como Developer, quiero registrar un evento y generar una alerta asociada mediante API, asegurando respuestas HTTP 201 (Created) o HTTP 400 (Bad Request). & 8 \\
\hline
8 & US-15 & Asignación de nivel de prioridad a alertas & Como Developer, quiero asignar un nivel de prioridad a cada alerta en el backend, exponiéndolo mediante códigos HTTP 200 (OK). & 5 \\
\hline
9 & US-07 & Resumen inicial de alertas pendientes & Como médico, quiero ver un resumen inicial con pacientes pendientes, para priorizar mi atención al iniciar el día. & 5 \\
\hline
10 & US-08 & Nivel de urgencia visual en cada alerta & Como médico, quiero ver el nivel de urgencia visual, para decidir rápido qué revisar primero. & 3 \\
\hline
11 & US-09 & Acceso al detalle de paciente desde el resumen & Como médico, quiero acceder al detalle de un paciente desde el resumen, para revisar contexto sin buscar en varias pantallas. & 3 \\
\hline
12 & US-18 & Cambio de estado de alerta sin eliminar & Como Developer, quiero actualizar el estado lógico de una alerta sin eliminarla (soft-delete), confirmando la persistencia con HTTP 200 (OK). & 5 \\
\hline
13 & US-11 & Marcar alerta como en revisión o atendida & Como médico, quiero marcar una alerta como "en revisión" o "atendida", para que otros sepan el estado del caso. & 3 \\
\hline
14 & US-17 & Trazabilidad de atención de alertas & Como Developer, quiero registrar quién atendió una alerta y cuándo, validando la transacción en base de datos con un código HTTP 200 (OK). & 3 \\
\hline
15 & US-12 & Observación breve al atender una alerta & Como médico, quiero agregar una observación breve al atender una alerta, para dejar registro rápido de lo ocurrido. & 2 \\
\hline
16 & US-13 & Visibilidad de revisión previa por otro profesional & Como médico, quiero ver si un caso ya fue revisado, para evitar duplicar esfuerzos. & 2 \\
\hline
17 & US-16 & Almacenamiento del historial del paciente & Como Developer, quiero persistir el historial de un paciente, para permitir consultas posteriores mediante endpoints GET que retornen HTTP 200 (OK). & 8 \\
\hline
18 & US-10 & Historial de registros del paciente ordenado por fecha & Como médico, quiero ver el historial ordenado por fecha, para entender la evolución sin papeles dispersos. & 5 \\
\hline
19 & US-20 & Validación de datos básicos del paciente & Como Developer, quiero validar a nivel de servidor que los datos básicos estén completos, retornando HTTP 400 (Bad Request) si el payload falla. & 3 \\
\hline
20 & US-19 & Asociación de paciente con proveedor de salud & Como Developer, quiero asociar un paciente con un proveedor en la API, retornando HTTP 200 (OK) o HTTP 404 (Not Found) si no existe. & 3 \\
\hline
21 & US-21 & Panel visual del estado general & Como familiar cuidador, quiero ver un estado general y simple al abrir la app, para reducir mi ansiedad cuando estoy lejos. & 3 \\
\hline
22 & US-22 & Confirmación rápida de atención de alertas & Como familiar cuidador, quiero confirmar con un solo botón que estoy atendiendo una alerta, para avisar a mi familia rápidamente. & 2 \\
\hline
23 & US-23 & Visualización de información centralizada & Como familiar, quiero ver si otro familiar ya atendió un caso, para evitar coordinaciones telefónicas duplicadas. & 2 \\
\hline

\end{longtable}
\endgroup

