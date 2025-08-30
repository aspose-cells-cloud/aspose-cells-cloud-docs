---
title: Konvertera en Excel-fil till ett annat format
second_title: Aspose.Cells Cloud Documen
linktitle: Konvertera Excel
type: docs
url: /sv/convert-an-excel-file-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/,/convert/excel-to-different-formats/]
keywords: Convert excel files to kinds of format files
description: Aspose.Cells Cloud REST API stöder konvertering av Excel-filer till olika typer av filer. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 10
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Convert Excel
---
Denna REST API indikerar att `convert` Excel-filen är till en fil i ett annat format.

Begäran är en HTTP-begäran med flerdelat innehåll (se[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)eller[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)Den första delen av flerdelat innehåll innehåller datafilen och den andra innehåller alternativ för att spara.

**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|formatera|sträng|Filformaten: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg, och så vidare.|
|lösenord|sträng| Lösenordet som behövs för att öppna en Excel-fil.|
|utväg|sträng| Sökväg för att spara resultatet. Om det är en enda fil ska `outPath` omfatta både filnamnet och filändelsen. Om det gäller flera filer ska `outPath` endast inkludera mappen.|
|lagringsnamn|sträng| Lagringsnamnet där filen finns.|
|kontrolleraExcelBegränsning|bool| Om begränsning av Excel-filen ska kontrolleras när användaren ändrar celler relaterade objekt.|
|strömformat|sträng| Formatet för indatafilströmmen.|
|område|sträng| De regionala inställningarna för arbetsboken.|
|sidaBredAnpassningPerArk|bool| Sidanpassning på arbetsbladet.|
|sidaHögAnpassaPerArk|bool| Sidans höjd får plats på arbetsbladet.|
|arknamn|sträng| Konvertera det angivna kalkylbladet.|
|sidaIndex|sträng| Konvertera den angivna sidan i kalkylbladet, arknamn är obligatoriskt.|
|enSidaPerArk|bool| Vid konvertering till formatet PDF, en sida per ark.|
|AutoRowsFit|bool| Anpassar automatiskt alla rader i den här arbetsboken.|
|AutoColumnsFit|bool| Anpassar automatiskt kolumnbredden i den här arbetsboken.|

**Begäran om brödtextparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|datafil| datafil|Datafilen sparas i den första delen av det flerdelade innehållet.|
|SparaAlternativ| Objekt|Spara-alternativet spara i den andra delen av det flerdelade innehållet.|

## REST API

|**API**|**Typ**|**Beskrivning**|**Swagger-länk**|
|:- |:- |:- |:- |
|/celler/konvertera|SÄTTA|Konverterar arbetsboken från begäraninnehåll till något format|[PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt webbtjänsterna Aspose.Cells. Följande exempel visar hur man anropar Cloud API med cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
