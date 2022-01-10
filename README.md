
<!-- README.md is generated from README.Rmd. Please edit that file -->

## 1. Datos y análisis del laboratorio de instrumentos

<!-- badges: start -->

[![Lifecycle:
experimental](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://lifecycle.r-lib.org/articles/stages.html#experimental)
[![CRAN
status](https://www.r-pkg.org/badges/version/labinstrumentos)](https://CRAN.R-project.org/package=labinstrumentos)
[![R-CMD-check](https://github.com/SEREMICTCI/labinstrumentos/workflows/R-CMD-check/badge.svg)](https://github.com/SEREMICTCI/labinstrumentos/actions)
<!-- badges: end -->

Este es un paquete de <i class="fab fa-r-project"></i> que contiene los
datos procesados del laboratorio de intrumentos, así como herramientas
complementarias para su análisis y visualización.

## 2. Origen de los datos

El taller “Laboratorios de Instrumentos” tiene por objetivo generar una
propuesta de recomendaciones a programas/instrumentos ANID teniendo en
cuenta las brechas regionales y el sistema CTCI local. El análisis
actual se focalizó en los los instrumentos más utilizados en la
Macrozona Austral y seleccionando aquellos investigadores principales
con proyectos vigentes con año de finalización desde 2020 en adelante.
Se obtuvieron un total de 4 programas con 6 instrumentos en total.

| Programa                                                        | Instrumento                                |
|-----------------------------------------------------------------|--------------------------------------------|
| Programa de Inserción, PAI                                      | Subvención a la Instalación en la Academia |
| Programa de Equipamiento Científico y Tecnológico, Fondequip    | Fondequip Mediano                          |
| Fondo Nacional de Desarrollo Científico y Tecnológico, Fondecyt | Regular                                    |
| Fondo Nacional de Desarrollo Científico y Tecnológico, Fondecyt | Iniciación                                 |
| Fondo Nacional de Desarrollo Científico y Tecnológico, Fondecyt | Postdoctorado                              |
| Fondo de Fomento al Desarrollo Científico y Tecnológico, Fondef | IDEA                                       |

Por último se seleccionaron a los investigadores que pertenecen a las
instituciones que tienen comprobada residencia en la región de Aysén y
Magallanes, pero se realizaron invitaciones especiales con el criterio
de mejorar el desarrollo del taller e incluir miradas particulares que
se consideraron necesarias, debido a esto en el programa FONDEQUIP se
sumaron investigadores de fuera de la macrozona pero con proyectos cuya
región de ejecución es Aysén o Magallanes.

Para llevar a cabo el objetivo de este trabajo, se llevó a cabo el
siguiente plan de acción:

| Etapa                     | 1\. Preparación de indicadores                                                                                          | 2\. Análisis y generación de propuestas                                                                                                                                                    | 3\. Desarrollo técnico de propuestas                                                                                                           |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción               | Preparación de indicadores relativos a los programas de financiamiento a partir de información disponibilizada por ANID | Talleres de participación “Laboratorio de Instrumentos” en donde se analizarán los problemas locales relacionados con los programas de financiamiento de la ciencia por usuarios vigentes. | Mesa de trabajo para sistematizar las propuestas entregadas en la etapa 2 y consolidar un documento de recomendaciones con identidad regional. |
| Participantes             | Seremi Macrozona Austral                                                                                                | Investigadores de la macrozona                                                                                                                                                             | Selección de investigadores de la macrozona proveniente de la etapa 2.                                                                         |
| Cantidad de participantes | 3 (Seremi)                                                                                                              | 5-7 personas por facilitador                                                                                                                                                               | 7 personas (Seremi (2) + representantes (5))                                                                                                   |
| Fecha                     | 3 meses (marzo a mayo)                                                                                                  | 3 meses (junio a agosto)                                                                                                                                                                   | 3 meses (septiembre a noviembre)                                                                                                               |
| Metodología               | Análisis y visualización de datos                                                                                       | Talleres participativos                                                                                                                                                                    | Mesa técnica                                                                                                                                   |

La secuencia didáctica de los Laboratorios se basa en la producción
creativa individual y colectiva, un fenómeno complejo influenciado por
múltiples variables y distintos niveles, que a su vez depende de
variables contextuales y medioambientales. La mayoría de los autores
están de acuerdo en que los procesos centrales necesarios para la
resolución creativa de problemas son (1) la identificación y
construcción de problemas, (2) la identificación de información
relevante, (3) la generación de nuevas ideas y la (4) evaluación de
estas ideas (Basadur & Gelade, 2003; Montag-Smit & Maertz, 2017;
Mumford, 2001; Pressman, 2019; Reiter-Palmon & Illies, 2004). Los
primeros tres procesos normalmente se consideran parte de la fase de
generación de ideas, mientras que el último se considera parte de la
fase de implementación (Mumford, 2001). A partir de lo anterior, se
definen 3 etapas dentro de la metodología del taller: Problemática,
Elaboración y Evaluación.

**Tabla 3**

| Problemática                                                          | Elaboración                                                       | Comunicación                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------|
| 1\. Entregar análisis sistema CTCI regional y roles de participantes. | 1\. Identificar y seleccionar información que respalde problemas. | 1\. Preparar recomendaciones                               |
| 2\. Reconocer, enumerar y describir problemas del instrumento.        | 2\. Filtrar información y crear fichas de los problemas           | 2\. Comunicar las propuestas                               |
| 3\. Agrupar los problemas detectados                                  | 3\. Priorizar los problemas                                       | 3\. Evaluar, discutir y recibir feedback de las propuestas |
| 4\. Profundizar y definir raíz del problema.                          | 4\. Generar recomendaciones                                       |                                                            |
| 5\. Identificar información para validar problemas.                   | 5\. Consolidar recomendaciones: priorización                      |                                                            |
| \* Grupos                                                             | \* Grupos                                                         | \* Plenario                                                |

## 3. Tratamiento de los datos

Los talleres fueron desarrollados a partir de la metodología anterior,
de la cual se obtuvo información de los problemas, causas,
consecuencias, indicadores y soluciones para cada problema detectado.

Esto fue compilado en formato largo y quedaron relacionados todos los
problemas con sus causas, consecuencias, indicadores y soluciones,
utilizando el problema como elemento pivot.

### 3.1. Limpieza manual

Para cada columna se realizó una limpieza manual que consistió en X
pasos:

1.  Se cambiaron palabras compuestas por palabras únicas, por ejemplo:
    no es flexible: inflexible, ‘falta de’: insuficiente, ‘demora
    en’:lenta, etc.

2.  Se estandarizaron las palabras que se refirieran a lo mismo pero con
    distintos términos, unificando en un solo término varias palabras,
    por ejemplo: rígido-faltadeflexibilidad-inmovilidad: inflexible,
    MZ-regiones: Macrozona, presupuesto-recursos-financiar-monto:
    financiamiento, etc.

Se unificaron con guiones las palabras compuestas, por ejemplo:
Capital-humano, costo-operacional, Macrozona-Austral, etc.

### 3.2. Limpieza programática

Descargamos los datos alojados en un Google Sheets, con las últimas
modificaciones del procesamiento manual de los datos.

Seguido a esto se asignó nombres sintácticamente válidos a las columnas
y se estandarizó el formato del texto, es decir, se eliminaron, puntos,
comas y se transformó todo a minúsculas.

Se procesó adicionalmente las columnas de problemas, causas,
consecuencias y soluciones, en donde se eliminaron las “stop-words”
(conectores), sin incluir aquellas que estuvieron precedidas o
antecedidas por un guión, i.e. palabra compuesta (e.g.,
‘no-consideran’).

## 4. Análsis de frecuencia de palabras

Se obtuvieron frecuencias de palabras mediante la selección de palabras
que se repitieran. Este proceso se replicó con grupos de dos y tres
palabras para obtener el contexto en el cual se dieron los términos. Los
cuales pueden apreciarse en el segmento de [análisis
exploratorio](https://seremictci.github.io/labinstrumentos/articles/articles/eda.html).

## 5. Detección de comunidades

Para el análisis de potenciales comunidades existentes en los datos se
crearon las matrices de adjacencia de los términos. Para esto se
implementó una función que lo calculó para cada dimensión, la cual puede
consultarse en su respectiva
[documentación](https://seremictci.github.io/labinstrumentos/reference/crear_redes_de_palabras.html).

### 5.1. Obtención de redes de palabras

Para la creación de las redes de palabras y su posterior estudio, se usó
la matriz de adjacencia calculada anteriormente (c.f., ver
[documentación](https://seremictci.github.io/labinstrumentos/reference/crear_redes_de_palabras.html)),
frente a lo cual realizamos vizualizaciones de redes de palabras y
análisis de comunidades.

### 5.2. Análisis alternando la inclusión de ANID

Se realizaron análisis incluyendo y excluyendo el término ANID, debido a
su influencia producto de su repetición y conexión con otros términos.
Los cuales pueden verse a continuación:

-   [Incluyendo
    ANID](https://seremictci.github.io/labinstrumentos/articles/articles/network.html)
-   [Excluyendo
    ANID](https://seremictci.github.io/labinstrumentos/articles/articles/network_sin_anid.html)

### 5.3. Relación interdimensional mediante gráficos Sankey

Para la exploración entre las diferentes dimensiones analizadas, se
representaron los términos (así como los grupos de términos) usando
gráficos Sankey, los cuales muestran la conexión existente entre
dimensiones, pudiendo hallar vínculos entre grupos de palabras y
conceptos, permitiendo un nivel de abstracción mayor. Estos pueden
apreciarse
[aquí](https://seremictci.github.io/labinstrumentos/articles/articles/sankey.html).

## Sobre <i class="fab fa-r-project"></i>

`R` es un lenguaje de programación estadística de alto nivel usado para
el análisis de datos, así como para el desarrollo de herramientas
informáticas como sitios web, reportes, aplicaciones, libros digitales,
etc. Para más información puedes visitar el sitio de
[R-project](https://www.r-project.org/about.html).

## Instalación

Para instalar el paquete directamente a tu computadora, asegurate de
tener instalado `R`, luego escribe en tu consola de `R` lo siguiente:

``` r
# install.packages("devtools")
devtools::install_github("SEREMICTCI/labinstrumentos")
```

## Dependencias

Este paquete, así como sus correspondientes análisis, dependen de los
siguientes paquetes.

<img src="man/figures/README-unnamed-chunk-2-1.png" width="100%" />

## Reconocimiento

Para citar este paquete en publicaciones puedes correr la siguiente
función en tu consola de `R`.

``` r
citation("labinstrumentos")
```

Lo que te dará el siguiente resultado.


    To cite package 'labinstrumentos' in publications use:

      Matías Castillo Aguilar and Carlos Morales Quiroz (2021).
      labinstrumentos: Datos del Laboratorio de Instrumentos. R package
      version 0.0.0.9012. https://github.com/SEREMICTCI/labinstrumentos

    A BibTeX entry for LaTeX users is

      @Manual{,
        title = {labinstrumentos: Datos del Laboratorio de Instrumentos},
        author = {Matías {Castillo Aguilar} and Carlos {Morales Quiroz}},
        year = {2021},
        note = {R package version 0.0.0.9012},
        url = {https://github.com/SEREMICTCI/labinstrumentos},
      }
