---
title: Doppeltes Array in Arbeitsblatt Excel importieren
second_title: Aspose.Cells Cloud Documen
linktitle: Doppeltes Arra importieren
type: docs
url: /de/import/double-array/
aliases: [/import-double-array-into-excel-worksheet/,/import-double-array-into-worksheet/,/import-data/double-array/]
keywords: Import double array data into Excel files
description: Aspose.Cells Cloud REST API unterstützt das Importieren von Double-Array-Daten in Excel-Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift.
weight: 20
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Double-Array in Excel Arbeitsblatt importieren
---
Dieses REST API `import double array data` in Excel Arbeitsblatt.

Bei der Anfrage handelt es sich um eine HTTP-Anfrage mit mehrteiligem Inhalt (siehe[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die ImportDoubleArrayOption-Daten und der zweite eine Datendatei.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Die wichtigen Parameter werden in der folgenden Tabelle beschrieben:


**ImportDoubleArrayOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Erste Reihe| int||
| Erste Spalte| int||
| IstVertikal| Schnur| wahr falsch.|
| Daten|Doppelt[]||
| ZielArbeitsblatt| Schnur| Name des Zielarbeitsblatts.|
| IstEinfügen| Schnur| wahr falsch.|
| ImportierenDatentyp| Schnur|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Quelle| Dateiquelle| Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.|



**Beispiel**

```xml

<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>

```

```json
{
    "Data": [1.99, 1.9, 2.0],
    "DestinationWorksheet": "Sheet1",
    "FirstRow": 0,
    "FirstColumn": 0,
    "IsVertical": false,
    "IsInsert": true,
    "importDataType": "DoubleArray"
}

```

## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte lesen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an die Webdienste Aspose.Cells tätigen:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




