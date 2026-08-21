---
title: "Excel-Dateien entsperren"
second_title: "Dokument"
linktitle: "Excel-Dateien entsperren"
type: docs
url: /de/unlock-excel-files/
aliases: [  /de/unlock/without-storage/ , /de/unlock/ , /de/unlock/without-using-storage/ ]
keywords: "Excel entsperren, Aspose.Cells Cloud, REST API, Excel entsperren, passwortgeschützte Arbeitsmappe, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Die Aspose.Cells Cloud REST API stellt einen Endpunkt zum Entsperrten passwortgeschützter Excel-Dateien bereit. SDKs sind für zahlreiche Programmiersprachen verfügbar, darunter Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift."
ArticleTitle: "Excel-Dateien mit der Aspose.Cells Cloud REST API entsperren"
weight: 70
---

Diese REST API entsperrt Excel-Dateien.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Anforderungsparameter

| Parametername   | Typ    | Speicherort              | Beschreibung                                     |
| ---------------- | ------ | ------------------------ | ------------------------------------------------ |
| file             | Datei  | formData (HTTP-Body)     | Hochzuladende Datei                              |
| password         | String | Query-String             | Passwort zum Entsperren der Datei (falls geschützt) |

### Antwort

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                             |
|------|-----------------------------|--------------------------------------------------------------------------|
| 200  | OK                          | Entsperrvorgang erfolgreich; Antwort enthält Details zum Vorgang.       |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                     |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größeinschränkung.             |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                               |

## Verwendung der PostUnlock-API mit SDKs

### PostUnlock-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf die Aufgaben Ihres Projekts zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

**Hinweise**  
- Die API kann mehrere Excel-Dateien in einer einzigen Anforderung entsperren; jede Datei wird im `Files`-Array der Antwort zurückgegeben.  
- Stellen Sie sicher, dass Ihre SDK-Version mit der API-Version (`v3.0`) übereinstimmt, um Kompatibilitätsprobleme zu vermeiden.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}