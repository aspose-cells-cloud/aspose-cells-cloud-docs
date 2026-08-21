---
title: "Hämta alla hyperlänkar – Aspose.Cells Cloud REST API"
type: docs
url: /hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, Hämta alla hyperlänkar, Excel API, REST API, Molntjänst SDK, cURL-exempel, hyperlänkar i kalkylark"
description: "Hämta alla hyperlänkar från ett kalkylark i en Excel-fil med Aspose.Cells Cloud REST API (v3.0). Innehåller HTTPS-slutpunkt, nödvändiga parametrar, cURL-exempel, svarsschema och kodexempel för SDK:er."
weight: 10
ArticleTitle: "Hämta alla hyperlänkar – Aspose.Cells Cloud REST API-dokumentation"
---

Detta REST API hämtar **alla hyperlänkar** från ett specifikt kalkylark i en Excel-arbetsbok.

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Begäranparametrar

| Parametername | Typ    | Plats  | Nödvändig | Standard | Beskrivning                            |
| ------------- | ------ | ------ | --------- | -------- | -------------------------------------- |
| name          | string | path   | Ja        | –        | Namn på Excel-dokumentet.              |
| sheetName     | string | path   | Ja        | –        | Namn på kalkylarket.                   |
| folder        | string | query  | Nej       | –        | Mapp som innehåller dokumentet.        |
| storageName   | string | query  | Nej       | –        | Namn på lagringstjänsten som ska användas. |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Exempel nedan visar hur API:et anropas med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

JSON-svaret innehåller ett `Hyperlinks`-objekt.

- **Count** – totalt antal hyperlänkar i kalkylarket.
- **HyperlinkList** – ett fält där varje post innehåller ett `link`-objekt. Egenskapen `Href` lagrar hyperlänkens adress, medan `Rel`, `Title` och `Type` tillhandahåller ytterligare metadata (ofta `null` för enkla länkar).

### Felrespons

| HTTP-kod | Anledning                                          | Exempel på kropp                                            |
| -------- | -------------------------------------------------- | ---------------------------------------------------------- |
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Invalid parameter value." }`   |
| **401**  | Obehörig – saknad eller ogiltig JWT-token.         | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Ej hittad – arbetsboken eller kalkylarket finns inte. | `{ "Code":"404", "Message":"File not found." }`             |
| **500**  | Internt serverfel – oväntat serverfel.              | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## Molntjänst SDK-familj

Att använda en SDK är det snabbaste sättet att integrera denna funktion. SDK:er hanterar detaljer på lägre nivå och låter dig fokusera på din affärslogik. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur Aspose.Cells webbtjänster anropas med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}