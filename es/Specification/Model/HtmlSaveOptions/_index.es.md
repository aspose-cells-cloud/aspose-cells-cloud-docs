---
title: Opción HTMLGuardar
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/htmlsaveoptions/
description: "Aspose.Cells Especificación del modelo de nube: HtmlSaveOptions. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
weight: 50
---
## **htmlGuardarOpciones**

 Representa opciones para guardar el archivo .html.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Exportar encabezados de página| Booleano| Verdadero| FALSO|||
| Exportar pies de página| Booleano| Verdadero| FALSO|||
| Exportar encabezados de columna de fila| Booleano| Verdadero| FALSO|||
| Mostrar todas las hojas| Booleano| Verdadero| FALSO|||
| Opciones de imagen| Clase: ImageOrPrintOptions| Verdadero| FALSO|||
| Guardar como archivo único| Booleano| Verdadero| FALSO|| Indica si se guarda el html como un solo archivo. El valor predeterminado es falso.|
| Exportar hoja de trabajo oculta| Booleano| Verdadero| FALSO|| Indica si se guarda el html como un solo archivo. El valor predeterminado es falso.|
| Exportar líneas de cuadrícula| Booleano| Verdadero| FALSO||Indicando si se exportan las líneas de la cuadrícula. El valor predeterminado es falso.|
| PresentaciónPreferencia| Booleano| Verdadero| FALSO|| Indica si el archivo html o mht es la preferencia de presentación. El valor predeterminado es falso. Si desea obtener una presentación más hermosa, establezca el valor en verdadero.|
| PrefijoCssCelda| Cadena| Verdadero| FALSO|| Obtiene y establece el prefijo del nombre CSS, el valor predeterminado es "".|
| TablaCssId| Cadena| Verdadero| FALSO|| Obtiene y establece el prefijo del nombre de tipo CSS, como tr,col,td, etc., que están contenidos en el elemento de tabla que tiene el atributo TableCssId específico. El valor predeterminado es "".|
| IsFullPathEnlace| Booleano| Verdadero| FALSO|| Indicando si se utiliza el enlace de ruta completa ensheet00x.htm,filelist.xml y tabstrip.htm. El valor predeterminado es falso.|
| Exportar hoja de trabajo CSS por separado| Booleano| Verdadero| FALSO|| Indicando si exportar la hoja de trabajo css por separado. El valor predeterminado es falso.|
| Exportar estilo de borde similar| Booleano| Verdadero| FALSO|||
| FusionarEmptyTdForcely| Booleano| Verdadero| FALSO||Indica si se debe fusionar el elemento TD vacío al exportar el archivo a html. El tamaño del archivo html se reducirá significativamente después de establecer el valor en verdadero. El valor predeterminado es falso. Si desea importar el archivo html para Excel o exportar líneas de cuadrícula perfectas al guardar el archivo en html, mantenga el valor predeterminado.|
| Exportar coordenadas de celda| Booleano| Verdadero| FALSO|| Indica si se exportan las coordenadas de Excel de celdas que no están en blanco al guardar el archivo en HTML. El valor predeterminado es falso. Si desea importar el HTML de salida a Excel, mantenga el valor predeterminado.|
| Exportar encabezados adicionales| Booleano| Verdadero| FALSO|| Indica si se exportan encabezados adicionales cuando la longitud del texto es mayor que la columna de visualización máxima. El valor predeterminado es falso. Si desea importar el archivo html a Excel, mantenga el valor predeterminado.|
| Exportar encabezados| Booleano| Verdadero| FALSO||Indica si se exportan encabezados al guardar el archivo en html. El valor predeterminado es falso. Si desea importar el archivo html a Excel, mantenga el valor predeterminado.|
| Fórmula de exportación| Booleano| Verdadero| FALSO|| Indica si se exporta la fórmula al guardar el archivo en html. El valor por defecto es verdadero. Si desea importar el HTML de salida a Excel, mantenga el valor predeterminado|
| Agregar texto de información sobre herramientas| Booleano| Verdadero| FALSO|| Indica si se agrega texto de información sobre herramientas cuando los datos no se pueden mostrar completamente.|
| ExportarBogusRowData| Booleano| Verdadero| FALSO|| Indicando si se exportan datos falsos de la fila inferior. El valor predeterminado es verdadero. Si desea importar el archivo html o mht a Excel, mantenga el valor predeterminado.|
| Excluir estilos no utilizados| Booleano| Verdadero| FALSO|| Indicando si se excluyen los estilos no utilizados. El valor predeterminado es falso. Si desea importar el archivo html o mht a Excel, mantenga el valor predeterminado.|
| Exportar propiedades del documento| Booleano| Verdadero| FALSO||Indicando si se exportan las propiedades del documento. El valor predeterminado es verdadero. Si desea importar el archivo html o mht a Excel, mantenga el valor predeterminado.|
| Exportar propiedades de la hoja de trabajo| Booleano| Verdadero| FALSO|| Indicando si se exportan las propiedades de la hoja de trabajo. El valor predeterminado es verdadero. Si desea importar el archivo html o mht a Excel, mantenga el valor predeterminado.|
| Exportar propiedades del libro de trabajo| Booleano| Verdadero| FALSO|| Indica si se exportan las propiedades del libro de trabajo. El valor predeterminado es verdadero. Si desea importar el archivo html o mht a Excel, mantenga el valor predeterminado.|
| ExportarFrameScriptsAndProperties| Booleano| Verdadero| FALSO|| Indica si se exportan scripts de marcos y propiedades del documento. El valor predeterminado es verdadero. Si desea importar el archivo html o mht a Excel, mantenga el valor predeterminado.|
| Directorio de archivos adjuntos| Cadena| Verdadero| FALSO|| El directorio en el que se guardarán los archivos adjuntos. Solo para guardar en secuencia html.|
| Prefijo de URL de archivos adjuntos| Cadena| Verdadero| FALSO||Especifique el prefijo de URL de los archivos adjuntos, como la imagen, en el archivo html. Solo para guardar en secuencia html.|
| Codificación| Cadena| Verdadero| FALSO|||
| Exportar solo hoja de trabajo activa| Booleano| Verdadero| FALSO|| Indica si se exporta todo el libro a un archivo html.|
| Exportar formato de imagen de gráfico| Cadena| Verdadero| FALSO|| Obtenga o establezca el formato de la imagen del gráfico antes de exportar|
| Exportar Imágenes Como Base64| Booleano| Verdadero| FALSO|||
| Tipo de visualización de col oculta| Cadena| Verdadero| FALSO|| Columna oculta (el ancho de esta columna es 0) en Excel, antes de guardarla en formato html, si HtmlHiddenColDisplayType es "Eliminar", la columna oculta no se generará, si el valor es "Oculto", la columna se generará. pero estaba oculto, el valor predeterminado es "Oculto"|
| Tipo de visualización de fila oculta| Cadena| Verdadero| FALSO||Fila oculta (la altura de esta fila es 0) en Excel, antes de guardarla en formato html, si HtmlHiddenRowDisplayType es "Eliminar", la fila oculta no se generará, si el valor es "Oculto", la fila se generará. pero estaba oculto, el valor predeterminado es "Oculto"|
| HtmlCrossStringTipo| Cadena| Verdadero| FALSO|| Indica si una cadena entre celdas se mostrará de la misma manera que MS Excel al guardar un archivo Excel en formato html. De forma predeterminada, el valor es Predeterminado, por lo que, para cadenas entre celdas, hay poca diferencia entre los archivos html creados por Aspose.Cells y MS Excel. Pero el rendimiento para crear archivos html grandes, estableciendo el valor en Cruz sería varias veces más rápido que configurándolo en Predeterminado o Fit2Cell.|
| IsExpImageToTempDir| Booleano| Verdadero| FALSO|| Indica si exportar archivos de imagen al directorio temporal. Solo para guardar en secuencia html.|
| Título de la página| Cadena| Verdadero| FALSO||El título de la página html. Solo para guardar en secuencia html.|
| AnalizarHtmlTagInCell| Booleano| Verdadero| FALSO|| Analizar la etiqueta html en la celda, como valor de celda o como etiqueta html, el valor predeterminado es verdadero|
| Guardar formato| Cadena| Verdadero| FALSO|||
| Carpeta de archivos en caché| Cadena| Verdadero| FALSO|||
| Borrar datos| Booleano| Verdadero| FALSO|||
| Crear directorio| Booleano| Verdadero| FALSO|||
| Habilitar compresión HTTP| Booleano| Verdadero| FALSO|||
| Actualizar caché de gráficos| Booleano| Verdadero| FALSO|||
|Ordenar nombres| Booleano| Verdadero| FALSO|||
| Validar áreas fusionadas| Booleano| Verdadero| FALSO|||

**Nombre del padre** : (GuardarOpciones)[guardaropciones]