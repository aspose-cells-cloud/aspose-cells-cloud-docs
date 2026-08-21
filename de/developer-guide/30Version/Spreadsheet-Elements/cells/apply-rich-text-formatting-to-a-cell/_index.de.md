---
title: "Rich-Text-Formatierung für eine Zelle anwenden"
type: docs
url: /de/apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, Rich-Text, Zellformatierung, REST-API, Aspose.Cells Cloud"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST-API eine Rich-Text-Formatierung für eine bestimmte Excel-Zelle anwenden. Enthält die Anforderungssyntax, Parameterdetails, ein cURL-Beispiel und SDK-Snippets."
ArticleTitle: "Rich-Text-Formatierung für eine Zelle mithilfe der Aspose.Cells Cloud API anwenden"
---

Diese REST-API wendet eine **Rich-Text-Formatierung** auf eine Zelle in einer Excel-Datei an.

**Voraussetzungen:** Sie müssen über ein gültiges JWT-Token verfügen, und die Ziel-Excel-Datei muss bereits im angegebenen Speicherordner vorhanden sein, bevor Sie diesen Vorgang aufrufen.

**Hintergrund:** Mit der Rich-Text-Formatierung können Sie innerhalb einer einzelnen Zelle mehrere Schriftartstile anwenden, wodurch eine ausdrucksstärkere Datendarstellung in Excel-Arbeitsblättern möglich ist.

## PostCellCharacters-API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Speicherort | Beschreibung                                                                 |
|-----------------|--------|-------------|-----------------------------------------------------------------------------|
| name            | string | path        | Der Name der Excel-Datei (z. B. `Book1.xlsx`).                             |
| sheetName       | string | path        | Das Arbeitsblatt, das die Zielzelle enthält.                               |
| cellName        | string | path        | Die Adresse der zu formatierenden Zelle (z. B. `A1`).                      |
| options         | object | body        | JSON-Objekt, das die Rich-Text-Formatierungseinstellungen für die Zelle definiert. |
| folder          | string | query       | Der Ordner im Speicher, in dem sich die Excel-Datei befindet.             |
| storageName     | string | query       | Der Name des Speicherdienstes (sofern ein benutzerdefinierter Speicher verwendet wird). |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                       |
|------|-----------------------------|-------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.            |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                        |

## Verwendung der PostCellCharacters-API mit SDKs

### PostCellCharacters-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices problemlos aufzurufen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
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

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene und ermöglicht es Ihnen, sich auf Ihre ProjektAufgaben zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*C# SDK-Beispiel*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*Java SDK-Beispiel*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*PHP SDK-Beispiel*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*Ruby SDK-Beispiel*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*Node.js SDK-Beispiel*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*Python SDK-Beispiel*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*Perl SDK-Beispiel*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*Go SDK-Beispiel*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}
---