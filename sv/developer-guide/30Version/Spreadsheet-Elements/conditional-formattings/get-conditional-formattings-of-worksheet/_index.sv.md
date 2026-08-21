---
title: "Hämta villkorsformateringsregler"
type: docs
url: /conditional-formattings/get-all/
aliases: [/get-conditional-formattings-of-worksheet/]
keywords: "Aspose.Cells Cloud, REST API, Excel, Villkorsformatering, Arbetsblad, Villkorsformaterings-API"
description: "Hämta alla villkorsformateringsregler som tillämpas på ett arbetsblad med Aspose.Cells Cloud REST API. Innehåller begärsyntax, autentiseringstred, parametrar, koncisa svarsexempel och felhantering."
weight: 20
---

Denna REST API hämtar de villkorsformateringsregler som tillämpas på ett arbetsblad.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Begärparametrar

| Parameternamn | Typ   | Plats  | Beskrivning                                |
| ------------- | ----- | ------ | ------------------------------------------ |
| name          | string | path  | Namnet på Excel-filen.                     |
| sheetName     | string | path  | Namnet på arbetsbladet.                    |
| folder        | string | query | Mappsökvägen där filen lagras.             |
| storageName   | string | query | Namnet på lagringstjänsten (valfritt).     |

### Felresponser

| HTTP-kod | Anledning                                         | Exempel på brödtext                                                 |
| -------- | ------------------------------------------------- | ------------------------------------------------------------------- |
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**  | Otillåten – saknad eller ogiltig JWT-token.       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Hittades inte – arbetsboken eller arbetsbladet finns inte. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**  | Internt serverfel – oväntat serverfel.             | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/GetWorksheetConditionalFormattings" target="_blank">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status": "OK",
  "ConditionalFormattings": {
    "Count": 1,
    "ConditionalFormattingList": [
      {
        "sqref": "A1:B10",
        "FormatConditions": [
          {
            "Priority": 1,
            "Type": "CellValue",
            "Operator": "GreaterThan",
            "Formula1": "100",
            "Style": {
              "Font": {
                "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                "IsBold": true
              }
            }
          }
        ]
      }
    ]
  }
}
```

_Exemplet ovan visar endast de mest relevanta fälten för att hålla nyttolasten kompakt._

**Svarparametrar**

| Parameter                             | Typ    | Beskrivning                                                    |
|---------------------------------------|--------|----------------------------------------------------------------|
| Status                                | string | Resultatstatus för begäran (t.ex. **OK**).                     |
| ConditionalFormattings                | object | Container för villkorsformateringsdata.                        |
| ConditionalFormattings.Count          | integer | Antal returnerade villkorsformateringsregler.                 |
| ConditionalFormattings.ConditionalFormattingList | array | Lista över villkorsformateringsobjekt.                        |
| ConditionalFormattingList[].sqref     | string | Cellomfång till vilken formateringen tillämpas (t.ex. **A1:B10**). |
| ConditionalFormattingList[].FormatConditions | array | Samling av formateringsvillkorsobjekt för omfången.           |
| FormatConditions[].Priority           | integer | Utvärderingsprioritet för villkoret.                           |
| FormatConditions[].Type               | string | Typ av villkor (t.ex. **CellValue**).                          |
| FormatConditions[].Operator           | string | Operator som används för villkoret (t.ex. **GreaterThan**).    |
| FormatConditions[].Formula1           | string | Första formeln eller värde för villkoret.                     |
| FormatConditions[].Style              | object | Formatering som tillämpas när villkoret är uppfyllt.           |
| Style.Font.Color                      | object | RGBA-färgdefinition för teckensnittet.                         |
| Style.Font.IsBold                     | boolean | Anger om teckensnittet är fetstilt.                            |

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                |
|-----|-----------------------------|------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Otillåten                   | Ogiltig eller saknad JWT-token.                            |
| 413 | Nyttolast för stor          | Den uppladdade filen överskrider storleksgränsen.          |
| 500 | Internt serverfel           | Oväntat serverfel.                                         |

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Ta en titt på <a href="https://github.com/aspose-cells-cloud" target="_blank">GitHub-lagringsplatsen</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-GetWorksheetConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-get-conditional-formatting-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-get_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-GetWorksheetConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-GetWorksheetConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b2a10009556f14d1f939a8433925c5f6" >}}

{{< /tab >}}

{{< /tabs >}}
---