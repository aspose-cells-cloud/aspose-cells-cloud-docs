﻿---
title: Autoajustar una columna en una hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: columna
type: docs
url: /es/worksheets/autofit/column/
aliases: [/autofit-single-column-of-worksheet/]
keywords: Autofit a column on an Excel workshee
description: Aspose.Cells Cloud REST API admite el ajuste automático de una columna en una hoja de trabajo Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 10
kwords: Excel, Office Cloud, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Autoajustar una columna en una hoja de trabajo Excel
---
Este REST API indica el ajuste automático de una columna en una hoja de trabajo Excel.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
 
```
 Los parámetros de la solicitud son:
 
| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino||
| nombre de la hoja| cadena| camino||
| primera columna| entero| consulta||
| última columna| entero| consulta||
| opciones de autoFitter|| cuerpo||
| primera fila| entero| consulta||
| última fila| entero| consulta||
| carpeta| cadena| consulta||
| nombredealmacenamiento| cadena| consulta| nombre del almacenamiento.|
 
 El[Especificación de API abierta](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.
 
Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=2&firstColumn=2" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells" : true, "IgnoreHidden" : true, "OnlyAuto" : true}' 

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


{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "9b4ccf2e3ba7d0f1d2a625d6cd40d2fd" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "3f17376a8d99f16f703fdb52c08a05ff" >}}

{{< /tab >}}

{{< /tabs >}}




