﻿---
title: Agregar una tabla dinámica en una hoja de cálculo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Agregar
type: docs
url: /es/pivot-tables/add/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: Add a pivot table in an Excel worksheet
description: Aspose.Cells Cloud REST API admite la adición de una tabla dinámica en una hoja de cálculo Excel. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Agregar una tabla dinámica en una hoja de cálculo Excel
---
Este REST API indica a `add` una tabla dinámica en la hoja de cálculo.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| Nombre del documento.|
| nombreHoja| cadena| camino| El nombre de la hoja de trabajo.|
| pedido|| cuerpo| CreatePivotTableRequest dto en el cuerpo de la solicitud.|
| carpeta| cadena| consulta| Carpeta de documentos.|
| nombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
| Datos de origen| cadena| consulta| Los datos para la nueva caché de tabla dinámica.|
|nombreCeldaDestino| cadena| consulta| La celda en la esquina superior izquierda del rango de destino del informe de tabla dinámica.|
| nombre de la tabla| cadena| consulta| El nombre del nuevo informe de tabla dinámica.|
| useSameSource| booleano| consulta| Indica si se usa la misma fuente de datos cuando otra tabla dinámica ya la ha usado. Si la propiedad es verdadera, se ahorrará memoria.|
 
 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v  "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables"
-X PUT \
-d '{"Name":"MyPivot", "SourceData":"A5:E10", "DestCellName":"H20", "UseSameSource":true, "PivotFieldRows":[1], "PivotFieldColumns":[1], "PivotFieldData ":[1]}'\
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
 
## Familia de SDK en la nube
 
 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.
 
Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}
