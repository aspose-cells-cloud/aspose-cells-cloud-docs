---
title: "Daten in einer Excel-Datei komprimieren"
ArticleTitle: "Daten in einer Excel-Datei komprimieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Excel-Dateien komprimieren"
type: docs
url: /compress-excel-files/
aliases: [/compress/]
keywords: "Excel-Datei komprimieren, Aspose.Cells Cloud, Excel-Komprimierung, Tabellenkalkulationskomprimierung, REST-API, Dateikomprimierung"
description: "Komprimieren Sie Excel-Dateien (XLS, XLSX, XLSM, XLSB, ODS) mithilfe der Aspose.Cells Cloud REST API. Legen Sie den Komprimierungsgrad fest, verarbeiten Sie mehrere Dateien und integrieren Sie über SDKs."
weight: 39
---

## Die PostCompress-API von Aspose.Cells Cloud-Webdiensten

**Voraussetzungen:**  
- Ein gültiges JWT-Token ist für die Authentifizierung erforderlich.  
- Unterstützte Dateiformate sind XLS, XLSX, XLSM, XLSB und ODS.  
- Die maximal zulässige Dateigröße beträgt 500 MB pro Anfrage (abhängig von den Dienstbeschränkungen).

Diese REST-API komprimiert Daten in einer Excel-Datei.

- Komprimiert XLS, XLSX, XLSM, XLSB, ODS  
- Komprimiert mehrere Excel-Tabellenkalkulationsdateien schnell  
- Wählen Sie den Komprimierungsgrad  
- Unterstützt mehrere Dateien  

### Web-API-Endpunkt

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anfrageparameter

| Parametername   | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                           |
|-----------------|-------|------------------------------------|--------------------------------------------------------|
| file            | Datei | formData                           | Hochzuladende Datei                                    |
| CompressLevel   | Integer | Abfrage                          | Komprimierungsgrad (0–100); höhere Werte bedeuten stärkere Komprimierung |

### Anforderungstextparameter

| Parametername | Typ  | Beschreibung                                      |
| ------------- | ---- | ------------------------------------------------ |
| data          | Datei | Binärinhalt der zu komprimierenden Arbeitsmappe. |

### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[zusammengeführter Dateiname]",
    "Filesize" : [Dateigröße],
    "FileContent" : "[Base64-Zeichenfolge]"
}
```

*Hinweis:* `FileContent` enthält die komprimierte Arbeitsmappe, codiert als Base64-Zeichenfolge. Die Länge der Zeichenfolge entspricht der Größe der komprimierten Datei; Sie können sie mit Standard-Base64-Utilities dekodieren, um die binäre Excel-Datei abzurufen.

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                             |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## Verwendung der PostCompress-API mit SDKs

### PostCompress-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
# Nutzen Sie HTTPS für eine sichere Verbindung
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
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

Die Verwendung eines SDKs ist die schnellste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK abstractiert die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre ProjektAufgaben zu konzentrieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}