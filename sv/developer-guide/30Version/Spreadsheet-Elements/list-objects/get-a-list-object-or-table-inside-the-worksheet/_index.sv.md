---
title: Hämta ett listobjekt i ett Excel-arbetsblad
second_title: Documen
linktitle: Ge
type: docs
url: /sv/list-objects/get/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/get/]
keywords: Get a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API stöder att hämta ett listobjekt (tabell) till ett Excel-arbetsblad. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 9
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Hämta ett listobjekt i ett Excel-kalkylblad
---
Denna REST API indikerar för `get` en lista med objektinformation efter index eller konverterar en `list object` till en annan filformat i ett Excel-arbetsblad.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
 
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokumentnamn.|
| arknamn| sträng| väg| Arbetsbladets namn.|
| listobjektindex| heltal| väg| lista objektindex.|
| formatera| sträng| fråga| exportformat.|
| mapp| sträng| fråga| Dokumentets mapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

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

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

Denna REST API hämtar ett Excel `listobject`-objekt till en fil i ett annat format.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
