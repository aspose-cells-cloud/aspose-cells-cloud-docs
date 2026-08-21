---
title: "Hämta hyperlänk i kalkylblad"
type: docs
url: /hyperlinks/get/
keywords: "Aspose.Cells Cloud, Hämta hyperlänk i kalkylblad, Excel-hyperlänk-API, REST, JWT-autentisering, Excel-kalkylblad, API-slutpunkt"
description: "Hämta en specifik hyperlänk från ett Excel-kalkylblad med Aspose.Cells Cloud API (v3.0). Innehåller slutpunktsinformation, parametrar, cURL-exempel, autentiseringsuppgifter, felhantering och SDK-utdrag."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Hämta hyperlänk i kalkylblad"
---

Denna REST API hämtar en **hyperlänk** i ett kalkylblad med **Aspose.Cells Get Hyperlink API**.

## Säkerhet och autentisering

Aspose.Cells Cloud-API:n är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
Innan du anropar slutpunkten, skaffa en JWT-åtkomsttoken med ditt klient-ID och hemlighet och inkludera den i `Authorization: Bearer <jwt token>`-headern.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Begäranparametrar

| Parameter namn | Typ     | Position | Beskrivning                                      |
| -------------- | ------- | -------- | ------------------------------------------------ |
| name           | string  | path     | Namnet på Excel-filen.                           |
| sheetName      | string  | path     | Namnet på kalkylbladet som innehåller länken.    |
| hyperlinkIndex | integer | path     | Nollbaserat index för den hyperlänk som ska hämtas. |
| folder         | string  | query    | Mappen där dokumentet lagras.                    |
| storageName    | string  | query    | Namnet på lagringstjänsten.                      |

### Felrespons

| HTTP-kod | Anledning                                          | Exempel på kropp                                            |
| -------- | -------------------------------------------------- | ---------------------------------------------------------- |
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Invalid parameter value." }`  |
| **401**  | Oautentiserad – saknad eller ogiltig JWT-token.     | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Ej hittad – arbetsboken eller kalkylbladet finns inte. | `{ "Code":"404", "Message":"File not found." }`            |
| **500**  | Internt serverfel – oväntat serverfel.              | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Besök [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}