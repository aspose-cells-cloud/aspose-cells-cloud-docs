---
title: Importar datos con almacenamiento
second_title: Aspose.Cells Cloud Documen
linktitle: Importar datos con almacenamiento
type: docs
url: /es/import-data-with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/,/import/with-using-storage/]
description: "Cells.Cloud API para Excel operar: Importar datos a la hoja de trabajo Excel"
weight: 10
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Importar datos con uso de almacenamiento
---
Este REST API indica `import data` en el archivo Excel.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```

Los parámetros de la solicitud son:

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/HTTPBody|Descripción|
|:- |:- |:- |:- |
| nombre| cadena| camino||
| carpeta| cadena| consulta||
| nombreDeAlmacenamiento| cadena| consulta| nombre de almacenamiento.|
| importar datos|| cuerpo||

**Los parámetros de opciones de importación de datos** se describen en[el enlace de referencia](/cells/es/import/#import-data-option-parameter).

 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

Puede usar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
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

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:
