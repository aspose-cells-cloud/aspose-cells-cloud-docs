﻿---
title: Avskydda en Excel-arbetsbok
second_title: Aspose.Cells Cloud Documen
linktitle: Avskydda Excel fil
type: docs
url: /sv/excel-file-unprotect/
aliases: [/unprotect-excel-workbooks/, /workbook/unprotect/]
keywords: REST API, spreadsheets, excel, merg
description: "Cells.Cloud API för Excel operate: skydda en Excel-arbetsbok"
weight: 60
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Avskydda en Excel-arbetsbok
---
Denna REST API avskyddar en Excel `workbook`.

**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|mapp|sträng|Original arbetsboksmapp.|
|lagringsnamn|sträng|Lagringsnamn.|

**Begäran om brödtextparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|skydd|Arbetsbokskyddsbegäran||

**Arbetsbokskyddsbegäran**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|Skyddstyp|sträng|ALLT/INNEHÅLL/INGET/OBJEKT/SCENARIER/STRUKTUR/FÖNSTER|
|Lösenord|sträng||

## REST API

|**API**|**Typ**|**Beskrivning**|**Swagger-länk**|
|:- |:- |:- |:- |
|/celler/{namn}/skydd|RADERA|Avskydda ett dokument|[Ta bort och avskydda arbetsbok](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectWorkbook)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/DeleteUnProtectWorkbook) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt webbtjänsterna Aspose.Cells. Följande exempel visar hur man anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection" -H "accept: application/json"  -H "Content-Type: application/json" -d "{ \"ProtectionType\": \"all\", \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
