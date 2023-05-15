---
title: Lägg till datumfilter i ett Excel arbetsblad
second_title: Aspose.Cells Cloud Documen
linktitle: Lägg till datumfilter
type: docs
url: /sv/autofilter/add-date-filter/
aliases: [/add-date-filter-in-a-worksheet/,/autofilter/add-a-date-filter/]
keywords: Adds a date filter on an Excel worksheet
description: Aspose.Cells Cloud API stöder att lägga till ett datumfilter på ett Excel kalkylblad.SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 65
---
Detta REST API indikerar att lägga till ett `date filter` på ett Excel arbetsblad.

## RSET API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter

```
Begärans parametrar är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| Väg|Arbetsbokens namn.|
| arknamn| sträng| Väg| Kalkylbladets namn.|
|räckvidd|sträng| Fråga||
|fieldIndex|heltal| Fråga||
|dateTimeGroupingType|sträng| Fråga| Dag/timme/minut/månad/andra/år|
|år|heltal| Fråga||
|månad|heltal| Fråga||
|dag|heltal| Fråga||
|timme|heltal| Fråga||
|minut|heltal| Fråga||
|andra|heltal| Fråga||
|matchBlanks|sträng| Fråga|sant falskt|
|uppdatera|sträng| Fråga|sant falskt|
|mapp|sträng| Fråga|Original arbetsboksmapp.|
|lagringsnamn|sträng| Fråga|Lagringsnamn.|


 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
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

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-AddDataFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-AddDateWorksheetExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-PutWorksheetDateFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-put_worksheet_date_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-AddDateFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-AddDateWorksheetExample-1.java" >}}



{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-AddDateFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "54cd61aee4496583dfacaf7dadef6463" >}}

{{< /tab >}}

{{< /tabs >}}
