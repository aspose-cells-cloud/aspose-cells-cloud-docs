---
title: Lägg till ett dynamiskt datumfilter i ett Excel-arbetsblad
second_title: Aspose.Cells Cloud Documen
linktitle: Lägg till dynamiskt filter
type: docs
url: /sv/autofilter/add-dynamic-filter/
aliases: [/filter-a-list-using-dynamic-filter/,/autofilter/add-a-dynamic-filter/]
keywords: Adds a dynamic filter on an Excel worksheet
description: "Aspose.Cells Cloud API stöder tillägg av dynamiska filter på ett Excel-arbetsblad. SDK:n stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift."
weight: 65
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Lägg till ett dynamiskt datumfilter i ett Excel-kalkylblad
---
Denna REST API anger att `dynamic filter` ska läggas till på ett Excel-arbetsblad.

## RSET API

```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
 
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg||
| arknamn| sträng| väg||
| räckvidd| sträng| fråga||
| fältindex| heltal| fråga||
| dynamiskFiltertyp| sträng| fråga||
| matchBlanks| boolesk| fråga||
| uppdatera| boolesk| fråga||
| mapp| sträng| fråga||
| lagringsnamn| sträng| fråga| lagringsnamn.|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDynamicFilter) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true"  \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

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

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDynamicFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDynamicFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDynamicFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDynamicFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDynamicFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDynamicFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDynamicFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDynamicFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
