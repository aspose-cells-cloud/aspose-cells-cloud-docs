---
title: Hur man skapar en Excel-arbetsbok med en mallfil
second_title: Aspose.Cells Cloud Documen
linktitle: Mallfil
type: docs
url: /sv/create-an-excel-file-with-template-file/
aliases: [/create-excel-workbook-from-a-template-file/,/workbook/new-from-a-template-file/,/workbook/create/template-file/]
keywords: How to create an Excel workbook with a smart marker template
description: Aspose.Cells Cloud REST API hur man skapar en Excel arbetsbok från en smart markörmall. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift
weight: 30
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Hur man skapar en Excel-arbetsbok med en mallfil
---
Denna REST API indikerar att `workbook` ska skapas från en `template file`.

**Frågeparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|mallFil|sträng||
|datafil|sträng||
|ärSkrivÖver|sträng| sant/falskt|
|mapp|sträng|Original arbetsboksmapp.|
|lagringsnamn|sträng|Lagringsnamn.|

**Begäran om brödtextparameter**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
|data|fil||

## REST API

|**API**|**Typ**|**Beskrivning**|**Swagger-länk**|
|:- |:- |:- |:- |
|/celler/{namn}|SÄTTA|Skapa en ny Excel-arbetsbok från en mallfil|[Lägg till arbetsbokSkapa](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate)|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt webbtjänsterna Aspose.Cells. Följande exempel visar hur man anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?templateFile=Calendar.xlsx&dataFile=Sample_Data.xml&isWriteOver=true" -H "accept: application/json" -H "x-aspose-client: Containerize.Swagger"


```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{
  "Status": "string",
  "Workbook": {
    "FileName": "string",
    "Links": [
      {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    ],
    "Worksheets": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DefaultStyle": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "DocumentProperties": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Names": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "Settings": {
      "link": {
        "Href": "string",
        "Rel": "string",
        "Title": "string",
        "Type": "string"
      }
    },
    "IsWriteProtected": "string",
    "IsProtected": "string",
    "IsEncryption": "string",
    "Password": "string"
  }
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateTemplate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateTemplate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateTemplate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateTemplate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateTemplate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateTemplate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateTemplate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateTemplate.go" >}}

{{< /tab >}}

{{< /tabs >}}
