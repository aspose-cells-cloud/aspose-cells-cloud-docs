---
title: Kryptera en Excel-arbetsbok
second_title: Documen
linktitle: Kryptera en Excel-fil
type: docs
url: /sv/excel-file-encrypt/
aliases: [/encrypt-excel-workbooks/,/workbook/encrypt/]
keywords: Encrypt Excel workbook
description: Aspose.Cells Cloud REST API stöder kryptering av Excel-arbetsböcker. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 20
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Kryptera en Excel-arbetsbok
---
Denna REST API krypterar en Excel `workbook`.

**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|mapp|sträng|Original arbetsboksmapp.|
|lagringsnamn|sträng|Lagringsnamn.|

**Begäran om brödtextparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|kryptering|Arbetsbokkrypteringsbegäran||

**Arbetsbokkrypteringsbegäran**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|Krypteringstyp|sträng|XOR/Kompatibel/FörbättradKryptografiskProviderV1/StrongKryptografiskProvider|
|Nyckellängd|heltal||
|Lösenord|sträng||

## REST API

|**API**|**Typ**|**Beskrivning**|**Swagger-länk**|
|:- |:- |:- |:- |
|/celler/{namn}/kryptering|POSTA|Kryptera Excel-dokumentet|[PostEncryptDocument](https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt webbtjänsterna Aspose.Cells. Följande exempel visar hur man anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"EncryptionType\": \"XOR\", \"KeyLength\": 128, \"Password\": \"mateen\"}"

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

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
