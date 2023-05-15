---
title: Uppdatera flera Cells Styl
type: docs
url: /sv/update-multiple-cells-style/
weight: 20
---
Denna REST API indikerar set `cells style` till en cell i en Excel fil.

 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Arbetsbokens namn.|
| arknamn| sträng| väg| Arbetsbladsnamn.|
| räckvidd| sträng| fråga| Räckvidden.|
| stil|| kropp| med uppdatera stilinställningar.|
| mapp| sträng| fråga| Arbetsboksmappen.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
-X POST \
 -d "{ \"Font\": { \"Color\": { \"A\":255, \"R\": 255, \"G\": 255, \"B\": 0 }, \"DoubleSize\": 10, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true, \"Name\": \"Arial\", \"Size\": 22 }, \"Name\": \"string\", \"CultureCustom\": \"string\", \"Custom\": \"string\", \"BackgroundColor\": { \"A\": 10, \"R\": 10, \"G\": 10, \"B\": 10 }, \"ForegroundColor\": { \"A\": 255, \"R\": 255, \"G\": 255, \"B\": 0 } \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
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
 

 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:



{{< tabs tabTotal="3" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostUpdateWorksheetCellStyle-.php" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-post_update_worksheet_cell_style-.rb" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "59dae0a6697e3c68ade244ed28b27d10" >}}

{{< /tab >}}

{{< /tabs >}}
