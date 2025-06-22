---
title: Actualizar el estilo de celda de la tabla dinámica
second_title: Aspose.Cells Cloud Documen
linktitle: Formato
type: docs
url: /es/pivot-tables/format/
aliases: [/update-cell-style-for-pivot-table/]
keywords: Update cell style for a pivot table
description: Aspose.Cells Cloud REST API admite la actualización del estilo de celda de una tabla dinámica. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 90
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Actualizar estilo de celda para tabla dinámica
---
Este REST API indica la actualización de la celda `style` para la tabla dinámica.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino| Nombre del documento.|
| nombreHoja| cadena| camino| El nombre de la hoja de trabajo.|
| índice de tabla dinámica| entero| camino| Índice de tabla dinámica|
| columna| entero| consulta||
| fila| entero| consulta||
| estilo|| cuerpo| Estilo dto en el cuerpo de la solicitud.|
| necesitoRecalcular| booleano| consulta|FALSO|
| carpeta| cadena| consulta| Carpeta de documentos.|
| nombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
 
 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
-X POST \
-d '{"Font":{"Name":"Arial", "Size":10}}'  \
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
 
 
 
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}




