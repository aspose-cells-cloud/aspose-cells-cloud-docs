---
title: Carbonizarse
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/chart/
description: "Aspose.Cells Especificación del modelo de nube: Tabla. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, hoja de cálculo, nube REST API, gráfico
weight: 50
---
## **cuadro**

 Encapsula el objeto que representa un único gráfico Excel.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Escala automática| Booleano| Verdadero| FALSO|| Verdadero si Microsoft Excel escala un gráfico 3D para que tenga un tamaño más cercano al gráfico 2D equivalente. La propiedad RightAngleAxes debe ser True.|
| Pared posterior| Clase:Paredes| Verdadero| FALSO|| Devuelve un objeto que representa la pared posterior de un gráfico 3D.|
| CategoríaEje| Clase:Eje| Verdadero| FALSO|| Obtiene el eje X del gráfico.|
| Área del gráfico| Clase:Área del gráfico| Verdadero| FALSO|| Obtiene el área del gráfico en la hoja de cálculo.|
| Tabla de datos del gráfico| Clase: Tabla de datos del gráfico| Verdadero| FALSO|| Representa la tabla de datos del gráfico.|
| Objeto gráfico| Clase: elemento de enlace| Verdadero| FALSO|| Representa la forma del gráfico;|
| Porcentaje de profundidad| Entero| Verdadero| FALSO||Representa la profundidad de un gráfico 3D como porcentaje del ancho del gráfico (entre 20 y 2000 por ciento).|
| Elevación| Entero| Verdadero| FALSO|| Representa la elevación de la vista del gráfico 3D, en grados.|
| Primer ángulo de corte| Entero| Verdadero| FALSO|| Obtiene o establece el ángulo del primer gráfico circular o de anillos, en grados (en el sentido de las agujas del reloj desde la vertical). Se aplica solo a gráficos circulares, circulares 3D y de anillos, de 0 a 360.|
| Piso| Clase: Piso| Verdadero| FALSO|| Devuelve un objeto que representa las paredes de un gráfico 3D.|
| Profundidad de la brecha| Entero| Verdadero| FALSO|| Obtiene o establece la distancia entre las series de datos en un gráfico 3D, como porcentaje del ancho del marcador. El valor de esta propiedad debe estar entre 0 y 500.|
| Anchura de rendija| Entero| Verdadero| FALSO|| Devuelve o establece el espacio entre grupos de barras o columnas, como porcentaje del ancho de la barra o columna. El valor de esta propiedad debe estar entre 0 y 500.|
| AlturaPorcentaje| Entero| Verdadero| FALSO||Devuelve o establece la altura de un gráfico 3D como porcentaje del ancho del gráfico (entre 5 y 500 por ciento).|
| Ocultar botones de campo dinámico| Booleano| Verdadero| FALSO|| Indica si se ocultan los botones del campo del gráfico dinámico solo cuando el gráfico es un gráfico dinámico.|
| es3D| Booleano| Verdadero| FALSO|| Indica si el gráfico es un gráfico 3D.|
| EsRectangularAcorralado| Booleano| Verdadero| FALSO|| Obtiene o establece un valor que indica si el área del gráfico tiene esquinas rectangulares. El valor predeterminado es verdadero.|
| Leyenda| Clase: Leyenda| Verdadero| FALSO|| Obtiene la leyenda del gráfico.|
| Nombre| Cadena| Verdadero| FALSO|| Representa el nombre del gráfico.|
| Serie N| Clase: Artículos de serie| Verdadero| FALSO|| Obtiene una colección que representa la serie de datos del gráfico.|
| Configuración de página| Clase: elemento de enlace| Verdadero| FALSO|| Representa la descripción de configuración de página en este gráfico.|
| Perspectiva| Entero| Verdadero| FALSO|| Devuelve o establece la perspectiva de la vista del gráfico 3D. Debe estar entre 0 y 100. Esta propiedad se ignora si la propiedad RightAngleAxes es True.|
| Fuente dinámica| Cadena| Verdadero| FALSO||La fuente son los datos de la tabla dinámica. Si PivotSource no está vacío, el gráfico es PivotChart.|
| Colocación| Cadena| Verdadero| FALSO|| Representa la forma en que el gráfico se adjunta a las celdas debajo de él.|
| Área de parcela| Clase:Áreadetrama| Verdadero| FALSO|| Obtiene el área de trazado del gráfico que incluye etiquetas de marcas de eje.|
| Trazar tipo de celdas vacías| Cadena| Verdadero| FALSO|| Obtiene y establece cómo trazar las celdas vacías.|
| TrazarCélulasVisibles| Booleano| Verdadero| FALSO|| Indica si solo se trazan las celdas visibles.|
| Tamaño de impresión| Cadena| Verdadero| FALSO|| Obtiene y establece el tamaño del gráfico impreso.|
| Ejes De Ángulo Recto| Booleano| Verdadero| FALSO|| Verdadero si los ejes del gráfico están en ángulo recto. Se aplica solo a gráficos 3D (excepto gráficos circulares 3D y columnas 3D).|
| Ángulo de rotación| Entero| Verdadero| FALSO|| Representa la rotación de la vista del gráfico 3D (la rotación del área de trazado alrededor del eje z, en grados).|
| Eje de segunda categoría| Clase: elemento de enlace| Verdadero| FALSO|| Obtiene el segundo eje X del gráfico.|
| Segundo eje de valor| Clase: elemento de enlace| Verdadero| FALSO|| Obtiene el segundo eje Y del gráfico.|
| SerieEje| Clase: elemento de enlace| Verdadero| FALSO|| Obtiene el eje de la serie del gráfico.|
| formas| Clase: elemento de enlace| Verdadero| FALSO|| Devuelve todas las formas de dibujo en este gráfico.|
|Mostrar tabla de datos| Booleano| Verdadero| FALSO|| Obtiene o establece un valor que indica si el gráfico muestra una tabla de datos.|
| Mostrar leyenda| Booleano| Verdadero| FALSO|| Obtiene o establece un valor que indica si se mostrará la leyenda del gráfico. El valor predeterminado es verdadero.|
| Pared lateral| Clase: elemento de enlace| Verdadero| FALSO|| Devuelve un objeto que representa la pared lateral de un gráfico 3D.|
| TamañoConVentana| Booleano| Verdadero| FALSO|| Verdadero si Microsoft Excel cambia el tamaño del gráfico para que coincida con el tamaño de la ventana de la hoja del gráfico.|
| Estilo| Entero| Verdadero| FALSO|| Obtiene y establece el estilo integrado.|
| Título| Clase: elemento de enlace| Verdadero| FALSO|| Representa el título del gráfico.|
| Tipo| Cadena| Verdadero| FALSO|| Representa el tipo de gráfico.|
| Eje de valor| Clase:Eje| Verdadero| FALSO|| Obtiene el eje Y del gráfico.|
| Paredes| Clase: elemento de enlace| Verdadero| FALSO|| Devuelve un objeto que representa las paredes de un gráfico 3D.|
| Paredes y líneas de cuadrícula 2D| Booleano| Verdadero| FALSO|| Verdadero si las líneas de cuadrícula se dibujan en dos dimensiones en un gráfico 3D.|
| enlace| Clase: enlace| Verdadero| FALSO|||

**Nombre del padre** : [Elemento de enlace](/specification/model/linkelement)

