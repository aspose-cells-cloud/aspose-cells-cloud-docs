---
title: OpciónGuardarImagen
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/imagesaveoptions/
description: "Aspose.Cells Especificación del modelo de nube: ImageSaveOptions. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Nube REST API, ImageSaveOptions
weight: 50
---
## **OpcionesGuardarImagen**

 Representa opciones para guardar archivos de imagen.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Tipo de imagen de gráfico| Cadena| Verdadero| FALSO|| Indique el tipo de imagen del gráfico al realizar la conversión.|
| ImagenIncrustadaNombreEnSvg| Cadena| Verdadero| FALSO|| Indique el nombre del archivo de la imagen incrustada en svg. Esta debería ser la ruta completa con un directorio como "c:\\xpsEmbeded"|
| Resolucion horizontal| Entero| Verdadero| FALSO|| Obtiene o establece la resolución horizontal de las imágenes generadas, en puntos por pulgada. Aplica el método de generación de imágenes excepto imágenes en formato Emf. El valor predeterminado es 96.|
| Formato de imagen| Cadena| Verdadero| FALSO|| Obtiene o establece el formato de las imágenes generadas. No aplique el método que devuelve un objeto Bitmap. El valor predeterminado es ImageFormat.Bmp. No aplique el método que devuelve un objeto Bitmap.|
| IsCellAutoFit| Booleano| Verdadero| FALSO|| Indica si el ancho y el alto de las celdas se ajustan automáticamente según el valor de la celda. El valor predeterminado es falso.|
| Una página por hoja| Booleano| Verdadero| FALSO||Si OnePagePerSheet es verdadero, todo el contenido de una hoja se generará en una sola página. El tamaño del papel de configuración de página no será válido y las demás configuraciones de configuración de página seguirán teniendo efecto.|
| Área única| Booleano| Verdadero| FALSO|| Si esta propiedad es verdadera, solo se generará un área y no se aplicará ninguna escala.|
| Página de impresión| Cadena| Verdadero| FALSO|| Indica qué páginas no se imprimirán.|
| Imprimir con cuadro de diálogo de estado| Booleano| Verdadero| FALSO|| Si PrintWithStatusDialog = true, habrá un cuadro de diálogo que muestra el estado de impresión actual. de lo contrario, no se mostrará ningún cuadro de diálogo de este tipo.|
| Calidad| Entero| Verdadero| FALSO|| Obtiene o establece un valor que determina la calidad de las imágenes generadas para aplicarlas solo al guardar páginas en formato Jpeg. Tiene efecto solo al guardar en JPEG. El valor debe estar entre 0 y 100. El valor predeterminado es 100.|
| Compresión Tiff| Cadena| Verdadero| FALSO|| Obtiene o establece el tipo de compresión que se aplicará sólo al guardar páginas en formato Tiff. Tiene efecto sólo al guardar en TIFF. El valor predeterminado es Lzw.|
| Resolución vertical| Entero| Verdadero| FALSO||Obtiene o establece la resolución vertical de las imágenes generadas, en puntos por pulgada. Aplica el método de generación de imágenes excepto la imagen en formato Emf. El valor predeterminado es 96.|
| Guardar formato| Cadena| Verdadero| FALSO|||
| Carpeta de archivos en caché| Cadena| Verdadero| FALSO|||
| Borrar datos| Booleano| Verdadero| FALSO|||
| Crear directorio| Booleano| Verdadero| FALSO|||
| Habilitar compresión HTTP| Booleano| Verdadero| FALSO|||
| Actualizar caché de gráficos| Booleano| Verdadero| FALSO|||
| Ordenar nombres| Booleano| Verdadero| FALSO|||
| Validar áreas fusionadas| Booleano| Verdadero| FALSO|||

**Nombre del padre** : [Guardar Opciones](/specification/model/saveoptions)

