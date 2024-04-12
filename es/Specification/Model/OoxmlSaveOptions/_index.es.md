---
title: OoxmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/ooxmlsaveoptions/
description: "Aspose.Cells Especificación del modelo de nube: OoxmlSaveOptions. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
weight: 50
---
## **ooxmlGuardarOpciones**

 Representa opciones para guardar el archivo ooxml.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Exportar nombre de celda| Booleano| Verdadero| FALSO||Indica si se exporta el nombre de la celda al archivo Excel2007 .xlsx (.xlsm, .xltx, .xltm). Si SQL Server DTS puede acceder al archivo de salida, este valor debe ser verdadero. Establecer el valor en falso aumentará considerablemente el rendimiento y reducirá el tamaño del archivo al crear archivos grandes. El valor predeterminado es falso.|
| ActualizarZoom| Booleano| Verdadero| FALSO|| Indica si se actualiza el factor de escala antes de guardar el archivo si las propiedades PageSetup.FitToPagesWide y PageSetup.FitToPagesTall controlan cómo se escala la hoja de cálculo.|
| HabilitarZip64| Booleano| Verdadero| FALSO|| Utilice siempre extensiones ZIP64 al escribir archivos zip, incluso cuando no sean necesarias.|
| InsertarOoxmlAsOleObject| Booleano| Verdadero| FALSO|| Indica si se incrustan archivos Ooxml de OleObject como objeto OLE.|
| Tipo de compresión| Cadena| Verdadero| FALSO|| Obtiene y establece el tipo de compresión del archivo ooxml.|
| Guardar formato| Cadena| Verdadero| FALSO|||
| Carpeta de archivos en caché| Cadena| Verdadero| FALSO|||
| Borrar datos| Booleano| Verdadero| FALSO|||
| Crear directorio| Booleano| Verdadero| FALSO|||
| Habilitar compresión HTTP| Booleano| Verdadero| FALSO|||
| Actualizar caché de gráficos| Booleano| Verdadero| FALSO|||
|Ordenar nombres| Booleano| Verdadero| FALSO|||
| Validar áreas fusionadas| Booleano| Verdadero| FALSO|||

**Nombre del padre** : (GuardarOpciones)[guardaropciones]