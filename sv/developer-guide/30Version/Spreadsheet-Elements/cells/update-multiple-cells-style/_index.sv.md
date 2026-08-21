---
title: "Uppdatera flera cellers stil – Aspose.Cells Cloud API-referens (v3.0)"
type: docs
url: /sv/update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "uppdatera flera cellers stil", "Excel-cellstil-API", "molntjänst (SDK)", "REST API", "cURL-exempel", "JSON-förfrågan", "JWT-autentisering"]
description: "Lär dig hur du uppdaterar stil för ett intervall av celler i en Excel-arbetsbok med Aspose.Cells Cloud REST API v3.0. Inkluderar endpoint, HTTP-metod, parametrar, cURL- och SDK-exempel, autentisering, felhantering och versionsinformation."
ArticleTitle: "Uppdatera flera cellers stil – Aspose.Cells Cloud API-referens (v3.0)"
---

## REST API

Denna REST API ställer in **stilen** för ett intervall av celler i en Excel-arbetsbok.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Förfrågningsparametrar

| ParameterNamn   | Typ    | Plats  | Beskrivning |
|----------------|--------|--------|-------------|
| **name**       | string | path   | Namn på arbetsboken. |
| **sheetName**  | string | path   | Namn på kalkylbladet. |
| **range**      | string | query  | Cellintervallet (t.ex. `A1:A10`). |
| **style**      | object | body   | JSON-objekt som definierar den stil som ska tillämpas. |
| **folder**     | string | query  | Mapp som innehåller arbetsboken. |
| **storageName**| string | query  | Namn på lagringsutrymmet. |

#### Style-objekt
`style`-JSON-objektet representerar cellformatering. Det kan innehålla någon av följande valfria egenskaper:

- **Font** – Teckensnittsinställningar (`Name`, `Size`, `IsBold`, `IsItalic`, `Color`, etc.).  
- **BackgroundColor** – Bakgrundsfärg i ARGB-format.  
- **ForegroundColor** – Förgrundsfärg i ARGB-format.  
- **Name**, **CultureCustom**, **Custom** – Ytterligare stilmetadata.

## **Svar**

Returnerar CellCloudResponse.

- **Översikt över svarsfält**

| Fält            | Typ     | Beskrivning                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`        | string  |                                                       |
| `Code`          | integer | 200,400,401,500,...                                 |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod  | Betydelse                   | Beskrivning                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter har tillämpats korrekt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Oautentiserad               | Ogiltig eller saknad JWT-token. |
| 413  | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500  | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PostUpdateWorksheetRangeStyle API med SDK:er

### PostUpdateWorksheetRangeStyle API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle) innehåller hela schemat.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells molntjänster. Följande exempel visar hur man gör förfrågningar till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells molntjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}
---