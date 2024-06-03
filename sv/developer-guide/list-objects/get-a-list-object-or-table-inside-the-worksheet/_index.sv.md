---
title: Hämta ett listobjekt i ett Excel kalkylblad
second_title: Aspose.Cells Cloud Documen
linktitle: Ge
type: docs
url: /sv/list-objects/get/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/get/]
keywords: Get a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API stöder att få ett listobjekt(tabell) till ett Excel kalkylblad. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 9
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Hämta ett listobjekt i ett Excel kalkylblad
---
 Denna REST API indikerar till `get` en lista objektinformation efter index eller konvertera en `list object` till annat format fil i ett Excel kalkylblad.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokument namn.|
| arknamn| sträng| väg| Kalkylbladets namn.|
| listobjektindex| heltal| väg| listobjektindex.|
| formatera| sträng| fråga| exportformat.|
| mapp| sträng| fråga| Dokumentets mapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
	"ListObject": {
		"AutoFilter": {
			"FilterColumns": [],
			"Range": "B2:F11",
			"Sorter": {
				"CaseSensitive": false,
				"HasHeaders": false,
				"KeyList": [],
				"SortLeftToRight": false
			}
		},
		"DisplayName": "Table3",
		"StartColumn": 1,
		"StartRow": 1,
		"EndColumn": 5,
		"EndRow": 10,
		"ListColumns": [{
			"Name": "Column1",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 1,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$B$2:$B$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column2",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 2,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$C$2:$C$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column3",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 3,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$D$2:$D$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column4",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 4,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$E$2:$E$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column5",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 5,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$F$2:$F$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}],
		"ShowHeaderRow": true,
		"ShowTableStyleColumnStripes": false,
		"ShowTableStyleFirstColumn": false,
		"ShowTableStyleLastColumn": false,
		"ShowTableStyleRowStripes": true,
		"ShowTotals": false,
		"TableStyleName": "None",
		"TableStyleType": "None",
		"link": {
			"Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
			"Rel": "self"
		}
	},
	"Code": 200,
	"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-familj
 
 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
 
Denna REST API får ett excel `listobject`-objekt till annan formatfil.


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
