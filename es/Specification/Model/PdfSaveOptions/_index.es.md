---
title: OpciónGuardarPdf
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/pdfsaveoptions/
description: "Aspose.Cells Especificación del modelo de nube: PdfSaveOptions. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
weight: 50
---
## **pdfGuardarOpciones**

 Representa opciones para guardar un archivo pdf.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Mostrar título del documento| Booleano| Verdadero| FALSO|| Indica si la barra de título de la ventana debe mostrar el título del documento.|
| ExportarDocumentoEstructura| Booleano| Verdadero| FALSO|| Indica si se exporta la estructura del documento.|
| EmfRenderConfiguración| Cadena| Verdadero| FALSO|| Configuración para renderizar el metarchivo Emf.|
| Exportación de propiedades personalizadas| Cadena| Verdadero| FALSO|| Especifica la forma en que se exportan CustomDocumentPropertyCollection al archivo PDF.|
| Tipo de optimización| Cadena| Verdadero| FALSO|| Obtiene y establece el tipo de optimización de pdf.|
| Productor| Cadena| Verdadero| FALSO|| Obtiene y establece el productor del documento pdf generado.|
| Compresión PDF| Cadena| Verdadero| FALSO||Indique el algoritmo de compresión.|
| Codificación de fuentes| Cadena| Verdadero| FALSO|| Obtiene o establece la codificación de fuentes incrustadas en pdf.|
| Filigrana| Clase:RepresentaciónMarca de agua| Verdadero| FALSO|| Obtiene o establece una marca de agua para la salida.|
| CalcularFórmula| Booleano| Verdadero| FALSO|| Indica si se calculan las fórmulas antes de guardar el archivo pdf. El valor predeterminado es falso.|
| Comprobar compatibilidad de fuentes| Booleano| Verdadero| FALSO|| Indica si se debe comprobar la compatibilidad de fuentes para cada carácter del texto. El valor por defecto es verdadero. Deshabilitar esta propiedad puede brindar un mejor rendimiento. Pero cuando la fuente de texto/carácter predeterminada o especificada no se puede utilizar para representarlo, es posible que aparezcan caracteres ilegibles (como un bloque) en el pdf generado. En tal situación, el usuario debe mantener esta propiedad como verdadera para poder buscar y utilizar fuentes alternativas para representar el texto;|
| Cumplimiento| Cadena| Verdadero| FALSO|| El libro de trabajo se convierte a PDF de acuerdo con PdfCompliance en esta propiedad.|
| Fuente predeterminada| Cadena| Verdadero| FALSO||Cuando los caracteres en Excel son Unicode y no están configurados con la fuente correcta en el estilo de celda, pueden aparecer como un bloque en una imagen en PDF. Configure la fuente predeterminada, como MingLiu o MS Gothic, para mostrar estos caracteres. Si esta propiedad no está configurada, Aspose.Cells utilizará la fuente predeterminada del sistema para mostrar estos caracteres Unicode.|
| Una página por hoja| Booleano| Verdadero| FALSO|| Si OnePagePerSheet es verdadero, todo el contenido de una hoja se generará en una sola página. El tamaño del papel de configuración de página no será válido y las demás configuraciones de configuración de página seguirán teniendo efecto.|
| Tipo de página de impresión| Cadena| Verdadero| FALSO|| Indica qué páginas no se imprimirán.|
| Opciones de seguridad| Clase:PdfSecurityOptions| Verdadero| FALSO|| Configure estas opciones cuando se necesite seguridad en el resultado de xls2pdf.|
| PPI deseado| Entero| Verdadero| FALSO||Establezca el PPI (píxeles por pulgada) deseado de las imágenes de remuestreo y la calidad jpeg. Todas las imágenes se convertirán a JPEG con la configuración de calidad especificada y se volverán a muestrear las imágenes que sean mayores que el PPI (píxeles por pulgada) especificado. Píxeles por pulgada deseados. 220 de alta calidad. Calidad de pantalla 150. 96 calidad de correo electrónico.|
| calidad JPEG| Entero| Verdadero| FALSO|| Establezca el PPI (píxeles por pulgada) deseado de las imágenes de remuestreo y la calidad jpeg. Todas las imágenes se convertirán a JPEG con la configuración de calidad especificada y se volverán a muestrear las imágenes que sean mayores que el PPI (píxeles por pulgada) especificado. 0 - 100% JPEG calidad.|
| Tipo de imagen| Cadena| Verdadero| FALSO|| Representa el tipo de imagen al convertir el gráfico y la forma.|
| Guardar formato| Cadena| Verdadero| FALSO|||
| Carpeta de archivos en caché| Cadena| Verdadero| FALSO|||
| Borrar datos| Booleano| Verdadero| FALSO|||
| Crear directorio| Booleano| Verdadero| FALSO|||
| Habilitar compresión HTTP| Booleano| Verdadero| FALSO|||
| Actualizar caché de gráficos| Booleano| Verdadero| FALSO|||
|Ordenar nombres| Booleano| Verdadero| FALSO|||
| Validar áreas fusionadas| Booleano| Verdadero| FALSO|||

**Nombre del padre** : (GuardarOpciones)[guardaropciones]