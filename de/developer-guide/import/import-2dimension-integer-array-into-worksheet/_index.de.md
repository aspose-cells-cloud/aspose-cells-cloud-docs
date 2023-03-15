---
title: Importieren Sie ein 2-dimensionales ganzzahliges Array in das Arbeitsblatt Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importieren Sie 2-dimensionale Integer-Arrays
type: docs
url: /de/import/2dimension-integer-array/
aliases: [/import-2dimension-integer-array-into-excel-worksheet/,/import-2dimension-integer-array-into-worksheet/, /import-data/2dimension-integer-array/]
keywords: Import 2 dimension integer array data into Excel files
description: Aspose.Cells Cloud REST API unterstützt den Import von zweidimensionalen Integer-Array-Daten in Excel-Dateien. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 20
---
Dieses REST API `import 2 dimension integer array data` in Excel Arbeitsblatt.

Die Anfrage ist eine HTTP-Anfrage mit mehrteiligem Inhalt (vgl[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC-1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die Import2DimensionIntegerArrayOption-Daten und der zweite eine Datendatei.

Die wichtigen Parameter sind in der folgenden Tabelle beschrieben:

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

**Import2DimensionIntegerArrayOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Erste Reihe| int||
| Erste Spalte| int||
| Daten|Ganze Zahl[,]||
| ZielArbeitsblatt| Schnur| Name des Zielarbeitsblatts.|
| IstEinfügen| Schnur| wahr falsch.|
| Datentyp importieren| Schnur|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Quelle| Dateiquelle| Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.|



**Beispiel**

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
## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

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




