---
title: CSV-Daten in das Arbeitsblatt Excel importieren
second_title: Aspose.Cells Cloud Documen
linktitle: CSV-Daten importieren
type: docs
url: /de/import/csv-data/
aliases: [/import-csv-data-into-excel-worksheet/, /import-csv-data-into-worksheet/,/import-data/csv-data/]
keywords: Import csv data into Excel files
description: Aspose.Cells Cloud REST API unterstützt das Importieren von CSV-Daten in Excel-Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 19
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, CSV-Daten in Excel Arbeitsblatt importieren
---
Dieses REST API `import csv data` in Excel Arbeitsblatt.

Bei der Anfrage handelt es sich um eine HTTP-Anfrage mit mehrteiligem Inhalt (siehe[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die ImportCSVDataOption-Daten und der zweite eine Datendatei.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Die wichtigen Parameter werden in der folgenden Tabelle beschrieben:


**ImportCSVDataOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Trennzeichen| Schnur||
| NumerischeDatenKonvertieren| Schnur|wahr falsch.|
| Erste Reihe| int||
| Erste Spalte| int||
| Quelldatei| Schnur||
| BenutzerdefinierteParser|Aufführen<CustomParserConfig> ||


**BenutzerdefinierteParserConfig**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Spaltenindex| int||
| ParseMethod| Schnur||
| Benutzerdefinierter Stil| Schnur||

**Beispiel**

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

## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte lesen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an die Webdienste Aspose.Cells tätigen:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
