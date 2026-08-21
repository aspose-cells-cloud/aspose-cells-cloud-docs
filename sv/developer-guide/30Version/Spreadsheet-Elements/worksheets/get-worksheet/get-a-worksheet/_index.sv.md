---
title: "Exportera ett kalkylblad med Aspose.Cells Cloud API – format, cURL- och SDK-exempel"
second_title: "Dokument"
linktitle: "Exportera kalkylblad"
type: docs
url: /sv/worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Get Worksheet, exportera kalkylblad, Excel API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, moln-API"
description: "Lär dig hur du exporterar ett enskilt kalkylblad från en Excel-fil med Aspose.Cells Cloud REST API. Inkluderar endpoint, parametrar, ett korregerat cURL-exempel, autentiseringsinformation, felhantering och SDK-utdrag för C#, Java, Python och mer."
weight: 10
ArticleTitle: "Exportera ett kalkylblad med Aspose.Cells Cloud API – format, cURL- och SDK-exempel"
---

Detta REST API gör det möjligt att **exportera ett kalkylblad** från en Excel-fil till många olika filformat.

**Sammanfattning** – Använd endpointet **Get Worksheet** för att ladda ner ett enskilt kalkylblad från en arbetsbok i det format du önskar.

Du kan exportera till följande format:

| Format  | Filändelse | MIME-typ                                                          |
| ------- | ---------- | ----------------------------------------------------------------- |
| XLS     | .xls       | application/vnd.ms-excel                                          |
| XLSX    | .xlsx      | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb      | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV     | .csv       | text/csv                                                          |
| TSV     | .tsv       | text/tab-separated-values                                         |
| XLSM    | .xlsm      | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS     | .ods       | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT     | .txt       | text/plain                                                        |
| PDF     | .pdf       | application/pdf                                                   |
| OTS     | .ots       | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS     | .xps       | application/vnd.ms-xpsdocument                                    |
| DIF     | .dif       | application/x-dif                                                 |
| PNG     | .png       | image/png                                                         |
| JPEG    | .jpeg      | image/jpeg                                                        |
| GIF     | .gif       | image/gif                                                         |
| BMP     | .bmp       | image/bmp                                                         |
| WMF     | .wmf       | image/wmf                                                         |
| TIFF    | .tiff      | image/tiff                                                        |
| EMF     | .emf       | image/emf                                                         |
| NUMBERS | .numbers   | application/vnd.apple.numbers                                     |
| FODS    | .fods      | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Begärparametrar**

| Parameternamn            | Typ     | Plats  | Beskrivning                                                         |
| ------------------------ | ------- | ------ | ------------------------------------------------------------------- |
| **name**                 | string  | path   | **Obligatoriskt.** Namn på Excel-filen.                             |
| **sheetName**            | string  | path   | **Obligatoriskt.** Namn på det kalkylblad som ska exporteras.      |
| **format**               | string  | query  | Målfilformat för det exporterade kalkylbladet (t.ex. `pdf`, `png`). |
| **verticalResolution**   | integer | query  | Bild-DPI för format som stöder upplösning (t.ex. PNG, JPEG).        |
| **horizontalResolution** | integer | query  | Bild-DPI för format som stöder upplösning.                          |
| **area**                 | string  | query  | Cellområde som ska exporteras (t.ex. `A1:D10`).                     |
| **pageIndex**            | integer | query  | Sidindex för den sida som ska exporteras när kalkylbladet är uppdelat i sidor. |
| **folder**               | string  | query  | Mappväg i lagringen där källfilen finns.                           |
| **storageName**          | string  | query  | Namn på Aspose Cloud-lagringen.                                     |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<binär data>
```

{{< /tab >}}

{{< /tabs >}}

## Felhantering

API:et returnerar standard-HTTP-statuskoder. Vanliga svar inkluderar:

| Statuskod | Betydelse                                                    | Exempel på JSON-svartext             |
| --------- | ------------------------------------------------------------ | ------------------------------------ |
| **200**   | Lyckades – kalkylbladsströmmen returneras.                   | `{ "stream": "..." }`                |
| **400**   | Ogiltig begäran – saknade eller ogiltiga parametrar.         | `{ "error": "Invalid format parameter." }` |
| **401**   | Autentisering misslyckades – ogiltig eller saknad JWT-token. | `{ "error": "Authentication failed." }`    |
| **404**   | Hittades inte – den angivna filen eller det angivna kalkylbladet finns inte. | `{ "error": "Worksheet not found." }`      |
| **500**   | Internt serverfel – oväntat tillstånd på servern.            | `{ "error": "Unexpected error." }`   |

Hantera dessa svar i din klientkod för att ge lämplig återkoppling till användarna.

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lägre nivå och låter dig fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

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