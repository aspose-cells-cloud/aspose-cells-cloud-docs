﻿---
title: Ta bort cellområde
type: docs
url: /sv/conditional-formattings/delete-cell-area/
aliases: [/remove-cell-area-from-conditional-formatting/]
keywords: REST API, spreadsheets, excel, delete cell area from condition formattin
description: "Cells.Cloud API för Excel operation: ta bort cellområde från villkorsformatering"
weight: 70
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Ta bort cellområde
---
Denna REST API indikerar att cellområdet ska tas bort från villkorsstyrd formatering.
 
## RSET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
 
```
 Begäranparametrarna är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg||
| arknamn| sträng| väg||
| startrad| heltal| fråga||
| startkolumn| heltal| fråga||
| totala rader| heltal| fråga||
| totalaKolumner| heltal| fråga||
| mapp| sträng| fråga||
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.
 

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "Code": "200",
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familjen
 
 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.
 
Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}



{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}



{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}



{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}



{{< /tab >}}

{{< tab tabNum="7" >}}



{{< /tab >}}

{{< tab tabNum="8" >}}



{{< /tab >}}

{{< tab tabNum="9" >}}



{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}
