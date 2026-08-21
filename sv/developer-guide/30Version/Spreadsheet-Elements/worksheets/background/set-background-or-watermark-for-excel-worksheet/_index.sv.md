---
title: "Ställ in bakgrund på ett Excel-ark"
ArticleTitle: "Ställ in bakgrund på ett Excel-ark – Aspose.Cells Cloud API-guide"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /worksheets/background/add/
aliases: [/set-background-or-watermark-for-excel-worksheet/]
keywords: "Aspose.Cells, Excel, ark, bakgrund, REST API, SDK, lägg till bild"
description: "Lär dig hur du lägger till en bakgrundsbild (PNG, JPEG, BMP) till ett Excel-ark med Aspose.Cells Cloud REST API. Inkluderar slutpunkt, nödvändiga parametrar, autentiseringssteg, cURL-exempel och SDK-kodexempel."
weight: 180
---

Denna REST API lägger till en bakgrundsbild till ett ark.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Begäran parametrar**

| Parameter namn | Typ    | Plats  | Beskrivning                                                     |
| -------------- | ------ | ------ | --------------------------------------------------------------- |
| name           | string | path   | Namn på Excel-arbetsboken.                                      |
| sheetName      | string | path   | Namn på det ark som bilden ska tillämpas på.                   |
| imageFile      | file   | body   | Binär bildfil (PNG, JPEG, BMP, etc.) som ska användas som bakgrund. |
| folder         | string | query  | Mapp i lagringen där arbetsboken finns.                         |
| storageName    | string | query  | Namn på Aspose Cloud-lagringen.                                 |

**Stödda format och begränsningar**

- Godkända bildändelser: **PNG, JPEG, BMP, GIF**.
- Maximal filstorlek: **5 MB**.
- Bilden är fylld i mönster för att fylla hela arkets bakgrund.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

_Möjliga felsvar_

| HTTP-kod | Beskrivning                                                  |
| -------- | ------------------------------------------------------------ |
| 400      | Felaktig begäran – saknade eller ogiltiga parametrar.        |
| 401      | Auktoriseringsfel – ogiltig eller utgången JWT-token.         |
| 404      | Inte hittad – arbetsboken eller arket finns inte.            |
| 500      | Internt serverfel – oväntat tillstånd på servern.             |

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}