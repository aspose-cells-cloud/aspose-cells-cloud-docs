---
title: "Datensammlung für die Erstellung eines Excel-Berichts"
second_title: "Dokument"
linktitle: "Datensammlung"
type: docs
url: /de/assembly-data-for-the-creation-of-an-excel-report/
aliases: [  /de/assembly/ ]
keywords: "Aspose.Cells, Excel-Bericht, Datensammlung, Cloud API, REST, SDK, cURL, PDF, ODS"
description: "Erfahren Sie, wie Sie die Assembly-API von Aspose.Cells Cloud verwenden können, um Daten in Excel-Berichte (XLSX, PDF, ODS) einzufügen. Enthält Endpunkt, Parameter, cURL-Beispiel, SDK-Code, Authentifizierungsanleitung und Fehlerbehandlung."
weight: 40
---

Diese REST-API fügt Daten **in** eine Excel-Datei ein.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter


| Parametername | Typ   | Speicherort                  | Beschreibung                                                            |
| -------------- | ------ | ------------------------- | ---------------------------------------------------------------------- |
| file           | Datei  | formData (multipart body) | Die hochzuladende Tabellendatei.                                        |
| DataSource     | Zeichenkette | Abfragezeichenfolge              | Bezeichner der Datenquelle, die die Daten für die Zusammenführung bereitstellt. |
| format         | Zeichenkette | Abfragezeichenfolge              | Gewünschtes Ausgabeformat (z. B. `xlsx`, `pdf`).                           |

### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[Dateiname2]",
    "Filesize" : [Dateigröße],
    "FileContent" : "[Base64-Zeichenkette]"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                     | Beschreibung                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Ungültige Anforderung       | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert           | Ungültiges oder fehlendes JWT-Token. |
| 413  | Anforderungstext zu groß    | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Interner Serverfehler       | Unerwarteter Serverfehler. |

## Verwendung der PostAssemble-API mit SDKs

### PostAssemble-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Base64-Zeichenkette--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Base64-Zeichenkette--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDK ist die schnellste Methode zur Entwicklung gegen die API. Ein SDK abstrahiert Details auf niedriger Ebene, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}