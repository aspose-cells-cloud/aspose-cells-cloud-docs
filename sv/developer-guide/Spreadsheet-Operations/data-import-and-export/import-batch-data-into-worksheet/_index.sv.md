---
title: Importera batchdata till Excel-arbetsbladet
second_title: Aspose.Cells Cloud Documen
linktitle: Importera batchdata
type: docs
url: /sv/import-batch-data-into-excel/
aliases: [/import-batch-data-into-worksheet/,/import-data/batch-data/,/import/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API stöder import av batchdata till Excel-filer. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 19
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Importera batchdata till Excel-arbetsblad
---
Detta REST API `import batch data` till Excel-arbetsblad.

Begäran är en HTTP-begäran med flerdelat innehåll (se[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)eller[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)Den första delen av flerdelat innehåll innehåller ImportBatchDataOption-data och den andra innehåller en datafil.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

De viktiga parametrarna beskrivs i följande tabell:

**ImportBatchDataAlternativ**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| BatchData|Lista<CellValue> | batchdata|
| Destinationsarbetsblad| sträng| namn på destinationsarbetsblad.|
| ÄrInfoga| sträng| sant/falskt.|
| Importera datatyp| sträng|IntArray/DubbelArray/StringArray/TvåDimensionIntArray/TvåDimensionDubbelArray/TvåDimensionStringArray/BatchData/CSVData.|
| Källa| Filkälla| Anger datafilens position när BatchData-parametern är null.|

**Cellvärde**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| radindex| int||
|kolumnindex| int||
| typ| sträng| datatyp|
| värde| sträng||
| stil| Stil (objekt)||

**Filkälla**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Filkällatyp| sträng| InMemoryFiles/CloudFileSystem/RequestFiles|
| Filsökväg| sträng| filposition|

**Exempel**

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

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

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
