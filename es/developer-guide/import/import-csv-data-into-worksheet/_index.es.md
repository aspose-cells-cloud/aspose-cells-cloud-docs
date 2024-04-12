---
title: Importar datos CSV a la hoja de trabajo Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importar datos csv
type: docs
url: /es/import/csv-data/
aliases: [/import-csv-data-into-excel-worksheet/, /import-csv-data-into-worksheet/,/import-data/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API admite la importación de datos csv en archivos Excel. SDK admite tipos de lenguajes de desarrollo. Incluyen Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift.
weight: 19
---
Este REST API `import csv data` en la hoja de trabajo Excel.

La solicitud es una solicitud HTTP con contenido de varias partes (consulte[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)o[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La primera parte del contenido de varias partes contiene los datos ImportCSVDataOption y la segunda contiene un archivo de datos.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

Los parámetros importantes se describen en la siguiente tabla:


**Importar opción CSVData**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Cadena separadora| cadena||
| Convertir datos numéricos| cadena|verdadero Falso.|
| Primera fila| En t||
| Primera columna| En t||
| Archivo fuente| cadena||
| Analizadores personalizados|Lista<CustomParserConfig> ||


**Configuración de analizador personalizado**

|Nombre del parámetro|Tipo|Descripción|
|:- |:- |:- |
| Índice de columnas| En t||
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

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite concentrarse en las tareas de su proyecto. Por favor revisa el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK de nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
