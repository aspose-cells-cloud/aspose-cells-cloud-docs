---
title: "Hämta textobjekt från ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Hämta textobjekt i arbetsblad"
type: docs
url: /sv/worksheets/get-text-items/
aliases: [  /sv/get-text-items-from-a-worksheet/ ]
weight: 20
keywords: "Aspose.Cells, molntjänst-API, Excel, arbetsblad, textobjekt, REST"
description: "Hämta alla textobjekt från ett specifikt arbetsblad i en Excel-fil med Aspose.Cells Cloud REST API. Innehåller exempel med cURL, SDK-kod, autentiseringssteg och svarsschema."
ArticleTitle: "Hämta textobjekt från ett Excel-arbetsblad"
---

## REST API

Detta REST API läser ett arbetsblads textobjekt i en Excel-fil.

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Begäranparametrar


| Parameternamn | Typ   | Plats  | Krävs | Beskrivning                                   |
| ------------- | ----- | ------ | ----- | --------------------------------------------- |
| name          | string | path   | Ja    | Namn på arbetsboksfilen.                      |
| sheetName     | string | path   | Ja    | Namn på arbetsbladet.                         |
| folder        | string | query  | Nej   | Sökväg till mappen som innehåller arbetsboken. |
| storageName   | string | query  | Nej   | Namn på Aspose Cloud-lagringen.               |

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

| Kod | Betydelse                   | Beskrivning                                       |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder GetWorksheetTextItems API med SDK:er

### GetWorksheetTextItems API-specificering

[OpenAPI-specificeringen](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"} definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
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

### Använd Aspose.Cells Cloud SDK:er

SDK:er förenklar integrationen genom att hantera detaljer på låg nivå och låta dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}

---