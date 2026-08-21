---
title: "Ta bort cellområde – Aspose.Cells Cloud API-dokumentation"
type: docs
url: /conditional-formattings/delete-cell-area/
aliases: [/remove-cell-area-from-conditional-formatting/]
keywords: "Aspose.Cells Cloud, ta bort cellområde, API för villkorsformatering, Excel REST API"
description: "Använd Aspose.Cells Cloud REST API för att ta bort ett specifikt cellområde från villkorsformatering i ett Excel-ark. Innehåller exempel i ASP.NET, Java och Python."
ArticleTitle: "Ta bort cellområde – Aspose.Cells Cloud API-dokumentation"
weight: 70
---

Denna REST API tar bort ett cellområde från en regel för villkorsformatering.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### Parametrar för begäran

| Parametername | Typ     | Plats  | Beskrivning                                                       |
| ------------- | ------- | ------ | ----------------------------------------------------------------- |
| `name`        | string  | path   | Namnet på Excel-filen.                                            |
| `sheetName`   | string  | path   | Namnet på arket som innehåller villkorsformateringen.            |
| `startRow`    | integer | query  | Nollbaserat index för den första raden i det område som ska tas bort. |
| `startColumn` | integer | query  | Nollbaserat index för den första kolumnen i det område som ska tas bort. |
| `totalRows`   | integer | query  | Antal rader i det område som ska tas bort.                        |
| `totalColumns`| integer | query  | Antal kolumner i det område som ska tas bort.                     |
| `folder`      | string  | query  | Mapp i molnlagring där filen finns (valfritt).                    |
| `storageName` | string  | query  | Namn på lagringstjänsten (valfritt).                              |

### Felrespons

| HTTP-status | Kod             | Beskrivning                                         | Exempel på JSON                                               |
| ----------- | --------------- | --------------------------------------------------- | ------------------------------------------------------------- |
| 400         | `BadRequest`    | Saknade eller ogiltiga parametrar.                  | `{ "Code": "400", "Message": "Ogiltiga begärningsparametrar." }` |
| 401         | `Unauthorized`  | Saknad eller ogiltig JWT-token.                     | `{ "Code": "401", "Message": "Autentisering misslyckades." }`      |
| 404         | `NotFound`      | Fil, ark eller villkorsformatering hittades inte.   | `{ "Code": "404", "Message": "Resursen hittades inte." }`         |
| 500         | `InternalError` | Oväntat serverfel.                                  | `{ "Code": "500", "Message": "Internt serverfel." }`      |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells Cloud-tjänster. Följande exempel visar hur du anropar slutpunkten **Ta bort cellområde** med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-lagret](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}