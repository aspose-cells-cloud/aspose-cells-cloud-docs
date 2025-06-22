---
title: Uppdatera stil för pivottabell
second_title: Aspose.Cells Cloud Documen
linktitle: Formatera alla
type: docs
url: /sv/pivot-tables/format-all/
aliases: [/update-style-for-pivot-table/]
keywords: Update all cell style for a pivot table
description: Aspose.Cells Cloud REST API stöder uppdatering av alla cellstilar för en pivottabell. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Uppdatera stil för pivottabell
---
Denna REST API indikerar `update`-stil för pivottabellen.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
 
```
 Begäranparametrarna är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokumentnamn.|
| arknamn| sträng| väg| Arbetsbladets namn.|
| pivottabellindex| heltal| väg| Pivottabellindex|
| stil|| kropp| Formatera dto i begäran.|
| behöverOmBeräkna| boolesk| fråga|Falsk|
| mapp| sträng| fråga| Dokumentets mapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.com/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
-X POST \
-d '{"Font":{"Name":"Arial", "Size":10}}'
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
 
## Cloud SDK-familjen
 
 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.
 
Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
 
 
 
{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}
