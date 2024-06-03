---
title: forma
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/shape/
description: "Aspose.Cells Especificación del modelo de nube: Forma. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Nube REST API, Forma
weight: 50
---
## **forma**

 Representa el objeto msodrawing.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Nombre| Cadena| Verdadero| FALSO|| Obtiene y establece el nombre de la forma.|
| Tipo de dibujo Mso| Cadena| Verdadero| FALSO|| Obtiene el tipo de dibujo mso.|
| Tipo de autoforma| Cadena| Verdadero| FALSO|| Obtiene y establece el tipo de forma automática.|
| Colocación| Cadena| Verdadero| FALSO|| Representa la forma en que el objeto de dibujo se adjunta a las celdas debajo de él. La propiedad controla la ubicación de un objeto en una hoja de trabajo.|
| Fila superior izquierda| Entero| Verdadero| FALSO|| Representa el índice de la fila de la esquina superior izquierda.|
| Arriba| Entero| Verdadero| FALSO|| Representa el desplazamiento vertical de la forma desde su fila superior, en unidades de píxeles.|
| Columna superior izquierda| Entero| Verdadero| FALSO|| Representa el índice de la columna de la esquina superior izquierda.|
| Izquierda| Entero| Verdadero| FALSO|| Representa el desplazamiento horizontal de la forma desde su columna izquierda, en unidades de píxeles.|
| Fila inferior derecha| Entero| Verdadero| FALSO|| Representa el índice de la fila de la esquina inferior derecha.|
| Abajo| Entero| Verdadero| FALSO||Representa el ancho del desplazamiento vertical de la forma desde la fila de la esquina inferior inferior, en unidades de píxeles.|
| Columna inferior derecha| Entero| Verdadero| FALSO|| Representa el índice de la columna de la esquina inferior derecha.|
| Bien| Entero| Verdadero| FALSO|| Representa el ancho del desplazamiento horizontal de la forma desde la columna de la esquina inferior derecha, en unidades de píxeles.|
| Ancho| Entero| Verdadero| FALSO|| Representa el ancho de la forma, en unidades de píxeles.|
| Altura| Entero| Verdadero| FALSO|| Representa la altura de la forma, en unidades de píxel.|
| X| Entero| Verdadero| FALSO|| Obtiene y establece el desplazamiento horizontal de la forma desde el borde izquierdo de la hoja de cálculo, en unidades de píxeles.|
| Y| Entero| Verdadero| FALSO|| Obtiene y establece el desplazamiento vertical de la forma desde el borde superior de la hoja de cálculo, en unidades de píxeles.|
| Ángulo de rotación| Flotante| Verdadero| FALSO|| Obtiene y establece la rotación de la forma.|
|Texto HTML| Cadena| Verdadero| FALSO|| Obtiene y establece la cadena html que contiene datos y algunos formatos en este cuadro de texto.|
| Texto| Cadena| Verdadero| FALSO|| Representa la cadena en este objeto TextBox.|
| Texto alternativo| Cadena| Verdadero| FALSO|| Devuelve o establece la cadena de texto descriptivo (alternativo) del objeto.|
| TextoAlineaciónHorizontal| Cadena| Verdadero| FALSO|| Obtiene y establece el tipo de alineación horizontal del texto de la forma.|
| TextoHorizontalDesbordamiento| Cadena| Verdadero| FALSO|| Obtiene y establece el tipo de desbordamiento horizontal de texto de la forma que contiene texto.|
| Tipo de orientación de texto| Cadena| Verdadero| FALSO||Obtiene y establece el tipo de orientación del texto de la forma.|
| TextoAlineaciónVertical| Cadena| Verdadero| FALSO|| Obtiene y establece el tipo de alineación vertical del texto de la forma.|
| TextoVerticalDesbordamiento| Cadena| Verdadero| FALSO|| Obtiene y establece el tipo de desbordamiento vertical de texto de la forma que contiene texto.|
| esgrupo| Booleano| Verdadero| FALSO|| Indica si la forma es un grupo.|
| Está oculto| Booleano| Verdadero| FALSO|| Indica si el objeto es visible.|
| IsLockAspectRatio| Booleano| Verdadero| FALSO|| Verdadero significa que no permite cambios en la relación de aspecto.|
| Está bloqueado| Booleano| Verdadero| FALSO|| Verdadero si el objeto está bloqueado, Falso si el objeto se puede modificar cuando la hoja está protegida.|
| Es imprimible| Booleano| Verdadero| FALSO|| Verdadero si el objeto es imprimible|
| Está envuelto en texto| Booleano| Verdadero| FALSO|| Obtiene y establece el tipo de texto ajustado de la forma que contiene texto.|
| esWordArt| Booleano| Verdadero| FALSO|| Indica si esta forma es un arte de palabras.|
| celda vinculada| Cadena| Verdadero| FALSO|| Obtiene o establece el rango de la hoja de cálculo vinculado al valor del control.|
| Posición de orden Z| Entero| Verdadero| FALSO|| Devuelve la posición de una forma en el orden z.|
| Fuente| Clase:Fuente| Verdadero| FALSO|| Representa la fuente de la forma.|
| Hipervínculo| Cadena| Verdadero| FALSO|| Obtiene el hipervínculo de la forma.|
| enlace| Clase: enlace| Verdadero| FALSO|||

**Nombre del padre** : [Elemento de enlace](/specification/model/linkelement)

**Nombre de los niños** : 
	-  [Forma de arco](arcshape) 
	-  [Autoforma](autoshape) 
	-  [Botón](button) 
	-  [CélulasDibujo](cellsdrawing) 
	-  [Caja](checkbox) 
	-  [Caja combo](combobox) 
	-  [ComentarioForma](commentshape) 
	-  [Forma](form) 
	-  [Cuadro de grupo](groupbox) 
	-  [Forma de grupo](groupshape) 
	-  [Etiqueta](label) 
	-  [Forma de línea](lineshape) 
	-  [Cuadro de lista](listbox) 
	-  [Objeto OLE](oleobject) 
	-  [Oval](oval) 
	-  [Imagen](picture) 
	-  [Boton de radio](radiobutton) 
	-  [Forma rectangular](rectangleshape) 
	-  [Barra de desplazamiento](scrollbar) 
	-  [Hilandero](spinner) 
	-  [Caja de texto](textbox) 
	-  [Forma del gráfico](chartshape) 
