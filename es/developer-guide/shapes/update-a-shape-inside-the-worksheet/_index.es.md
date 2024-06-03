---
title: Actualizar una forma en una hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Actualizar
type: docs
url: /es/shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: Update a shape on an Excel workshee
description: Aspose.Cells Cloud REST API admite la actualización de una forma en una hoja de trabajo Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 31
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Actualizar una forma en una hoja de trabajo Excel
---
Este REST API indica actualizar una forma en una hoja de trabajo Excel.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| nombre del documento.|
| nombre de la hoja| cadena| camino| nombre de la hoja de trabajo.|
| índice de forma| entero| camino| índice de formas en formas de hojas de trabajo.|
| dto|| cuerpo||
| carpeta| cadena| consulta| Carpeta del documento.|
| nombredealmacenamiento| cadena| consulta| nombre del almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d "{ \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"Name\": \"string\", \"MsoDrawingType\": \"string\", \"AutoShapeType\": \"string\", \"Placement\": \"string\", \"UpperLeftRow\": 0, \"Top\": 0, \"UpperLeftColumn\": 0, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 10, \"Right\": 0, \"Width\": 0, \"Height\": 0, \"X\": 0, \"Y\": 0, \"RotationAngle\": 0, \"HtmlText\": \"string\", \"Text\": \"string\", \"AlternativeText\": \"string\", \"TextHorizontalAlignment\": \"string\", \"TextHorizontalOverflow\": \"string\", \"TextOrientationType\": \"string\", \"TextVerticalAlignment\": \"string\", \"TextVerticalOverflow\": \"string\", \"IsGroup\": true, \"IsHidden\": true, \"IsLockAspectRatio\": true, \"IsLocked\": true, \"IsPrintable\": true, \"IsTextWrapped\": true, \"IsWordArt\": true, \"LinkedCell\": \"string\", \"ZOrderPosition\": 0, \"Font\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"DoubleSize\": 0, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true, \"Name\": \"string\", \"Size\": 0, \"Underline\": \"string\" }, \"Hyperlink\": \"string\"}"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Familia de SDK en la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:
 

{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-PostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example-PostWorksheetShape.go" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-PostWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}
