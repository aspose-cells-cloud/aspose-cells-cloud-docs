---
title: Eliminar salto de página horizontal
second_title: Aspose.Cells Cloud Documen
linktitle: Eliminar salto de página horizontal
type: docs
url: /es/page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: Delete a page break in an Excel worksheet
description: Aspose.Cells Cloud REST API admite la eliminación de un salto de página en una hoja de trabajo Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 50
---
 Este REST API indica eliminar un salto de página `horizontal`.
 
## RESET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino||
| hojaNombre| cadena| camino||
| índice| entero| camino||
| carpeta| cadena| consulta||
| NombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
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


{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "16a442c2c2fb97afac8bd89fbbdca563" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "8ec70b4733866d10eae5e5e8c687d3ca" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "0a767f9030525d7f9be51bf9c6342b7d" >}}

{{< /tab >}}

{{< /tabs >}}
