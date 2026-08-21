---
title: "Exportera ett arbetsbladsområde till PNG, PDF, CSV – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Område"
type: docs
url: /sv/worksheets/area-to-different-formats/
aliases: [  /sv/get-worksheet-for-area/ ]
keywords: "Aspose.Cells, exportera arbetsbladsområde, PNG, PDF, CSV, Excel-konvertering, REST API, SDK"
description: "Lär dig hur du exporterar ett specifikt cellområde från ett Excel-arbetsblad till PNG, PDF, CSV och över 20 andra format med Aspose.Cells Cloud REST API eller SDK:er (C#, Java, Python, …)."
weight: 230
ArticleTitle: "Exportera arbetsbladsområde till PNG, PDF, CSV med Aspose.Cells Cloud API – Fullständig guide"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API:et låter dig konvertera ett angivet område i ett arbetsblad till olika filformat. Stödda format: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Den här guiden visar hur du exporterar ett **specifikt cellområde** från ett Excel-arbetsblad till PNG, PDF, CSV och mer än 20 ytterligare format med Aspose.Cells Cloud API. För relaterade åtgärder som export av hela arbetsblad eller konvertering av arbetsbok, se sidorna **[Exportera hela arbetsbladet](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** och **[Konvertera arbetsbok till PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)**.

## REST API

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Begärparametrar

| Parameter              | Typ    | Krävs | Beskrivning                                   |
|------------------------|--------|-------|-----------------------------------------------|
| `name`                 | string | Ja    | Arbetsbokens filnamn.                         |
| `sheetName`            | string | Ja    | Målarbetsbladets namn.                        |
| `format`               | string | Ja    | Önskat utdataformat (png, pdf, csv, …).       |
| `area`                 | string | Nej   | Cellområde att exportera (t.ex. `B3:K8`).     |
| `verticalResolution`   | int    | Nej   | Vertikal DPI för rasterformat.                |
| `horizontalResolution` | int    | Nej   | Horisontell DPI för rasterformat.             |
| `folder`               | string | Nej   | Mapp i molnlagring där filen finns.           |
| `storage`              | string | Nej   | Namn på lagringstjänsten.                     |

### Lyckad svarskod

* **200 OK** – Returnerar den begärda filen i binärt format (PNG, PDF, CSV, etc.).

### Felaktiga svarskoder

| Statuskod | Beskrivning                                       |
|-----------|---------------------------------------------------|
| 400       | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401       | Ej auktoriserad – autentiseringstoken saknas eller är ogiltig. |
| 404       | Hittades inte – angiven arbetsbok eller arbetsblad finns inte. |
| 500       | Internt serverfel – oväntat tillstånd på servern. |

**Exempel på feldata**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "Parametern 'area' är felaktig. Förväntat format: B3:K8."
  }
}
```

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Konverterad bild (binär PNG)

{{< /tab >}}

{{< /tabs >}}

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på din projektlogik. Kontrollera [GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}