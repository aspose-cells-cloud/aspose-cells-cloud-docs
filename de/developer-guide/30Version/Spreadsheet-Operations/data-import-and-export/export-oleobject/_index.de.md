---
title: "OLE-Objekt exportieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "OLE-Objekt"
type: docs
url: /de/export-excel-ole-object/
aliases: [  /de/export/excel-ole-object/ ]
keywords: "Aspose.Cells, OLE-Objekt, Export, Excel, Cloud-API, PDF, PNG, DOCX, PPTX"
description: "Exportieren Sie OLE-Objekte aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud API. Erfahren Sie mehr über das Anforderungsformat, die Parameter, ein Beispiel mit cURL und die Fehlerbehandlung."
weight: 20
ArticleTitle: "OLE-Objekt exportieren – Aspose.Cells Cloud API"
---

## **REST-API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Anforderungsparameter

| Parameter       | Ort        | Typ  | Erforderlich | Beschreibung                                                                 |
| --------------- | ---------- | ---- | ------------ | ---------------------------------------------------------------------------- |
| `file`          | Form‑data  | Datei | Ja           | Die Excel-Arbeitsmappe (`.xlsx`, `.xls`, usw.), die die OLE-Objekte enthält. |
| `outputFormat`  | Query      | String | Ja         | Zielformat für die exportierten Objekte (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`    | Query      | String | Ja         | Fester Wert `oleobject`.                                                     |


### Antwort

Eine erfolgreiche Anfrage gibt ein JSON-Objekt zurück, das die exportierten Dateien auflistet:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                   |
|------|-----------------------------|--------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.           |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).       |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                           |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größeinschränkung.                   |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                     |

## Verwendung der PostExport API mit SDKs

### PostExport API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud API mit cURL erfolgt.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### Was ist ein OLE-Objekt?

Ein **OLE-Objekt (Object Linking and Embedding)** integriert externen Inhalt – wie Word-Dokumente, PowerPoint-Folien, Bilder oder andere Dateien – direkt in eine Excel-Arbeitsmappe. Beim Export wird der eingebettete Inhalt extrahiert und im angeforderten Ausgabeformat gespeichert.

### Endpunktübersicht

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – Muss auf `oleobject` gesetzt werden.
- `format` – Gewünschtes Ausgabeformat (z. B. `pdf`, `png`, `jpeg`, `docx`, `pptx`).

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details der unteren Schichten, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---