---
title: "Ställ in zoom för ett Excel-ark – Aspose.Cells Cloud API v3.0"
second_title: "Dokument"
linktitle: "Zoom"
type: docs
url: /worksheets/zoom/
aliases: [/set-zoom-in-excel-worksheet/]
keywords: "Aspose.Cells, Excel-zoom, ark-zoom, REST API, molntjänst, Excel-automatisering"
description: "Lär dig hur du ställer in arkzoom (10–400 %) med Aspose.Cells Cloud API v3.0. Inkluderar cURL- och SDK-exempel samt felhantering."
weight: 20
ArticleTitle: "Ställ in zoom för ett Excel-ark – Aspose.Cells Cloud API v3.0"
---

Denna REST API ställer in zoomvärdet för ett Excel-ark. **Autentisering** krävs; inkludera en giltig Bearer JWT-token i `Authorization`-huvudet för varje förfrågan.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **Förfrågningsparametrar**

| Parameter   | Typ     | Plats  | Beskrivning                                                       |
| ----------- | ------- | ------ | ----------------------------------------------------------------- |
| name        | string  | path   | Namn på Excel-filen (arbetsboken).                                |
| sheetName   | string  | path   | Namn på arket som ska ändras.                                     |
| value       | integer | query  | Zoomprocent (tillåtet intervall **10–400**, t.ex. `40` för 40 %). |
| folder      | string  | query  | Mappväg där filen är lagrad.                                      |
| storageName | string  | query  | Namn på lagringstjänsten.                                         |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör en förfrågan till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <ditt_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Information om felresponser**  
Möjliga HTTP-statuskoder inkluderar:

- `400 Bad Request` – saknade eller ogiltiga parametrar.
- `401 Unauthorized` – saknad eller ogiltig JWT-token.
- `404 Not Found` – angiven fil eller ark finns inte.
- `500 Internal Server Error` – oväntat serverfel.

Varje felrespons returnerar en JSON-kropp med en `Code` och en beskrivande `Message`.

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör förfrågningar till Aspose.Cells-webbtjänster med diverse SDK:er:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}