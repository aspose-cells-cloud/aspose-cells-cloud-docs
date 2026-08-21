---
title: "Excel-Dateien im Batch schützen"
second_title: "Dokument"
type: docs
url: /batch/protect
keywords: "Excel-Dateien im Batch schützen, Aspose Cells Cloud, REST-API, Excel-Schutz, Batch-Schutz"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud REST-API verwenden, um mehrere Excel-Dateien im Batch zu schützen. Enthält Anforderungsdetails, cURL-Beispiel und SDK-Codebeispiele für verschiedene Sprachen."
weight: 100
---

Diese REST-API ermöglicht die **Batch-Schützung** berechtigter Excel-Dateien.

## REST-API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername         | Typ                 | Ort     | Beschreibung                                                                                              |
|-----------------------|---------------------|---------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body    | JSON-Payload, der den Quellordner, die Übereinstimmungsbedingungen, den Schutztyp, das Passwort und den Ausgabefolder angibt. |

### BatchProtectRequest-Eigenschaften

| Name            | Typ                     | Beschreibung                                                                                 | Hinweise |
|-----------------|-------------------------|----------------------------------------------------------------------------------------------|----------|
| SourceFolder    | string                  | Ordner, der die Quell-Excel-Dateien enthält.                                                | optional |
| MatchCondition  | MatchConditionRequest   | Kriterien zur Auswahl der zu schützenden Dateien.                                            | optional |
| ProtectionType  | string                  | Art des anzuwendenden Schutzes (z. B. `All`, `ReadOnly`).                                    | optional |
| Password        | string                  | Passwort, das für die geschützten Dateien festgelegt werden soll.                            | optional |
| OutFolder       | string                  | Zielordner für die geschützten Dateien.                                                      | optional |

### MatchConditionRequest-Eigenschaften

| Name                | Typ        | Beschreibung                                   | Hinweise |
|---------------------|------------|------------------------------------------------|----------|
| RegexPattern        | string     | Regulärer Ausdruck zur Übereinstimmung mit Dateinamen. | optional |
| FullMatchConditions | string[]   | Liste exakter Dateinamenbedingungen.          | optional |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | Binärinhalt der zu erstellenden Arbeitsmappe. |

### **Antwort**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```
**HTTP-Statuscodes**

| Code | Bedeutung                     | Wann zurückgegeben                           |
|------|-------------------------------|----------------------------------------------|
| 200 OK | Arbeitsmappe erfolgreich erstellt | Normaler Ablauf                              |
| 201 Created | Arbeitsmappe erstellt (Alternative Antwort) | Wenn die API den „Created“-Status zurückgibt |
| 400 Bad Request | Ungültige Parameter | Client-seitiger Fehler                        |
| 401 Unauthorized | Fehlendes oder ungültiges Token | Authentifizierungsfehler                    |
| 409 Conflict | Datei existiert und `isWriteOver=false` | Konflikt mit vorhandener Datei              |

## So verwenden Sie die PostProtectConvert-API mit SDKs

### PostProtectConvert-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PostProtectConvert) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDKs verwenden

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}
---