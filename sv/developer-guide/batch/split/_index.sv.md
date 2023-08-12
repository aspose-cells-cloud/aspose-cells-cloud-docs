---
title: Batch Spli
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API stöder batchdelad fil. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 100
---
Denna REST API indikerar till `batch split` av kvalificerad fil.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| BatchSplitRequest|| kropp||

**BatchSplitRequest-egenskaper**
 
Namn | Skriv | Beskrivning | Anteckningar
------------ | ------------- | ------------- | -------------
 Källmapp | sträng | | [valfritt]SourceStorage | sträng | | [valfritt]MatchCondition | MatchConditionRequest | | [valfritt]Format | sträng | | [valfritt]FrånIndex | heltal | | [valfritt]ToIndex | heltal | | [valfritt]Outfolder | sträng | | [valfritt]Sparaalternativ | Spara Alternativ | | [frivillig]**MatchConditionRequest-egenskaper**
 
Namn | Skriv | Beskrivning | Anteckningar
------------ | ------------- | ------------- | -------------
 RegexPattern | sträng | | [valfritt]FullMatchvillkor | sträng[]| | [valfritt]Den[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/Batch/PostBatchsplit) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-familj
 
Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina delade uppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
 
 
  
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

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

{{< tab tabNum="10" >}}


{{< /tab >}}

{{< /tabs >}}

