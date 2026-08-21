---
title: "Massenfreigabe"
second_title: "Dokument"
type: docs
url: /de/batch/unlock
keywords: "Massenfreigabe, Aspose.Cells Cloud, Excel, REST-API, Tabellendokument, Cloud-SDK"
description: "Freigeben mehrerer Excel-Dateien in einem Rutsch mithilfe der Aspose.Cells Cloud REST-API. Unterstützt SDKs für C#, Java, Python und weitere Sprachen."
weight: 100
---

Diese REST-API führt die Massenfreigabe für berechtigte Excel-Dateien durch.

## REST-API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ | Speicherort | Beschreibung |
|---------------|-----|-------------|--------------|
| **BatchLockRequest** |  | body | Anforderungstext, der die Freigabeeinstellungen enthält. |

### **BatchLockRequest**-Eigenschaften

| Name            | Typ                      | Beschreibung                                      | Hinweise |
|-----------------|--------------------------|---------------------------------------------------|----------|
| SourceFolder    | string                   | Ordner, der die Quell-Excel-Dateien enthält.     | [optional] |
| MatchCondition  | MatchConditionRequest    | Kriterien zur Auswahl der Dateien für die Freigabe.| [optional] |
| Password        | string                   | Kennwort, das für geschützte Arbeitsmappen verwendet wird. | [optional] |
| OutFolder       | string                   | Zielordner für die freigegebenen Dateien.        | [optional] |

### **MatchConditionRequest**-Eigenschaften

| Name               | Typ       | Beschreibung                                     | Hinweise |
|--------------------|-----------|--------------------------------------------------|----------|
| RegexPattern       | string    | Regulärer Ausdruck zum Abgleich von Dateinamen. | [optional] |
| FullMatchConditions| string[]  | Exakte Dateinamensbedingungen zum Abgleich.    | [optional] |

### Anforderungstextparameter

| Parametername | Typ | Beschreibung                                      |
|---------------|-----|---------------------------------------------------|
| data          | file | Binärinhalt der zu erstellenden Arbeitsmappendatei. |

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

| Code | Bedeutung                     | Wann zurückgegeben                          |
|------|-------------------------------|---------------------------------------------|
| 200 OK | Arbeitsmappe erfolgreich erstellt | Normaler Ablauf                             |
| 201 Created | Arbeitsmappe erstellt (Alternative Antwort) | Wenn die API einen „created“-Status zurückgibt |
| 400 Bad Request | Ungültige Parameter | Client-seitiger Fehler                      |
| 401 Unauthorized | Fehlendes oder ungültiges Token | Authentifizierungsfehler                   |
| 409 Conflict | Datei vorhanden und `isWriteOver=false` | Konflikt mit bestehender Datei             |

## Verwendung der PostBatchLock-API mit SDKs

### PostBatchLock-API-Spezifikation

Die [OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

Die Verwendung eines SDKs ist der schnellste Weg, um Freigabefunktionen zu entwickeln. Ein SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}