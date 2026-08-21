---
title: "Textelemente aus einer Excel-Arbeitsmappe abrufen"
second_title: "Dokument"
linktitle: "Textelemente in Arbeitsmappe abrufen"
type: docs
url: /de/worksheets/get-text-items/
aliases: [  /de/get-text-items-from-a-worksheet/ ]
weight: 20
keywords: "Aspose.Cells, Cloud API, Excel, Arbeitsmappe, Textelemente, REST"
description: "Rufen Sie alle Textelemente aus einer bestimmten Arbeitsmappe in einer Excel-Datei mithilfe der Aspose.Cells Cloud REST API ab. Enthält Beispiel-cURL-, SDK-Code, Authentifizierungsschritte und Antwort-Schema."
ArticleTitle: "Textelemente aus einer Excel-Arbeitsmappe abrufen"
---

## REST API

Diese REST API liest die Textelemente einer Arbeitsmappe in einer Excel-Datei.

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Anforderungsparameter


| Parametername   | Typ    | Ort    | Erforderlich | Beschreibung                                   |
| ---------------- | ------ | ------ | ------------ | ---------------------------------------------- |
| name             | string | path   | Ja           | Dateiname der Arbeitsmappe.                    |
| sheetName        | string | path   | Ja           | Name der Arbeitsmappe.                         |
| folder           | string | query  | Nein         | Pfad zum Ordner, der die Arbeitsmappe enthält. |
| storageName      | string | query  | Nein         | Name des Aspose Cloud-Speichers.               |

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

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Detailinformationen zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

## So verwenden Sie die GetWorksheetTextItems-API mit SDKs

### GetWorksheetTextItems-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"} definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
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

### Verwenden Sie Aspose.Cells Cloud SDKs

SDKs vereinfachen die Integration, indem sie niedrigstufige Details übernehmen und Ihnen ermöglichen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte schauen Sie sich das [GitHub-Repository](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}