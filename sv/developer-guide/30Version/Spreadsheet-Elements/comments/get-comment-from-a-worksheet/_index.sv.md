---
title: "Hämta kalkylbladskommentar – Aspose.Cells Cloud API-dokumentation"
type: docs
url: /comments/get/
aliases: [/get-comment-from-a-worksheet/]
keywords: "Aspose.Cells, kalkylbladskommentar, API, GET, Excel"
description: "Lär dig hur du hämtar en kalkylbladskommentar med cellnamn med Aspose.Cells Cloud API (v3.0). Inkluderar begärans-URL, parametrar, cURL-exempel, svarsinformation och SDK-kodstycken."
weight: 10
ArticleTitle: "Hämta kalkylbladskommentar – Aspose.Cells Cloud API-dokumentation"
---

Denna REST API hämtar en kalkylbladskommentar med cellnamn med **Aspose.Cells Cloud**.

**Förutsättningar:** För att utföra den här åtgärden måste du inkludera en giltig JWT-åtkomsttoken i `Authorization`-headern (`Bearer <jwt token>`). Tokens kan erhållas via Aspose.Cells Cloud:s autentiseringsflöde som beskrivs i [Autentiseringsguide](/cells/authentication/).

## GetWorksheetComment API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parametername   | Typ    | Plats (URL-sökväg / Frågesträng) | Beskrivning                                                        |
| --------------- | ------ | -------------------------------- | ------------------------------------------------------------------ |
| name            | string | URL-sökväg                       | Namnet på Excel-filen.                                             |
| sheetName       | string | URL-sökväg                       | Namnet på kalkylbladet som innehåller kommentaren.                |
| cellName        | string | URL-sökväg                       | Cellens adress (t.ex. **A1**) vars kommentar ska hämtas.          |
| folder          | string | Frågesträng                      | Sökvägen till mappen där dokumentet lagras.                       |
| storageName     | string | Frågesträng                      | Namnet på lagringstjänsten.                                        |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Svar:** API:et returnerar ett JSON-objekt som innehåller ett `Comment`-objekt med följande fält:

| Fält                      | Typ     | Beskrivning                                           |
| ------------------------- | ------- | ----------------------------------------------------- |
| `CellName`                | string  | Cellens adress (t.ex. **A1**).                        |
| `Author`                  | string  | Namn på kommentarens författare.                      |
| `HtmlNote`                | string  | Kommentarinnehåll i HTML-format (om tillämpligt).     |
| `Note`                    | string  | Klartextversion av kommentaren.                       |
| `AutoSize`                | boolean | Indikerar om kommentarsrutan autoanpassas.            |
| `IsVisible`               | boolean | Bestämmer om kommentaren är synlig.                   |
| `Width`                   | integer | Bredd på kommentarsrutan (i tecken).                  |
| `Height`                  | integer | Höjd på kommentarsrutan (i tecken).                   |
| `TextHorizontalAlignment` | string  | Horisontell justering av texten (t.ex. **Bottom**).   |
| `TextOrientationType`     | string  | Textens orientering (t.ex. **TopToBottom**).          |
| `TextVerticalAlignment`   | string  | Vertikal justering av texten (t.ex. **Bottom**).      |

## Vanliga fel

- **401 Unauthorized (Obehörig)** – Verifiera att JWT-token är giltig, inte utgången och korrekt placerad i `Authorization`-headern.
- **404 Not Found (Hittades inte)** – Se till att filnamn, kalkylbladsnamn och celladress är korrekta och att filen finns i den angivna mappen/lagringen.
- **500 Internal Server Error (Internt serverfel)** – Kontrollera begärans payload på felaktigt formaterad data och verifiera att tjänsten är driftad.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                       |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request (Ogiltig begäran) | Saknade eller ogiltiga parametrar (t.ex. ostödd filtyp). |
| 401 | Unauthorized (Obehörig)     | Ogiltig eller saknad JWT-token.                  |
| 413 | Payload Too Large (För stor payload) | Uppladdad fil överskrider storleksgränsen.      |
| 500 | Internal Server Error (Internt serverfel) | Oväntat serverfel.                         |

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar lågnivådetaljerna och låter dig fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}