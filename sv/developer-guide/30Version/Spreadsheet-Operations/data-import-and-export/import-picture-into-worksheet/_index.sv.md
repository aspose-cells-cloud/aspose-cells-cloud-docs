---
title: Importera bild till Excel-arbetsbladet
second_title: Documen
linktitle: Importera bild
type: docs
url: /sv/import-picture-into-excel-worksheet/
aliases: [/import-picture-into-worksheet/,/import-data/picture/, /import/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API stöder import av bilder till Excel-filer. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 19
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Importera bild till Excel-kalkylblad
---
Detta REST API `import picture data` till Excel-arbetsblad.

Begäran är en HTTP-begäran med flerdelat innehåll (se[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)eller[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)Den första delen av det flerdelade innehållet innehåller ImportPictureOption-data och den andra innehåller en datafil.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

De viktiga parametrarna beskrivs i följande tabell:

**Importera bildalternativ**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| Övre vänsterrad| int||
| Övre vänsterkolumn| int||
| Nedre högerrad| int||
| Nedre högerkolumn| int||
| Filnamn| sträng||
| Data| Sträng||
|Destinationsarbetsblad| sträng| namn på destinationsarbetsblad.|
| ÄrInfoga| sträng| sant/falskt.|
| Importera datatyp| sträng|IntArray/DubbelArray/StringArray/TvåDimensionIntArray/TvåDimensionDubbelArray/TvåDimensionStringArray/BatchData/CSVData/Bild.|
| Källa| Filkälla| Anger datafilens position när BatchData-parametern är null.|

**Exempel**

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

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
