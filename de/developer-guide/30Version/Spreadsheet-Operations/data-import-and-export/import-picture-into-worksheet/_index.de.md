---
title: Bild in Arbeitsblatt Excel importieren
second_title: Documen
linktitle: Bild importieren
type: docs
url: /de/import-picture-into-excel-worksheet/
aliases: [/import-picture-into-worksheet/,/import-data/picture/, /import/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API unterstützt den Import von Bildern in Excel Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 19
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Bild in Excel Arbeitsblatt importieren
---
Dieses REST API `import picture data` in Excel Arbeitsblatt.

Bei der Anfrage handelt es sich um eine HTTP-Anfrage mit mehrteiligem Inhalt (siehe[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die ImportPictureOption-Daten und der zweite eine Datendatei.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

Die wichtigen Parameter sind in der folgenden Tabelle beschrieben:

**ImportPictureOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Obere Linke Zeile| int||
| Obere linke Spalte| int||
| UntereRechteReihe| int||
| Untere Rechte Spalte| int||
| Dateiname| Schnur||
| Daten| Zeichenfolge||
|ZielArbeitsblatt| Schnur| Name des Zielarbeitsblatts.|
| IsInsert| Schnur| wahr/falsch.|
| ImportDataType| Schnur|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Quelle| Dateiquelle| Gibt die Datendateiposition an, wenn der BatchData-Parameter null ist.|

**Beispiel**

## Cloud SDK-Familie

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
