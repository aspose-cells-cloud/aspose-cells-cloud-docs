---
title: Lägg till en form på ett Excel arbetsark
second_title: Aspose.Cells Cloud Documen
linktitle: Ad
type: docs
url: /sv/shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: Add shape on an Excel workshee
description: Aspose.Cells Cloud REST API stöder att lägga till form på ett Excel kalkylblad. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 30
---
Denna REST API indikerar att lägga till en form på ett Excel kalkylblad.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokument namn.|
| arknamn| sträng| väg| kalkylbladsnamn.|
| shapeDTO|| kropp||
| drawingType| sträng| fråga| formobjektstyp|
| övre Vänsterrad| heltal| fråga| Övre vänstra radens index.|
| övre vänstra kolumnen| heltal| fråga| Övre vänstra kolumnindex.|
| topp| heltal| fråga| Representerar den vertikala förskjutningen av Spinner från dess vänstra rad, i pixelenhet.|
| vänster| heltal| fråga| Representerar den horisontella förskjutningen av Spinner från dess vänstra kolumn, i pixelenhet.|
| bredd| heltal| fråga| Representerar höjden på Spinner, i pixelenhet.|
| höjd| heltal| fråga| Representerar bredden på Spinner, i pixelenhet.|
| mapp| sträng| fråga| Dokumentets mapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-PutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "34f478cae8c02848db0e376bd592a087" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-PutWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}
