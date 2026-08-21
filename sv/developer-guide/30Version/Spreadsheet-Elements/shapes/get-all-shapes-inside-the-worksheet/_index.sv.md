---
title: "Hämta alla former på ett Excel-arbetsblad"
second_title: "Document"
linktitle: "Get-all"
type: docs
url: /sv/shapes/get-all/
aliases: [/sv/get-all-shapes-inside-the-worksheet/]
keywords: "Aspose.Cells, Molntjänst-API, Excel-former, hämta former, REST, SDK"
description: "Hämta alla former (diagram, bilder, textrutor) från ett arbetsblad med Aspose.Cells Cloud REST API. Innehåller cURL-exempel, SDK-utdrag, autentiseringssteg och felhantering."
ArticleTitle: "Hämta alla former på ett Excel-arbetsblad"
weight: 10
---

Detta REST API möjliggör hämtning av alla former på ett Excel-arbetsblad.

## Säkerhet och autentisering
Aspose.Cells molntjänst-API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### Begärandeparametrar

| Parameternamn   | Typ    | Plats  | Beskrivning                                                                                              |
| --------------- | ------ | ------ | -------------------------------------------------------------------------------------------------------- |
| **name**        | string | path   | Namnet på Excel-filen.                                                                                   |
| **sheetName**   | string | path   | Namnet på arbetsbladet.                                                                                  |
| **folder**      | string | query  | Mappen som innehåller dokumentet.                                                                        |
| **storageName** | string | query  | Namnet på lagringstjänsten som ska användas.                                                             |
| **include**     | string | query  | Ställ in på `details` för att returnera fullständiga formegenskaper; annars returneras endast `link`-objekten. |

> **Valfritt**: `folder`, `storageName` och `include` kan utelämnas om filen finns i rotlagringen.

Du kan använda kommandoradsverktyget cURL för att komma åt Aspose.Cells webbtjänster. Exemplet nedan visar en begäran som inkluderar de valfria frågeparametrarna.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Svarsfält

`Shapes`-objektet innehåller en lista med `Shape`-objekt. Varje form innehåller följande egenskaper (om flaggan `include=details` används; annars returneras endast `link`-objektet).

| Egenskap   | Typ    | Beskrivning                                                               |
| ---------- | ------ | ------------------------------------------------------------------------- |
| **Name**   | string | Namnet som tilldelats formen (t.ex. “Diagram 1”).                         |
| **Type**   | string | Formens typ (t.ex. `Chart`, `Picture`, `TextBox`).                        |
| **Top**    | number | Avståndet i punkter från övre kanten av arbetsbladet till formen.         |
| **Left**   | number | Avståndet i punkter från vänstra kanten av arbetsbladet till formen.      |
| **Width**  | number | Formens bredd i punkter.                                                  |
| **Height** | number | Formens höjd i punkter.                                                   |
| **Link**   | object | Hyperlänksinformation (`Href`, `Rel`, `Type`, `Title`).                   |

## Felhantering

| HTTP-status | Beskrivning                                       | Exempel på felkropp                                           |
| ----------- | ------------------------------------------------- | ------------------------------------------------------------ |
| **400**     | Felaktig begäran – felaktiga parametrar.          | `{ "Code": 400, "Message": "Ogiltigt parametervärde." }`     |
| **401**     | Obehörig – saknad eller ogiltig token.            | `{ "Code": 401, "Message": "Tillgångstoken saknas eller är ogiltig." }` |
| **404**     | Hittades inte – arbetsbok eller arbetsblad finns inte. | `{ "Code": 404, "Message": "Fil eller arbetsblad hittades inte." }` |
| **500**     | Internt serverfel – oväntat tillstånd.            | `{ "Code": 500, "Message": "Ett oväntat fel inträffade." }`  |

En lyckad begäran returnerar **HTTP 200** med ett `Shapes`-objekt som innehåller formlistan, som illustreras i ovanstående svarsexempel.

API:et tillämpar en gräns på **150 begäranden per minut per JWT-token**. Överskridning av denna gräns returnerar **HTTP 429** med en `Retry-After`-header som anger när en ny försök ska göras.

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagret](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}