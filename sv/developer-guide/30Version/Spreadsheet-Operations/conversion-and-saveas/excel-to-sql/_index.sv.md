---
title: Excel till SQ
second_title: Documen
linktitle: Excel till SQ
type: docs
url: /sv/convert-excel-file-to-sql-file/
keywords: Convert excel files to sql files
description: Aspose.Cells Cloud REST API stöder konvertering av Excel-filer till SQL-filer. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Excel till SQL
---
Denna REST API indikerar för `convert` en kalkylbladsfil till en SQL-formatfil.

**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|lösenord|sträng| Lösenordet som behövs för att öppna en Excel-fil.|
|lagringsnamn|sträng| Lagringsnamnet där filen finns.|
|kontrolleraExcelBegränsning|bool| Om begränsning av Excel-filen ska kontrolleras när användaren ändrar celler relaterade objekt.|

**Begäran om brödtextparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|datafil| datafil|Datafilen sparas i den första delen av det flerdelade innehållet.|

**Svar**

[Filinfo](/cells/sv/file-info/)

## REST API Specifikation

|**API**|**Typ**|**Beskrivning**|**Swagger-länk**|
|:- |:- |:- |:- |
|/celler/konvertera/sql|POSTA|Konvertera ett kalkylblad till en SQL-fil.|[PostConvertWorkbookToSQL](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL)|

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt webbtjänsterna Aspose.Cells. Följande exempel visar hur man anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.json",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andra API:er implementerar den här funktionen

[POST /celler/{namn}/sparaSom](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API låter dig spara MS Excel-filen som HTML-filen med ytterligare inställningar och spara resultatet till lagringsplatsen.

Denna REST API `convert` Excel-fil till HTML.

[PUT /celler/konvertera](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) Med API kan du konvertera MS Excel-filen till HTML-filen med ytterligare inställningar och spara resultatet i svaret.

Denna REST API `export` Excel-fil till HTML.

[HÄMTA /celler/{namn}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) Med API kan du konvertera MS Excel-filen till HTML-filen med ytterligare inställningar och spara resultatet i svaret.
