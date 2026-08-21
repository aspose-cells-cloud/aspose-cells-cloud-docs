---
title: "Arbeitsblatt-Hyperlink abrufen"
type: docs
url: /de/hyperlinks/get/
keywords: "Aspose.Cells Cloud, Arbeitsblatt-Hyperlink abrufen, Excel-Hyperlink-API, REST, JWT-Authentifizierung, Excel-Arbeitsblatt, API-Endpunkt"
description: "Rufen Sie einen spezifischen Hyperlink aus einer Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API (v3.0) ab. Enthält Endpunkt, Parameter, cURL-Beispiel, Authentifizierungsdetails, Fehlerbehandlung und SDK-Ausschnitte."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Arbeitsblatt-Hyperlink abrufen"
---

Diese REST-API ruft einen Arbeitsblatt**hyperlink** mithilfe der **Aspose.Cells Get Hyperlink API** ab.

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
Bevor Sie den Endpunkt aufrufen, beschaffen Sie ein JWT-Zugriffstoken mithilfe Ihrer Client-ID und des Geheimnisses und fügen es in den Header `Authorization: Bearer <jwt token>` ein.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### Anforderungsparameter

| Parametername   | Typ     | Ort   | Beschreibung                                           |
| --------------- | ------- | ----- | ------------------------------------------------------ |
| name            | string  | path  | Der Name der Excel-Datei.                              |
| sheetName       | string  | path  | Der Name des Arbeitsblatts, das den Link enthält.     |
| hyperlinkIndex  | integer | path  | Nullbasierten Index des abzurufenden Hyperlinks.      |
| folder          | string  | query | Der Ordner, in dem das Dokument gespeichert ist.      |
| storageName     | string  | query | Der Name des Speicherdienstes.                         |

### Fehlerantworten

| HTTP-Code | Grund                                                | Beispiel-Body                                                         |
| --------- | ---------------------------------------------------- | --------------------------------------------------------------------- |
| **400**   | Bad Request – fehlende oder ungültige Parameter.    | `{ "Code":"400", "Message":"Ungültiger Parameterwert." }`            |
| **401**   | Unauthorized – fehlendes oder ungültiges JWT-Token. | `{ "Code":"401", "Message":"Zugriffstoken fehlt oder ist ungültig." }` |
| **404**   | Not Found – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code":"404", "Message":"Datei nicht gefunden." }`              |
| **500**   | Internal Server Error – unerwarteter Serverfehler.  | `{ "Code":"500", "Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details, sodass Sie sich auf Ihre Projekt-Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}