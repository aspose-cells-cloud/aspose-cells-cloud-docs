---
title: Importar una matriz de enteros de dos dimensiones a la hoja de trabajo Excel
second_title: Documen
linktitle: Importar matriz entera de 2 dimensiones
type: docs
url: /es/import-a-2D-integer-array-into-excel-worksheet/
aliases: [/import-2dimension-integer-array-into-excel-worksheet/,/import-2dimension-integer-array-into-worksheet/, /import-data/2dimension-integer-array/, /import/2dimension-integer-array/]
keywords: Import 2 dimension integer array data into Excel files
description: Aspose.Cells Cloud REST API admite la importación de datos de matrices de enteros bidimensionales a archivos Excel. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 20
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Importar matriz de enteros de 2 dimensiones a la hoja de cálculo Excel
---
Esta hoja de trabajo REST API `import 2 dimension integer array data` en Excel.

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multiparte contiene los datos de Import2DimensionIntegerArrayOption y la segunda contiene un archivo de datos.

Los parámetros importantes se describen en la siguiente tabla:

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

**Importar2DimensionIntegerArrayOption**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Primera fila| entero||
| Primera columna| entero||
| Datos|Entero[,]||
|Hoja de trabajo de destino| cadena| Nombre de la hoja de trabajo de destino.|
| EsInsertar| cadena| verdadero/falso.|
| Importar tipo de datos| cadena|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fuente| Fuente del archivo| Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.|

**Ejemplo**

```json
{
    "Data": [
        [1, 2],
        [3, 4]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 4,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionIntArray"
}

```

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
