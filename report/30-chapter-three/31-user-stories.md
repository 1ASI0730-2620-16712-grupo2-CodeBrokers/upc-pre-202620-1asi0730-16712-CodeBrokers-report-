# 3. Capítulo III: Requirements Specification

## 3.1. User Stories

\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.08\textwidth}|p{0.18\textwidth}|p{0.28\textwidth}|p{0.36\textwidth}|p{0.08\textwidth}|}
\hline
\textbf{Epic / Story ID} & \textbf{Título} & \textbf{Descripción} & \textbf{Criterios de Aceptación} & \textbf{Relacionado con} \\
\hline
\endfirsthead

\hline
\textbf{Epic / Story ID} & \textbf{Título} & \textbf{Descripción} & \textbf{Criterios de Aceptación} & \textbf{Relacionado con} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

% ============================================================
% EPICA 1
% ============================================================
\textbf{EP-01} & \textbf{Landing Page} & Sitio web estático con vistas segmentadas para captar pacientes/familiares y profesionales de salud. & - & - \\
\hline
US-01 & Propuesta de valor segmentada en Landing Page & Como visitante, quiero entender en segundos qué problema resuelve VitaLink, para decidir si me interesa conocer más. & \textbf{Dado} que el visitante ingresa a la Landing Page, \textbf{Cuando} la página carga, \textbf{Entonces} el médico debe visualizar el titular "Optimice el seguimiento preventivo", y el familiar el titular "La tranquilidad de saber que tus padres están bien". & EP-01 \\
\hline
US-02 & Explicación del funcionamiento del sistema & Como visitante, quiero entender cómo funciona la plataforma paso a paso, para evaluar su utilidad. & \textbf{Dado} que el usuario explora la página, \textbf{Cuando} llega a la sección de funcionamiento, \textbf{Entonces} el médico debe ver el "Flujo clínico integrado", y el familiar los "Cuatro pilares fundamentales" del servicio. & EP-01 \\
\hline
US-03 & Visualización de Planes y Suscripciones & Como visitante, quiero conocer las opciones de planes y sus costos, para elegir el que mejor se adapte a mi necesidad. & \textbf{Dado} que el visitante navega a la sección de tarifas, \textbf{Cuando} revisa los planes, \textbf{Entonces} el sistema debe mostrar 3 opciones de suscripción específicas para su perfil (Básica/Pro/Institucional o Básico/Familiar/Plus) con sus respectivos precios. & EP-01 \\
\hline
US-04 & Sección de privacidad y seguridad de datos & Como profesional de salud, quiero ver una sección de seguridad de datos, para confiar en registrar información clínica. & \textbf{Dado} que un profesional de salud explora la landing page, \textbf{Cuando} navega hacia la sección respectiva, \textbf{Entonces} debe visualizar los protocolos de "Seguridad de grado médico", incluyendo cifrado E2E, HIPAA \& GDPR y control de acceso. & EP-01 \\
\hline
US-05 & Interfaz de captura de leads (Botones de acción) & Como visitante, quiero botones claros para iniciar mi registro o pedir información, para comenzar a usar la plataforma. & \textbf{Dado} que el visitante decide adoptar la plataforma, \textbf{Cuando} interactúa con los llamados a la acción, \textbf{Entonces} el familiar debe ser dirigido al registro mediante "Crear cuenta", y el médico al contacto mediante "Unirme como proveedor" o "Solicitar información técnica". & EP-01 \\
\hline
US-06 & Mockups visuales del producto & Como visitante, quiero ver ejemplos de la interfaz real, para entender rápidamente cómo se recibe la información. & \textbf{Dado} que un visitante revisa las funcionalidades, \textbf{Cuando} observa las imágenes ilustrativas, \textbf{Entonces} el médico debe ver un dashboard clínico en monitor, y el familiar una notificación de alerta en su smartphone. & EP-01 \\
\hline

% ============================================================
% EPICA 2
% ============================================================
\textbf{EP-02} & \textbf{Frontend (Vista Médico)} & Interfaz de usuario para que los profesionales de salud gestionen pacientes y alertas. & - & - \\
\hline
US-07 & Resumen inicial de alertas pendientes & Como médico, quiero ver un resumen inicial con pacientes pendientes, para priorizar mi atención al iniciar el día. & \textbf{Dado} que el médico inicia su jornada en la aplicación, \textbf{Cuando} accede a la pantalla principal, \textbf{Entonces} el sistema debe mostrar el número total de alertas pendientes y permitir la navegación hacia la lista completa. & EP-02 \\
\hline
US-08 & Nivel de urgencia visual en cada alerta & Como médico, quiero ver el nivel de urgencia visual, para decidir rápido qué revisar primero. & \textbf{Dado} que el médico revisa la lista de alertas, \textbf{Cuando} el sistema carga los datos, \textbf{Entonces} cada alerta debe mostrar una etiqueta que clasifique visualmente su urgencia (alto, medio o bajo) permitiendo ordenarlas. & EP-02 \\
\hline
US-09 & Acceso al detalle de paciente desde el resumen & Como médico, quiero acceder al detalle de un paciente desde el resumen, para revisar contexto sin buscar en varias pantallas. & \textbf{Dado} que el médico necesita más información de un caso, \textbf{Cuando} selecciona una alerta específica, \textbf{Entonces} el sistema debe navegar al expediente detallado del paciente manteniendo una opción de regreso al resumen. & EP-02 \\
\hline
US-10 & Historial de registros del paciente ordenado & Como médico, quiero ver el historial ordenado por fecha, para entender la evolución sin papeles dispersos. & \textbf{Dado} que el médico visualiza el detalle de un paciente, \textbf{Cuando} accede a la sección de historial, \textbf{Entonces} debe visualizar los eventos organizados cronológicamente, o un mensaje informativo si no existen registros previos. & EP-02 \\
\hline
US-11 & Marcar alerta como en revisión o atendida & Como médico, quiero marcar una alerta como "en revisión" o "atendida", para que otros sepan el estado del caso. & \textbf{Dado} que el médico gestiona una situación de riesgo, \textbf{Cuando} ejecuta la acción de cambiar el estado de la alerta, \textbf{Entonces} el sistema debe reflejar la actualización inmediatamente en el listado general de alertas. & EP-02 \\
\hline
US-12 & Observación breve al atender una alerta & Como médico, quiero agregar una observación breve al atender una alerta, para dejar registro rápido de lo ocurrido. & \textbf{Dado} que el médico actualiza el estado de un incidente, \textbf{Cuando} finaliza la acción, \textbf{Entonces} el sistema debe habilitar un campo opcional para registrar observaciones asociadas a la fecha y nombre del médico. & EP-02 \\
\hline
US-13 & Visibilidad de revisión previa por otro profesional & Como médico, quiero ver si un caso ya fue revisado, para evitar duplicar esfuerzos. & \textbf{Dado} que el médico analiza la lista de pendientes, \textbf{Cuando} visualiza las alertas, \textbf{Entonces} el sistema debe distinguir claramente aquellas que ya poseen revisión previa e indicar qué profesional interactuó con ellas. & EP-02 \\
\hline

% ============================================================
% EPICA 3
% ============================================================
\textbf{EP-03} & \textbf{Backend (API RESTful)} & Lógica de servidor, base de datos y procesamiento de reglas de negocio. & - & - \\
\hline
US-14 & Generación automática de alerta desde un evento & Como Developer, quiero registrar un evento y generar una alerta asociada mediante API, asegurando respuestas HTTP adecuadas para confirmar el flujo de atención. & \textbf{Dado} que el servidor recibe una solicitud de registro de evento, \textbf{Cuando} los datos cumplen los parámetros configurados, \textbf{Entonces} la API debe generar la alerta y retornar el código \textbf{HTTP 201 (Created)}, o retornar un error \textbf{HTTP 400 (Bad Request)} si los datos son inválidos. & EP-03 \\
\hline
US-15 & Asignación de nivel de prioridad a alertas & Como Developer, quiero asignar un nivel de prioridad a cada alerta en el backend, exponiéndolo a través del endpoint mediante códigos HTTP de éxito. & \textbf{Dado} que el sistema procesa una nueva alerta, \textbf{Cuando} evalúa el payload, \textbf{Entonces} debe almacenar la prioridad y retornar la entidad configurada con un código \textbf{HTTP 201 (Created)} o \textbf{HTTP 200 (OK)}. & EP-03 \\
\hline
US-16 & Almacenamiento del historial del paciente & Como Developer, quiero persistir el historial de un paciente, para permitir consultas posteriores mediante endpoints GET. & \textbf{Dado} que el backend procesa registros del paciente, \textbf{Cuando} la solicitud es procesada, \textbf{Entonces} debe persistir los datos retornando \textbf{HTTP 201 (Created)}, y permitir consultas filtradas que devuelvan código \textbf{HTTP 200 (OK)}. & EP-03 \\
\hline
US-17 & Trazabilidad de atención de alertas & Como Developer, quiero registrar quién atendió una alerta y cuándo, validando la transacción en el servidor. & \textbf{Dado} que se ejecuta un endpoint de cambio de estado, \textbf{Cuando} la transacción es exitosa, \textbf{Entonces} la base de datos debe registrar el timestamp y el ID del responsable, respondiendo con un código \textbf{HTTP 200 (OK)}. & EP-03 \\
\hline
US-18 & Cambio de estado de alerta sin eliminar & Como Developer, quiero actualizar el estado lógico de una alerta sin eliminarla físicamente (soft-delete), conservando el historial. & \textbf{Dado} que el sistema recibe una solicitud para cerrar o actualizar una alerta, \textbf{Cuando} procesa el registro, \textbf{Entonces} debe aplicar un soft-delete, manteniendo la persistencia y confirmando la acción con un código \textbf{HTTP 200 (OK)}. & EP-03 \\
\hline
US-19 & Asociación de paciente con proveedor de salud & Como Developer, quiero asociar un paciente con un proveedor en la API, validando la existencia de los registros. & \textbf{Dado} que se envía el ID del proveedor, \textbf{Cuando} el backend procesa la vinculación, \textbf{Entonces} debe registrarla retornando \textbf{HTTP 200 (OK)}, o arrojar un código de error \textbf{HTTP 404 (Not Found)} si el proveedor no existe. & EP-03 \\
\hline
US-20 & Validación de datos básicos del paciente & Como Developer, quiero validar a nivel de servidor que los datos básicos estén completos antes de insertarlos en la base de datos. & \textbf{Dado} que se solicita la activación del seguimiento, \textbf{Cuando} el payload carece de campos obligatorios, \textbf{Entonces} la API debe abortar la operación y retornar un código \textbf{HTTP 400 (Bad Request)} detallando qué atributos faltan en el response body. & EP-03 \\
\hline

% ============================================================
% EPICA 4
% ============================================================
\textbf{EP-04} & \textbf{Frontend (Vista Familiar / Cuidador)} & Interfaz para que la red de apoyo supervise el estado del adulto mayor. & - & - \\
\hline
US-21 & Panel visual del estado general & Como familiar cuidador, quiero ver un estado general y simple al abrir la app, para reducir mi ansiedad cuando estoy lejos. & \textbf{Dado} que el familiar inicia sesión en la aplicación móvil, \textbf{Cuando} carga la pantalla de inicio, \textbf{Entonces} debe visualizar un indicador claro en tiempo real sobre el bienestar del adulto mayor sin necesidad de navegar más profundo. & EP-04 \\
\hline
US-22 & Confirmación rápida de atención de alertas & Como familiar cuidador, quiero confirmar con un solo botón que estoy atendiendo una alerta, para avisar a mi familia rápidamente. & \textbf{Dado} que el sistema reporta una situación irregular, \textbf{Cuando} el familiar interactúa con la notificación, \textbf{Entonces} debe disponer de un botón visible que marque la alerta como "atendida por familiar" informando a la red de cuidadores. & EP-04 \\
\hline
US-23 & Visualización de información centralizada & Como familiar, quiero ver si otro familiar ya atendió un caso, para evitar coordinaciones telefónicas duplicadas. & \textbf{Dado} que ocurre un incidente, \textbf{Cuando} el familiar revisa el historial en la aplicación, \textbf{Entonces} el sistema debe indicar si algún miembro de la red de cuidadores o médico ya se hizo cargo de la situación. & EP-04 \\
\hline

\end{longtable}
\endgroup

