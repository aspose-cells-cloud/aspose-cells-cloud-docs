---
title: Få celldata baserat på namngiven ring
second_title: Aspose.Cells Cloud Documen
linktitle: Värde
type: docs
url: /sv/ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: Get cells data based on named range on an Excel worksheet
description: Aspose.Cells Cloud REST API stöder att hämta celldata baserat på namngivet intervall på ett Excel-kalkylblad. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 20
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Hämta celldata baserat på namngett område
---
 Denna REST API indikerar Hämta celllista i ett intervall efter intervallnamn eller radkolumnindex

 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| arbetsbokens namn|
| arknamn| sträng| väg| kalkylbladsnamn|
| namnintervall| sträng| fråga| intervallnamn, till exempel: 'A1:B2' eller 'intervallnamn1'|
| första raden| heltal| fråga| den första raden i intervallet|
| första kolumnen| heltal| fråga| den första kolumnen i intervallet|
| rowCount| heltal| fråga| antalet rader i intervallet|
| columnCount| heltal| fråga| antalet kolumner i intervallet|
| mapp| sträng| fråga| Arbetsboksmapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "CellsList": [

    {

      "Name": "B10",

      "Row": 9,

      "Column": 1,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "C10",

      "Row": 9,

      "Column": 2,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "D10",

      "Row": 9,

      "Column": 3,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "E10",

      "Row": 9,

      "Column": 4,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "F10",

      "Row": 9,

      "Column": 5,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "G10",

      "Row": 9,

      "Column": 6,

      "Value": null,

      "Type": "IsNull",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    },

    {

      "Name": "H10",

      "Row": 9,

      "Column": 7,

      "Value": "a8",

      "Type": "IsString",

      "Formula": null,

      "IsFormula": false,

      "IsMerged": false,

      "IsArrayHeader": false,

      "IsInArray": false,

      "IsErrorValue": false,

      "IsInTable": false,

      "IsStyleSet": false,

      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",

      "Style": {

        "link": {

          "Href": "/style",

          "Rel": "self",

          "Title": null,

          "Type": null

        }

      },

      "Worksheet": null,

      "link": null

    }

  ],

  "Code": 200,

  "Status": "OK"

}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-familj
 
 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
 
 
