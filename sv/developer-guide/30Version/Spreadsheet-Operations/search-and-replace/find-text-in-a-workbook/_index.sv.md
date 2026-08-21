---
title: "Sök text i en Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Sök i arbetsbok"
type: docs
url: /sv/workbook/find-text/
aliases: [  /sv/find-text-in-a-workbook/ ]
weight: 30
keywords: "Aspose.Cells, sök text, Excel-API, arbetsbokssökning"
description: "Lär dig hur du använder Aspose.Cells Cloud API för att **söka efter text** i Excel-arbetsböcker (XLS‑X, ODS). Innehåller cURL-exempel, SDK-utdrag och respons-schema. Kom igång idag."
ArticleTitle: "Sök text i en Excel-arbetsbok med Aspose.Cells Cloud API"
---

Denna REST API söker efter text i en Excel-arbetsbok.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/findText
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Begärparametrar

| Parameter_name | Typ    | Plats  | Beskrivning                                               |
| -------------- | ------ | ------ | --------------------------------------------------------- |
| name           | string | path   | Namnet på Excel-arbetsboken.                              |
| text           | string | query  | Textsträng som ska sökas efter.                          |
| folder         | string | query  | Mapp som innehåller arbetsboken (valfritt).               |
| storageName    | string | query  | Namnet på lagringen där arbetsboken finns (valfritt).    |

### **Respons**

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

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filtrering lyckades; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
## Hur du använder PostWorkbooksTextSearch API med SDK:er

### PostWorkbooksTextSearch API-specificering

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbooksTextSearch" target="_blank" rel="noopener noreferrer">OpenAPI-specificeringen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/findText?text=a" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <your_access_token>"
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

Att använda ett SDK är det snabbaste sättet att utveckla. Ett SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbooksTextSearch.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbooksTextSearch.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbooksTextSearch.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbooksTextSearch.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbooksTextSearch.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbooksTextSearch.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbooksTextSearch.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbooksTextSearch.go" >}}

{{< /tab >}}

{{< /tabs >}}
---