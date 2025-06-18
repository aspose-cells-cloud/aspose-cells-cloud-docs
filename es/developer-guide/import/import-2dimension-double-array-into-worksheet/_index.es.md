---
title: Importar matriz doble de 2 dimensiones a la hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importar matriz doble de 2 dimensiones
type: docs
url: /es/import/2dimension-double-array/
aliases: [/import-2dimension-double-array-into-excel-worksheet/,/import-2dimension-double-array-into-worksheet/, /import-data/2dimension-double-array/]
keywords: Import 2 dimension double array data into Excel files
description: Aspose.Cells Cloud REST API admite la importación de datos de matriz doble bidimensional en archivos Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 20
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdwon, Importar matriz doble de 2 dimensiones en hoja de trabajo Excel
---
Este REST API `import 2 dimension double array data` en la hoja de trabajo Excel.

La solicitud es una solicitud HTTP con contenido de varias partes (consulte[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido de varias partes contiene los datos de Import2DimensionDoubleArrayOption y la segunda contiene un archivo de datos.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```
Los parámetros importantes se describen en la siguiente tabla:

**Import2DimensionDoubleArrayOption**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Primera fila| En t||
| Primera columna| En t||
| Datos|Doble[,]||
| Hoja de trabajo de destino| cadena| nombre de la hoja de trabajo de destino.|
| EsInsertar| cadena| verdadero Falso.|
| Importar tipo de datos| cadena|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fuente| Fuente de archivo| Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.|



**Ejemplo**

```json

{
    "Data": [
        [1.0, 2.9, 3.1],
        [2.0, 2.1, 3.1]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 4,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionDoubleArray"
}

```

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




