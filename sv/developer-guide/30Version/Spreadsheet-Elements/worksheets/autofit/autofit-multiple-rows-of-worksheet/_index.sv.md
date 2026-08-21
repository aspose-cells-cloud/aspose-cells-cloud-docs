---
title: "Autojustera flera rader i ett Excel-ark"
second_title: "Dokument"
linktitle: "Rader"
type: docs
url: /worksheets/autofit/rows/
aliases: [/autofit-multiple-rows-of-worksheet/]
keywords: "autojustera rader, Excel, Aspose.Cells Cloud, REST API, kalkylark, kalkylark"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att autojustera flera rader i ett Excel-ark. Inkluderar begärandsyntax, parametrar, cURL-exempel, SDK-utdrag och felhantering."
weight: 40
ArticleTitle: "Autojustera flera rader i ett Excel-ark – Aspose.Cells Cloud API-dokumentation"
---

Denna REST API justerar automatiskt höjden på rader i ett Excel-ark.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrows
```

### **Begärparametrar**

| Parameternamn         | Typ     | Plats  | Beskrivning                                                                                                                         | Krävs  |
| --------------------- | ------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------- | ------ |
| **name**              | string  | path   | Namnet på Excel-filen.                                                                                                              | ✔      |
| **sheetName**         | string  | path   | Namnet på kalkylarket.                                                                                                              | ✔      |
| **autoFitterOptions** | object  | body   | Alternativ som styr hur rader autojusteras (t.ex. ignorera dolda rader). Se kortfattad fältbeskrivning nedan.                      | ✖      |
| **startRow**          | integer | query  | Den första raden att autojustera (1-baserat index).                                                                                | ✔      |
| **endRow**            | integer | query  | Den sista raden att autojustera (inklusive).                                                                                       | ✔      |
| **onlyAuto**          | boolean | query  | När `true` justerar API:et endast rader vars höjd automatiskt beräknas av Excel. När `false` utförs en fullständig autojustering. | ✖      |
| **folder**            | string  | query  | Mappen som innehåller dokumentet.                                                                                                   | ✖      |
| **storageName**       | string  | query  | Namnet på lagringstjänsten.                                                                                                         | ✖      |

**autoFitterOptions**-fält (alla valfria):

- `AutoFitMergedCells` _(boolean)_ – Om `true` tas sammanfogade celler hänsyn till vid beräkning av radhöjd.
- `IgnoreHidden` _(boolean)_ – När `true` ignoreras dolda rader under autojusteringsprocessen.
- `OnlyAuto` _(boolean)_ – Speglar frågeparametern `onlyAuto`; när den är inställd åsidosätts värdet från frågan.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetRows) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur Cloud API:et anropas med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrows?startRow=1&endRow=7" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": false}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Typiska felsvar inkluderar:

- **400 Bad Request** – Ogiltiga parametervärden eller felaktigt formaterad JSON-kropp.
- **401 Unauthorized** – Saknas eller ogiltig JWT-token.
- **404 Not Found** – Den angivna filen eller det angivna kalkylarket finns inte.
- **500 Internal Server Error** – Ett oväntat serverfel uppstod.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknas eller ogiltiga parametrar (t.ex. ej stödd filtyp). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                         |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internal Server Error       | Oväntat serverfel.                                      |

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur Aspose.Cells-webbtjänster anropas med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}