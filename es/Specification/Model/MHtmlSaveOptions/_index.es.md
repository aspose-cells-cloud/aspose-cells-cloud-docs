---
title: MHtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/mhtmlsaveoptions/
description: "Aspose.Cells Especificación del modelo de nube: MHtmlSaveOptions. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
weight: 50
---
## **mHtmlSaveOptions**

 Representa opciones para guardar el archivo .mhtml.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Directorio de archivos adjuntos| Cadena| Verdadero| FALSO|| El directorio en el que se guardarán los archivos adjuntos. Solo para guardar en secuencia html.|
| Prefijo de URL de archivos adjuntos| Cadena| Verdadero| FALSO||Especifique el prefijo de URL de los archivos adjuntos, como la imagen, en el archivo html. Solo para guardar en secuencia html.|
| Codificación| Cadena| Verdadero| FALSO|| Si no está configurado, utilice Encoding.UTF8 como tipo de codificación predeterminado.|
| Exportar solo hoja de trabajo activa| Booleano| Verdadero| FALSO|| Indica si se exporta todo el libro a un archivo html.|
| Exportar formato de imagen de gráfico| Cadena| Verdadero| FALSO|| Obtenga o establezca el formato de la imagen del gráfico antes de exportar|
| Exportar Imágenes Como Base64| Booleano| Verdadero| FALSO|| Especifica si las imágenes se guardan en formato Base64 en HTML, MHTML o EPUB.|
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