---
title: "Uppdatera en form i ett Excel-ark"
second_title: "Dokument"
linktitle: "Uppdatera"
type: docs
url: /shapes/update/
aliases: [/update-a-shape-inside-the-worksheet/]
keywords: "uppdatera form Excel API, Aspose.Cells Cloud, uppdatera Excel-form, REST API, SDK, C#, Java, Python, Node.js, Go, Ruby, PHP, Perl, Swift"
description: "Lär dig hur du uppdaterar en form i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller HTTPS-slutpunkt, autentiseringsuppgifter, DTO-schemat, steg-för-steg-användning, cURL-exempel och SDK-kodexempel för flera språk."
ArticleTitle: "Uppdatera en form i ett Excel-ark – Aspose.Cells Cloud API"
weight: 31
---

Denna REST API uppdaterar en form i ett Excel-ark.

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### Begäranparametrar

| Parametername   | Typ     | Plats  | Beskrivning                                                                                   |
| --------------- | ------- | ------ | --------------------------------------------------------------------------------------------- |
| **name**        | string  | path   | Namnet på arbetsboksfilen.                                                                    |
| **sheetName**   | string  | path   | Namnet på arket som innehåller formen.                                                        |
| **shapeindex**  | integer | path   | Det nollbaserade indexet för formen i arket.                                                  |
| **dto**         | object  | body   | Objektet för formens dataöverföring som innehåller de uppdaterade egenskaperna (se _DTO-schema_ nedan). |
| **folder**      | string  | query  | Mappen där arbetsboken är lagrad.                                                             |
| **storageName** | string  | query  | Namnet på Aspose Cloud-lagringen.                                                             |

### DTO-schema

`dto`-objektet innehåller de egenskaper som kan uppdateras. Alla fält är valfria om inget annat anges.

| Fält                | Typ     | Obligatoriskt | Beskrivning                                                                         |
| ------------------- | ------- | ------------- | ----------------------------------------------------------------------------------- |
| **Name**            | string  | Nej           | Nytt namn för formen.                                                               |
| **UpperLeftRow**    | integer | Nej           | Radindex för formens övre vänstra hörn.                                             |
| **UpperLeftColumn** | integer | Nej           | Kolumnindex för formens övre vänstra hörn.                                          |
| **Width**           | integer | Nej           | Bredd på formen (i punkter).                                                        |
| **Height**          | integer | Nej           | Höjd på formen (i punkter).                                                         |
| **RotationAngle**   | integer | Nej           | Rotationsvinkel i grader.                                                           |
| **IsHidden**        | boolean | Nej           | `true` för att dölja formen.                                                        |
| **IsLocked**        | boolean | Nej           | `true` för att låsa formen.                                                         |
| **Font**            | object  | Nej           | Teckensnittsinställningar (se OpenAPI-specifikationen för underordnade egenskaper). |
| **...**             | …       | Nej           | Ytterligare egenskaper såsom `HtmlText`, `AlternativeText`, `ZOrderPosition`, etc. |

> För en fullständig lista, se den officiella OpenAPI-specifikationen: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### Begärandehuvuden

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(JWT-token från _Autentisering_-steget)_

### Begärantext (exempel)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## Exempel med cURL (kommandoradsverktyg)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### Svar

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Felhantering** – API:et kan returnera följande statuskoder:

| Kod | Beteende              | Vanlig orsak                                        |
| --- | --------------------- | --------------------------------------------------- |
| 400 | Felaktig begäran      | Ogiltig JSON eller obligatoriska fält saknas.     |
| 401 | Autentisering krävs   | Saknas eller ogiltig JWT-token.                    |
| 404 | Hittades inte         | Arbetsboken, arket eller formindexet finns inte.  |
| 500 | Internt serverfel     | Oväntat problem på servern.                         |

**Exempel på felaktiga svar**

*400 – Felaktig begäran*

```json
{
  "Code": 400,
  "Message": "Ogiltig begäran. Fältet 'Name' överskrider maxlängden."
}
```

*401 – Autentisering krävs*

```json
{
  "Code": 401,
  "Message": "Autentisering misslyckades. Ogiltig eller utgången JWT-token."
}
```

*404 – Hittades inte*

```json
{
  "Code": 404,
  "Message": "Den angivna arbetsboken, arket eller formindexet hittades inte."
}
```

*500 – Internt serverfel*

```json
{
  "Code": 500,
  "Message": "Ett oväntat fel uppstod på servern."
}
```

## SDK-familj för molnet

Användning av en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Besök [GitHub-lagret](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}