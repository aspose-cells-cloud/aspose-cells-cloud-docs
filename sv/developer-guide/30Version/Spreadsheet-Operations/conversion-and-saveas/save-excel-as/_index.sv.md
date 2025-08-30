---
title: Spara som Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Spara en
type: docs
url: /sv/save-an-excel-file-as-other-formats-files/
aliases: [/convert-excel-workbook-to-different-file-formats/, /saveas-other-formats/]
keywords: Save excel files as kinds of format files
description: Aspose.Cells Cloud REST API stöder sparning av Excel-filer som olika typer av formatfiler. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 30
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Spara som Excel
---
Denna REST API indikerar att Excel-filen `save` är en fil i ett annat format.

**Sökvägsparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|namn|sträng| Filnamnet.|

**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|nytt filnamn|sträng| nytt filnamn|
|ärAutoFitRaws|sträng| Anpassar automatiskt alla rader i den här arbetsboken. Standardvärdet är falskt.|
|ärAutoFitColumns|sträng| Anpassar automatiskt kolumnbredden i den här arbetsboken. Standardvärdet är falskt.|
|mapp|sträng|Original arbetsboksmapp.|
|lagringsnamn|sträng| Lagringsnamnet där filen finns.|
|outStorageName|sträng| Lagringsnamnet där den sparade filen finns.|
|kontrolleraExcelBegränsning|bool| Om begränsning av Excel-filen ska kontrolleras när användaren ändrar celler relaterade objekt.|
|område|sträng| De regionala inställningarna för arbetsboken.|
|sidaBredAnpassningPerArk|bool| Sidanpassning på arbetsbladet.|
|sidaHögAnpassaPerArk|bool| Sidans höjd får plats på arbetsbladet.|
|arknamn|sträng| Konvertera det angivna kalkylbladet.|
|sidaIndex|sträng| Konvertera den angivna sidan i kalkylbladet, arknamn är obligatoriskt.|
|enSidaPerArk|bool| Vid konvertering till formatet PDF, en sida per ark.|

**Begäran om brödtextparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|SparaAlternativ| Objekt|Spara-alternativet spara i den andra delen av det flerdelade innehållet.|

## REST API

|**API**|**Typ**|**Beskrivning**|**Resurslänk**|
|:- |:- |:- |:- |
|/celler/{namn}/sparaSom|POSTA|Exportera arbetsbok till format|[Spara dokument som](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt webbtjänsterna Aspose.Cells. Följande exempel visar hur man anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "SaveResult": {
    "SourceDocument": {
      "Href": "test.xlsx",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "DestDocument": {
      "Href": "test.pdf",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "AdditionalItems": []
  },
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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}
