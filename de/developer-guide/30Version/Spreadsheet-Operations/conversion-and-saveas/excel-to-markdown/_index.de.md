---
title: "Excel in Markdown konvertieren"
second_title: "Dokument"
linktitle: "Excel zu Markdown"
type: docs
url: /de/convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, Konvertierung, Aspose.Cells Cloud, REST API, Excel-zu-Markdown-Konvertierung, Aspose Cells Markdown API, Excel-Markdown-Export"
description: "Konvertieren Sie Excel-Arbeitsblätter mithilfe der Aspose.Cells Cloud REST API in Markdown – inklusive cURL-Beispiel, SDK-Snippets, erforderlichen Parametern und Authentifizierungsdetails."
weight: 100
ArticleTitle: "Excel in Markdown konvertieren – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST API konvertiert eine Spreadsheet-Datei in eine Datei im Markdown-Format.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Abfrageparameter


| Parametername         | Typ    | Ort    | Beschreibung                                                                                      |
| --------------------- | ------ | ------ | ------------------------------------------------------------------------------------------------- |
| password              | string | query  | Passwort, das zum Öffnen der Excel-Datei erforderlich ist.                                       |
| storageName           | string | query  | Name des Speichers, in dem sich die Datei befindet.                                              |
| checkExcelRestriction | bool   | query  | Gibt an, ob Excel-spezifische Einschränkungen beim Ändern von Zellen oder zugehörigen Objekten erzwungen werden sollen. |
| datafile              | file   | body   | Die Excel-Datei, die als erster Teil des multipart-Inhalts hochgeladen werden soll.             |

### Antwort

Die API gibt ein JSON-Objekt vom Typ **FileInfo** zurück:

- **FileInfo** – Objekt, das den Namen, die Größe und den base64-codierten Inhalt der generierten Markdown-Datei enthält.

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### Fehlerantworten

| HTTP-Code | Beschreibung                                                     | Beispiel-JSON-Body                              |
| --------- | ---------------------------------------------------------------- | ----------------------------------------------- |
| 401       | Nicht autorisiert – fehlender oder ungültiger Token.            | `{"error":"Invalid access token."}`             |
| 400       | Ungültige Anforderung – fehlende erforderliche Parameter oder ungültiges Dateiformat. | `{"error":"The 'datafile' field is required."}` |
| 500       | Interner Serverfehler – unerwartetes Serverproblem.             | `{"error":"An unexpected error occurred."}`     |



## Verwendung der PostConvertWorkbookToMarkdown API mit SDKs

### PostConvertWorkbookToMarkdown API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Befehlszeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt die Details der unteren Schicht, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Weitere APIs, die diese Funktion implementieren

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Speichert eine Excel-Datei als HTML mit zusätzlichen Einstellungen und speichert das Ergebnis.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konvertiert eine Excel-Datei mit zusätzlichen Optionen in HTML und gibt das Ergebnis in der Antwort zurück.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Ruft eine Excel-Datei ab und kann sie mit optionalen Einstellungen in HTML konvertieren.
---