---
title: "Zoom für ein Excel-Arbeitsblatt festlegen – Aspose.Cells Cloud API v3.0"
second_title: "Dokument"
linktitle: "Zoom"
type: docs
url: /worksheets/zoom/
aliases: [/set-zoom-in-excel-worksheet/]
keywords: "Aspose.Cells, Excel-Zoom, Arbeitsblatt-Zoom, REST-API, Cloud-SDK, Excel-Automatisierung"
description: "Erfahren Sie, wie Sie den Zoom eines Arbeitsblatts (10–400 %) mit der Aspose.Cells Cloud API v3.0 festlegen. Enthält cURL- und SDK-Beispiele sowie Fehlerbehandlung."
weight: 20
ArticleTitle: "Zoom für ein Excel-Arbeitsblatt festlegen – Aspose.Cells Cloud API v3.0"
---

Diese REST-API legt den Zoom-Wert eines Excel-Arbeitsblatts fest. **Authentifizierung** ist erforderlich; fügen Sie in den `Authorization`-Header jeder Anforderung ein gültiges Bearer-JWT-Token ein.

## Sicherheit und Authentifizierung  
Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
```

### **Anforderungsparameter**

| Parameter   | Typ     | Ort     | Beschreibung                                                         |
| ----------- | ------- | ------- | -------------------------------------------------------------------- |
| name        | string  | path    | Name der Excel-Datei (Arbeitsmappe).                                |
| sheetName   | string  | path    | Name des zu ändernden Arbeitsblatts.                                 |
| value       | integer | query   | Zoom-Prozentsatz (zulässiger Bereich **10–400**, z. B. `40` für 40 %). |
| folder      | string  | query   | Pfad des Ordners, in dem die Datei gespeichert ist.                 |
| storageName | string  | query   | Name des Speicherdienstes.                                           |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webservices einfach aufzurufen. Im folgenden Beispiel wird gezeigt, wie mit cURL ein Aufruf an die Cloud-API erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Informationen zur Fehlerantwort**  
Mögliche HTTP-Statuscodes sind:

- `400 Bad Request` – fehlende oder ungültige Parameter.
- `401 Unauthorized` – fehlendes oder ungültiges JWT-Token.
- `404 Not Found` – die angegebene Datei oder das angegebene Arbeitsblatt ist nicht vorhanden.
- `500 Internal Server Error` – unerwarteter serverseitiger Fehler.

Jede Fehlerantwort enthält einen JSON-Body mit einem `Code` und einer aussagekräftigen `Message`.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf die Aufgaben Ihres Projekts zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}