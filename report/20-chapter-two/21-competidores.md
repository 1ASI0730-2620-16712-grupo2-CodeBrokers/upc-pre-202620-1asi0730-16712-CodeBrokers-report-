# Capítulo II: Requirements Elicitation & Analysis

## 2.1. Competidores

Para el análisis de competidores se priorizó la identificación de soluciones digitales con un modelo de negocio similar al de VitaLink: aplicaciones orientadas al monitoreo remoto de adultos mayores y a la conexión entre el adulto mayor, sus familiares/cuidadores y, en algunos casos, proveedores de atención. Dado que en el mercado peruano no se identificaron startups comerciales activas con una oferta equivalente (solo iniciativas académicas no comercializadas), se consideraron competidores directos de alcance internacional/regional, cuya propuesta de valor es comparable a la de VitaLink.

Los competidores identificados son:

1. **cuYdo** (España) — aplicación móvil que, mediante sensores instalados en el hogar, permite a familiares y cuidadores conocer en tiempo real la situación del adulto mayor que vive solo, sin uso de cámaras.

\par
\noindent
\includegraphics[
    width=\linewidth,
    height=0.1\textheight,
    keepaspectratio
]{assets/21-competidores-cuydo.png}
\par

2. **CuidApp** (Argentina) — aplicación orientada a coordinar el cuidado de un adulto mayor entre un "cuidador principal" y un grupo de "ayudantes" (familiares/cuidadores secundarios).

\par
\noindent
\includegraphics[
    width=\linewidth,
    height=0.1\textheight,
    keepaspectratio
]{assets/21-competidores-cuidapp.png}
\par

3. **Silver-Digi** (España) — aplicación que facilita la independencia de adultos mayores mediante videollamadas automáticas con cuidadores/familiares y monitoreo remoto de datos de sensores.

\par
\noindent
\includegraphics[
    width=\linewidth,
    height=0.1\textheight,
    keepaspectratio
]{assets/21-competidores-silverdigi.png}
\par


### 2.1.1. Análisis competitivo

**Competitive Analysis Landscape**

\begin{longtable}{
|>{\centering\arraybackslash}p{0.07\textwidth}
|>{\raggedright\arraybackslash}p{0.14\textwidth}
|>{\raggedright\arraybackslash}p{0.175\textwidth}
|>{\raggedright\arraybackslash}p{0.175\textwidth}
|>{\raggedright\arraybackslash}p{0.175\textwidth}
|>{\raggedright\arraybackslash}p{0.175\textwidth}|
}

% ============================================================
% TÍTULO
% ============================================================

\hline

\multicolumn{6}{|c|}{
    \textbf{Competitive Analysis Landscape}
}
\\

\hline


% ============================================================
% OBJETIVO DEL ANÁLISIS
% ============================================================

\multicolumn{2}{
|>{\raggedright\arraybackslash}p{0.21\textwidth}|
}{
    \textbf{¿Por qué llevar a cabo este análisis?}
}
&
\multicolumn{4}{
>{\raggedright\arraybackslash}p{0.70\textwidth}|
}{
    Conocer cómo VitaLink se posiciona frente a soluciones existentes de monitoreo
    y acompañamiento de adultos mayores, en términos de propuesta de valor,
    alcance funcional y modelo comercial, para reforzar su ventaja competitiva.
}
\\

\hline


% ============================================================
% NOMBRES Y LOGOS
% ============================================================

\multicolumn{2}{
|>{\raggedright\arraybackslash}p{0.21\textwidth}|
}{
    \textbf{}
}
&
{
\begin{minipage}[c]{0.9\linewidth}
\centering
\textbf{VitaLink}

\vspace{3pt}

\includegraphics[
    width=1.7cm,
    height=0.75cm,
    keepaspectratio
]{assets/logo-vitalink.png}
\end{minipage}
}
&
{
\begin{minipage}[c]{0.9\linewidth}
\centering
\textbf{cuYdo}

\vspace{3pt}

\includegraphics[
    width=1.7cm,
    height=0.75cm,
    keepaspectratio
]{assets/21-competidores-cuydo.png}
\end{minipage}
}
&
{
\begin{minipage}[c]{0.9\linewidth}
\centering
\textbf{CuidApp}

\vspace{3pt}

\includegraphics[
    width=1.7cm,
    height=0.75cm,
    keepaspectratio
]{assets/21-competidores-cuidapp.png}
\end{minipage}
}
&
{
\begin{minipage}[c]{0.9\linewidth}
\centering
\textbf{Silver-Digi}

\vspace{3pt}

\includegraphics[
    width=1.7cm,
    height=0.75cm,
    keepaspectratio
]{assets/21-competidores-silverdigi.png}
\end{minipage}
}
\\

\hline


% ============================================================
% PERFIL
% ============================================================

\multirow{3}{*}{
    \rotatebox[origin=c]{90}{
        \textbf{Perfil}
    }
}
&
\textbf{Overview}
&
Plataforma de CodeBrokers que centraliza el estado de salud del adulto mayor y
conecta a familiares y proveedores de salud mediante alertas preventivas.
&
App para familiares de adultos mayores que viven solos, basada en sensores de
movimiento en el hogar que aprenden rutinas y detectan posibles riesgos.
&
App de coordinación del cuidado organizada en torno a un cuidador principal
(administrador) y un grupo de cuidadores secundarios (ayudantes).
&
App que promueve la independencia de adultos mayores de 65+ mediante
videollamadas automáticas y monitoreo remoto de sensores.
\\

\cline{2-6}

&
\textbf{Ventaja competitiva}
&
Integra en un mismo ecosistema al adulto mayor, la red familiar y proveedores
de salud (clínicas/hospitales), no solo el entorno familiar.
&
Detección de patrones de riesgo sin cámaras, preservando la privacidad del
adulto mayor.
&
Estructura simple de roles (principal/ayudantes) que facilita la coordinación
entre varios cuidadores.
&
Interacción por videollamada automática, pensada para adultos mayores con
baja alfabetización digital.
\\

\cline{2-6}

&
\textbf{¿Qué valor ofrece a los clientes?}
&
Tranquilidad familiar, detección temprana de riesgos y canal directo con
proveedores de salud.
&
Tranquilidad sobre la seguridad del adulto mayor en su propio hogar.
&
Organización y reparto de responsabilidades de cuidado entre varios familiares.
&
Compañía, supervisión remota y reducción de la brecha digital para el adulto mayor.
\\

\hline


% ============================================================
% PERFIL DE MARKETING
% ============================================================

\multirow{2}{*}{
    \rotatebox[origin=c]{90}{
        \textbf{Perfil de Marketing}
    }
}
&
\textbf{Mercado objetivo}
&
Familias con adultos mayores de 60+ en Lima Metropolitana y ciudades del Perú;
clínicas y hospitales.
&
Familiares de adultos mayores que viven solos (España/Europa).
&
Familias con más de un cuidador involucrado (Argentina/Latinoamérica).
&
Adultos mayores 65+ y sus cuidadores/familiares (España).
\\

\cline{2-6}

&
\textbf{Estrategias de marketing}
&
Landing page con call-to-action segmentado (familiares vs. proveedores de
salud), alianzas con clínicas.
&
Difusión a través de fundaciones y programas de buenas prácticas en cuidado
de mayores.
&
Distribución vía tiendas de aplicaciones (Google Play / App Store).
&
Distribución vía App Store, enfocada en accesibilidad y facilidad de uso.
\\

\hline


% ============================================================
% PERFIL DE PRODUCTO
% ============================================================

\multirow{3}{*}{
    \rotatebox[origin=c]{90}{
        \textbf{Perfil de Producto}
    }
}
&
\textbf{Productos \& Servicios}
&
App web/móvil de monitoreo preventivo, sistema de alertas, panel de seguimiento,
canal de comunicación con proveedores.
&
App móvil + kit de sensores para el hogar.
&
App móvil de coordinación de cuidados y grupo de cuidadores.
&
App (solo iOS) + tablet con descuelgue automático para videollamadas.
\\

\cline{2-6}

&
\textbf{Precios \& Costos}
&
Modelo a definir (freemium para familiares, planes para clínicas).
&
No publica precios de forma abierta; requiere instalación de hardware.
&
Información no publicada públicamente.
&
Aplicación gratuita; costo de la tablet/hardware no publicado.
\\

\cline{2-6}

&
\textbf{Canales de distribución (Web y/o Móvil)}
&
Landing Page + Web Application (responsive).
&
Aplicación móvil (Android/iOS).
&
Aplicación móvil (Android/iOS).
&
Aplicación móvil (solo iOS).
\\

\hline


% ============================================================
% ANÁLISIS SWOT
% ============================================================

\multirow{4}{*}{
    \rotatebox[origin=c]{90}{
        \textbf{Análisis SWOT}
    }
}

&
\textbf{Fortalezas}
&
Integra familiares y proveedores de salud en un mismo ecosistema; enfoque
preventivo con sistema de alertas automáticas.
&
Detección de riesgos sin cámaras, preservando la privacidad del adulto mayor.
&
Modelo simple de roles entre cuidadores (principal/ayudantes).
&
Interfaz pensada para reducir la brecha digital del adulto mayor.
\\

\cline{2-6}

&
\textbf{Debilidades}
&
Producto aún en fase de validación, sin usuarios reales ni alianzas confirmadas
con clínicas u hospitales.
&
Depende de instalación física de sensores en el hogar.
&
No incorpora un sistema de alertas ni conexión con proveedores de salud.
&
Disponible solo para iOS, lo que limita su alcance.
\\

\cline{2-6}

&
\textbf{Oportunidades}
&
Crecimiento acelerado de la población adulta mayor en el Perú; ausencia de
un competidor local consolidado.
&
Expansión a mercados latinoamericanos.
&
Alta necesidad de coordinación familiar en el cuidado del adulto mayor.
&
Interés creciente en soluciones de acompañamiento remoto por videollamada.
\\

\cline{2-6}

&
\textbf{Amenazas}
&
Adopción tecnológica limitada en adultos mayores; ingreso de competidores
internacionales (cuYdo, Silver-Digi) al mercado peruano.
&
Soluciones basadas solo en software (como VitaLink), sin hardware, con
menor fricción de adopción.
&
Plataformas con enfoque preventivo/predictivo (como VitaLink) que ofrecen
mayor valor agregado.
&
Soluciones multiplataforma y con mayor cobertura funcional (alertas + panel +
proveedores de salud).
\\

\hline

\end{longtable}

### 2.1.2. Estrategias y tácticas frente a competidores

Con base en el análisis competitivo anterior, CodeBrokers adoptará las siguientes estrategias y tácticas preliminares para VitaLink:

- **Frente a la falta de conexión con proveedores de salud (debilidad común en cuYdo, CuidApp y Silver-Digi):** posicionar como diferenciador principal el canal de comunicación directo entre familiares y clínicas/hospitales, resaltándolo en la Landing Page y en el flujo de onboarding.
- **Frente a la dependencia de hardware de cuYdo:** comunicar que VitaLink no requiere instalación de sensores físicos, reduciendo la fricción de adopción y el costo inicial para las familias.
- **Frente a la limitación de plataforma de Silver-Digi (solo iOS):** desarrollar la Web Application con diseño responsive, accesible desde cualquier dispositivo, ampliando el alcance a segmentos con menor poder adquisitivo.
- **Frente a la baja adopción tecnológica en adultos mayores (amenaza para todo el mercado):** diseñar una interfaz simple e inclusiva (a11y) dirigida principalmente a familiares/cuidadores como usuarios primarios, sin exigir que el adulto mayor interactúe directamente con la plataforma.
- **Frente al posible ingreso de competidores internacionales al mercado peruano (amenaza):** priorizar alianzas tempranas con clínicas y hospitales locales como barrera de entrada, aprovechando que VitaLink nace con enfoque en el ecosistema de salud peruano.
- **Aprovechando la ausencia de un competidor local consolidado (oportunidad):** enfocar la estrategia de marketing inicial en Lima Metropolitana, apoyándose en el crecimiento de la población adulta mayor en el país.