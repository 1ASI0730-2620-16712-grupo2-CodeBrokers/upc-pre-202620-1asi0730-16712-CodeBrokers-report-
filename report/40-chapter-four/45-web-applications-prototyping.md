## 4.5. Web Applications Prototyping

El prototipo navegable de VitaLink se elaboró en Figma a partir de los mock-ups de la sección 4.4.3, incorporando la simulación de interacción y navegación que recorre los paths definidos en los User Flow Diagrams de la sección 4.4.4. El objetivo del prototipo no es mostrar pantallas aisladas, sino demostrar que los recorridos completos del médico y del familiar pueden ejecutarse de principio a fin sin callejones sin salida.

### Criterios de interacción

Las decisiones de interacción responden directamente a la arquitectura de información definida en la sección 4.2, y en particular al sistema de navegación del punto 4.2.5:

* **Estructura de navegación unificada con contenido diferenciado por perfil.** Tal como establece el 4.2.5, el prototipo mantiene una misma estructura de navegación para ambos perfiles y adapta el contenido y las acciones principales según el tipo de usuario. El médico entra al tablero de alertas pendientes; el familiar entra al panel de seguimiento del adulto mayor. La ubicación de los elementos de navegación no cambia entre perfiles, de modo que el aprendizaje de la interfaz es transferible.
* **Prioridad visual determinada por la urgencia.** La jerarquía visual descrita en el 4.2.1 se traduce en el prototipo en el orden de lectura del tablero: el resumen de alertas pendientes ocupa la posición dominante al cargar la vista del médico, y cada alerta expone su nivel de gravedad mediante color y etiqueta antes que cualquier otro dato. Esto materializa las historias US-08 y US-09.
* **Navegación en profundidad sin pérdida de contexto.** Desde el resumen, cada alerta conduce al detalle del paciente conservando un camino de retorno explícito, según el criterio de aceptación de la US-10. El prototipo simula esta ida y vuelta para evitar que el médico deba reconstruir el contexto al regresar al listado.
* **Confirmación explícita en las acciones que alteran el estado del caso.** El cambio de estado de una alerta y el registro de la observación se presentan como una misma interacción encadenada, en coherencia con la organización secuencial descrita en el 4.2.1 y con el carácter opcional de la observación establecido en la US-13.
* **Adaptación a dos anchos de pantalla.** El prototipo cubre Desktop y Mobile Web Browser. En mobile la navegación colapsa según el criterio ya definido para la landing page en el 4.2.5, y el tablero de alertas pasa de disposición en columnas a una lista vertical priorizada por gravedad.

### Prototipo de la Web Application

El siguiente screenshot corresponde al video de demostración, en el que se recorren los principales flujos de interacción cubiertos por el prototipo: el ingreso del profesional de salud, la revisión del tablero de alertas, el acceso al detalle del paciente y el registro de la atención.

\includegraphics[width=\linewidth]{assets/45-prototyping-screenshot.png}

**URL:** \href{https://upcedupe-my.sharepoint.com/:v:/g/personal/u202312348_upc_edu_pe/IQCPQT4LsLiRR4JCkfWa232UAVSPK-NeCDNGllI7seUJNVs?e=dTaqom&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D}{Link del vídeo}
