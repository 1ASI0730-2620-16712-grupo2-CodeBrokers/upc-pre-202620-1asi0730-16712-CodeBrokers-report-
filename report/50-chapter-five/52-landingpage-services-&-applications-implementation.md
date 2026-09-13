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



#### 5.2.1.5. Execution Evidence for Sprint Review



#### 5.2.1.6. Services Documentation Evidence for Sprint Review



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




