---
title:  Range Sortera
second_title: Aspose.Cells Cloud Documen
linktitle: Sor
type: docs
keywords: Range Sort
url: /sv/ranges/sort/
description:  Anger konturkant runt ett cellintervall.
weight: 20
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Range Sort
---
 Denna REST API indikerar intervallsortering.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

 Begärans parametrar är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody| Beskrivning|
|:- |:- |:- |:- |
|namn|Sträng|Väg|Arbetsbokens namn.|
|arknamn|Sträng|Väg|Kalkylbladets namn.|
|räckviddOperera|Klass|Kropp| Range Sort Request|
|mapp|Sträng|Fråga|Original arbetsboksmapp.|
|lagringsnamn|Sträng|Fråga|Lagringsnamn.|



 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in GitHub-förvaret för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:

