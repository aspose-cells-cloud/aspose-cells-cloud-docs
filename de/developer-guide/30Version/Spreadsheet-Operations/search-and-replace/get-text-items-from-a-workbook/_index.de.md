---
title: "Textelemente aus einer Excel-Arbeitsmappe abrufen"
ArticleTitle: "Textelemente aus einer Excel-Arbeitsmappe mit der Aspose.Cells Cloud API abrufen"
second_title: "Dokument"
linktitle: "Textelemente in der Arbeitsmappe abrufen"
type: docs
url: /de/workbook/get-text-items/
aliases: [  /de/get-text-items-from-a-workbook/ ]
weight: 10
keywords: "Excel, Aspose.Cells Cloud, REST API, Tabellenkalkulation, Textelemente abrufen, Arbeitsmappe"
description: "Rufen Sie Textelemente aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API ab. Verfügbar über SDKs für C#, Java, Python, PHP, Ruby, Go, Node.js, Perl und Swift."
---

## REST API

Diese REST API liest die **Textelemente** einer Arbeitsmappe in einer Excel-Datei.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/textItems
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung                                          |
| --------------- | ------ | ------ | ----------------------------------------------------- |
| name            | string | path   | Der Name der Arbeitsmappen-Datei.                    |
| folder          | string | query  | Der Ordnerpfad im Speicher, in dem sich die Arbeitsmappe befindet. |
| storageName     | string | query  | Der Name des Speicherdienstes.                        |

### **Antwort**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                             |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                    |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                               |

## So verwenden Sie die GetWorkbookTextItems API mit SDKs

### API-Spezifikation für GetWorkbookTextItems

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookTextItems) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/textItems" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

Typische HTTP-Antwortcodes:

| Code | Beschreibung                                         |
|------|------------------------------------------------------|
| 200  | Anforderung erfolgreich; Textelemente werden zurückgegeben. |
| 401  | Unauthorized – fehlender oder ungültiger Token.     |
| 403  | Forbidden – unzureichende Berechtigungen.           |
| 404  | Not Found – Arbeitsmappe oder Ressource nicht gefunden. |
| 500  | Internal Server Error – unerwarteter Fehler.        |

### Verwenden der Aspose.Cells Cloud SDKs

Dieses Beispiel verwendet API-Version **v3.0**; lesen Sie das Changelog für neuere Versionen. Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}
---