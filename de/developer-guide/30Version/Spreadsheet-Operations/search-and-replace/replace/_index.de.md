---
title: "Text aus Excel-Dateien ersetzen"
second_title: "Dokument"
linktitle: "Ersetzen ohne Speicherung"
type: docs
url: /de/replace/
keywords: "Excel-Text ersetzen, Aspose.Cells Cloud, REST-API, Tabellenkalkulation ersetzen, API, Textersetzung in Excel-Dateien"
description: "Verwenden Sie die Aspose.Cells Cloud REST-API, um vorhandenen Text in Excel-Dateien durch neue Werte zu ersetzen. Unterstützt SDKs für C#, Java, Python, Node.js, PHP, Ruby, Go und Perl."
weight: 80
---


## REST-API

Diese REST-API ersetzt Daten in Excel-Dateien.

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### Sicherheit und Authentifizierung

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Anforderungsparameter

| Parametername | Typ   | Speicherort               | Beschreibung                                      |
|---------------|-------|---------------------------|---------------------------------------------------|
| **file**      | Datei | formData (multipart)      | Zu verarbeitende Excel-Datei.                    |
| **text**      | Zeichenkette | query             | Zu ersetzender Textstring.                        |
| **newtext**   | Zeichenkette | query             | Ersatztext.                                       |
| **password**  | Zeichenkette | query             | Passwort für eine geschützte Arbeitsmappe (optional). |
| **sheetname** | Zeichenkette | query             | Name des Ziel-Worksheets (optional).             |

### **Antwort**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[Dateiname1]",
      "Filesize" : [Dateigröße],
      "FileContent" : "[Base64-Zeichenkette]"
    },
    {
      "Filename" : "[Dateiname2]",
      "Filesize" : [Dateigröße],
      "FileContent" : "[Base64-Zeichenkette]"
    },
    {
      "Filename" : "[Dateiname3]",
      "Filesize" : [Dateigröße],
      "FileContent" : "[Base64-Zeichenkette]"
    }
  ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.            |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                       |

## So verwenden Sie die PostReplace-API mit SDKs

### PostReplace-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
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
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64-Zeichenkette--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64-Zeichenkette--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}