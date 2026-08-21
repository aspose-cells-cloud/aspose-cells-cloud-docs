---
title: "Excel zu CSV"
second: "Dokument"
linktitle: "Excel zu CSV"
type: docs
url: /de/deconvert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel zu CSV, Aspose.Cells Cloud, REST API, Tabellenkalkulationskonvertierung, CSV-Datei, Dateikonvertierung"
description: "Konvertieren Sie Excel-Tabellenkalkulationen mit der Aspose.Cells Cloud REST API in CSV. Unterstützt mehrere SDKs und Programmiersprachen für eine einfache Integration."
weight: 90
---

Diese REST API konvertiert eine Tabellenkalkulationsdatei in eine CSV-Formatdatei.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Abfrageparameter

| Parametername           | Typ    | Beschreibung                                                                                     |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------ |
| `password`              | string | Das Passwort, das zum Öffnen der Excel-Datei erforderlich ist.                                  |
| `storageName`           | string | Der Name des Speichers, in dem sich die Datei befindet.                                         |
| `checkExcelRestriction` | bool   | Ob die Excel-Dateieinschränkungen geprüft werden sollen, wenn der Benutzer zellbezogene Objekte ändert. |

### Anforderungstextparameter

| Parametername | Typ       | Beschreibung                                                   |
| ------------- | --------- | -------------------------------------------------------------- |
| `datafile`    | data file | Die Datenfile, die im ersten Teil des multipart-Anforderungstexts enthalten ist. |

### Antwort

Die API gibt ein **FileInfo**-Objekt zurück, das die generierte CSV-Datei enthält.

| Feld            | Typ    | Beschreibung                                       |
| --------------- | ------ | -------------------------------------------------- |
| **Filename**    | string | Name der CSV-Datei (z. B. `example.csv`).         |
| **FileSize**    | int    | Größe der Datei in Bytes.                          |
| **FileContent** | string | Base64-kodierter Inhalt der CSV-Datei.            |

[FileInfo](/cells/file-info/)


**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                   |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                           |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.          |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                     |

## So verwenden Sie die PostConvertWorkbookToCSV-API mit SDKs

### PostConvertWorkbookToCSV-API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}