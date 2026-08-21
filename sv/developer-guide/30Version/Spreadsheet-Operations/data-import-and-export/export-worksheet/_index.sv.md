---
title: "Exportera kalkylblad – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Kalkylblad"
type: docs
url: /export-excel-worksheet-to-different-formats/
aliases: [/export/excel-worksheet-to-different-formats/]
keywords: "Aspose.Cells, exportera kalkylblad, Excel--API, PDF, CSV, TIFF, ODS, bildformat"
description: "Lär dig hur du exporterar ett Excel-kalkylblad till PDF, CSV, TIFF och andra format med Aspose.Cells Cloud REST API. Innehåller cURL-exempel, nödvändig autentisering, parameterbeskrivningar och svarshantering."
weight: 20
ArticleTitle: "Exportera Excel-kalkylblad till flera format – Aspose.Cells Cloud"
---

Du kan exportera ett kalkylblad till följande format:

- **XLS** – [XLS-formatinformation](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [XLSX-formatinformation](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [XLSB-formatinformation](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [CSV-formatinformation](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [TSV-formatinformation](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [XLSM-formatinformation](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [ODS-formatinformation](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [TXT-formatinformation](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [PDF-formatinformation](https://docs.fileformat.com/pdf/)
- **OTS** – [OTS-formatinformation](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [XPS-formatinformation](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [DIF-formatinformation](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [PNG-formatinformation](https://docs.fileformat.com/Image/png/)
- **JPEG** – [JPEG-formatinformation](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [BMP-formatinformation](https://docs.fileformat.com/image/bmp/)
- **SVG** – [SVG-formatinformation](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [TIFF-formatinformation](https://docs.fileformat.com/image/tiff/)
- **EMF** – [EMF-formatinformation](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Numbers-formatinformation](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [FODS-formatinformation](https://docs.fileformat.com/spreadsheet/fods/)

[Utforska relaterade exportoperationer, t.ex. export av hela arbetsboken eller ett diagram.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## PostExport-API

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parametername | Typ   | Sökväg/frågesträng/HTTP-body | Obligatorisk | Beskrivning                                                                 |
|---------------|-------|------------------------------|--------------|-----------------------------------------------------------------------------|
| file          | fil   | formData                     | Ja           | Fil som ska laddas upp                                                      |
| objectType    | sträng | fråga                        | Ja           | Objekttyp som ska exporteras. Använd `chart` för diagramexport. Andra möjliga värden är t.ex. `worksheet`, `picture`, etc. |
| format        | sträng | fråga                        | Ja           | Önskat utdataformat. Stödda värden: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### Svar

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **Felhantering**

Om begäran misslyckas returnerar API:et ett JSON-felobjekt som innehåller fält som `Code` och `Message`. Typiska HTTP-statuskoder är **401 Unauthorized** (token saknas eller ogiltig) och **400 Bad Request** (ogiltiga parametrar).

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                               |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token. |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel. |

**Anteckningar**

- Maximal filstorlek för uppladdning är 50 MB.  
- API:et stöder export av flera kalkylblad i en enda begäran; varje kalkylblad returneras som en separat fil i `Files`-arrayen.  
- Asynkron bearbetning är tillgänglig för stora arbetsböcker; använd `202 Accepted`-svaret för att pollinga åtgärdens status.

## Hur du använder PostExport-API:et med SDK:er

### Krav

Innan du anropar API:et, skaffa en giltig JWT-åtkomsttoken med Aspose.Cells Cloud-autentiseringsflödet. Se till att token ingår i `Authorization`-huvudet i varje begäran. SDK:erna hanterar tokeninhämtningen automatiskt när de konfigurerats med dina klientuppgifter.

### PostExport-API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar Cloud-API:et med cURL.

```bash
# Exportera ett kalkylblad till TIFF-format
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla mot Aspose.Cells Cloud. En SDK abstraherar lågnivådetaljer så att du kan fokusera på din affärslogik. För en fullständig lista över stödda SDK:er, besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---