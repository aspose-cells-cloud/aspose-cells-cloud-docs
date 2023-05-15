---
title: Importar matriz de cadenas de 2 dimensiones en la hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importar matriz de cadenas de 2 dimensiones
type: docs
url: /es/import/2dimension-string-array/
aliases: [/import-2dimension-string-array-into-excel-worksheet/,/import-2dimension-string-array-into-worksheet/,/import-data/-2dimension-string-array/,/import-data/2dimension-string-array/]
keywords: Import 2 dimension string array data into Excel files
description: Aspose.Cells Cloud REST API admite la importación de datos de matriz de cadenas de 2 dimensiones en archivos Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift
weight: 20
---
Este REST API `import 2 dimension string array data` en Excel hoja de trabajo.

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido de varias partes contiene los datos Import2DimensionStringArrayOption y la segunda contiene un archivo de datos.

## RESET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

Los parámetros importantes se describen en la siguiente tabla:

**Importar2DimensionStringArrayOption**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Primera fila| En t||
| Primera columna| En t||
| Datos|Cadena[,]||
| DestinationWorksheet| cadena| nombre de la hoja de trabajo de destino.|
| EsInsertar| cadena| verdadero Falso.|
| Tipo de datos de importación| cadena|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fuente| Origen del archivo| Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.|



**Ejemplo**

```json

{
    "Data": [
        ["1.0", "2.9"],
        ["2.0", "2.1"]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 1,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionStringArray"
}

```

## Familia SDK de la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se ocupa de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor, echa un vistazo a la[repositorio GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




