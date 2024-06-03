---
title: Serie
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/series/
description: "Aspose.Cells Especificación del modelo de nube: Serie. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Cloud REST API, Serie
weight: 50
---
## **serie**

 Encapsula el objeto que representa una única serie de datos en un gráfico.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Área| Clase:Área| Verdadero| FALSO|| Representa el área de fondo del objeto Serie.|
| Tipo de forma de barra 3D| Cadena| Verdadero| FALSO|| Obtiene o establece el tipo de forma 3D utilizado con el gráfico de columnas o barras 3D.|
| Borde| Clase: Línea| Verdadero| FALSO|| Representa el borde del objeto Serie.|
| Escala de burbujas| Entero| Verdadero| FALSO||Obtiene o establece el factor de escala de las burbujas en el grupo de gráficos especificado. Puede ser un valor entero de 0 (cero) a 300, correspondiente a un porcentaje del tamaño predeterminado. Se aplica únicamente a los gráficos de burbujas.|
| Tamaños de burbujas| Cadena| Verdadero| FALSO|| Obtiene o establece los valores del tamaño de las burbujas de la serie de gráficos.|
| Recuento de valores de datos| Entero| Verdadero| FALSO|| Obtiene el número de valores de datos.|
| Etiquetas de datos| Clase:Etiquetas de datos| Verdadero| FALSO|| Representa el objeto DataLabels para la ASeries especificada.|
| Nombre para mostrar| Cadena| Verdadero| FALSO|| Obtiene el nombre de la serie que se muestra en el gráfico.|
| Tamaño Del Agujero| Entero| Verdadero| FALSO|| Devuelve o establece el tamaño del agujero en un grupo de gráficos de anillos. El tamaño del agujero se expresa como un porcentaje del tamaño del gráfico, entre el 10 y el 90 por ciento.|
| Barras abajo| Clase: barras de caída| Verdadero| FALSO|| Devuelve un objeto que representa las barras hacia abajo en un gráfico de líneas. Se aplica solo a gráficos de líneas.|
| Líneas de caída| Clase: Línea| Verdadero| FALSO||Devuelve un objeto que representa las líneas de colocación de una serie en el gráfico de líneas o de áreas. Se aplica solo a gráficos de líneas o de áreas.|
| Explosión| Entero| Verdadero| FALSO|| La distancia de un sector circular abierto desde el centro del gráfico circular se expresa como porcentaje del diámetro circular.|
| Primer ángulo de corte| Entero| Verdadero| FALSO|| Obtiene o establece el ángulo del primer gráfico circular o de anillos, en grados (en el sentido de las agujas del reloj desde la vertical). Se aplica solo a gráficos circulares, circulares 3D y de anillos, de 0 a 360.|
| Anchura de rendija| Entero| Verdadero| FALSO|| Devuelve o establece el espacio entre grupos de barras o columnas, como porcentaje del ancho de la barra o columna. El valor de esta propiedad debe estar entre 0 y 500.|
| Tiene efecto 3DE| Booleano| Verdadero| FALSO|| Verdadero si la serie tiene apariencia tridimensional. Se aplica únicamente a los gráficos de burbujas.|
| TieneDropLines| Booleano| Verdadero| FALSO|| Verdadero si el gráfico tiene líneas desplegables. Se aplica solo a gráficos de líneas o de áreas.|
| HasHiLoLines| Booleano| Verdadero| FALSO|| Verdadero si el gráfico de líneas tiene líneas altas y bajas. Se aplica solo a gráficos de líneas.|
| Tiene líneas de líder| Booleano| Verdadero| FALSO|| Verdadero si la serie tiene líneas guía.|
| TieneRadarAxisLabels| Booleano| Verdadero| FALSO|| Verdadero si un gráfico de radar tiene etiquetas de eje de categorías. Se aplica sólo a cartas de radar.|
| TieneSeriesLineas| Booleano| Verdadero| FALSO||Verdadero si un gráfico de columnas apiladas o de barras tiene líneas de serie o si un gráfico circular o de barras tiene líneas conectoras entre las dos secciones. Se aplica solo a gráficos de columnas apiladas, gráficos de barras, gráficos circulares o gráficos circulares de barras.|
| Tiene barras arriba y abajo| Booleano| Verdadero| FALSO|| Verdadero si un gráfico de líneas tiene barras hacia arriba y hacia abajo. Se aplica solo a gráficos de líneas.|
| HolaLoLines| Clase: Línea| Verdadero| FALSO|| Devuelve un objeto HiLoLines que representa las líneas altas y bajas de una serie en un gráfico de líneas. Se aplica solo a gráficos de líneas.|
| EsAutoSplit| Booleano| Verdadero| FALSO|| Indica si el valor del umbral es automático.|
| EsColorVariado| Booleano| Verdadero| FALSO|| Representa si se varía el color de los puntos. El gráfico debe contener sólo una serie.|
| Líneas guía| Clase: Línea| Verdadero| FALSO||Representa líneas guía en un gráfico. Las líneas guía conectan etiquetas de datos con puntos de datos. Este objeto no es una colección; no hay ningún objeto que represente una única línea guía.|
| Entrada de leyenda| Clase:Entrada de leyenda| Verdadero| FALSO|| Obtiene la entrada de leyenda según esta serie.|
| Marcador| Clase: marcador| Verdadero| FALSO|| Obtiene el marcador.|
| Nombre| Cadena| Verdadero| FALSO|| Obtiene o establece el nombre de la serie de datos.|
| Superposición| Entero| Verdadero| FALSO|| Especifica cómo se colocan las barras y columnas. Puede ser un valor entre – 100 y 100. Se aplica solo a gráficos de barras y columnas 2D.|
| Trazar en el segundo eje| Booleano| Verdadero| FALSO|| Indica si esta serie se traza en el segundo eje de valores.|
| Puntos| Clase: elemento de enlace| Verdadero| FALSO|| Obtiene la colección de puntos de una serie en un gráfico.|
| Segundo tamaño de parcela| Entero| Verdadero| FALSO|| Devuelve o establece el tamaño de la sección secundaria de un gráfico circular o de barras, como porcentaje del tamaño del gráfico circular principal. Puede ser un valor de 5 a 200.|
| SerieLíneas| Clase: Línea| Verdadero| FALSO||Devuelve un objeto SeriesLines que representa las líneas de serie de un gráfico de barras apiladas o un gráfico de columnas apiladas. Se aplica solo a gráficos de barras y columnas apiladas.|
| Sombra| Booleano| Verdadero| FALSO|| Verdadero si la serie tiene una sombra.|
| Mostrar burbujas negativas| Booleano| Verdadero| FALSO|| Verdadero si se muestran burbujas negativas para el grupo de gráficos. Válido sólo para gráficos de burbujas.|
| TamañoRepresenta| Cadena| Verdadero| FALSO|| Obtiene o establece lo que representa el tamaño de la burbuja en un gráfico de burbujas.|
| Liso| Booleano| Verdadero| FALSO|| Representa el suavizado de curvas. Verdadero si el suavizado de curvas está activado para el gráfico de líneas o el gráfico de dispersión. Se aplica solo a gráficos de líneas y de dispersión conectados por líneas.|
| Dividido| Cadena| Verdadero| FALSO|| Devuelve o establece un valor que permite determinar qué puntos de datos están en el segundo pastel o barra de un gráfico circular o de barras.|
| Valor dividido| Flotante| Verdadero| FALSO||Devuelve o establece un valor que se utilizará para determinar qué puntos de datos están en el segundo pastel o barra de un gráfico circular o de barras.|
| Líneas de tendencia| Clase: líneas de tendencia| Verdadero| FALSO|| Devuelve un objeto que representa una colección de todas las líneas de tendencia de la serie.|
| Tipo| Cadena| Verdadero| FALSO|| Obtiene o establece el tipo de una serie de datos.|
| Barras arriba| Clase: barras de caída| Verdadero| FALSO|| Devuelve un objeto DropBars que representa las barras ascendentes en un gráfico de líneas. Se aplica solo a gráficos de líneas.|
| Valores| Cadena| Verdadero| FALSO|| Representa los datos de la serie de gráficos.|
| Barra de errores X| Clase: barra de errores| Verdadero| FALSO|| Representa la barra de error de dirección X de la serie.|
| Valores XV| Cadena| Verdadero| FALSO|| Representa los valores x de la serie de gráficos.|
| Barra de errores| Clase: barra de errores| Verdadero| FALSO|| Representa la barra de error de dirección Y de la serie.|
| enlace| Clase: enlace| Verdadero| FALSO|||

**Nombre del padre** : [Elemento de enlace](/specification/model/linkelement)

