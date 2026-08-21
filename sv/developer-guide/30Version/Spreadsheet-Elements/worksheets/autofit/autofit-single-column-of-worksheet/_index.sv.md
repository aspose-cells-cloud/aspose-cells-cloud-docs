---
title: "Autojustera kolumn i Excel med Aspose.Cells Cloud API – Snabbguide"
second_title: "Dokument"
linktitle: "Kolumn"
type: docs
url: /sv/worksheets/autofit/column/
aliases: [  /sv/autofit-single-column-of-worksheet/ ]
keywords: "Aspose.Cells Cloud, autojustera kolumn, Excel API, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Lär dig hur du automatiskt justerar bredden på en kolumn (eller ett kolumnintervall) i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller cURL- och SDK-exempel (C#, Java, Python m.fl.) samt detaljerad information om begäran och svar."
weight: 10
---

Denna REST API justerar automatiskt bredden på en enskild kolumn eller ett sammanhängande intervall av kolumner i ett Excel-ark.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
```

### Begärparametrar

| Parameternamn     | Typ     | Plats  | Beskrivning                                                                                      |
| ----------------- | ------- | ------ | ------------------------------------------------------------------------------------------------ |
| name              | string  | path   | Namnet på Excel-filen.                                                                           |
| sheetName         | string  | path   | Namnet på arket.                                                                                 |
| firstColumn       | integer | query  | Nollbaserat index för den första kolumn som ska autojusteras.                                   |
| lastColumn        | integer | query  | Nollbaserat index för den sista kolumn som ska autojusteras.                                    |
| autoFitterOptions | object  | body   | Alternativ som styr autojusteringsbeteendet (se [AutoFitterOptions](/cells/auto-filter-options)). |
| firstRow          | integer | query  | Nollbaserat index för den första rad som beaktas vid beräkning av kolumnbredd.                  |
| lastRow           | integer | query  | Nollbaserat index för den sista rad som beaktas vid beräkning av kolumnbredd.                   |
| folder            | string  | query  | Mappen i lagringen där filen finns.                                                             |
| storageName       | string  | query  | Namnet på lagringstjänsten.                                                                      |

### Felresponser

| HTTP-status | Betydelse                                  | Exempel på JSON-svar                                        |
| ----------- | ------------------------------------------ | ----------------------------------------------------------- |
| 400         | Ogiltig parameter(e)                       | `{"Code":400,"Message":"Invalid parameter 'firstColumn'."}` |
| 401         | Auktorisering misslyckades – JWT-token saknas eller är ogiltig | `{"Code":401,"Message":"Authorization failed."}`            |
| 404         | Fil eller ark hittades inte                | `{"Code":404,"Message":"Worksheet 'Sheet1' not found."}`    |
| 500         | Internt serverfel                            | `{"Code":500,"Message":"An unexpected error occurred."}`    |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells Cloud-tjänster. Exemplet nedan visar hur du anropar endpoint för autojustering av kolumn.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?firstColumn=2&lastColumn=2" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells": true, "IgnoreHidden": true, "OnlyAuto": true}'
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

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att integrera API:et i din applikation. SDK:er hanterar detaljer på lågnivå så att du kan fokusera på affärslogik. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar endpoint för autojustering av kolumn med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}