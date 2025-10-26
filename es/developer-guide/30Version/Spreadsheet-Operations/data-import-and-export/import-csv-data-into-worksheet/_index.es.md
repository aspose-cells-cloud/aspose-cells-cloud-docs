---
title: Importar datos CSV a la hoja de trabajo Excel
second_title: Documen
linktitle: Importar datos csv
type: docs
url: /es/import-csv-data-into-excel/
aliases: [/import-csv-data-into-worksheet/,/import-data/csv-data/,/import/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API admite la importación de datos CSV a archivos Excel. El SDK admite varios lenguajes de desarrollo, como Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 19
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Importar datos CSV a la hoja de trabajo Excel
---
Esta hoja de trabajo REST API `import csv data` en Excel.

La solicitud es una solicitud HTTP con contenido de varias partes (ver[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido multiparte contiene los datos de ImportCSVDataOption y la segunda contiene un archivo de datos.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Los parámetros importantes se describen en la siguiente tabla:

**ImportarOpción de Datos CSV**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Cadena separadora| cadena||
| Convertir datos numéricos| cadena|verdadero/falso.|
| Primera fila| entero||
| Primera columna| entero||
| Archivo fuente| cadena||
| Analizadores personalizados|Lista<CustomParserConfig> ||

**Configuración del analizador personalizado**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Índice de columna| entero||
| Método de análisis| cadena||
| Estilo personalizado| cadena||

**Ejemplo**

```xml

 <ImportCSVDataOption>
     <DestinationWorksheet>Sheet1</DestinationWorksheet>
     <IsInsert>true</IsInsert>
     <ImportDataType>CSVData</ImportDataType>
     <SeparatorString>;</SeparatorString>
     <ConvertNumericData>true</ConvertNumericData>
     <FirstRow>1</FirstRow>
     <FirstColumn>2</FirstColumn>
     <SourceFile>TestImportDataCSV.csv</SourceFile>
     <CustomParsers>
         <CustomParserConfig>
             <ColumnIndex>0</ColumnIndex>
             <ParseMethod>ToString</ParseMethod>
             <CustomStyle>#</CustomStyle>
         </CustomParserConfig>
     </CustomParsers>
 </ImportCSVDataOption>

```

## Familia de SDK en la nube

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
