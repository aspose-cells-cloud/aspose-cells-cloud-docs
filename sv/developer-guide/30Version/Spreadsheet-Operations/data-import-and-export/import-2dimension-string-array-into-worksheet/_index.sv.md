---
title: Importera en 2-dimensionell strängmatris till arbetsbladet Excel
second_title: Documen
linktitle: Importera 2-dimensionell strängarray
type: docs
url: /sv/import-a-2D-string-array-into-excel-worksheet/
aliases: [/import-2dimension-string-array-into-excel-worksheet/,/import-2dimension-string-array-into-worksheet/,/import-data/-2dimension-string-array/,/import-data/2dimension-string-array/,/import/2dimension-string-array/ ]
keywords: Import 2 dimension string array data into Excel files
description: Aspose.Cells Cloud REST API stöder import av 2-dimensionella strängmatrisdata till Excel-filer. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 20
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Importera 2-dimensionell strängmatris till Excel-arbetsblad
---
Detta REST API `import 2 dimension string array data` till Excel-arbetsblad.

Begäran är en HTTP-begäran med flerdelat innehåll (se[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)eller[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)Den första delen av flerdelat innehåll innehåller Import2DimensionStringArrayOption-data och den andra innehåller en datafil.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

De viktiga parametrarna beskrivs i följande tabell:

**Importera2DimensionStringArrayAlternativ**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Första raden| int||
| Första kolumnen| int||
| Data|Sträng[,]||
|Destinationsarbetsblad| sträng| namn på destinationsarbetsblad.|
| ÄrInfoga| sträng| sant/falskt.|
| Importera datatyp| sträng|IntArray/DubbelArray/StringArray/TvåDimensionIntArray/TvåDimensionDubbelArray/TvåDimensionStringArray/BatchData/CSVData.|
| Källa| Filkälla| Anger datafilens position när BatchData-parametern är null.|

**Exempel**

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

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

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
