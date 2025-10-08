---
title: Hämtar Excel-filen till ett annat format
second_title: Documen
linktitle: Hämta Excel
type: docs
url: /sv/get different formats files/
aliases: [/export-excel-workbook-to-different-file-formats/, /export-different-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API stöder hämta Excel-filer till olika typer av filformat. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 10
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Hämtar Excel-filen till andra format
---
Denna REST API indikerar att `get` Excel-filen är till en fil i ett annat format.

**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|formatera|sträng|Filformaten: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, och så vidare.|
|lösenord|sträng|Lösenordet som behövs för att öppna en Excel-fil.|
|ärAutoFit|sträng|Anpassar automatiskt rad- och kolumnbredden i den här arbetsboken. Standardvärdet är falskt.|
|endastSparaTabell|sträng|sant/falskt|
|utväg|sträng| Sökväg för att spara resultatet. Om det är en enda fil ska `outPath` omfatta både filnamnet och filändelsen. Om det gäller flera filer ska `outPath` endast inkludera mappen.|
|outStorageName|sträng| Lagringsnamnet där den sparade filen finns.|
|kontrolleraExcelBegränsning|bool| Om begränsning av Excel-filen ska kontrolleras när användaren ändrar celler relaterade objekt.|
|område|sträng| De regionala inställningarna för arbetsboken.|
|sidaBredAnpassningPerArk|bool| Sidanpassning på arbetsbladet.|
|sidaHögAnpassaPerArk|bool| Sidans höjd får plats på arbetsbladet.|
|enSidaPerArk|bool| Vid konvertering till formatet PDF, en sida per ark.|
|mapp|sträng|Original arbetsboksmapp.|
|lagringsnamn|sträng|Lagringsnamnet där filen finns.|

## REST API

|**API**|**Typ**|**Beskrivning**|**Swagger-länk**|
|:- |:- |:- |:- |
|/celler/{namn}|FÅ|Exporterar arbetsboken till ett annat format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt webbtjänsterna Aspose.Cells. Följande exempel visar hur man anropar Cloud API med cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
