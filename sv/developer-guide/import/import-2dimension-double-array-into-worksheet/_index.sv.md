---
title: Importera 2 Dimension Double Array till Excel Worksheet
second_title: Aspose.Cells Cloud Documen
linktitle: Importera 2 dimension dubbel arra
type: docs
url: /sv/import/2dimension-double-array/
aliases: [/import-2dimension-double-array-into-excel-worksheet/,/import-2dimension-double-array-into-worksheet/, /import-data/2dimension-double-array/]
keywords: Import 2 dimension double array data into Excel files
description: Aspose.Cells Cloud REST API stöder import av tvådimensionell dubbelmatrisdata till Excel-filer. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 20
---
Detta REST API `import 2 dimension double array data` till Excel arbetsblad.

Begäran är en HTTP-begäran med innehåll i flera delar (se[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)eller[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Den första delen av innehållet med flera delar innehåller Import2DimensionDoubleArrayOption-data och den andra innehåller en datafil.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```
De viktiga parametrarna beskrivs i följande tabell:

**Import2DimensionDoubleArrayOption**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Första raden| int||
| Första kolumnen| int||
| Data|Dubbel[,]||
| Destinationsarbetsblad| sträng| destinationsarbetsbladets namn.|
| IsInsert| sträng| sant falskt.|
| ImportDataType| sträng|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Källa| FileSource| Indikerar datafilens position när BatchData-parametern är null.|



**Exempel**

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

## Cloud SDK-familj

 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:

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




