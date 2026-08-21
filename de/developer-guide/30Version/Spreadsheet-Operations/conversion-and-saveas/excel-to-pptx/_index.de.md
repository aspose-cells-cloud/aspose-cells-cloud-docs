---
title: "Konvertieren Sie Excel in PPTX mithilfe der Aspose.Cells Cloud API v3.0"
second_title: "Dokument"
linktitle: "Excel zu PPTX"
type: docs
url: /convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, Konvertierung, REST API, Cloud"
description: "Erfahren Sie, wie Sie Excel-Arbeitsmappen mithilfe der Aspose.Cells Cloud REST API v3.0 in PPTX-Präsentationen konvertieren. Enthält cURL-Anforderungen, SDK-Codebeispiele, Authentifizierung und Fehlerbehandlung."
weight: 90
ArticleTitle: "Konvertieren Sie Excel in PPTX mithilfe der Aspose.Cells Cloud API v3.0"
---

Diese REST API konvertiert eine Tabellendatei in das PPTX-Format.

## PostConvertWorkbookToPptx API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Abfrageparameter

| Parametername           | Typ    | Beschreibung                                                                                      |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------- |
| `password`              | string | Passwort zum Öffnen der Excel-Arbeitsmappe.                                                      |
| `storageName`           | string | Name des Speichers, in dem sich die Quelldatei befindet.                                         |
| `checkExcelRestriction` | bool   | Gibt an, ob Excel-Dateibeschränkungen beim Ändern zellbezogener Objekte erzwungen werden sollen. |

### Anforderungstextparameter

| Parametername | Typ       | Beschreibung                                                   |
| ------------- | --------- | -------------------------------------------------------------- |
| `datafile`    | Dateidaten | Die Excel-Datei im ersten Teil des multipart-Anforderungstexts. |

**Beispiel für multipart-Anforderungstext (vereinfacht):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<binärer Inhalt von input.xlsx>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### Antwort

Die API gibt ein **FileInfo**-Objekt zurück, das die generierte PPTX-Datei enthält.

| Feld            | Typ    | Beschreibung                                         |
| --------------- | ------ | ---------------------------------------------------- |
| **Filename**    | string | Name der PPTX-Datei (z. B. `example.pptx`).         |
| **FileSize**    | int    | Dateigröße in Bytes.                                 |
| **FileContent** | string | Base64-codierter Inhalt der PPTX-Datei.             |

[FileInfo](/cells/file-info/)


**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                            |
|------|-----------------------------|-------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Operationsdetails.      |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).|
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                   |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                  |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                             |

*Hinweise:* Der Endpunkt unterstützt gängige Excel-Formate (`.xlsx`, `.xls`, `.xlsm`). Die maximale Dateigröße beträgt 50 MB. Die Konvertierung kann für Arbeitsmappen mit Makros oder geschützten Blättern eingeschränkt sein, sofern nicht die entsprechenden Parameter übermittelt werden.

## Verwendung der PostConvertWorkbookToPptx API mit SDKs

### PostConvertWorkbookToPptx API-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstractiert die Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud" rel="noopener noreferrer").

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Weitere APIs, die diese Funktion implementieren

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Konvertiert eine Excel-Datei in PDF.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Konvertiert eine Excel-Datei in PNG-Bilder.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Konvertiert eine Excel-Datei in SVG-Format.