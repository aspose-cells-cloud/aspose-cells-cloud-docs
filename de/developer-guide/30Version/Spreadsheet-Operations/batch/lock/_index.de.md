---
title: "Excel-Dateien im Stapel verriegeln"
second_title: "Dokument"
type: docs
url: /de/batch/lock
keywords: "Stapelverriegelung, Excel, Aspose.Cells, Cloud API, Tabellenkalkulation, Dateischutz"
description: "Die Aspose.Cells Cloud API ermöglicht das Stapelverriegeln mehrerer Excel-Dateien. Nutzen Sie den REST-Endpunkt oder eines der unterstützten SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go usw.), um Dateien in großen Mengen zu verriegeln."
weight: 100
---

Diese REST-API ermöglicht das **Stapelverriegeln** von kompatiblen Excel-Dateien.

## REST-API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Anforderungsparameter

| Parametername    | Typ                | Ort     | Beschreibung                                 |
|------------------|--------------------|---------|---------------------------------------------|
| BatchLockRequest | BatchLockRequest   | body    | JSON-Body, der die Verriegelungsparameter enthält. |

#### **BatchLockRequest**-Eigenschaften

| Name            | Typ                      | Beschreibung                                          | Hinweise   |
|-----------------|--------------------------|-------------------------------------------------------|------------|
| SourceFolder    | string                   | Ordner, der die Quell-Excel-Dateien enthält.         | optional   |
| MatchCondition  | MatchConditionRequest    | Bedingungen zur Auswahl der zu verriegelnden Dateien.| optional   |
| Password        | string                   | Passwort, das auf die verriegelten Dateien angewendet wird. | optional   |
| OutFolder       | string                   | Zielordner für die verriegelten Dateien.             | optional   |

#### **MatchConditionRequest**-Eigenschaften

| Name               | Typ       | Beschreibung                                          | Hinweise   |
|--------------------|-----------|-------------------------------------------------------|------------|
| RegexPattern       | string    | Regulärer Ausdruck zur Übereinstimmung mit Dateinamen.| optional   |
| FullMatchConditions| string[]  | Exakte Dateinamenübereinstimmungen für die Verriegelung. | optional   |

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

| Code | Bedeutung                   | Wann zurückgegeben                      |
|------|-----------------------------|-----------------------------------------|
| 200 OK | Arbeitsmappe erfolgreich erstellt | Normaler Ablauf                         |
| 201 Created | Arbeitsmappe erstellt (Alternative Antwort) | Wenn die API den Status „Created“ zurückgibt |
| 400 Bad Request | Ungültige Parameter | Clientseitiger Fehler                   |
| 401 Unauthorized | Fehlendes oder ungültiges Token | Authentifizierungsfehler               |
| 409 Conflict | Datei existiert und `isWriteOver=false` | Konflikt mit vorhandener Datei          |

## Verwendung der PostBatchLock-API mit SDKs

### PostBatchLock-API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

Die Verwendung eines SDKs ist die schnellste Methode zur Entwicklung. Ein SDK abstractiert die Low-Level-Details, sodass Sie sich auf Ihre Verriegelaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}