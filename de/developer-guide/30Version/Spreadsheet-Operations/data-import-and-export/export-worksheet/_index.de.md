---
title: "Arbeitsblatt exportieren – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Arbeitsblatt"
type: docs
url: /export-excel-worksheet-to-different-formats/
aliases: [/export/excel-worksheet-to-different-formats/]
keywords: "Aspose.Cells, Arbeitsblatt exportieren, Excel-API, PDF, CSV, TIFF, ODS, Bildformate"
description: "Erfahren Sie, wie Sie ein Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API in PDF, CSV, TIFF und andere Formate exportieren können. Enthält cURL-Beispiel, erforderliche Authentifizierung, Parameterdetails und Antwortbehandlung."
weight: 20
ArticleTitle: "Excel-Arbeitsblatt in verschiedene Formate exportieren – Aspose.Cells Cloud"
---

Sie können ein Arbeitsblatt in die folgenden Formate exportieren:

- **XLS** – [Details zum XLS-Format](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [Details zum XLSX-Format](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [Details zum XLSB-Format](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [Details zum CSV-Format](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [Details zum TSV-Format](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [Details zum XLSM-Format](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [Details zum ODS-Format](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [Details zum TXT-Format](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [Details zum PDF-Format](https://docs.fileformat.com/pdf/)
- **OTS** – [Details zum OTS-Format](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [Details zum XPS-Format](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [Details zum DIF-Format](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [Details zum PNG-Format](https://docs.fileformat.com/Image/png/)
- **JPEG** – [Details zum JPEG-Format](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [Details zum BMP-Format](https://docs.fileformat.com/image/bmp/)
- **SVG** – [Details zum SVG-Format](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [Details zum TIFF-Format](https://docs.fileformat.com/image/tiff/)
- **EMF** – [Details zum EMF-Format](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Details zum Numbers-Format](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [Details zum FODS-Format](https://docs.fileformat.com/spreadsheet/fods/)

[Erkunden Sie verwandte Exportvorgänge wie den Export einer gesamten Arbeitsmappe oder eines Diagramms.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## PostExport-API

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Erforderlich | Beschreibung                                                                 |
|-----------------|--------|------------------------------------|--------------|------------------------------------------------------------------------------|
| file            | Datei  | formData                           | Ja           | Hochzuladende Datei                                                          |
| objectType      | string | query                              | Ja           | Der Typ des zu exportierenden Objekts. Für den Diagramm-Export verwenden Sie `chart`. Weitere mögliche Werte sind `worksheet`, `picture`, usw. |
| format          | string | query                              | Ja           | Gewünschtes Ausgabeformat. Unterstützte Werte: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### Antwort

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

### **Fehlerbehandlung**

Falls die Anforderung fehlschlägt, gibt die API ein JSON-Fehlerobjekt zurück, das Felder wie `Code` und `Message` enthält. Typische HTTP-Statuscodes sind **401 Unauthorized** (fehlendes oder ungültiges Token) und **400 Bad Request** (ungültige Parameter).

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                       |
|------|-----------------------------|--------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.   |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                              |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größenbeschränkung.          |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                        |

**Hinweise**

- Die maximale Dateigröße für den Upload beträgt 50 MB.  
- Die API unterstützt den Export mehrerer Arbeitsblätter in einer einzigen Anforderung; jedes Arbeitsblatt wird als separate Datei im `Files`-Array zurückgegeben.  
- Asynchrone Verarbeitung ist für große Arbeitsmappen verfügbar; verwenden Sie den HTTP-Statuscode `202 Accepted`, um den Vorgangsstatus abzufragen.

## Verwendung der PostExport-API mit SDKs

### Voraussetzungen

Bevor Sie die API aufrufen, beschaffen Sie ein gültiges JWT-Zugriffstoken mithilfe des Aspose.Cells Cloud-Authentifizierungsablaufs. Stellen Sie sicher, dass das Token im `Authorization`-Header jeder Anforderung enthalten ist. Die SDKs übernehmen die Token-Beschaffung automatisch, sobald sie mit Ihren Client-Anmeldeinformationen konfiguriert wurden.

### PostExport-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

```bash
# Exportieren eines Arbeitsblatts in das TIFF-Format
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung mit Aspose.Cells Cloud. Ein SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der unterstützten SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

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