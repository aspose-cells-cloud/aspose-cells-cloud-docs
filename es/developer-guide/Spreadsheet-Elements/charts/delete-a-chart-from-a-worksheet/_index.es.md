﻿---
title: Eliminar un gráfico de una hoja de trabajo
type: docs
url: /es/charts/delete/
aliases: [/delete-a-chart-from-a-worksheet/]
weight: 40
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Eliminar un gráfico de una hoja de cálculo
---
Este REST API indica eliminar el gráfico de la hoja de trabajo por índice.
 
## RSET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| Nombre del libro de trabajo.|
| nombreHoja| cadena| camino| Nombre de la hoja de trabajo.|
| Índice de gráficos| entero| camino| El índice del gráfico.|
| carpeta| cadena| consulta| La carpeta del libro de trabajo.|
| nombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
 
 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.


{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" 
-X DELETE 
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
"Code": 200,
"Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}
## Familia de SDK en la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
 
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}
