---
title: Uppdatera en form på ett Excel arbetsblad
second_title: Aspose.Cells Cloud Documen
linktitle: Uppdatering
type: docs
url: /sv/shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: Update a shape on an Excel workshee
description: Aspose.Cells Cloud REST API stöder uppdatering av en form på ett Excel-kalkylblad. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 31
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Uppdatera en form på ett Excel kalkylblad
---
Denna REST API indikerar att en form ska uppdateras på ett Excel kalkylblad.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokument namn.|
| arknamn| sträng| väg| kalkylbladsnamn.|
| formindex| heltal| väg| formindex i kalkylbladsformer.|
| dto|| kropp||
| mapp| sträng| fråga| Dokumentets mapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d "{ \"link\": { \"Href\": \"string\", \"Rel\": \"string\", \"Title\": \"string\", \"Type\": \"string\" }, \"Name\": \"string\", \"MsoDrawingType\": \"string\", \"AutoShapeType\": \"string\", \"Placement\": \"string\", \"UpperLeftRow\": 0, \"Top\": 0, \"UpperLeftColumn\": 0, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 10, \"Right\": 0, \"Width\": 0, \"Height\": 0, \"X\": 0, \"Y\": 0, \"RotationAngle\": 0, \"HtmlText\": \"string\", \"Text\": \"string\", \"AlternativeText\": \"string\", \"TextHorizontalAlignment\": \"string\", \"TextHorizontalOverflow\": \"string\", \"TextOrientationType\": \"string\", \"TextVerticalAlignment\": \"string\", \"TextVerticalOverflow\": \"string\", \"IsGroup\": true, \"IsHidden\": true, \"IsLockAspectRatio\": true, \"IsLocked\": true, \"IsPrintable\": true, \"IsTextWrapped\": true, \"IsWordArt\": true, \"LinkedCell\": \"string\", \"ZOrderPosition\": 0, \"Font\": { \"Color\": { \"A\": 0, \"R\": 0, \"G\": 0, \"B\": 0 }, \"DoubleSize\": 0, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true, \"Name\": \"string\", \"Size\": 0, \"Underline\": \"string\" }, \"Hyperlink\": \"string\"}"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-familj
 
 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
 

{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-PostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example-PostWorksheetShape.go" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-PostWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}
