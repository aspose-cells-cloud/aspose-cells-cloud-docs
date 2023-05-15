---
title: Establecer alturas de filas dentro del rango
second_title: Aspose.Cells Cloud Documen
linktitle: altura de fila
type: docs
url: /es/ranges/update/row-height/
aliases: [/change-heights-of-rows-inside-the-range/]
keywords: Set row height for range on an Excel workshee
description: Aspose.Cells Cloud REST API admite la configuración de la altura de fila para el rango en una hoja de trabajo Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 76
---
Este REST API indica establecer la altura de fila del rango en una hoja de trabajo Excel.
 
## RESET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/rowHeight
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino||
| hojaNombre| cadena| camino||
| valor| número| consulta||
| rango|| cuerpo||
| carpeta| cadena| consulta||
| NombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeRowHeight) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/rowHeight?value=15" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-d "{ \"ColumnCount\": 7, \"ColumnWidth\": 19, \"FirstColumn\": 0, \"FirstRow\": 9, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 1, \"RowHeight\": 15, \"Worksheet\": \"Sheet1\"}"
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
 
## Familia SDK de la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:


{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "18574f2f44071ac9d80be95568c193ff" >}}

{{< /tab >}}

{{< /tabs >}}
