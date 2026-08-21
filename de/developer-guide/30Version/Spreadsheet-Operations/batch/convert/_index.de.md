---
title: "Stapelverarbeitung von Excel-Dateien"
second: "Dokument"
type: docs
url: /batch/convert
keywords: "Stapelverarbeitung, Excel, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, Tabellenkalkulation"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud API nutzen können, um mehrere Excel-Dateien gleichzeitig in Formate wie PDF, CSV, JSON oder Markdown zu konvertieren. Dieser Leitfaden enthält Details zur REST-API, Anforderungsparameter, ein cURL-Beispiel und SDK-Codebeispiele für verschiedene Sprachen."
weight: 100
---

Diese REST-API ermöglicht die **Stapelverarbeitung** (Batch-Konvertierung) kompatibler Dateien.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername         | Typ    | Ort   | Beschreibung                                          |
|-----------------------|--------|-------|-------------------------------------------------------|
| **batchConvertRequest** | Objekt | body  | Anforderungstext mit Konvertierungseinstellungen.   |

#### Eigenschaften von BatchConvertRequest

| Name               | Typ                 | Beschreibung                                          | Hinweise     |
|--------------------|---------------------|-------------------------------------------------------|--------------|
| **SourceFolder**     | Zeichenkette        | Pfad zum Ordner, der die Quell-Excel-Dateien enthält. | [optional]   |
| **MatchCondition**   | MatchConditionRequest | Bedingungen zur Auswahl von Dateien für die Konvertierung. | [optional] |
| **Format**           | Zeichenkette        | Zielformat für die Konvertierung (z. B. `pdf`, `csv`). | [optional] |
| **OutFolder**        | Zeichenkette        | Zielordner, in dem die konvertierten Dateien gespeichert werden. | [optional] |
| **SaveOptions**      | SaveOptions         | Zusätzliche Optionen zur Steuerung des Dateispeichervorgangs. | [optional] |

#### Eigenschaften von MatchConditionRequest

| Name                    | Typ         | Beschreibung                                          | Hinweise     |
|-------------------------|-------------|-------------------------------------------------------|--------------|
| **RegexPattern**        | Zeichenkette | Regulärer Ausdruck zur Filterung von Dateinamen.     | [optional]   |
| **FullMatchConditions** | Zeichenketten-Array | Liste exakter Dateinamenbedingungen für die Übereinstimmung. | [optional] |

### Anforderungstext-Parameter

| Parametername | Typ | Beschreibung                                     |
|---------------|-----|--------------------------------------------------|
| data          | Datei | Binärinhalt der zu erstellenden Arbeitsmappe.  |

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

| Code | Bedeutung                   | Wann wird dieser zurückgegeben?           |
|------|-----------------------------|-------------------------------------------|
| 200 OK | Arbeitsmappe erfolgreich erstellt | Normaler Ablauf                           |
| 201 Created | Arbeitsmappe erstellt (Alternative Antwort) | Wenn die API einen „Created“-Status zurückgibt |
| 400 Bad Request | Ungültige Parameter | Client-seitiger Fehler                    |
| 401 Unauthorized | Fehlendes oder ungültiges Token | Authentifizierungsfehler                 |
| 409 Conflict | Datei existiert bereits und `isWriteOver=false` | Konflikt mit vorhandener Datei |

## Verwendung der PostBatchConvert API mit SDKs

### PostBatchConvert API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PostBatchConvert) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
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

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud), das eine vollständige Liste der Aspose.Cells Cloud SDKs enthält.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}