---
title: "Alle Hyperlinks abrufen – Aspose.Cells Cloud REST API"
type: docs
url: /hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells, Alle Hyperlinks abrufen, Excel-API, REST-API, Cloud-SDK, cURL-Beispiel, Hyperlinks in Tabellenkalkulationen"
description: "Rufen Sie alle Hyperlinks aus einem Arbeitsblatt einer Excel-Datei mithilfe der Aspose.Cells Cloud REST API (v3.0) ab. Enthält HTTPS-Endpunkt, erforderliche Parameter, cURL-Beispiel, Antwortschema und SDK-Codebeispiele."
weight: 10
ArticleTitle: "Alle Hyperlinks abrufen – Dokumentation der Aspose.Cells Cloud REST API"
---

Diese REST API ruft **alle Hyperlinks** aus einem bestimmten Arbeitsblatt einer Excel-Arbeitsmappe ab.

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Erforderlich | Standardwert | Beschreibung                                      |
| --------------- | ------ | ------ | ------------ | ------------ | ------------------------------------------------- |
| name            | string | path   | Ja           | –            | Name der Excel-Datei.                            |
| sheetName       | string | path   | Ja           | –            | Name des Arbeitsblatts.                          |
| folder          | string | query  | Nein         | –            | Ordner, der das Dokument enthält.                |
| storageName     | string | query  | Nein         | –            | Name des zu verwendenden Speicherdienstes.       |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Die JSON-Antwort enthält ein `Hyperlinks`-Objekt.

- **Count** – Gesamtanzahl der Hyperlinks im Arbeitsblatt.
- **HyperlinkList** – ein Array, bei dem jedes Element ein `link`-Objekt enthält. Die Eigenschaft `Href` speichert die Hyperlink-Adresse, während `Rel`, `Title` und `Type` zusätzliche Metadaten liefern (häufig `null` bei einfachen Links).

### Fehlerantworten

| HTTP-Code | Grund                                              | Beispiel-Body                                                       |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – fehlende oder ungültige Parameter.  | `{ "Code":"400", "Message":"Ungültiger Parameterwert." }`          |
| **401**   | Unauthorized – fehlender oder ungültiger JWT-Token. | `{ "Code":"401", "Message":"Zugriffstoken fehlt oder ist ungültig." }` |
| **404**   | Not Found – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code":"404", "Message":"Datei nicht gefunden." }`            |
| **500**   | Internal Server Error – unerwarteter Serverfehler. | `{ "Code":"500", "Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

## Cloud SDK Family

Die Verwendung eines SDKs ist die schnellste Möglichkeit, diese Funktionalität zu integrieren. SDKs übernehmen die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}