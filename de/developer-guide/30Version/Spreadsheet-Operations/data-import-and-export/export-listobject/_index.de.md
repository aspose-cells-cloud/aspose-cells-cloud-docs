---
title: "Listobjekt exportieren"
second_title: "Dokument"
linktitle: "Listobjekt"
type: docs
url: /de/export-excel-listobject-to-different-formats/
aliases: [  /de/export/excel-listobject-to-different-formats/ ]
keywords: "Listobjekt exportieren, Excel-Listobjekt, Aspose.Cells Cloud, REST-API, PDF, CSV, JSON, XLSX, ODS, PNG, TIFF, SDKs"
description: "Die Aspose.Cells Cloud REST-API ermöglicht den Export von Excel-Listobjekten in eine Vielzahl von Dateiformaten. SDKs sind für viele Programmiersprachen verfügbar, darunter C#, Java, Python, Node.js, Go, PHP, Ruby, Perl und Swift."
weight: 20
---

Sie können die folgenden Formate exportieren: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Anforderungsparameter

| Parametername | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Erforderlich | Beschreibung |
|---------------|--------|------------------------------------|--------------|--------------|
| file          | Datei  | formData                           | Ja           | Hochzuladende Datei |
| objectType    | Zeichenkette | query                       | Ja           | Typ des zu exportierenden Objekts. Für den Diagrammexport verwenden Sie `chart`. Weitere mögliche Werte sind `worksheet`, `picture`, usw. |
| format        | Zeichenkette | query                       | Ja           | Gewünschtes Ausgabeformat. Unterstützte Werte: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### Antwort

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2_ListObjects_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung |
|------|-----------------------------|--------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Ungültige Anforderung       | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert           | Ungültiges oder fehlendes JWT-Token. |
| 413  | Anforderungstext zu groß    | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Interner Serverfehler       | Unerwarteter Serverfehler. |

## Verwendung der PostExport-API mit SDKs

### PostExport-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das Befehlszeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von cURL Aufrufe an die Cloud-API durchführen.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=listobject&format=tiff" \
-H "accept: multipart/form-data" \
-H "Content-Type: multipart/form-data" \
-H "x-aspose-client: Containerize.Swagger" \
-d '{"File":{}}'
```

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportListObject.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportListObject.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportListObject.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportListObject.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportListObject.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportListObject.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportListObject.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportListObject.go" >}}
{{< /tab >}}

{{< /tabs >}}