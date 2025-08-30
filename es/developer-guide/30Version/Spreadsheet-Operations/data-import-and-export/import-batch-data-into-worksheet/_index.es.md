---
title: Importar datos por lotes a la hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importar datos por lotes
type: docs
url: /es/import-batch-data-into-excel/
aliases: [/import-batch-data-into-worksheet/,/import-data/batch-data/,/import/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API admite la importación de datos por lotes a archivos Excel. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 19
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Importar datos por lotes a la hoja de trabajo Excel
---
Esta hoja de trabajo REST API `import batch data` en Excel.

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multiparte contiene los datos de ImportBatchDataOption y la segunda contiene un archivo de datos.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Los parámetros importantes se describen en la siguiente tabla:

**Opción de importación de datos por lotes**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Datos por lotes|Lista<CellValue> | datos del lote|
| Hoja de trabajo de destino| cadena| Nombre de la hoja de trabajo de destino.|
| EsInsertar| cadena| verdadero/falso.|
| Importar tipo de datos| cadena|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Fuente| Fuente del archivo| Indica la posición del archivo de datos cuando el parámetro BatchData es nulo.|

**Valor de celda**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| índice de fila| entero||
| índice de columna| entero||
| tipo| cadena| tipo de datos|
| valor| cadena||
| estilo| Estilo(objeto)||

**Fuente del archivo**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Tipo de origen del archivo| cadena| Archivos en memoria/Sistema de archivos en la nube/Archivos de solicitud|
| Ruta de archivo| cadena| posición del archivo|

**Ejemplo**

```xml
<ImportIntArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportIntArrayOption>

```

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
