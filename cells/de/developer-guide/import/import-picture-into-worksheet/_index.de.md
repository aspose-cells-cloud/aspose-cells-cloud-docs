---
title: Bild in Excel Arbeitsblatt importieren
second_title: Aspose.Cells Cloud Documen
linktitle: Bild importieren
type: docs
url: /de/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API unterstützt das Importieren von Bildern in Excel-Dateien. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 19
---
Dieses REST API `import picture data` in Excel Arbeitsblatt.

Die Anfrage ist eine HTTP-Anfrage mit mehrteiligem Inhalt (vgl[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC-1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die ImportPictureOption-Daten und der zweite eine Datendatei.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```


Die wichtigen Parameter sind in der folgenden Tabelle beschrieben:


**ImportPictureOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| ObereLinkeReihe| int||
|UpperLeftColumn| int||
| LowerRightRow| int||
| LowerRightColumn| int||
| Dateinamen| Schnur||
| Daten| Schnur||
| ZielArbeitsblatt| Schnur| Name des Zielarbeitsblatts.|
| IstEinfügen| Schnur| wahr falsch.|
| Datentyp importieren| Schnur|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Quelle| Dateiquelle| Gibt die Position der Datendatei an, wenn der BatchData-Parameter null ist.|


**Beispiel**


## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

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

