---
title: Få namngivna intervall på en Excel workboo
second_title: Aspose.Cells Cloud Documen
linktitle: Nam
type: docs
url: /sv/ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: Get cells data based on named range on an Excel worksheet
description: Aspose.Cells Cloud REST API stöder att hämta celldata baserat på namngivet intervall på ett Excel-kalkylblad. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 10
---
Denna REST API indikerar information om intervall för Läs kalkylblad.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg| Dokument namn.|
| mapp| sträng| fråga| Dokumentmapp.|
| lagringsnamn| sträng| fråga| lagringsnamn.|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{

  "Ranges": {

    "RangeList": [

      {

        "ColumnCount": 7,

        "ColumnWidth": 8.428571428571429,

        "FirstColumn": 1,

        "FirstRow": 9,

        "Name": "data",

        "RefersTo": "=Sheet1!$B$10:$H$10",

        "RowCount": 1,

        "RowHeight": 15,

        "Worksheet": "Sheet1"

      }

    ]

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
 
 
{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Ruby" tabName3="Go" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}



{{< /tab >}}

{{< tab tabNum="3" >}}



{{< gist "aspose-cells-cloud-gists" "c75da9aa06645e27e899a9fb6cdc134c" >}}

{{< /tab >}}

{{< /tabs >}}
