---
title: "Excel zu PNG"
second_title: "Dokument"
linktitle: "Excel zu PNG"
type: docs
url: /deconvert-excel-file-to-png-file/
keywords: "Excel zu PNG, Aspose.Cells Cloud, REST-API, Tabellenkonvertierung, PNG-Format"
description: "Konvertieren Sie Excel-Tabellen mit der Aspose.Cells Cloud REST-API in PNG-Bilder. Unterstützt mehrere SDKs und liefert detaillierte Beispiele für verschiedene Programmiersprachen."
weight: 90
---

Diese REST-API konvertiert eine Tabellendatei in das PNG-Format.

## REST-API-Spezifikation

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Abfrageparameter**

| Parametername         | Typ    | Beschreibung                                                                                      |
| --------------------- | ------ | ------------------------------------------------------------------------------------------------- |
| password              | string | Das Passwort, das zum Öffnen der Excel-Datei erforderlich ist.                                  |
| storageName           | string | Der Name des Speichers, in dem sich die Datei befindet.                                          |
| checkExcelRestriction | bool   | Gibt an, ob Excel-Dateieinschränkungen beim Ändern von Zellen oder zugehörigen Objekten geprüft werden sollen. |

### **Anforderungstextparameter**

| Parametername | Typ       | Beschreibung                                                               |
| ------------- | --------- | -------------------------------------------------------------------------- |
| datafile      | data file | Die Tabellendatei, die im ersten Teil der Multi-Part-Anforderung enthalten ist. |

### **Antwort**

Die API gibt ein **FileInfo**-Objekt zurück, das die generierte PNG-Datei enthält.

| Feld            | Typ    | Beschreibung                                 |
| --------------- | ------ | -------------------------------------------- |
| **Filename**    | string | Name der PNG-Datei (z. B. `beispiel.png`).  |
| **FileSize**    | int    | Größe der Datei in Bytes.                    |
| **FileContent** | string | Base64-kodierter Inhalt der PNG-Datei.       |

[FileInfo](/cells/file-info/)


**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.                |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Verwendung der PostConvertWorkbookToPNG-API mit SDKs

### PostConvertWorkbookToPNG-API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das Befehlszeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt-Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Weitere APIs mit ähnlichen Funktionen

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Speichert eine Excel-Datei als CSV (oder andere Formate) mit zusätzlichen Einstellungen und speichert das Ergebnis.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konvertiert eine Excel-Datei in CSV (oder andere Formate) mit optionalen Parametern und gibt das Ergebnis in der Antwort zurück.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Ruft eine Excel-Datei ab und kann sie bei Bedarf dynamisch in CSV (oder andere Formate) konvertieren.

---