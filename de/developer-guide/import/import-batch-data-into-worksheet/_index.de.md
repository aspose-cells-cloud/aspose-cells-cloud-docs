﻿---
title: Chargendaten in das Arbeitsblatt Excel importieren
second_title: Aspose.Cells Cloud Documen
linktitle: Chargendaten importieren
type: docs
url: /de/import/batch-data/
aliases: [/import-batch-data-into-excel-worksheet/,/import-batch-data-into-worksheet/,/import-data/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API unterstützt das Importieren von Stapeldaten in Excel-Dateien. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 19
---
Dieses REST API `import batch data` in Excel Arbeitsblatt.

Die Anfrage ist eine HTTP-Anfrage mit mehrteiligem Inhalt (vgl[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC-1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die ImportBatchDataOption-Daten und der zweite eine Datendatei.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

Die wichtigen Parameter sind in der folgenden Tabelle beschrieben:


**ImportBatchDataOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| BatchData|Aufführen<CellValue> | Chargendaten|
| ZielArbeitsblatt| Schnur| Name des Zielarbeitsblatts.|
| IstEinfügen| Schnur| wahr falsch.|
| Datentyp importieren| Schnur|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| Quelle| Dateiquelle| Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.|



**Zellwert**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Zeilenindex| int||
| Spaltenindex| int||
| Typ| Schnur| Datentyp|
| Wert| Schnur||
| Stil| Stil (Objekt)||



**Dateiquelle**
|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| FileSourceType| Schnur| InMemoryFiles/CloudFileSystem/RequestFiles|
| Dateipfad| Schnur| Dateiposition|


**Beispiel**

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

## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:


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
