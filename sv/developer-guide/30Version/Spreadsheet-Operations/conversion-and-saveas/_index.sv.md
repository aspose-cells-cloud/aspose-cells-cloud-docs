---
title: "Konvertera en Excel-fil till ett annat format eller spara den på ett annat sätt."
second_title: "Dokument"
linktitle: "Konvertering och Spara som"
type: docs
url: /sv/conversion-and-save-as/
aliases: [  /sv/convert-excel/ , /sv/convert/ ]
keywords: "Aspose.Cells, Excel-konverterings-API, konvertera Excel till PDF, Excel till CSV, Excel till JSON, molnspreadsheetskonvertering"
description: "Lär dig hur du konverterar Excel-arbetsböcker till PDF, CSV, JSON, HTML och över 15 andra format med Aspose.Cells Cloud REST API. Innehåller detaljerad information om slutpunkter, exempel på cURL-kommandon och SDK-utdrag för Java, .NET, Python och mer."
weight: 30
ArticleTitle: "Konvertera Excel-filer till PDF, CSV, JSON och mer med Aspose.Cells Cloud"
---

Om du ursprungligen skapade en Excel-fil i ett visst format – till exempel [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), eller [CSV](https://docs.fileformat.com/spreadsheet/csv/) – kan det vara användbart att konvertera Excel-filen till ett annat format för att utnyttja speciella funktioner. Exempelvis skyddar konvertering av en Excel-fil till [PDF](https://docs.fileformat.com/pdf/) dess innehåll mot obehöriga ändringar och gör det lättare att läsa och dela den.

**Förutsättningar**  
Innan du anropar konverterings-API:erna ska du skaffa en OAuth 2.0-åtkomsttoken från Aspose Cloud och säkerställa att arbetsboken finns lagrad i din Aspose Cloud-lagring (eller inkluderad i begärans brödtext för PUT-konverteringsändpunkten).

Dokumentkonvertering är en komplex process. Många faktorer påverkar komplexiteten i konverteringsprocessen och bör beaktas under omvandlingen. Att erbjuda exakt, professionellkvalitativ konvertering mellan Excel-format är en nyckelfunktion i Aspose.Cells Cloud.

Tjänsten fungerar sömlöst för konvertering av dokument i valfritt format. Du kan både importera och exportera dokument i följande format:

**Stödda format**  
- Import/Export: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- Endast export: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### Konverterings-API:er

| API                         | Beskrivning                                                                                      |
| :-------------------------- | :----------------------------------------------------------------------------------------------- |
| `GET /cells/{name}`         | Hämtar en Excel-arbetsbok från molnlagringen och konverterar den till det begärda formatet.     |
| `PUT /cells/convert`        | Konverterar en Excel-arbetsbok som skickas i begärons brödtext till det angivna utdataformatet. |
| `POST /cells/{name}/saveAs` | Sparar en befintlig Excel-arbetsbok som ett annat format direkt i molnlagringen.                 |

**API-detaljer**

- **GET /cells/{name}**  
  - **Sökvägsparametrar:** `name` – arbetsbokens filnamn (obligatoriskt).  
  - **Frågeparametrar:** `format` – målformat (t.ex. pdf, csv, json); `storage` – namn på molnlagring (valfritt); `folder` – mappsökväg inom lagringen (valfritt).  
  - **Svar:** Filström för den konverterade arbetsboken; `Content‑Type` matchar målformatet.  
  - **Statuskoder:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **Begäran (brödtext):** multipart/form‑data som innehåller källarbetsbokens fil (`file`) och ett obligatoriskt fält `format` som anger önskat utdataformat.  
  - **Svar:** Binär ström för den konverterade filen.  
  - **Statuskoder:** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **Sökvägsparametrar:** `name` – namn på den befintliga arbetsboken.  
  - **Frågeparametrar:** `format` – målformat; `outPath` – målsökväg i molnlagringen (valfritt); `storage` – namn på lagringen (valfritt).  
  - **Svar:** JSON-objekt med åtgärdens resultat och sökvägen till den sparade filen. Exempel på svar:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "Filen sparades framgångsrikt.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **Statuskoder:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

**Exempel på cURL för konvertering till PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Java SDK-utdrag (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**.NET SDK-utdrag (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Python SDK-utdrag (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

Följande artiklar förklarar varje API i detalj och innehåller ytterligare cURL- och SDK-exempel:

- [Konvertera en Excel-fil till ett annat format](/sv/cells/convert-an-excel-file-to-different-formats)
- [Spara en Excel-fil som ett annat format](/sv/cells/save-an-excel-file-as-other-formats-files)
- [Konvertera en Excel-fil till en CSV-fil](/sv/cells/convert-excel-file-to-csv-file)
- [Konvertera en Excel-fil till en DOCX-fil](/sv/cells/convert-excel-file-to-docx-file)
- [Konvertera en Excel-fil till en HTML-fil](/sv/cells/convert-excel-file-to-html-file)
- [Konvertera en Excel-fil till en JSON-fil](/sv/cells/convert-excel-file-to-json-file)
- [Konvertera en Excel-fil till en Markdown-fil](/sv/cells/convert-excel-file-to-markdown-file)
- [Konvertera en Excel-fil till en PDF-fil](/sv/cells/convert-excel-file-to-pdf-file)
- [Konvertera en Excel-fil till en PNG-fil](/sv/cells/convert-excel-file-to-png-file)
- [Konvertera en Excel-fil till en PPTX-fil](/sv/cells/convert-excel-file-to-pptx-file)
- [Konvertera en Excel-fil till en SQL-fil](/sv/cells/convert-excel-file-to-sql-file)
- [Konvertera en Excel-fil till en TIFF-fil](/sv/cells/convert-excel-file-to-tiff-file)
---