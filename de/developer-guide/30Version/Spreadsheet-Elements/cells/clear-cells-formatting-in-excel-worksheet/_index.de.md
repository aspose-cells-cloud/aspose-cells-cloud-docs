---
title: "Zellformatierung in einem Excel-Arbeitsblatt löschen"
type: docs
url: /de/clear-cells-formatting-in-excel-worksheet/
weight: 100
keywords: "Aspose.Cells Cloud, Excel, Zellformatierung löschen, REST-API, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Verwenden Sie die Aspose.Cells Cloud REST-API, um die Zellformatierung in einem Excel-Arbeitsblatt zu löschen. Enthält Anforderungsdetails, ein cURL-Beispiel und SDK-Codebeispiele für mehrere Sprachen."
ArticleTitle: "Zellformatierung in einem Excel-Arbeitsblatt löschen – Aspose.Cells Cloud API"
---

**Hinweis:** Alle Aspose.Cells Cloud API-Aufrufe müssen über **HTTPS** erfolgen. HTTP-Endpunkte sind veraltet und können von Browsern blockiert werden.

- **Methode:** POST  
- **Endpunkt:** `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats`

Diese REST-API löscht die Zellformatierung in einer Excel-Datei und ist Teil der Aspose.Cells Cloud-Suite zum Löschen der Zellformatierung in Excel-Arbeitsblättern.

## PostClearFormats API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearformats
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Antwort-Schema**

| Feld   | Typ     | Beschreibung                                      |
|--------|---------|---------------------------------------------------|
| Code   | integer | vom API zurückgegebener HTTP-Statuscode (z. B. 200). |
| Status | string  | Ergebnis des Vorgangs (`OK` bei Erfolg).          |

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                               |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                       |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.     |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                 |

## Verwendung der PostClearFormats API mit SDKs

### PostClearFormats API-Spezifikation

Die <a href="https://apireference.aspose.cloud/cells/#/Cells/PostClearFormats" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht direkte REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/clearformats?range=a1%3Aa10&startRow=1&startColumn=1&endRow=10&endColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearFormats.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearFormats.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearFormats.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearFormats.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearFormats.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearFormats.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearFormats.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Siehe auch**

- [Inhalte und Formatierungen von Zellen löschen](https://docs.aspose.cloud/cells/clear-contents-and-styles)  
- [Zellformatierung festlegen](https://docs.aspose.cloud/cells/set-cell-style)
---