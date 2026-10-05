# 5. Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

En esta sección se establecen las decisiones de gestión de configuración que rigen el desarrollo de VitaLink: el entorno de trabajo de cada integrante, la política de control de versiones sobre los repositorios del equipo, las convenciones de codificación por tipo de artefacto y el procedimiento de despliegue. El objetivo es que cualquier integrante pueda incorporarse al proyecto, reproducir el entorno y contribuir sin ambigüedades sobre cómo configurar, nombrar, escribir, versionar y publicar el código.

### 5.1.1. Software Development Environment Configuration

En esta sección, el equipo CodeBrokers especifica los productos de software y herramientas colaborativas adoptadas para gestionar el ciclo de vida de VitaLink. Se detallan las herramientas utilizadas en las distintas fases del proyecto, desde la concepción y diseño hasta el desarrollo, despliegue y documentación.

Con el objetivo de facilitar la reproducibilidad del entorno, se documentan las herramientas actualmente utilizadas por el equipo y aquellas previstas para etapas posteriores del proyecto. Cuando una tecnología aún no corresponde al incremento actual, se identifica explícitamente como de uso futuro.

\begingroup
\centering
\small
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.4}

\begin{longtable}{|p{0.17\textwidth}|p{0.14\textwidth}|p{0.13\textwidth}|p{0.35\textwidth}|p{0.16\textwidth}|}
\hline
\textbf{Categoría} & \textbf{Producto} & \textbf{Versión / Estado} & \textbf{Propósito en el proyecto} & \textbf{Ruta de referencia / Descarga} \\
\hline
\endfirsthead

\hline
\textbf{Categoría} & \textbf{Producto} & \textbf{Versión / Estado} & \textbf{Propósito en el proyecto} & \textbf{Ruta de referencia / Descarga} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

\multirow{2}{=}{\textbf{Project \& Requirements Management}}
& Jira & SaaS & Gestión ágil del proyecto, administración del Product Backlog, Sprint Backlogs y seguimiento de incidencias. & \href{https://www.atlassian.com/software/jira}{SaaS: Atlassian Jira} \\
\cline{2-5}

& Discord & Desktop / Web & Medio de comunicación utilizado por el equipo para reuniones de Sprint Planning, Daily Scrums y coordinación remota. & \href{https://discord.com/download}{Descarga: Discord} \\
\hline

\multirow{2}{=}{\textbf{Product UX/UI Design}}
& Figma & SaaS & Creación de wireframes, mockups, prototipos interactivos de alta fidelidad y diseño de artefactos UX/UI. & \href{https://www.figma.com/}{SaaS: Figma} \\
\cline{2-5}

& UXPressia & SaaS & Elaboración de artefactos de Needfinding, incluyendo User Personas, User Journey Maps y Empathy Maps. & \href{https://uxpressia.com/}{SaaS: UXPressia} \\
\hline

\multirow{7}{=}{\textbf{Software Development}}
& Visual Studio Code & \textit{Pendiente de verificar versión} & Editor principal para el desarrollo de la Landing Page, la aplicación Frontend y la edición de archivos Markdown. & \href{https://code.visualstudio.com/}{Descarga: VS Code} \\
\cline{2-5}

& Node.js & \texttt{v24.15.0} & Entorno de ejecución de JavaScript utilizado durante el desarrollo local de la aplicación Frontend basada en Vue.js. & \href{https://nodejs.org/}{Descarga: Node.js} \\
\cline{2-5}

& npm & \texttt{12.2.0} & Gestor de paquetes utilizado para administrar las dependencias y scripts de la aplicación Frontend. & \href{https://www.npmjs.com/}{Package Manager: npm} \\
\cline{2-5}

& Visual Studio 2022 & \textit{Uso futuro} & IDE previsto para el desarrollo de la REST API con ASP.NET Core y C\#. El Backend todavía no corresponde al incremento actual del proyecto. & \href{https://visualstudio.microsoft.com/}{Descarga: Visual Studio} \\
\cline{2-5}

& Git & \texttt{2.51.2.windows.1} & Sistema de control de versiones distribuido utilizado para gestionar localmente el código fuente y la documentación. & \href{https://git-scm.com/downloads}{Descarga: Git} \\
\cline{2-5}

& GitHub & SaaS & Plataforma de alojamiento de repositorios, administración de ramas, revisión de código y gestión de Pull Requests. & \href{https://github.com/}{SaaS: GitHub} \\
\cline{2-5}

& PostgreSQL & \textit{Uso futuro} & Motor de base de datos previsto para la persistencia de la REST API. Su configuración será incorporada cuando corresponda implementar el Backend. & \href{https://www.postgresql.org/download/}{Descarga: PostgreSQL} \\
\hline

\multirow{2}{=}{\textbf{Software Deployment}}
& GitHub Pages & SaaS & Servicio utilizado para publicar la Landing Page de VitaLink directamente desde su repositorio en GitHub. & \href{https://pages.github.com/}{SaaS: GitHub Pages} \\
\cline{2-5}

& Vercel & SaaS & Plataforma utilizada para el despliegue público de la aplicación Frontend de VitaLink. & \href{https://vercel.com/}{SaaS: Vercel} \\
\hline

\multirow{3}{=}{\textbf{Software Documentation}}
& Pandoc \& LaTeX & Pandoc \texttt{3.9.0.2} / Lua \texttt{5.4} & Herramientas utilizadas para transformar el contenido Markdown y LaTeX del informe en su versión final en PDF. & \href{https://pandoc.org/installing.html}{Descarga: Pandoc} \\
\cline{2-5}

& Structurizr (DSL) & SaaS / DSL & Herramienta Diagram-as-Code utilizada para elaborar el C4 Model de la arquitectura de software. & \href{https://structurizr.com/}{SaaS: Structurizr} \\
\cline{2-5}

& PlantUML & SaaS / Local & Lenguaje y herramienta de modelado utilizada para elaborar los diagramas de clases orientados a objetos. & \href{https://plantuml.com/}{SaaS / Local: PlantUML} \\
\hline

\end{longtable}
\endgroup

Table: Herramientas y productos utilizados para el desarrollo de VitaLink

Las versiones registradas para Node.js, Git y Pandoc corresponden al entorno de trabajo utilizado actualmente por el equipo. Para npm se registra la versión estable adoptada como referencia para el entorno Frontend. Visual Studio 2022 y PostgreSQL se mantienen como tecnologías previstas para la implementación posterior de la REST API, debido a que dicho producto todavía no corresponde al alcance implementado en el incremento actual.

La versión específica de Visual Studio Code permanece pendiente de verificación.

### 5.1.2. Source Code Management

El equipo CodeBrokers gestiona el código fuente y la documentación del proyecto mediante **Git** y **GitHub**. Los repositorios se encuentran alojados bajo la organización:

`1ASI0730-2620-16712-grupo2-CodeBrokers`

URL de la organización:

https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers

El control de versiones utiliza las ramas permanentes `main` y `develop`, complementadas por ramas temporales asociadas al tipo de trabajo realizado. El historial del proyecto evidencia el empleo de ramas `feature/*` para funcionalidades o secciones específicas y `docs/*` para modificaciones documentales.

Los cambios se integran mediante Pull Requests, permitiendo revisar y consolidar las modificaciones antes de incorporarlas a las ramas de integración o de entrega.

#### Repositorios del proyecto

\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.3}

\begin{longtable}{|p{0.40\textwidth}|p{0.38\textwidth}|p{0.17\textwidth}|}
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

\texttt{upc-pre-202620-1asi0730-16712-CodeBrokers-report} & Informe académico del proyecto en formato Markdown, diagramas como código mediante Structurizr DSL y PlantUML, assets y configuración utilizada para la generación del PDF. & \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-report-}{Ver repositorio} \\
\hline

\texttt{upc-pre-202620-1asi0730-16712-CodeBrokers-Landing\_Page} & Landing Page pública de VitaLink implementada como aplicación web estática y desplegada mediante GitHub Pages. & \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page}{Ver repositorio} \\
\hline

\texttt{upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application} & Aplicación Frontend de VitaLink desarrollada con Vue.js y con soporte de internacionalización en inglés y español mediante \texttt{vue-i18n}. & \href{https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application}{Ver repositorio} \\
\hline

\texttt{RESTful API / Backend} & Servicios de Backend previstos para VitaLink. Su implementación todavía no corresponde al avance actual del proyecto, por lo que el repositorio aún no ha sido creado. & \textit{Pendiente de implementación} \\
\hline

\end{longtable}
\endgroup

Table: Repositorios del proyecto VitaLink

#### Modelo de ramificación: GitFlow

El equipo emplea una estrategia de ramificación basada en **GitFlow**, adaptada al flujo de trabajo académico del proyecto. Las ramas `main` y `develop` permanecen durante todo el ciclo de desarrollo, mientras que las ramas temporales permiten aislar funcionalidades, documentación y correcciones antes de su integración.

El historial real del repositorio evidencia actualmente el uso de ramas `feature/*` y `docs/*`. Las convenciones `fix/*`, `release/*` y `hotfix/*` forman parte de la política establecida para los casos en que sean necesarias, aunque su utilización debe diferenciarse de aquellas ramas que ya cuentan con evidencia en el historial.

\begingroup
\centering
\small
\setlength{\tabcolsep}{3pt}
\renewcommand{\arraystretch}{1.4}

\begin{longtable}{|p{0.20\textwidth}|p{0.10\textwidth}|p{0.11\textwidth}|p{0.14\textwidth}|p{0.37\textwidth}|}
\hline
\textbf{Rama} & \textbf{Tipo} & \textbf{Origen habitual} & \textbf{Destino del merge} & \textbf{Descripción} \\
\hline
\endfirsthead

\hline
\textbf{Rama} & \textbf{Tipo} & \textbf{Origen habitual} & \textbf{Destino del merge} & \textbf{Descripción} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

\texttt{main} & Permanente & --- & --- & Contiene las versiones estables correspondientes a los hitos evaluados del proyecto: AV1, TB1, AV2 y TB2. No se realiza desarrollo directo sobre esta rama. \\
\hline

\texttt{develop} & Permanente & \texttt{main} & \texttt{main} & Rama principal de integración. Concentra los cambios terminados antes de que estos formen parte de una versión estable. \\
\hline

\texttt{feature/*} & Temporal & \texttt{develop} & \texttt{develop} & Utilizada para el desarrollo de nuevas funcionalidades o secciones. El historial del proyecto evidencia ramas de este tipo, entre ellas \texttt{feature/collaboration-insights}. \\
\hline

\texttt{docs/*} & Temporal & \texttt{develop} & \texttt{develop} o rama estable según el flujo aplicado & Utilizada para cambios exclusivamente documentales. Existen evidencias reales como \texttt{docs/12-lean-ux-validation}, \texttt{docs/03-collaboration-insights} y \texttt{docs/61-conclusiones}. \\
\hline

\texttt{fix/*} & Temporal & \texttt{develop} & \texttt{develop} & Convención definida para corregir errores encontrados durante el desarrollo sin introducir nuevas funcionalidades. Su evidencia de uso se encuentra pendiente de verificar. \\
\hline

\texttt{release/*} & Temporal & \texttt{develop} & \texttt{main} y \texttt{develop} & Convención prevista para la estabilización de una versión antes de una entrega, admitiendo únicamente los ajustes necesarios para su publicación. \\
\hline

\texttt{hotfix/*} & Temporal & \texttt{main} & \texttt{main} y \texttt{develop} & Convención prevista para una corrección urgente sobre una versión estable ya publicada. \\
\hline

\end{longtable}
\endgroup

Table: Modelo de ramificación GitFlow aplicado en VitaLink

Las ramas temporales se crean a partir de la rama que corresponda al tipo de cambio. Como práctica de trabajo, una rama temporal puede eliminarse del repositorio remoto una vez que su Pull Request haya sido integrado y se haya verificado que no existe trabajo pendiente asociado a ella.

Durante los primeros incrementos se conservaron algunas ramas históricas como evidencia del proceso de desarrollo. Por este motivo, la eliminación de ramas después de un merge se considera una convención de trabajo para los cambios posteriores y no una condición que necesariamente se haya aplicado de forma retroactiva a todo el historial del proyecto.

#### Flujo de integración de cambios

El flujo habitual para incorporar modificaciones comienza con la actualización de la rama `develop`. A partir de ella se crea una rama temporal asociada al trabajo que se realizará, como `feature/*`, `docs/*` o `fix/*`, según corresponda.

Durante el desarrollo, los cambios son registrados mediante commits descriptivos. Una vez finalizada la tarea, la rama se publica en GitHub y se genera un **Pull Request** hacia la rama de integración correspondiente.

El Pull Request permite documentar el objetivo del cambio, revisar las modificaciones realizadas y verificar posibles conflictos antes de la integración. Cuando las observaciones son atendidas y el cambio se encuentra listo, el Pull Request se integra a la rama correspondiente.

El historial del repositorio del informe contiene evidencia de este proceso. Entre los registros observados se encuentran los Pull Requests `#33`, `#34`, `#35` y `#37`, junto con sus respectivos commits de integración.

**Evidencia visual de Pull Request:** \textit{Pendiente de incorporar captura.}

#### Versionado semántico

Las versiones estables del proyecto se identifican siguiendo como referencia **Semantic Versioning 2.0.0**, mediante el formato `MAJOR.MINOR.PATCH`:

- **MAJOR:** incrementa cuando se introducen cambios incompatibles con una versión anterior.
- **MINOR:** incrementa al incorporar nuevas funcionalidades manteniendo compatibilidad.
- **PATCH:** incrementa ante correcciones que no alteran la funcionalidad existente.

En el historial real del repositorio del informe se registra la etiqueta `v1.0.0`, asociada a la consolidación de la entrega **AV1** en la rama `main`.

Las siguientes etiquetas correspondientes a TB1, AV2 y TB2 deberán registrarse conforme avance el proyecto y se consoliden las respectivas entregas.

#### Convención de mensajes de commit

El equipo adopta **Conventional Commits 1.0.0** para estandarizar los nuevos mensajes de commit. La estructura utilizada es:

`<type>(<scope>): <description>`

La descripción debe redactarse en **inglés**, preferentemente en modo imperativo, utilizando minúsculas y sin punto final. El `scope` identifica el módulo, sección o área afectada cuando resulte necesario.

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

\texttt{feat} & Incorporación de una nueva funcionalidad del producto o capacidad significativa. \\
\hline

\texttt{fix} & Corrección de un error de contenido, comportamiento o código. \\
\hline

\texttt{docs} & Cambios exclusivamente relacionados con documentación. \\
\hline

\texttt{style} & Cambios de formato que no modifican el comportamiento del producto. \\
\hline

\texttt{refactor} & Reestructuración del código o contenido sin modificar su comportamiento funcional. \\
\hline

\texttt{chore} & Tareas de mantenimiento del repositorio y de su estructura. \\
\hline

\texttt{build} & Cambios relacionados con compilación, dependencias o generación de artefactos. \\
\hline

\end{longtable}
\endgroup

Table: Tipos de commit admitidos

El historial reciente evidencia la aplicación de la convención mediante mensajes redactados en inglés, entre ellos:

```text
docs(lean-ux): add early validation hypotheses and metrics
docs(frontmatter): add project report collaboration insights with ABET SO-5 table
build(report): add latex packages and migrate tables to longtable
docs(8): add annexes with expo videos, repositories and tools
docs(6,7): add conclusions, recommendations and APA bibliography
docs(61): add conclusions and recommendations
```

El historial también conserva algunos mensajes anteriores redactados en español, por ejemplo merges asociados a la consolidación de AV1. Estos registros se mantienen como evidencia histórica y no representan la convención vigente. A partir de la estandarización definida por el equipo, los nuevos mensajes de commit deben redactarse en inglés.

#### Política de integración

Los cambios desarrollados en ramas temporales deben ser integrados mediante **Pull Requests** y no mediante desarrollo directo sobre `main`.

Para los nuevos cambios del proyecto, el Pull Request debe:

- Describir brevemente el propósito y alcance de la modificación.
- Identificar la funcionalidad, módulo o sección afectada.
- Verificar que no existan conflictos pendientes con la rama destino.
- Permitir la revisión del cambio antes de su integración.
- Mantener los mensajes de commit de acuerdo con la convención establecida.

La exigencia de aprobación explícita por parte de otro integrante se encuentra **pendiente de verificar mediante evidencia de los Pull Requests existentes**, por lo que no se establece todavía como una condición demostrada en el historial del proyecto.

Después de integrar una rama temporal y comprobar que no contiene trabajo pendiente, esta puede ser eliminada del repositorio remoto. Las ramas históricas conservadas previamente pueden mantenerse como evidencia del proceso realizado.

### 5.1.3. Source Code Style Guide & Conventions

El equipo adopta guías de estilo reconocidas por la industria para cada tecnología utilizada en VitaLink, con el objetivo de mantener consistencia, legibilidad y facilidad de revisión.

Los identificadores utilizados en código fuente, tales como nombres de variables, funciones, clases, componentes y archivos, se redactan principalmente en **inglés** siguiendo las convenciones de cada tecnología.

El informe académico se redacta en **español**, mientras que los productos de software establecen el **inglés como idioma predeterminado de la interfaz**, ofreciendo español como idioma alternativo cuando corresponde.

#### Language and Localization Conventions

La aplicación Frontend de VitaLink implementa internacionalización mediante la biblioteca **vue-i18n**, permitiendo presentar la interfaz en inglés y español.

El inglés constituye el idioma predeterminado del producto, mientras que el español se ofrece como idioma alternativo. Los textos visibles de la interfaz se gestionan mediante recursos de traducción separados de los componentes, reduciendo el acoplamiento entre el contenido dependiente del idioma y la lógica de presentación.

Las siguientes convenciones lingüísticas se aplican al proyecto:

- Los textos base de la interfaz se definen utilizando inglés como idioma principal.
- El usuario puede cambiar el idioma de la aplicación a español mediante la funcionalidad de internacionalización implementada.
- Los identificadores utilizados en el código fuente se redactan en inglés.
- Los nuevos mensajes de commit se redactan en inglés.
- El informe académico permanece redactado en español.

Los identificadores exactos de los locales utilizados por `vue-i18n` quedan pendientes de documentar a partir de la configuración del repositorio Frontend.

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

Fin de línea & LF (\texttt{\textbackslash{}n}) como convención definida por el equipo. La normalización automática mediante \texttt{.gitattributes} se encuentra pendiente de verificar. \\
\hline

Indentación & 2 espacios en HTML, CSS, JavaScript y Vue; 4 espacios en C\# \\
\hline

Longitud máxima de línea & 100 caracteres como referencia general para mantener la legibilidad \\
\hline

Nombres de archivo & \texttt{kebab-case} para archivos web y recursos generales; \texttt{PascalCase} para componentes Vue y archivos asociados a tipos o clases en C\# \\
\hline

Idioma de los identificadores & Inglés \\
\hline

Idioma predeterminado de la interfaz & Inglés, con español disponible mediante la funcionalidad de internacionalización \\
\hline

\end{longtable}
\endgroup

Table: Convenciones generales de codificación

#### HTML5 y CSS3

Se sigue como referencia la **Google HTML/CSS Style Guide**. En HTML se prioriza el empleo de etiquetas semánticas como `<header>`, `<nav>`, `<main>`, `<section>` y `<footer>` cuando representan correctamente la estructura del documento.

Los atributos HTML se delimitan con comillas dobles y las imágenes deben declarar un atributo `alt` descriptivo cuando corresponde.

En CSS se utiliza una nomenclatura consistente para las clases y se centralizan valores reutilizables, como colores y tipografías, mediante variables CSS declaradas en `:root`, en concordancia con los Style Guidelines definidos en la sección 4.1.

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

La aplicación exacta de la metodología BEM en todos los estilos del producto se encuentra **pendiente de verificar directamente en los repositorios correspondientes**, por lo que se mantiene como convención recomendada y no como una afirmación sobre la totalidad del código implementado.

#### JavaScript y Vue.js

Para JavaScript y Vue.js se utilizan como referencia buenas prácticas de la **Airbnb JavaScript Style Guide** y de la **Vue.js Style Guide**.

Las variables y funciones se nombran en `camelCase`, mientras que los componentes Vue utilizan `PascalCase`. Se utiliza `const` cuando la referencia no debe ser reasignada y `let` cuando la reasignación resulta necesaria, evitando el uso de `var`.

Los componentes Vue utilizan nombres descriptivos y de más de una palabra cuando corresponde, por ejemplo:

```text
AlertSummaryCard.vue
```

La aplicación Frontend cuenta con soporte de internacionalización mediante **vue-i18n**, permitiendo presentar la interfaz en inglés y español. El inglés se establece como idioma predeterminado y el español como idioma alternativo.

Los identificadores exactos utilizados para los locales y la estructura específica de los archivos de traducción quedan pendientes de documentar a partir de la configuración actual del repositorio Frontend.

#### C# y ASP.NET Core

C\# y ASP.NET Core forman parte de la tecnología prevista para la futura REST API de VitaLink. Debido a que el Backend todavía no corresponde al avance actual del proyecto, las siguientes reglas constituyen las convenciones que deberán aplicarse cuando inicie su implementación.

Se seguirán como referencia las **Microsoft C# Coding Conventions**. Los tipos, métodos y propiedades públicas se nombrarán en `PascalCase`; los parámetros y variables locales, en `camelCase`; y los campos privados podrán utilizar el prefijo `_` seguido de `camelCase`.

Las interfaces se nombrarán utilizando el prefijo `I`, por ejemplo:

```text
IAlertRepository
```

Los métodos asíncronos deberán devolver `Task` o `Task<T>` y utilizar el sufijo `Async` cuando corresponda.

La organización definitiva de namespaces y capas se documentará cuando se implemente la REST API y deberá mantenerse alineada con la arquitectura definida para VitaLink.

#### PostgreSQL

PostgreSQL corresponde al motor de persistencia previsto para la futura REST API. Debido a que esta parte del sistema todavía no ha sido implementada, las siguientes reglas representan las convenciones de diseño acordadas y deberán verificarse durante su desarrollo.

Los identificadores de base de datos se escribirán en `snake_case` y en minúsculas. Las claves foráneas seguirán un patrón consistente basado en el identificador de la entidad relacionada.

Las restricciones deberán utilizar nombres explícitos y consistentes, pudiendo aplicarse prefijos como:

- `pk_` para claves primarias.
- `fk_` para claves foráneas.
- `uq_` para restricciones de unicidad.
- `ck_` para restricciones de validación.
- `ix_` para índices.

La aplicación definitiva de estas convenciones deberá mantenerse alineada con el Database Design documentado en la sección 4.8.

#### Markdown y diagramas como código

El informe se redacta principalmente en Markdown y se complementa con bloques LaTeX cuando el formato requerido no puede ser representado adecuadamente mediante Markdown puro, como ocurre con determinadas tablas de gran tamaño.

Las imágenes y demás recursos del informe se referencian mediante rutas relativas dentro del repositorio, evitando dependencias de rutas locales propias de un integrante.

Los diagramas de arquitectura y diseño se mantienen como código cuando corresponde. El C4 Model utiliza **Structurizr DSL**, mientras que los diagramas orientados a objetos utilizan **PlantUML**, permitiendo que los cambios realizados en estos artefactos queden registrados mediante el sistema de control de versiones.

Las tablas utilizadas en el informe incluyen una descripción mediante la sintaxis:

```text
Table: <descripción>
```

para permitir su identificación durante el proceso de generación del documento.

### 5.1.4. Software Deployment Configuration

VitaLink cuenta actualmente con dos productos desplegados públicamente: la **Landing Page** y la **Frontend Application**. Cada producto utiliza una estrategia de despliegue acorde con sus características tecnológicas.

#### Landing Page Deployment

La Landing Page de VitaLink se encuentra publicada mediante **GitHub Pages**, aprovechando la integración directa con el repositorio alojado en GitHub.

El repositorio utilizado para el despliegue es:

`upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page`

Repositorio:

https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page

Dentro de **Settings > Pages**, el mecanismo de publicación está configurado mediante **Deploy from a branch**. La fuente de despliegue corresponde a la rama `main`, utilizando el directorio `/ (root)` como origen de los archivos publicados.

De esta manera, los archivos estáticos consolidados en la rama estable son utilizados por GitHub Pages para generar el entorno público de la Landing Page.

El entorno de producción se encuentra disponible en:

https://1asi0730-2620-16712-grupo2-codebrokers.github.io/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page/

#### Frontend Application Deployment

La aplicación Frontend de VitaLink se encuentra desplegada públicamente mediante **Vercel**, utilizando el repositorio:

`upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application`

Repositorio:

https://github.com/1ASI0730-2620-16712-grupo2-CodeBrokers/upc-pre-202620-1asi0730-16712-CodeBrokers-frontend-application

El entorno público de la aplicación está disponible en:

https://vitalink-opal.vercel.app/#/

La rama configurada como Production Branch dentro de Vercel queda pendiente de verificar antes de documentarla como parte del procedimiento definitivo de despliegue.

#### Deployment Status

\begingroup
\centering
\small
\setlength{\tabcolsep}{4pt}
\renewcommand{\arraystretch}{1.4}

\begin{longtable}{|p{0.18\textwidth}|p{0.17\textwidth}|p{0.27\textwidth}|p{0.31\textwidth}|}
\hline
\textbf{Producto} & \textbf{Proveedor} & \textbf{Fuente de despliegue} & \textbf{Estado} \\
\hline
\endfirsthead

\hline
\textbf{Producto} & \textbf{Proveedor} & \textbf{Fuente de despliegue} & \textbf{Estado} \\
\hline
\endhead

\hline
\endfoot

\hline
\endlastfoot

Landing Page & GitHub Pages & Deploy from a branch utilizando la rama \texttt{main} y el directorio \texttt{/ (root)} & Desplegada públicamente \\
\hline

Frontend Application & Vercel & Despliegue de la aplicación Vue.js. Production Branch pendiente de verificar. & Desplegada públicamente \\
\hline

RESTful API & \textit{Pendiente} & \textit{Pendiente} & Todavía no corresponde su implementación \\
\hline

\end{longtable}
\endgroup

Table: Estado de despliegue de los productos de VitaLink

La RESTful API todavía no forma parte del incremento implementado actualmente. Por este motivo, su proveedor, estrategia de despliegue y URL de producción serán documentados cuando corresponda desarrollar el Backend.