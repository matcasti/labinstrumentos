# labinstrumentos 0.0.0.9011

* Se crea función `obtener_datos()` para descargar los datos en su última versión desde el documento de hojas de Google, tratando los datos y devolviéndolos limpios. Eventualmente y cuando se tenga la versión definitiva de los datos, se procederá por una alternativa local en el paquete.
* En relación a este último punto, se eliminó los datos almacenados de manera local en el paquete, dado que con la función `obtener_datos()` se puede acceder a una versión actualizada de ellos, eventualmente se recuperarán este modalidad cuando se disponga de una base de datos final.

# labinstrumentos 0.0.0.9010

* Se agrega función `crear_sankey()`, que facilita la creación de diagramas Sankey.

# labinstrumentos 0.0.0.9001

* Se incluyó argumento `vertex.cex` en la función `grafico_red_circular()` para personalizar el tamaño de los nodos.
* Se eliminó el argumento `main` de la función `grafico_red_hubs()`.
* Se mejora el proceso de limpieza de los datos ([ver script](https://github.com/SEREMICTCI/labinstrumentos/blob/master/data-raw/lab_instrumentos.R)) utilizando funciones vectorizadas para mejorar los tiempos de computación. Del mismo modo se notan mejoras en el resultado final, eliminando stopWords que antes no se podían eliminar con facilidad.
* Corrección de documentación de las funciones de creación de análisis de comunidades.
* Uso de `lifecycle` para la declaración de funciones experimentales en la documentación de las funciones.

# labinstrumentos 0.0.0.9000

* Se mejora la estética del sitio web inicial.
* Se crean dos funciones para el análisis de comunidades basados en el algoritmo de optimización 'greedy': `red_comunidades_greedy()`; y el algoritmo Spinglass: `red_comunidades_spinglass()`.
* Se crean dos funciones para la visualización de redes usando un layout circular: `grafico_red_circular()`; y el score de *Hubs*: `grafico_red_hubs()`.
* se crea una función para la creación de redes: `crear_redes_de_palabras()`.
* Se añadió archivo `NEWS.md` para rastrear los cambios del paquete.