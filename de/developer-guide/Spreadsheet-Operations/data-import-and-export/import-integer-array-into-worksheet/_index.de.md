---
title: Importieren Sie ein Integer-Array in das Arbeitsblatt Excel
linktitle: Integer-Array importieren
type: docs
url: /de/import-integer-array-into-excel-worksheet/
aliases: [/import-integer-array-into-excel-worksheet/,/import-integer-array-into-worksheet/,/import-data/integer-array/, /import/integer-array/]
keywords: Import integer array data into Excel files
description: Aspose.Cells Cloud REST API unterstützt den Import von Integer-Array-Daten in Excel-Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift.
weight: 30
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Integer-Array in Excel Arbeitsblatt importieren
---
Dieses REST API `import int array data` in Excel Arbeitsblatt.

Bei der Anfrage handelt es sich um eine HTTP-Anfrage mit mehrteiligem Inhalt (siehe[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die ImportIntegerArrayOption-Daten und der zweite eine Datendatei.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Die wichtigen Parameter sind in der folgenden Tabelle beschrieben:

**ImportIntegerArrayOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Erste Reihe| int||
| Erste Spalte| int||
| IsVertical| Schnur| wahr/falsch.|
| Daten|Ganze Zahl[]||
| ZielArbeitsblatt| Schnur| Name des Zielarbeitsblatts.|
| IsInsert| Schnur| wahr/falsch.|
| ImportDataType| Schnur|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Quelle| Dateiquelle| Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.|

**Beispiel**

```JSON

{
    "Data": [1, 2, 4],
    "DestinationWorksheet": "Sheet1",
    "FirstRow": 1,
    "FirstColumn": 2,
    "IsVertical": true,
    "IsInsert": true,
    "importDataType": "IntArray"
}

```

## Cloud SDK-Familie

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um grundlegende Details und ermöglicht Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
