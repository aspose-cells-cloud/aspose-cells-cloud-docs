---
title: "Excel-Datei in mehrere Dateien aufteilen"
second_title: "Dokument"
linktitle: "Mehrseitige Excel-Dateien aufteilen"
type: docs
url: /split-an-excel-file-to-multi-files/
aliases: [/split-excel-workbooks/,/workbook/split/]
keywords: "Aspose.Cells, Cloud, Excel, Aufteilen, API, PDF, CSV, JSON"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um mehrseitige Excel-Arbeitsmappen in separate Dateien aufzuteilen. Unterstützt Ausgabeformate wie PDF, CSV und JSON und ist über SDKs für Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift verfügbar."
weight: 32
ArticleTitle: "Excel-Datei in mehrere Dateien aufteilen – Aspose.Cells Cloud-Dokumentation"
---

Die Aspose.Cells Cloud REST API teilt mehrseitige Excel-Arbeitsmappen in separate Dateien auf.

**Voraussetzungen**  
Bevor Sie die API aufrufen, müssen Sie ein gültiges JWT-Token erhalten und es in den `Authorization`-Header jeder Anforderung einbinden. Details dazu finden Sie im [Authentifizierungsleitfaden](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## PostSplit API

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ   | Ort       | Beschreibung                                                      |
|---------------|-------|-----------|-------------------------------------------------------------------|
| file          | file  | formData  | Die hochzuladende Excel-Arbeitsmappe.                            |
| format        | string| query     | Gewünschtes Ausgabeformat (z. B. `pdf`, `csv`, `json`).          |
| password      | string| query     | Passwort für eine verschlüsselte Arbeitsmappe (optional).        |
| from          | integer| query    | Index des ersten einzubeziehenden Blatts (1-basiert).            |
| to            | integer| query    | Index des letzten einzubeziehenden Blatts (inklusiv).            |

### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[Dateiname1]",
            "Filesize" : [Dateigröße],
            "FileContent" : "[Base64-Zeichenfolge]"
        },        
        {
            "Filename" : "[Dateiname2]",
            "Filesize" : [Dateigröße],
            "FileContent" : "[Base64-Zeichenfolge]"
        },        
        {
            "Filename" : "[Dateiname3]",
            "Filesize" : [Dateigröße],
            "FileContent" : "[Base64-Zeichenfolge]"
        }
    ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.        |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.                |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

## Verwendung der PostSplit API mit SDKs

### PostSplit API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

**HTTP-Statuscodes**

| Code | Bedeutung                     | Beschreibung                                                                 |
|------|-------------------------------|------------------------------------------------------------------------------|
| 200  | OK                            | Die Arbeitsmappe wurde erfolgreich aufgeteilt; Antwort enthält Dateiliste.  |
| 400  | Bad Request                   | Fehlende oder ungültige Parameter (z. B. nicht unterstütztes Format).       |
| 401  | Unauthorized                  | Ungültiges oder fehlendes JWT-Token.                                        |
| 500  | Internal Server Error         | Auf Serverseite ist ein unerwarteter Fehler aufgetreten.                    |

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach zu nutzen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# Ersetzen Sie xxxxx1.xlsx und xxxxx2.xlsx durch die Pfade zu Ihren Excel-Dateien
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64-Zeichenfolge--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64-Zeichenfolge--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt Low-Level-Details und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---