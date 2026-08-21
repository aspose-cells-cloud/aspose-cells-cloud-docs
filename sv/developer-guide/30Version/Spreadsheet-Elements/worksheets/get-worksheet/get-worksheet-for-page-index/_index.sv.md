---
title: "Exportera en arbetsbladssida – Aspose.Cells Cloud API-referens"
articleTitle: "Exportera en arbetsbladssida – Aspose.Cells Cloud API-referens"
secondTitle: "Dokument"
linkTitle: "Sida"
type: docs
url: /sv/worksheets/page-to-different-formats/
aliases: [  /sv/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud, export av arbetsbladssida, PDF, PNG, CSV, REST API, JWT-autentisering, filformat"
description: "Lär dig hur du exporterar en specifik arbetsbladssida till PDF, PNG, CSV och mer med Aspose.Cells Cloud REST API. Innehåller cURL-förfrågan, parameterguide och SDK-exempel för flera språk."
weight: 240
---

Att exportera en specifik arbetsbladssida är användbart när du behöver en utskriftsvänlig ögonblicksbild av en rapport, ett diagrambild eller en dataextrakt utan att ladda ner hela arbetsboken. Denna slutpunkt låter dig hämta en enskild sida i det filformat som bäst passar din efterföljande arbetsflödesbehov.

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API:et låter dig konvertera en angiven sida i ett arbetsblad till olika filformat. Stödda format: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt för dig att utföra REST-interaktioner direkt från en webbläsare.

> **Förutsättningar** – Du måste ha en giltig JWT-autentiseringstoken och arbetsboken måste lagras i en molnmapp som du anger med parametern `folder`.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör en förfrågan till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Svar** – Tjänsten returnerar den begärda sidan i det valda formatet. För bildformat (png, jpeg, gif, etc.) innehåller responskroppen den binära bilden; för dokumentformat (pdf, xls, csv, …) innehåller responskroppen filinnehållet. Ett lyckat anrop returnerar HTTP 200.

*Exempel på ett PNG-svar (inledande base64-utdrag):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**Parametrar**

| Parameter              | Typ     | Beskrivning                                                         | Standardvärde |
| ---------------------- | ------- | ------------------------------------------------------------------- | ------------- |
| `format`               | string  | Utdatafilformat (t.ex. `pdf`, `png`, `csv`).                        | `pdf`         |
| `verticalResolution`   | integer | Vertikal DPI för den renderade bilden.                              | `100`         |
| `horizontalResolution` | integer | Horisontell DPI för den renderade bilden.                            | `100`         |
| `pageIndex`            | integer | Nollbaserat index för den arbetsbladssida som ska exporteras (`0` = första sidan). | `0`           |
| `folder`               | string  | Molnlagringsmapp där källarbetsboken finns.                        | —             |

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Ogiltig förfrågan           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad               | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel           | Oväntat serverfel.                                      |

**Möjliga fel**

- **401 Oautentiserad** – Ogiltig eller saknad JWT-token.
- **404 Ej hittad** – Den angivna arbetsboken eller arbetsbladet finns inte.
- **400 Ogiltig förfrågan** – Ogiltigt parametervärde (t.ex. ej stödd `format`).
- **500 Internt serverfel** – Oväntat problem på serversidan.

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}