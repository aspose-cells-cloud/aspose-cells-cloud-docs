---
title: "Wasserzeichen zu Excel-Dateien hinzufügen"
second_title: "Dokument"
linktitle: "Wasserzeichen zu Excel-Dateien hinzufügen"
type: docs
url: /de/add-watermark-into-excel-files/
aliases: [/de/watermark/]
keywords: "Wasserzeichen zu Excel hinzufügen, Aspose.Cells Cloud, REST-API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Erfahren Sie, wie Sie einen Textwasserzeichen mit der Aspose.Cells Cloud REST-API (v3.0) zu Excel-Arbeitsmappen hinzufügen. Enthält ein cURL-Beispiel, erforderliche Parameter und Antwortdetails."
weight: 39
ArticleTitle: "Wasserzeichen zu Excel-Dateien hinzufügen – Aspose.Cells Cloud-Dokumentation"
---

Diese REST-API fügt **Wasserzeichen** zu Excel-Dateien hinzu.

**Voraussetzungen:** Sie müssen ein gültiges JWT-Access-Token erhalten und sicherstellen, dass die Excel-Datei in einem unterstützten Format vorliegt (z. B. `.xlsx`, `.xls`).  
**Hintergrund:** Ein Wasserzeichen ist ein halbtransparenter Textüberlagerung, der auf jeder Arbeitsmappe angezeigt wird, um den Besitz oder die Vertraulichkeit kenntlich zu machen.

## PostWatermark API

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ    | Speicherort                     | Beschreibung                                               |
| --------------- | ------ | ------------------------------- | ---------------------------------------------------------- |
| `file`          | file   | formData (multipart body)       | Die Excel-Datei, der das Wasserzeichen hinzugefügt werden soll. |
| `text`          | string | query                           | Der anzuzeigende Wasserzeichen-Text.                      |
| `color`         | string | query                           | Die Wasserzeichenfarbe im ARGB-Hex-Format (z. B. `004433ff`). |

### **Antwort**

Die JSON-Antwort enthält ein **Files**-Array. Für jedes Dateiobjekt:

- **Filename** – Name der verarbeiteten Arbeitsmappe.  
- **FileSize** – Dateigröße in Byte.  
- **FileContent** – Base64-kodierter Inhalt der mit Wasserzeichen versehenen Excel-Datei; dekodieren Sie diesen, um die eigentliche Datei zu erhalten.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[Dateiname1]",
            "Filesize" : [Dateigröße],
            "FileContent" : "[Base64String]"
        },
        {
            "Filename" : "[Dateiname2]",
            "Filesize" : [Dateigröße],
            "FileContent" : "[Base64String]"
        },
        {
            "Filename" : "[Dateiname3]",
            "Filesize" : [Dateigröße],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                           |
|------|-----------------------------|--------------------------------------------------------|
| 200  | OK                          | Wasserzeichen erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                   |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.  |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                             |

## Verwendung der PostWatermark API mit SDKs

### PostWatermark API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Befehlszeilentool **cURL** verwenden, um Aspose.Cells-Webdienste aufzurufen. Das folgende Beispiel zeigt eine vollständige Anforderung einschließlich des erforderlichen Authentifizierungs-Headers. Ersetzen Sie `<your-jwt-token>` durch ein gültiges JWT-Access-Token, das Sie vom Aspose-Authentifizierungsendpunkt erhalten haben.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}