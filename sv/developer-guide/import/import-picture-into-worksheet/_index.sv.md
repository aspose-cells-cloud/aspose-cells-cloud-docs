---
title: Importera bild till Excel Worksheet
second_title: Aspose.Cells Cloud Documen
linktitle: Importera bild
type: docs
url: /sv/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API stödjer import av bild till Excel-filer. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 19
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdwon, Importera bild till Excel Kalkylblad
---
Detta REST API `import picture data` till Excel arbetsblad.

Begäran är en HTTP-begäran med innehåll i flera delar (se[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)eller[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Den första delen av innehållet med flera delar innehåller ImportPictureOption-data och den andra innehåller en datafil.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```


De viktiga parametrarna beskrivs i följande tabell:


**ImportPictureOption**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| UpperLeftRow| int||
| Övre vänstra kolumnen| int||
| Nedre högerrad| int||
| Nedre högerkolumn| int||
| Filnamn| sträng||
| Data| Sträng||
| Destinationsarbetsblad| sträng| destinationsarbetsbladets namn.|
| IsInsert| sträng| sant falskt.|
| ImportDataType| sträng|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| Källa| FileSource| Indikerar datafilens position när BatchData-parametern är null.|


**Exempel**


## Cloud SDK-familj

 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:


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

