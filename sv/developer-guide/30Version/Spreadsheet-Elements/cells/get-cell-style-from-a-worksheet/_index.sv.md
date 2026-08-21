---
title: "Hämta cellstil från ett kalkylblad – Aspose.Cells Cloud API"
type: docs
url: /sv/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, REST API, cellstil, kalkylark, molnbaserat SDK, API-dokumentation"
description: "Lär dig hur du hämtar stilinformation för en specifik cell i ett Excel-kalkylblad med Aspose.Cells Cloud REST API v3. Innehåller cURL-exempel, svarsschema, statuskoder och SDK-utdrag."
ArticleTitle: "Hämta cellstil från ett kalkylblad med Aspose.Cells Cloud API – detaljerad guide"
---

Använd detta REST API för att hämta **stilen** på en cell i ett Excel-kalkylblad.

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärningsparametrar


| Parameternamn | Typ   | Plats  | Beskrivning                        |
| ------------- | ----- | ------ | ---------------------------------- |
| name          | string | path   | Namnet på Excel-dokumentet.        |
| sheetName     | string | path   | Namnet på kalkylbladet.            |
| cellName      | string | path   | Cellens adress (t.ex. A1).         |
| folder        | string | query  | Mappen som innehåller filen.       |
| storageName   | string | query  | Namnet på den lagringsplats som ska användas. |


### **Svar**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering misslyckades  | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel           | Oväntat serverfel.                                      |

**Felaktiga svar**  
Typiska fel-svar för denna slutpunkt följer det standardiserade Aspose.Cells-felformatet. Ett 400 Bad Request-svar ser till exempel ut så här:

```json
{
  "Code": 400,
  "Message": "Ogiltig parameter 'cellName'.",
  "Description": "Cellnamnet som angavs är inte i giltigt A1-format."
}
```

Ett 401 Unauthorized-svar ser i sin tur ut så här:

```json
{
  "Code": 401,
  "Message": "Autentisering misslyckades.",
  "Description": "JWT-token saknas eller är ogiltig."
}
```

## Hur man använder GetWorksheetCellStyle API med SDK:er

### GetWorksheetCellStyle API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör ett anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
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

## Svarschema

| Fält                     | Typ    | Beskrivning                                                          |
| ------------------------ | ------ | -------------------------------------------------------------------- |
| **Style**                | objekt | Container för alla stilrelaterade egenskaper för cellen.            |
| Style.Font               | objekt | Teckensnittsinställningar (namn, storlek, färg, stilflaggor).        |
| Style.Font.Color         | objekt | RGBA-färgvärden för teckensnittet.                                   |
| Style.Font.IsBold        | boolean | `true` om teckensnittet är fetstilt.                                 |
| Style.Font.IsItalic      | boolean | `true` om teckensnittet är kursivt.                                  |
| Style.Font.IsStrikeout   | boolean | `true` om teckensnittet är genomstruken.                             |
| Style.Font.IsSubscript   | boolean | `true` om teckensnittet är nedsänkt.                                 |
| Style.Font.IsSuperscript | boolean | `true` om teckensnittet är upphöjt.                                  |
| Style.Font.Name          | string  | Teckensnittsfamiljens namn (t.ex. **Calibri**).                      |
| Style.Font.Size          | number  | Teckensnittets storlek i punkter.                                    |
| Style.Font.Underline     | string  | Understruksstil (t.ex. **Single**).                                  |
| Style.IsLocked           | boolean | Anger om cellen är skyddad mot redigering.                           |
| Style.IsTextWrapped      | boolean | `true` om textbrytning är aktiverat.                                 |
| Style.IsGradient         | boolean | `true` om ett gradientfyllning är tillämpat.                         |
| Style.Pattern            | string  | Namn på fyllningsmönster (t.ex. **None**).                           |
| Style.BorderCollection   | array   | Lista med objekt som definierar linjestil, färg och bordertyp.       |
| Style.BackgroundColor    | objekt  | RGBA-värden för cellens bakgrund.                                    |
| Style.ForegroundColor    | objekt  | RGBA-värden för cellens förgrund.                                    |
| …                        | …       | _(Andra fält följer samma mönster som beskrivs i API-referensen.)_   |

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå, så att du kan fokusera på dina projektuppgifter. Besök [GitHub-lagret](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Se även**  
- [Ställ in cellstil](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [Hämta cellvärde](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---