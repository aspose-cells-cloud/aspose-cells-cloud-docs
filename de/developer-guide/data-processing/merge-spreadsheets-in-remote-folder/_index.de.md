---
title: "Zusammenführen übereinstimmender Tabellenkalkulationen in einem Remotepfad"
description: "Kombinieren Sie Tabellenkalkulationsdateien, die im Aspose Cloud-Speicher gespeichert sind, in einer einzigen Datei. Unterstützt über 30 Ausgabeformate wie PDF, CSV, JSON, XLSX, ODS, XPS und mehr."
keywords: "Aspose.Cells, Tabellenkalkulationen zusammenführen, Remotepfad, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /de/merge-spreadsheets-in-remote-folder/
---

Kombinieren Sie mehrere Tabellenkalkulationsdateien, die sich in einem Remotepfad des Aspose Cloud-Speichers befinden, in einer einzigen Ausgabedatei. Der Vorgang erfolgt vollständig in der Cloud, sodass das Herunterladen der Quelldateien lokal entfällt. Über 30 Ausgabeformate werden unterstützt (PDF, CSV, JSON, XLSX, ODS, XPS, …).

## MergeSpreadsheetsInRemoteFolder API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter <a id="request-parameters"></a>

| Name                    | Typ     | Ort      | Erforderlich | Beschreibung                                                                                         |
| ----------------------- | ------- | -------- | ------------ | ---------------------------------------------------------------------------------------------------- |
| **folder**              | Zeichenkette | Abfrage  | **Ja**     | Cloud-Speicherordner, der die Quell-Tabellenkalkulationen enthält.                                  |
| **fileMatchExpression** | Zeichenkette | Abfrage  | **Ja**     | Muster zur Auswahl von Dateien (z. B. `*report*.xlsx`). Unterstützt Platzhalter `*` und `?`.         |
| **outFormat**           | Zeichenkette | Abfrage  | **Ja**     | Gewünschtes Ausgabeformat (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, …).                           |
| **mergeInOneSheet**     | Boolean | Abfrage  | **Ja**     | `true` – alle Daten werden in ein einziges Arbeitsblatt zusammengeführt. `false` – jede Quelldatei erhält ihr eigenes Arbeitsblatt. |
| **storageName**         | Zeichenkette | Abfrage  | Nein        | Benutzerdefinierter Speichername; bei Weglassung wird der Primärspeicher verwendet.                 |
| **outPath**             | Zeichenkette | Abfrage  | Nein        | Zielordner für die zusammengeführte Datei. Bei Weglassung wird die Datei im Quellordner gespeichert. |
| **outStorageName**      | Zeichenkette | Abfrage  | Nein        | Speichername, in dem die zusammengeführte Datei geschrieben wird.                                    |
| **fontsLocation**       | Zeichenkette | Abfrage  | Nein        | Pfad zu einem Ordner mit benutzerdefinierten Schriftarten (erforderlich für PDF-/Bildexport).        |
| **region**              | Zeichenkette | Abfrage  | Nein        | Gebietsschema für Zahlen-, Datums- und Währungsformatierung (z. B. `de-DE`, `en-US`).                |
| **password**            | Zeichenkette | Abfrage  | Nein        | Passwort zum Öffnen einer beliebigen geschützten Quelltabellenkalkulation.                           |

## Anforderungsbeispiel (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **Antwort**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

Die Datei kann direkt über die `FileUrl` heruntergeladen oder an dem durch `outPath` angegebenen Speicherort gespeichert werden.

**Details bei erfolgreicher Antwort**

| Statuscode | Content‑Type               | Beschreibung                                  |
| ---------- | -------------------------- | --------------------------------------------- |
| 200 OK     | `application/octet-stream` | Binärer Datenstrom der zusammengeführten Arbeitsmappe. |
| 202 Accepted | `application/json`         | JSON mit `FileUrl`, `FileName` usw.          |

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet die Größenbeschränkung.   |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                      |

## Verwenden der Merge-Spreadsheet-API mit SDKs

### OpenAPI-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">OpenAPI-Spezifikation</a> bietet eine maschinenlesbare Beschreibung der API und ermöglicht direkte REST-Interaktionen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encodiert)",
  "contentType": "MIME-Typ",
  "fileDownloadName": "optionaler Dateiname"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie die Low-Level-Details abstrahieren und Ihnen das Einfügen von Daten in ein Tabellenkalkulationsarbeitsblatt mit nur wenigen Codezeilen ermöglichen. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

---