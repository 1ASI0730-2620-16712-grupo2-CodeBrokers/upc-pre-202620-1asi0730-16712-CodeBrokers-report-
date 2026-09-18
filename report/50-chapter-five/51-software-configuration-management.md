# 5. Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management


En esta sección se establecen las decisiones de gestión de configuración que rigen el desarrollo de VitaLink: el entorno de trabajo de cada integrante, la política de control de versiones sobre los repositorios del equipo, las convenciones de codificación por tipo de artefacto y el procedimiento de despliegue. El objetivo es que cualquier integrante pueda incorporarse al proyecto, reproducir el entorno y contribuir sin ambigüedades sobre cómo nombrar, escribir y publicar el código.


### 5.1.1. Software Development Environment Configuration


En esta sección, el equipo CodeBrokers especifica los productos de software y herramientas colaborativas adoptadas para gestionar el ciclo de vida de VitaLink. Se detallan las herramientas utilizadas en las distintas fases del proyecto, desde la concepción y diseño hasta el desarrollo, despliegue y documentación, asegurando que todos los miembros del equipo cuenten con el mismo entorno de trabajo configurado.

\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.4}

\begin{longtable}{|p{0.18\textwidth}|p{0.15\textwidth}|p{0.42\textwidth}|p{0.20\textwidth}|}
\hline
\textbf{Categoría} & \textbf{Producto} & \textbf{Propósito en el proyecto} & \textbf{Ruta de referencia / Descarga} \\
\hline
\endfirsthead

\hline
\textbf{Categoría} & \textbf{Producto} & \textbf{Propósito en el proyecto} & \textbf{Ruta de referencia / Descarga} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

\multirow{2}{=}{\textbf{Project \& Requirements Management}} 
& Jira & Gestión ágil del proyecto, administración del Product Backlog, Sprint Backlogs y seguimiento de incidencias. & \href{https://www.atlassian.com/software/jira}{SaaS: Atlassian Jira} \\
\cline{2-4}
& Discord & Medio de comunicación oficial del equipo para las reuniones de Sprint Planning, Daily Scrums y coordinación remota. & \href{https://discord.com/download}{Descarga: Discord} \\
\hline

\multirow{2}{=}{\textbf{Product UX/UI Design}} 
& Figma & Creación de wireframes, mockups, prototipos interactivos de alta fidelidad y diseño del Lean UX Canvas. & \href{https://www.figma.com/}{SaaS: Figma} \\
\cline{2-4}
& UXPressia & Elaboración de artefactos de Needfinding (User Personas, User Journey Maps y Empathy Maps). & \href{https://uxpressia.com/}{SaaS: UXPressia} \\
\hline

\multirow{5}{=}{\textbf{Software Development}} 
& Visual Studio Code & Editor de código ligero y principal para el desarrollo Frontend (HTML5, CSS3, JavaScript, Vue.js) y redacción en Markdown. & \href{https://code.visualstudio.com/}{Descarga: VS Code} \\
\cline{2-4}
& Visual Studio 2022 & IDE principal para el desarrollo de la lógica Backend y REST API utilizando ASP.NET Core y C\#. & \href{https://visualstudio.microsoft.com/}{Descarga: Visual Studio} \\
\cline{2-4}
& Git & Sistema de control de versiones distribuido para la gestión local del código fuente mediante GitFlow. & \href{https://git-scm.com/downloads}{Descarga: Git} \\
\cline{2-4}
& GitHub & Plataforma de alojamiento (SaaS) para el repositorio centralizado, code reviews y gestión de Pull Requests. & \href{https://github.com/}{SaaS: GitHub} \\
\cline{2-4}
& PostgreSQL & Motor de base de datos relacional para el almacenamiento del modelo de dominio del Backend. & \href{https://www.postgresql.org/download/}{Descarga: PostgreSQL} \\
\hline

\textbf{Software Deployment} 
& GitHub Pages & Servicio de hosting de archivos estáticos utilizado para el despliegue continuo y alojamiento de la Landing Page. & \href{https://pages.github.com/}{SaaS: GitHub Pages} \\
\hline

\multirow{3}{=}{\textbf{Software Documentation}} 
& Pandoc \& LaTeX & Motor de compilación utilizado para transformar el código Markdown y LaTeX del informe hacia su versión final en PDF. & \href{https://pandoc.org/installing.html}{Descarga: Pandoc} \\
\cline{2-4}
& Structurizr (DSL) & Herramienta Diagram-as-Code utilizada para elaborar el C4 Model de la arquitectura de software. & \href{https://structurizr.com/}{SaaS: Structurizr} \\
\cline{2-4}
& PlantUML & Lenguaje de modelado utilizado para diseñar los diagramas de clases orientados a objetos. & \href{https://plantuml.com/}{SaaS / Local: PlantUML} \\
\hline

\end{longtable}
\endgroup


### 5.1.2. Source Code Management


El equipo CodeBrokers gestiona el código fuente y la documentación del proyecto en **GitHub**, bajo la organización `CodeBrokers-web-app-1ASI0730-2620-16712`. El control de versiones se realiza con **Git**, aplicando el modelo de ramificación **GitFlow** y la especificación **Conventional Commits** para los mensajes.


#### Repositorios del proyecto


\begingroup
\centering
\small
\setlength{\tabcolsep}{6pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.32\textwidth}|p{0.48\textwidth}|p{0.15\textwidth}|}
\hline
\textbf{Repositorio} & \textbf{Propósito} & \textbf{URL} \\
\hline
\endfirsthead

\hline
\textbf{Repositorio} & \textbf{Propósito} & \textbf{URL} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

\texttt{upc-pre-202620-1asi0730-16712-CodeBrokers-report-} & Informe del proyecto en formato Markdown, diagramas como código (Structurizr DSL, PlantUML) y script de compilación a PDF mediante Pandoc. & \href{https://github.com/CodeBrokers-web-app-1ASI0730-2620-16712/upc-pre-202620-1asi0730-16712-CodeBrokers-report-}{Ver repositorio} \\
\hline
\texttt{vitalink-landing-page} & Landing Page de VitaLink implementada en HTML5, CSS3 y JavaScript. & \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page}{Ver repositorio} \\
\hline
\texttt{vitalink-frontend} & Aplicación web de VitaLink desarrollada en Vue.js con PrimeVue. & \textit{(Pendiente — se crea a partir del Sprint 2)} \\
\hline
\texttt{vitalink-backend} & Servicios RESTful de VitaLink desarrollados en ASP.NET Core con Entity Framework Core. & \textit{(Pendiente — se crea a partir del Sprint 2)} \\
\end{longtable}
\endgroup


Table: Repositorios del proyecto VitaLink

#### Modelo de ramificación: GitFlow

El equipo adopta GitFlow, propuesto por Vincent Driessen, por ajustarse a un desarrollo iterativo por sprints con entregables parciales evaluados. Las ramas se organizan de la siguiente manera:


\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.4}

\begin{longtable}{|p{0.22\textwidth}|p{0.10\textwidth}|p{0.08\textwidth}|p{0.14\textwidth}|p{0.38\textwidth}|}
\hline
\textbf{Rama} & \textbf{Tipo} & \textbf{Origen} & \textbf{Destino del merge} & \textbf{Descripción} \\
\hline
\endfirsthead

\hline
\textbf{Rama} & \textbf{Tipo} & \textbf{Origen} & \textbf{Destino del merge} & \textbf{Descripción} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

\texttt{main} & Permanente & --- & --- & Contiene únicamente versiones estables y entregadas. Cada entrega evaluada (AV1, AV2, TP, TB) corresponde a un estado de esta rama. No se desarrolla directamente sobre ella. \\
\hline
\texttt{develop} & Permanente & \texttt{main} & \texttt{main} & Rama de integración. Concentra el trabajo terminado de todas las ramas de característica y refleja el estado actual del proyecto en curso. \\
\hline
\texttt{feature/<n>-<descripción>} & Temporal & \texttt{develop} & \texttt{develop} & Una rama por cada sección del informe o funcionalidad del producto. Se elimina tras su integración. Ejemplos reales del proyecto: \texttt{feature/48-database-design}, \texttt{feature/471-class-diagrams}, \texttt{feature/45-web-applications-prototyping}. \\
\hline
\texttt{release/<versión>} & Temporal & \texttt{develop} & \texttt{main} y \texttt{develop} & Rama de estabilización previa a una entrega. Solo admite correcciones, nunca nuevas funcionalidades. \\
\hline
\texttt{hotfix/<descripción>} & Temporal & \texttt{main} & \texttt{main} y \texttt{develop} & Corrección urgente sobre una versión ya entregada. \\
\end{longtable}
\endgroup


Table: Modelo de ramificación GitFlow aplicado en VitaLink

La convención `feature/<n>-<descripción>` emplea como `<n>` el número de la sección del informe que la rama desarrolla, de modo que la trazabilidad entre el índice del documento y el historial del repositorio sea directa y verificable.

#### Versionado semántico

Las entregas se etiquetan siguiendo **Semantic Versioning 2.0.0**, con el formato `MAJOR.MINOR.PATCH`:

- **MAJOR:** incrementa ante cambios incompatibles en la arquitectura o en los contratos de los servicios.
- **MINOR:** incrementa al incorporar nuevas funcionalidades manteniendo la compatibilidad.
- **PATCH:** incrementa ante correcciones que no alteran la funcionalidad existente.

La entrega correspondiente al Sprint 1 se etiqueta como `v1.0.0`.

#### Convención de mensajes de commit

El equipo aplica **Conventional Commits 1.0.0**, con la estructura `<tipo>(<alcance>): <descripción>`. La descripción se redacta en modo imperativo, en minúsculas y sin punto final. El `<alcance>` corresponde al número de sección del informe o al módulo afectado.


\begingroup
\centering
\small
\setlength{\tabcolsep}{6pt}
\renewcommand{\arraystretch}{1.4}

\begin{longtable}{|p{0.15\textwidth}|p{0.75\textwidth}|}
\hline
\textbf{Tipo} & \textbf{Uso} \\
\hline
\endfirsthead

\hline
\textbf{Tipo} & \textbf{Uso} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

\texttt{feat} & Incorporación de una nueva sección del informe o de una funcionalidad del producto. \\
\hline
\texttt{fix} & Corrección de un error de contenido, de formato o de código. \\
\hline
\texttt{docs} & Cambios exclusivamente documentales. \\
\hline
\texttt{style} & Cambios de formato que no alteran el significado del contenido. \\
\hline
\texttt{refactor} & Reestructuración que no modifica el comportamiento ni el contenido sustantivo. \\
\hline
\texttt{chore} & Tareas de mantenimiento del repositorio y de su estructura. \\
\hline
\texttt{build} & Cambios en la configuración de compilación del informe o del producto. \\
\end{longtable}
\endgroup


Table: Tipos de commit admitidos


Ejemplos tomados del historial real del repositorio:

```text
feat(4.8): diseno de base de datos normalizado en PostgreSQL
fix(45): limitar el alcance del prototipo a Desktop Web Browser
refactor(31): convert user stories table from latex to markdown
build(config): set up pandoc configuration files and pdf engine
```

#### Política de integración

Ninguna rama de característica se integra directamente. Todo cambio se incorpora a `develop` mediante un **Pull Request** que debe cumplir tres condiciones: describir el alcance del cambio y la sección que atiende, no presentar conflictos con `develop`, y contar con la aprobación de al menos un integrante distinto del autor. Una vez aprobado el Pull Request, la rama de característica se elimina del remoto.

### 5.1.3. Source Code Style Guide & Conventions

El equipo adopta guías de estilo reconocidas por la industria para cada tecnología del stack, con el fin de mantener la legibilidad del código y reducir la fricción en las revisiones de Pull Request. El idioma de todo identificador, comentario y nombre de archivo del código fuente es el **inglés**; el contenido del informe se redacta en **español**.

#### Convenciones generales


\begingroup
\centering
\small
\setlength{\tabcolsep}{6pt}
\renewcommand{\arraystretch}{1.4}

\begin{longtable}{|p{0.30\textwidth}|p{0.60\textwidth}|}
\hline
\textbf{Aspecto} & \textbf{Convención} \\
\hline
\endfirsthead

\hline
\textbf{Aspecto} & \textbf{Convención} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

Codificación de archivos & UTF-8 sin BOM \\
\hline
Fin de línea & LF (\texttt{\textbackslash{}n}), normalizado mediante \texttt{.gitattributes} \\
\hline
Indentación & 2 espacios en HTML, CSS, JavaScript y Vue; 4 espacios en C\# \\
\hline
Longitud máxima de línea & 100 caracteres \\
\hline
Nombres de archivo & \texttt{kebab-case}, salvo en C\#, donde se emplea \texttt{PascalCase} \\
\hline
Idioma de los identificadores & Inglés \\
\end{longtable}
\endgroup

Table: Convenciones generales de codificación


#### HTML5 y CSS3

Se sigue la **Google HTML/CSS Style Guide**. En HTML se emplean etiquetas semánticas (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`) en lugar de `<div>` genéricos, todos los atributos se delimitan con comillas dobles y toda imagen declara su atributo `alt`. En CSS se adopta la metodología **BEM** (`bloque__elemento--modificador`) para nombrar clases, las propiedades se ordenan por grupo (posicionamiento, modelo de caja, tipografía, y por último aspecto visual), y la paleta y la tipografía se declaran como variables CSS en `:root` a partir del Style Guideline de la sección 4.1.

```css
:root {
  --color-primary: #2E7D9A;
  --color-alert-high: #D64545;
  --font-family-base: 'Inter', sans-serif;
}

.alert-card__badge--high {
  background-color: var(--color-alert-high);
}
```

#### JavaScript y Vue.js

Se sigue la **Airbnb JavaScript Style Guide** junto con la **Vue.js Style Guide** en sus niveles de prioridad A y B. Las variables y funciones se nombran en `camelCase` y las clases en `PascalCase`; se declara con `const` por defecto y con `let` únicamente cuando la reasignación es necesaria, evitando `var`. Los componentes de Vue se nombran con al menos dos palabras en `PascalCase` (`AlertSummaryCard.vue`, nunca `Alert.vue`), emplean la **Composition API** con `<script setup>`, y declaran sus `props` con tipo y valor por defecto explícitos.

#### C# y ASP.NET Core

Se siguen las **Microsoft C# Coding Conventions**. Los tipos, métodos y propiedades públicas se nombran en `PascalCase`; los parámetros y variables locales, en `camelCase`; y los campos privados, con el prefijo `_` seguido de `camelCase`. Las interfaces se prefijan con `I` (`IAlertRepository`). Todo método asíncrono devuelve `Task` o `Task<T>` y termina su nombre con el sufijo `Async`. La organización de los espacios de nombres reproduce la estructura de bounded contexts definida en la sección 4.6, bajo el patrón `VitaLink.<BoundedContext>.<Capa>`.

#### PostgreSQL

Los identificadores de base de datos se escriben en `snake_case` y en minúsculas. Las tablas se nombran en plural (`older_adults`, `care_records`) y las claves foráneas siguen el patrón `<tabla_singular>_id`. Cada restricción se nombra explícitamente con el prefijo correspondiente a su tipo: `pk_` para clave primaria, `fk_` para clave foránea, `uq_` para unicidad, `ck_` para verificación e `ix_` para índice. Cada bounded context dispone de su propio esquema, conforme al diseño de la sección 4.8.

#### Markdown y diagramas como código

El informe se redacta en Markdown con un archivo por sección, nombrado con el prefijo numérico de la sección correspondiente. Los encabezados emplean la sintaxis ATN (`##`), las tablas se cierran con una línea `Table: <descripción>` para su numeración automática en Pandoc, y las imágenes se referencian mediante rutas relativas a `assets/` en formato PNG (no se emplea SVG, por incompatibilidad con el motor LuaLaTeX). Los diagramas se versionan como código: el modelo C4 en **Structurizr DSL** (`workspace.dsl`) y los diagramas de clases en **PlantUML** (`.puml`), de modo que todo cambio en un diagrama quede registrado en el historial del repositorio.

### 5.1.4. Software Deployment Configuration


Para el despliegue de la Landing Page de VitaLink, el equipo CodeBrokers utilizó **GitHub Pages**
como plataforma de publicación, aprovechando su integración directa con el repositorio de
GitHub. Esta decisión permite que cada actualización consolidada en la rama `main` se refleje
de forma automática en el entorno público, sin necesidad de configuración adicional de
infraestructura.

El proceso de configuración seguido fue el siguiente: en primer lugar, se accedió a la
configuración del repositorio de la Landing Page desde GitHub. Posteriormente, en la sección
**Pages**, se seleccionó la rama `main` como fuente de despliegue y se indicó la carpeta raíz
(`/root`) como directorio de publicación. GitHub Pages procesó automáticamente los archivos
estáticos (`index.html`, `styles.css`, `script.js`) y habilitó HTTPS por defecto mediante
sus certificados propios.


El entorno de producción de la Landing Page de VitaLink está accesible públicamente en la
siguiente URL: https://1asi0730-2620-16712-grupo2-codebrokers.github.io/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page/

