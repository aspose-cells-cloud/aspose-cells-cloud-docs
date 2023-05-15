---
title: Obtener salto de página vertical
second_title: Aspose.Cells Cloud Documen
linktitle: Obtener salto de página vertical
type: docs
url: /es/page-breaks/get-vertical-page-breaks/
aliases: [/get-vertical-page-breaks-inside-worksheet/]
keywords: Add a page break in an Excel worksheet
description: Aspose.Cells Cloud REST API admite agregar un salto de página en una hoja de trabajo Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 20
---
 Este REST API indica obtener `vertical` saltos de página.
 
## RESET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino||
| hojaNombre| cadena| camino||
| carpeta| cadena| consulta||
| NombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "VerticalPageBreaks": {

    "VerticalPageBreakList": [

      {

        "Column": 3,

        "EndRow": 1048575,

        "StartRow": 0

      }

    ],

    "link": {

      "Href": "http://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",

      "Rel": "self",

      "Title": null,

      "Type": null

    }

  },

  "Code": 200,

  "Status": "OK"

}
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Familia SDK de la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
 

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "537a7b794adab07f9ca929cf2c6f131a" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "34317a3fb628d9c3cd433f78b42bddc3" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "399b8d96afaffb51a07730c498e6eaf2" >}}

{{< /tab >}}

{{< /tabs >}}
