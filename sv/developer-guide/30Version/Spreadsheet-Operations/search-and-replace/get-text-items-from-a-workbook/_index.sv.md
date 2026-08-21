---
title: "Hämta textobjekt från en Excel-arbetsbok"
ArticleTitle: "Hämta textobjekt från en Excel-arbetsbok med Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Hämta i arbetsbok"
type: docs
url: /sv/workbook/get-text-items/
aliases: [  /sv/get-text-items-from-a-workbook/ ]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, kalkylark, hämta textobjekt, arbetsbok"
description: "Hämta textobjekt från en Excel-arbetsbok med Aspose.Cells Cloud REST API. Tillgängligt via SDK:er för C#, Java, Python, PHP, Ruby, Go, Node.js, Perl och Swift."
---


## REST API

Detta REST API läser en arbetsboks **textobjekt** i en Excel-fil.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Begäranparametrar

| Parametername | Typ    | Plats  | Beskrivning                                             |
| ------------- | ------ | ------ | ------------------------------------------------------- |
| name          | string | path   | Namnet på arbetsboksfilen.                              |
| folder        | string | query  | Mappsökvägen i lagringen där arbetsboken finns.         |
| storageName   | string | query  | Namnet på lagringstjänsten.                             |

### **Svar**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad               | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksbegränsningen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
## Hur du använder GetWorkbookTextItems API med SDK:er

### GetWorkbookTextItems API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör en anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

Typiska HTTP-statuskoder:

| Kod | Beskrivning                                  |
|-----|----------------------------------------------|
| 200 | Begäran lyckades; textobjekt returneras.     |
| 401 | Oautentiserad – saknad eller ogiltig token.  |
| 403 | Förbjuden – otillräckliga behörigheter.      |
| 404 | Ej hittad – arbetsbok eller resurs hittades inte. |
| 500 | Internt serverfel – oväntat misslyckande.     |

### Använd Aspose.Cells Cloud SDK:er

Detta exempel använder API-version **v3.0**; se ändringslogg för nyare versioner. Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}
---