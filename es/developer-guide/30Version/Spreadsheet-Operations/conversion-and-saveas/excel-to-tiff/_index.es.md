---
title: Excel a TIF
second_title: Documen
linketitle: Excel to Tif
type: docs
url: /es/convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/,/convert/excel-to-tiff/]
keywords: Convert excel files to tiff files
description: Aspose.Cells Cloud REST API admite la conversión de archivos Excel a TIFF. El SDK es compatible con varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 90
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Excel a TIFF
---
Este archivo de Excel REST API `saveas` a TIFF.

[POST /cells/{nombre}/guardar como](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API le permite guardar el archivo MS Excel como archivo TIFF con configuraciones adicionales y guardar el resultado en el almacenamiento.

Este archivo de Excel REST API `convert` a TIFF.

[PUT /celdas/convertir](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API le permite convertir el archivo MS Excel al archivo TIFF con configuraciones adicionales y guardar el resultado en la respuesta.

Este archivo de Excel REST API `export` a TIFF.

[OBTENER /células/{nombre}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API le permite convertir el archivo MS Excel al archivo TIFF con configuraciones adicionales y guardar el resultado en la respuesta.

## RESTO API

|**API**|**Tipo**|**Descripción**|**Enlace Swagger**|
|:- |:- |:- |:- |
|/células/convertir|PONER|Convierte el libro de trabajo del contenido de la solicitud a algún formato|[PonerConvertirLibroDeTrabajo](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|
|/células/{nombre}|CONSEGUIR|Exporta el libro de trabajo a otro formato.|[Obtener libro de trabajo](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|
|/cells/{nombre}/guardar como|CORREO|Exportar libro de trabajo a formato|[Guardar como después del documento](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

Estas API definen una interfaz de programación de acceso público y le permiten realizar interacciones REST directamente desde un navegador web.

 Puedes utilizar**cURL** Herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
-X PUT \
-d {"File":{}} \
-H "Content-Type:  multipart/form-data" \
-H "Accept:  multipart/form-data" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
-X POST \
-d "{'SaveFormat':'tiff', 'ImageFormat': 'tiff'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=html" \
-X GET \
-d "{'SaveFormat':'tiff', 'ExportImagesAsBase64': 'true'}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}
{{< /tabs >}}

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}
