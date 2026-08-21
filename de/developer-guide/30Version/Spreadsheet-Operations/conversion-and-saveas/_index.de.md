---
title: "Konvertieren einer Excel-Datei in ein anderes Format oder Speichern unter einem anderen Namen."
second_title: "Dokument"
linktitle: "Konvertierung und Speichern unter"
type: docs
url: /de/conversion-and-save-as/
aliases: [  /de/convert-excel/ , /de/convert/ ]
keywords: "Aspose.Cells, Excel-Konvertierungs-API, Excel in PDF konvertieren, Excel in CSV, Excel in JSON, Cloud-Tabellenkalkulations-Konvertierung"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mithilfe der Aspose.Cells Cloud REST-API in PDF, CSV, JSON, HTML und über 15 weitere Formate konvertieren. Enthält Endpunkt-Details, Beispiel-cURL-Befehle und SDK-Snippets für Java, .NET, Python und weitere."
weight: 30
ArticleTitle: "Konvertieren Sie Excel-Dateien in PDF, CSV, JSON und weitere Formate mit Aspose.Cells Cloud"
---

Wenn Sie eine Excel-Datei ursprünglich in einem bestimmten Format erstellt haben – beispielsweise [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) oder [CSV](https://docs.fileformat.com/spreadsheet/csv/) – kann es nützlich sein, die Excel-Datei in ein anderes Format zu konvertieren, um spezielle Funktionen nutzen zu können. Beispielsweise schützt die Konvertierung einer Excel-Datei in das [PDF](https://docs.fileformat.com/pdf/)-Format ihren Inhalt vor unbefugten Änderungen und erleichtert das Lesen und Teilen.

**Voraussetzungen**  
Bevor Sie die Konvertierungs-APIs aufrufen, holen Sie sich einen OAuth 2.0-Zugriffstoken von Aspose Cloud und stellen Sie sicher, dass die Arbeitsmappe in Ihrem Aspose Cloud-Speicher gespeichert ist (oder im Anforderungstext für den PUT-Konvertierungsendpunkt enthalten ist).

Die Dokumentenkonvertierung ist ein komplexer Prozess. Viele Faktoren tragen zur Komplexität dieses Prozesses bei und sollten während der Transformation berücksichtigt werden. Die Bereitstellung präziser, professionell qualitativ hochwertiger Konvertierungen zwischen Excel-Formaten ist eine Schlüsselfunktion von Aspose.Cells Cloud.

Der Dienst funktioniert nahtlos für jede Art von Dokumentformatkonvertierung. Sie können Dokumente sowohl importieren als auch in folgenden Formaten exportieren:

**Unterstützte Formate**  
- Import/Export: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/)
- Nur Export: [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/)

### Konvertierungs-APIs

| API                         | Beschreibung                                                                                             |
| :-------------------------- | :------------------------------------------------------------------------------------------------------- |
| `GET /cells/{name}`         | Ruft eine Excel-Arbeitsmappe aus dem Cloud-Speicher ab und konvertiert sie in das angeforderte Format.  |
| `PUT /cells/convert`        | Konvertiert eine im Anforderungstext übergebene Excel-Arbeitsmappe in das angegebene Ausgabeformat.    |
| `POST /cells/{name}/saveAs` | Speichert eine vorhandene Excel-Arbeitsmappe direkt im Cloud-Speicher in einem anderen Format.          |

**API-Details**

- **GET /cells/{name}**  
  - **Pfadparameter:** `name` – Dateiname der Arbeitsmappe (erforderlich).  
  - **Abfrageparameter:** `format` – Zielformat (z. B. pdf, csv, json); `storage` – Name des Cloud-Speichers (optional); `folder` – Ordnerpfad innerhalb des Speichers (optional).  
  - **Antwort:** Dateistream der konvertierten Arbeitsmappe; `Content‑Type` entspricht dem Zielformat.  
  - **Statuscodes:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

- **PUT /cells/convert**  
  - **Anforderungstext:** multipart/form‑data mit der Quell-Arbeitsmappe (`file`) und einem erforderlichen `format`-Feld für das gewünschte Ausgabeformat.  
  - **Antwort:** Binärstream der konvertierten Datei.  
  - **Statuscodes:** 200 OK, 400 Bad Request, 401 Unauthorized, 500 Internal Server Error.  

- **POST /cells/{name}/saveAs**  
  - **Pfadparameter:** `name` – Name der vorhandenen Arbeitsmappe.  
  - **Abfrageparameter:** `format` – Zielformat; `outPath` – Zielpfad im Cloud-Speicher (optional); `storage` – Name des Speichers (optional).  
  - **Antwort:** JSON-Objekt mit dem Ergebnis des Vorgangs und dem Pfad der gespeicherten Datei. Beispiel-Antwort:  

    ```json
    {
      "status": "OK",
      "code": 200,
      "message": "Datei erfolgreich gespeichert.",
      "path": "Converted/MyWorkbook.pdf"
    }
    ```  

  - **Statuscodes:** 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error.  

**Beispiel-cURL für die Konvertierung in PDF**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -o MyWorkbook.pdf
```

**Java-SDK-Snippet (GET /cells/{name})**

```java
CellsApi apiInstance = new CellsApi();
String name = "MyWorkbook.xlsx";
String format = "pdf";
File result = apiInstance.cellsGetWorkbook(name, format, null, null);
result.renameTo(new File("MyWorkbook.pdf"));
```

**.NET-SDK-Snippet (PUT /cells/convert)**

```csharp
var api = new CellsApi();
var file = File.ReadAllBytes("MyWorkbook.xlsx");
var format = "pdf";
var result = api.ConvertWorkbook(new MemoryStream(file), format);
File.WriteAllBytes("MyWorkbook.pdf", result);
```

**Python-SDK-Snippet (POST /cells/{name}/saveAs)**

```python
import asposecellscloud
api = asposecellscloud.CellsApi()
api.post_save_as(name="MyWorkbook.xlsx", format="pdf", out_path="Converted/MyWorkbook.pdf")
```

Die folgenden Artikel erläutern jede API im Detail und enthalten zusätzliche cURL- und SDK-Beispiele:

- [Konvertieren einer Excel-Datei in ein anderes Format](/de/cells/convert-an-excel-file-to-different-formats)
- [Speichern einer Excel-Datei in einem anderen Format](/de/cells/save-an-excel-file-as-other-formats-files)
- [Konvertieren einer Excel-Datei in eine CSV-Datei](/de/cells/convert-excel-file-to-csv-file)
- [Konvertieren einer Excel-Datei in eine DOCX-Datei](/de/cells/convert-excel-file-to-docx-file)
- [Konvertieren einer Excel-Datei in eine HTML-Datei](/de/cells/convert-excel-file-to-html-file)
- [Konvertieren einer Excel-Datei in eine JSON-Datei](/de/cells/convert-excel-file-to-json-file)
- [Konvertieren einer Excel-Datei in eine Markdown-Datei](/de/cells/convert-excel-file-to-markdown-file)
- [Konvertieren einer Excel-Datei in eine PDF-Datei](/de/cells/convert-excel-file-to-pdf-file)
- [Konvertieren einer Excel-Datei in eine PNG-Datei](/de/cells/convert-excel-file-to-png-file)
- [Konvertieren einer Excel-Datei in eine PPTX-Datei](/de/cells/convert-excel-file-to-pptx-file)
- [Konvertieren einer Excel-Datei in eine SQL-Datei](/de/cells/convert-excel-file-to-sql-file)
- [Konvertieren einer Excel-Datei in eine TIFF-Datei](/de/cells/convert-excel-file-to-tiff-file)
---