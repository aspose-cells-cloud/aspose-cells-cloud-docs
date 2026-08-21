---
title: "Excel zu Docx"
second_title: "Dokument"
linktitle: "Excel zu Docx"
type: docs
url: /de/deconvert-excel-file-to-docx-file/
keywords: "Excel-zu-Docx-Konvertierung, Aspose.Cells Cloud, REST API, Tabellenkalkulationskonvertierung, Dokumentengenerierung"
description: "Konvertieren Sie Excel-Tabellenkalkulationen mit der Aspose.Cells Cloud REST API in DOCX-Dokumente. Unterstützt mehrere SDKs und Programmiersprachen für nahtlose Integration."
weight: 90
---

Diese REST API konvertiert eine Tabellendatei in das DOCX-Format.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.



**Abfrageparameter**

| Parametername         | Typ    | Beschreibung                                                                                          |
| --------------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| password              | string | Das Passwort, das zum Öffnen der Excel-Datei erforderlich ist.                                      |
| storageName           | string | Der Name des Speichers, in dem sich die Datei befindet.                                              |
| checkExcelRestriction | bool   | Gibt an, ob Einschränkungen der Excel-Datei geprüft werden sollen, wenn der Benutzer zellbezogene Objekte ändert. |

**Anforderungstextparameter**

| Parametername | Typ       | Beschreibung                                                       |
| ------------- | --------- | ------------------------------------------------------------------ |
| datafile      | data file | Die Datendatei, die im ersten Teil des multipart-Anforderungstexts gespeichert ist. |

**Antwort**

Die API gibt ein **FileInfo**-Objekt zurück, das die generierte Word-Datei enthält.

| Feld            | Typ    | Beschreibung                                     |
| --------------- | ------ | ----------------------------------------------- |
| **Filename**    | string | Name der Word-Datei (z. B. `beispiel.docx`).   |
| **FileSize**    | int    | Größe der Datei in Bytes.                       |
| **FileContent** | string | Base64-kodierter Inhalt der Word-Datei.         |


[FileInfo](/cells/file-info/)

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                     |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                       |

## So verwenden Sie die PostConvertWorkbookToDocx API mit SDKs

### PostConvertWorkbookToDocx API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Befehlszeilentool **cURL** verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "beispiel.docx",
  "FileSize": 12345,
  "FileContent": "Dateiinhalt: base64_kodierter_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Weitere APIs, die diese Funktion implementieren

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Speichert eine Excel-Datei als DOCX-Datei mit zusätzlichen Einstellungen und speichert das Ergebnis im angegebenen Speicher.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konvertiert eine Excel-Datei mit optionalen Einstellungen in eine DOCX-Datei und gibt das Ergebnis in der Antwort zurück.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Ruft eine Excel-Arbeitsmappe ab und konvertiert sie mit optionalen Parametern in eine DOCX-Datei.

---