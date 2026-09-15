# Capítulo V: Product Implementation, Validation & Deployment

## 5.1. Software Configuration Management

En esta sección se establecen las decisiones de gestión de configuración que rigen el desarrollo de VitaLink: el entorno de trabajo de cada integrante, la política de control de versiones sobre los repositorios del equipo, las convenciones de codificación por tipo de artefacto y el procedimiento de despliegue. El objetivo es que cualquier integrante pueda incorporarse al proyecto, reproducir el entorno y contribuir sin ambigüedades sobre cómo nombrar, escribir y publicar el código.

### 5.1.1. Software Development Environment Configuration



### 5.1.2. Source Code Management

El equipo CodeBrokers gestiona el código fuente y la documentación del proyecto en **GitHub**, bajo la organización `CodeBrokers-web-app-1ASI0730-2620-16712`. El control de versiones se realiza con **Git**, aplicando el modelo de ramificación **GitFlow** y la especificación **Conventional Commits** para los mensajes.

#### Repositorios del proyecto

| Repositorio | Propósito | URL |
| :--- | :--- | :--- |
| `upc-pre-202620-1asi0730-16712-CodeBrokers-report-` | Informe del proyecto en formato Markdown, diagramas como código (Structurizr DSL, PlantUML) y script de compilación a PDF mediante Pandoc. | \href{https://github.com/CodeBrokers-web-app-1ASI0730-2620-16712/upc-pre-202620-1asi0730-16712-CodeBrokers-report-}{Ver repositorio} |
| `vitalink-landing-page` | Landing Page de VitaLink implementada en HTML5, CSS3 y JavaScript. | *(Completar con la URL del repositorio del equipo)* |
| `vitalink-frontend` | Aplicación web de VitaLink desarrollada en Vue.js con PrimeVue. | *(Pendiente — se crea a partir del Sprint 2)* |
| `vitalink-backend` | Servicios RESTful de VitaLink desarrollados en ASP.NET Core con Entity Framework Core. | *(Pendiente — se crea a partir del Sprint 2)* |

Table: Repositorios del proyecto VitaLink

#### Modelo de ramificación: GitFlow

El equipo adopta GitFlow, propuesto por Vincent Driessen, por ajustarse a un desarrollo iterativo por sprints con entregables parciales evaluados. Las ramas se organizan de la siguiente manera:

| Rama | Tipo | Origen | Destino del merge | Descripción |
| :--- | :--- | :--- | :--- | :--- |
| `main` | Permanente | — | — | Contiene únicamente versiones estables y entregadas. Cada entrega evaluada (AV1, AV2, TP, TB) corresponde a un estado de esta rama. No se desarrolla directamente sobre ella. |
| `develop` | Permanente | `main` | `main` | Rama de integración. Concentra el trabajo terminado de todas las ramas de característica y refleja el estado actual del proyecto en curso. |
| `feature/<n>-<descripción>` | Temporal | `develop` | `develop` | Una rama por cada sección del informe o funcionalidad del producto. Se elimina tras su integración. Ejemplos reales del proyecto: `feature/48-database-design`, `feature/471-class-diagrams`, `feature/45-web-applications-prototyping`. |
| `release/<versión>` | Temporal | `develop` | `main` y `develop` | Rama de estabilización previa a una entrega. Solo admite correcciones, nunca nuevas funcionalidades. |
| `hotfix/<descripción>` | Temporal | `main` | `main` y `develop` | Corrección urgente sobre una versión ya entregada. |

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

| Tipo | Uso |
| :--- | :--- |
| `feat` | Incorporación de una nueva sección del informe o de una funcionalidad del producto. |
| `fix` | Corrección de un error de contenido, de formato o de código. |
| `docs` | Cambios exclusivamente documentales. |
| `style` | Cambios de formato que no alteran el significado del contenido. |
| `refactor` | Reestructuración que no modifica el comportamiento ni el contenido sustantivo. |
| `chore` | Tareas de mantenimiento del repositorio y de su estructura. |
| `build` | Cambios en la configuración de compilación del informe o del producto. |

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

| Aspecto | Convención |
| :--- | :--- |
| Codificación de archivos | UTF-8 sin BOM |
| Fin de línea | LF (`\n`), normalizado mediante `.gitattributes` |
| Indentación | 2 espacios en HTML, CSS, JavaScript y Vue; 4 espacios en C# |
| Longitud máxima de línea | 100 caracteres |
| Nombres de archivo | `kebab-case`, salvo en C#, donde se emplea `PascalCase` |
| Idioma de los identificadores | Inglés |

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
siguiente URL: https://codebrokers-web-app-1asi0730-2620-16712.github.io/upc-pre-202620-1asi0730-16712-CodeBrokers-Landing_Page/

