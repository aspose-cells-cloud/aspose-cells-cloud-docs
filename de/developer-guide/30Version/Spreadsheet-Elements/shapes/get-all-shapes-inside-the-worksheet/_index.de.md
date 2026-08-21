---
title: "Alle Formen auf einem Excel-Arbeitsblatt abrufen"
second_title: "Dokument"
linktitle: "Alle-abrufen"
type: docs
url: /de/shapes/get-all/
aliases: [  /de/get-all-shapes-inside-the-worksheet/ ]
keywords: "Aspose.Cells, Cloud-API, Excel-Formen, Formen abrufen, REST, SDK"
description: "Rufen Sie alle Formen (Diagramme, Bilder, Textfelder) von einem Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API ab. Enthält ein cURL-Beispiel, SDK-Snippets, Authentifizierungsschritte und Fehlerbehandlung."
ArticleTitle: "Alle Formen auf einem Excel-Arbeitsblatt abrufen"
weight: 10
---

Diese REST API ermöglicht das Abrufen aller Formen auf einem Excel-Arbeitsblatt.

## Sicherheit und Authentifizierung  
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### Anforderungsparameter

| Parametername   | Typ    | Ort      | Beschreibung                                                                                             |
| --------------- | ------ | -------- | -------------------------------------------------------------------------------------------------------- |
| **name**        | string | path     | Der Name der Excel-Datei.                                                                                |
| **sheetName**   | string | path     | Der Name des Arbeitsblatts.                                                                              |
| **folder**      | string | query    | Der Ordner, der das Dokument enthält.                                                                    |
| **storageName** | string | query    | Der Name des zu verwendenden Speicherdienstes.                                                           |
| **include**     | string | query    | Auf `details` setzen, um vollständige Formeigenschaften zurückzugeben; andernfalls werden nur die `link`-Objekte zurückgegeben. |

> **Optional**: `folder`, `storageName` und `include` können weggelassen werden, wenn sich die Datei im Stammspeicher befindet.

Sie können das cURL-Befehlszeilentool verwenden, um auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt eine Anforderung mit optionalen Abfrageparametern.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Antwortfelder

Das Objekt `Shapes` enthält eine Liste von `Shape`-Elementen. Jede Form umfasst die folgenden Eigenschaften (sofern der Parameter `include=details` verwendet wird; andernfalls wird nur das `link`-Objekt zurückgegeben).

| Eigenschaft | Typ    | Beschreibung                                                               |
| ----------- | ------ | -------------------------------------------------------------------------- |
| **Name**    | string | Der der Form zugewiesene Name (z. B. „Diagramm 1“).                       |
| **Type**    | string | Der Formtyp (z. B. `Chart`, `Picture`, `TextBox`).                        |
| **Top**     | number | Der Abstand in Punkten vom oberen Rand des Arbeitsblatts bis zur Form.    |
| **Left**    | number | Der Abstand in Punkten vom linken Rand des Arbeitsblatts bis zur Form.    |
| **Width**   | number | Die Breite der Form in Punkten.                                            |
| **Height**  | number | Die Höhe der Form in Punkten.                                              |
| **Link**    | object | Hyperlink-Informationen (`Href`, `Rel`, `Type`, `Title`).                 |

## Fehlerbehandlung

| HTTP-Status | Beschreibung                                           | Beispiel-Fehlerbody                                                  |
| ----------- | ------------------------------------------------------ | -------------------------------------------------------------------- |
| **400**     | Ungültige Anforderung – fehlerhafte Parameter.         | `{ "Code": 400, "Message": "Ungültiger Parameterwert." }`           |
| **401**     | Nicht autorisiert – fehlender oder ungültiger Token.  | `{ "Code": 401, "Message": "Zugriffstoken fehlt oder ist ungültig." }` |
| **404**     | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code": 404, "Message": "Datei oder Arbeitsblatt nicht gefunden." }` |
| **500**     | Interner Serverfehler – unerwarteter Zustand.          | `{ "Code": 500, "Message": "Ein unerwarteter Fehler ist aufgetreten." }` |

Eine erfolgreiche Anforderung gibt **HTTP 200** mit einem `Shapes`-Objekt zurück, das die Liste der Formen enthält (siehe Beispielantwort oben).

Die API erzwingt ein Limit von **150 Anforderungen pro Minute pro JWT-Token**. Überschreiten Sie dieses Limit, wird **HTTP 429** mit einem `Retry-After`-Header zurückgegeben, der angibt, wann erneut versucht werden soll.

## Cloud SDK Family

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektanforderungen zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}