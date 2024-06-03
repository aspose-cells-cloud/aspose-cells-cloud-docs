---
title: Eliminar un filtro en una hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Eliminar filtro
type: docs
url: /es/delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/,/delete-auto-filter/]
keywords: Deletes a filter on an Excel worksheet
description: Aspose.Cells Cloud API admite la eliminación de un filtro en una hoja de trabajo Excel. El SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 100
kwords: Excel, Office Cloud, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Eliminar un filtro en una hoja de trabajo Excel
---
Este REST API indica eliminar un `filter` en una hoja de trabajo Excel.

## RSET API

```bash

DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter

```

Los parámetros de la solicitud son:
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| Camino| El nombre del libro de trabajo.|
| nombre de la hoja| cadena| Camino| El nombre de la hoja de trabajo.|
|rango|cadena| Consulta||
|índice de campo|entero| Consulta||
|FechaHoraTipo de agrupación|cadena| Consulta| Día/Hora/Minuto/Mes/Segundo/Año|
|año|entero| Consulta||
|mes|entero| Consulta||
|día|entero| Consulta||
|hora|entero| Consulta||
|minuto|entero| Consulta||
|segundo|entero| Consulta||
|MatchBlancos|cadena| Consulta|verdadero Falso|
|actualizar|cadena| Consulta|verdadero Falso|
|carpeta|cadena| Consulta|Carpeta del libro de trabajo original.|
|nombredealmacenamiento|cadena| Consulta|Nombre del almacenamiento.|

 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&criteria=Year" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

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

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-DeleteFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-DeleteFilterForFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-DeleteWorksheetFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-delete_worksheet_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-DeleteFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-DeleteFilterForFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-DeleteFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "4e5d4702f8c09698ab20c1a577b259c9" >}}

{{< /tab >}}

{{< /tabs >}}
