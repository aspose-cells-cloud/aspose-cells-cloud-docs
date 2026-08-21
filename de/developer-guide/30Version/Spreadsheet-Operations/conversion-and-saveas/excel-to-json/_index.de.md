---
title: "Excel zu JSON"
second_title: "Dokument"
linktitle: "Excel zu JSON"
type: docs
url: /de/convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel zu JSON, Cloud API, Tabellenkalkulationskonvertierung, REST API"
description: "Erfahren Sie, wie Sie Excel-Tabellen mit der Aspose.Cells Cloud REST API in JSON-Dateien konvertieren. Enthält cURL-Beispiel, SDK-Snippets (C#, Java, Python), erforderliche Parameter, Authentifizierung und Antwortformat."
weight: 100
ArticleTitle: "Konvertieren Sie Excel in JSON mit der Aspose.Cells Cloud API – Schnellleitfaden"
---


## REST API

Diese REST API konvertiert eine Tabellenkalkulationsdatei in eine im JSON-Format formatierte Datei.


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Anfrage

**Abfrageparameter**

| Parametername           | Typ    | Beschreibung                                                              |
| ----------------------- | ------ | ------------------------------------------------------------------------- |
| `password`              | string | Kennwort zum Öffnen der Excel-Datei (optional).                           |
| `storageName`           | string | Name des Speichers, in dem sich die Datei befindet (optional).            |
| `checkExcelRestriction` | bool   | Erzwingt Excel-spezifische Einschränkungen beim Ändern von Zellen (optional). |

**Anfragetextparameter**

| Parametername | Typ | Beschreibung                                                                                      |
| ------------- | --- | ------------------------------------------------------------------------------------------------- |
| `datafile`    | file | Die hochzuladende Excel-Datei. Muss als erster Teil einer `multipart/form-data`-Anfrage gesendet werden. |

#### Beispiel cURL-Aufruf

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### Antwort

Der Dienst gibt ein **FileInfo**-Objekt zurück. Die wichtigsten Felder sind wie folgt beschrieben:

| Feld          | Typ    | Beschreibung                                                                     |
| ------------- | ------ | -------------------------------------------------------------------------------- |
| `Filename`    | string | Name der generierten JSON-Datei (z. B. `myWorkbook.json`).                       |
| `FileSize`    | integer | Größe der generierten Datei in Bytes.                                            |
| `FileContent` | string | Base64-codierter Inhalt der JSON-Datei. Decodieren Sie, um den eigentlichen JSON-Inhalt abzurufen. |

**Beispielantwort**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (Base64-Zeichenfolge) ..."
}
```

#### Fehlerbehandlung

Falls die Anfrage fehlschlägt, gibt die API ein Fehlerobjekt mit folgender Struktur zurück:

| Feld      | Typ    | Beschreibung                              |
| --------- | ------ | ----------------------------------------- |
| `Code`    | string | Maschinenlesbarer Fehlerbezeichner.       |
| `Message` | string | Menschlich lesbare Beschreibung des Fehlers. |

Häufige HTTP-Statuscodes:

- **400** – Bad Request (z. B. fehlende Datei, ungültige Parameter).
- **401** – Unauthorized (ungültiger oder fehlender Zugriffstoken).
- **500** – Internal Server Error.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                             |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                     |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.   |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                               |
## So verwenden Sie die PostConvertWorkbookToJson API mit SDKs

### PostConvertWorkbookToJson API-Spezifikation

Die <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Aspose.Cells OpenAPI-Spezifikation – Konvertieren Sie Arbeitsmappe in JSON">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (Base64-Zeichenfolge)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="Aspose.Cells Cloud SDKs auf GitHub">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Weitere APIs mit ähnlicher Funktionalität

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Speichert eine Excel-Datei als HTML-Datei mit zusätzlichen Einstellungen und speichert das Ergebnis im angegebenen Speicher.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konvertiert eine Excel-Datei mit zusätzlichen Einstellungen in eine HTML-Datei und gibt das Ergebnis in der Antwort zurück.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Ruft eine Excel-Datei ab; kann mit Abfrageparametern verwendet werden, um die Datei im HTML-Format zu erhalten.
---