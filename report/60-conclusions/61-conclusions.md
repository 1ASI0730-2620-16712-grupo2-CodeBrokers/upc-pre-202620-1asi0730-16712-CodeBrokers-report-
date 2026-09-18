# 6. Conclusiones

## 6.1 Conclusiones y recomendaciones

Al cierre del Sprint 1, el equipo CodeBrokers ha completado la definición del producto VitaLink y ha entregado su primer incremento desplegado: una Landing Page pública que comunica la propuesta de valor a los dos segmentos objetivo. Esta sección contrasta lo alcanzado frente a los Problem Statements, los assumptions y los Hypothesis Statements formulados en el Capítulo I, y enuncia las recomendaciones que el equipo llevará a los sprints siguientes.

### Conclusiones respecto de los Problem Statements

El **Problem Statement 1** planteaba la ausencia de un sistema digital que permita el monitoreo continuo del adulto mayor y la detección oportuna de situaciones de riesgo. El proceso de needfinding confirmó que el acompañamiento actual descansa en la supervisión presencial y en comunicaciones manuales, y que ese esquema deja intervalos de tiempo sin cobertura. El problema quedó traducido en una arquitectura concreta —los bounded contexts de Monitoring y Alerting definidos en la sección 4.6— y en las historias de usuario US-07 a US-20, pero **no ha sido resuelto todavía a nivel de producto**: el incremento del Sprint 1 es una superficie de comunicación, no la capacidad de monitoreo en sí. Su resolución depende de los servicios previstos para los Sprints 2 y 3.

El **Problem Statement 2** planteaba la falta de un canal centralizado entre el adulto mayor, su red familiar y los proveedores de atención. El análisis de competidores mostró que las soluciones existentes en el mercado —cuYdo, CuidApp y Silver-Digi— atienden parcialmente la coordinación familiar, pero ninguna integra al proveedor de salud dentro del mismo flujo de atención. Esa brecha sostiene la diferenciación de VitaLink y quedó reflejada en el diseño de la doble vista (profesional y familiar) que la Landing Page ya comunica, y en los épicos EP-02 y EP-04 aún pendientes de implementación.

### Conclusiones respecto de los assumptions

De los cuatro supuestos formulados, el Sprint 1 permite pronunciarse sobre uno solo, y de forma parcial. El **Supuesto 2** —que los adultos mayores aceptarán herramientas digitales si la interfaz es simple y accesible— guio las decisiones de diseño recogidas en el Style Guideline (sección 4.1) y en la arquitectura de información (sección 4.2), en particular la jerarquía tipográfica amplia y el número reducido de acciones por pantalla. Se trata, sin embargo, de una decisión de diseño fundamentada en las entrevistas, **no de un supuesto verificado**: su contrastación requiere las entrevistas de validación previstas para el AV2.

Los **Supuestos 1, 3 y 4** —adopción por parte de los familiares, disposición de las clínicas a integrarse, y capacidad de anticipación derivada de centralizar la información— permanecen sin evidencia empírica. El equipo reconoce que ninguno de ellos puede considerarse confirmado por el hecho de que el incremento exista; asumirlo sería confundir la entrega de una funcionalidad con la validación de su efecto.

### Conclusiones respecto de los Hypothesis Statements

Las cinco hipótesis del Capítulo I comprometen resultados medibles sobre el comportamiento de los usuarios: adopción del monitoreo preventivo, reducción del tiempo de respuesta, mejora del seguimiento, reducción del tiempo de contacto con un proveedor y aumento de la frecuencia de uso. Todas ellas requieren que las funcionalidades correspondientes estén operativas y en manos de usuarios reales, condición que aún no se cumple. En consecuencia, **al cierre del Sprint 1 ninguna de las cinco hipótesis ha sido validada ni refutada**.

Lo que sí ha quedado establecido es la instrumentación necesaria para validarlas: cada hipótesis tiene asociadas historias de usuario con criterios de aceptación verificables en formato Gherkin, y el esquema de base de datos de la sección 4.8 contempla los registros —marcas de tiempo de generación y de atención de alertas, trazabilidad del responsable, historial por paciente— que permitirán medir el tiempo de respuesta y la frecuencia de uso cuando el sistema esté en operación. El equipo considera que dejar esa medición prevista desde el diseño es el resultado más relevante de esta etapa en términos de Lean UX.

### Conclusiones respecto del incremento entregado

El objetivo del Sprint 1 se cumplió en su totalidad: las seis historias del épico EP-01 y la historia técnica TS-01 alcanzaron sus criterios de aceptación, con 17 Story Points comprometidos y entregados, y la Landing Page se encuentra accesible públicamente mediante HTTPS. Los seis integrantes del equipo registraron contribuciones en el repositorio del producto, y la totalidad del trabajo se integró mediante Pull Requests revisados por pares conforme al modelo GitFlow adoptado en la sección 5.1.2.

### Recomendaciones

1. **Priorizar la instrumentación de métricas desde el Sprint 2.** Las hipótesis solo podrán contrastarse si los endpoints de Alerting registran desde el inicio los tiempos de generación y de atención. Incorporar esa medición después obligaría a descartar los datos del periodo previo.

2. **Ejecutar las entrevistas de validación sobre la Landing Page antes de avanzar en las Web Applications.** El enunciado las requiere para el AV2, pero adelantarlas permitiría corregir la propuesta de valor y la arquitectura de información mientras el costo del cambio sigue siendo bajo.

3. **Contrastar tempranamente el Supuesto 3.** La integración de clínicas y hospitales es el supuesto con mayor impacto sobre el modelo de negocio y el que más tiempo requiere para verificarse. El equipo recomienda iniciar contactos exploratorios con al menos un proveedor de salud durante el Sprint 2.

4. **Mantener la trazabilidad entre el Capítulo III y el Capítulo V.** Durante este sprint se detectó que el Sprint Backlog había quedado referido a una versión anterior del Product Backlog, lo que produjo inconsistencias en identificadores y estimaciones. Se recomienda que toda modificación del Capítulo III se propague en el mismo Pull Request a las secciones del Capítulo V que lo referencian.

5. **Verificar la compilación del informe en cada Pull Request.** Se identificó que el documento llevaba varios días sin poder generarse en PDF por un error de sintaxis en la inclusión de imágenes, sin que el equipo lo advirtiera. Incorporar la generación del PDF como paso de verificación previo a cada integración evitaría que un error de formato pase inadvertido hasta la fecha de entrega.

6. **Consolidar `develop` en `main` antes de cada entrega.** Los analíticos de colaboración de GitHub se calculan sobre la rama por defecto; mantenerla desactualizada invisibiliza el aporte de parte del equipo y contradice la política de versionado semántico declarada en la sección 5.1.2.

\newpage
