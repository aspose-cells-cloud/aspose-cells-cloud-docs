---
title: "Hochformatige Seitenumbrüche abrufen"
second_title: "Dokument"
linktitle: "Hochformatige Seitenumbrüche abrufen"
type: docs
url: /de/page-breaks/get-vertical-page-breaks/
aliases: [  /de/get-vertical-page-breaks-inside-worksheet/ ]
keywords: "Aspose.Cells, vertikale Seitenumbrüche, Excel-API, Cloud-Tabellenkalkulation, REST-API"
description: "Abrufen vertikaler Seitenumbrüche aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API (v3.0). Enthält HTTPS-Endpunkt, erforderliche Parameter, cURL-Beispiel, Antwortdetails, Fehlerbehandlung und SDK-Beispiele."
weight: 20
---

Diese REST-API ruft **vertikale** Seitenumbrüche aus einer Arbeitsmappe ab.

## Rest-API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung                                                | Erforderlich |
| --------------- | ------ | ------ | ----------------------------------------------------------- | ------------ |
| `name`          | string | path   | Der Name der Excel-Datei.                                   | Ja           |
| `sheetName`     | string | path   | Der Name des Arbeitsblatts, aus dem die Seitenumbrüche gelesen werden sollen. | Ja           |
| `folder`        | string | query  | Der Ordner im Speicher, der die Datei enthält.             | Nein         |
| `storageName`   | string | query  | Der Name des Aspose Cloud-Speichers, der verwendet werden soll. | Nein         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können **cURL** verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
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

### Antwortdetails

| Feld                    | Typ    | Beschreibung                                                                                      |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------- |
| `VerticalPageBreakList` | array  | Eine Sammlung von vertikalen Seitenumbruchobjekten.                                              |
| `Column`                | int    | Der Spaltenindex (nullbasiert), an dem der Seitenumbruch erfolgt.                               |
| `StartRow`              | int    | Die erste Zeile des Umbruchbereichs (nullbasiert).                                              |
| `EndRow`                | int    | Die letzte Zeile des Umbruchbereichs (nullbasiert, typischerweise `1048575` für die letzte Zeile). |
| `link.Href`             | string | Selbstreferenzierende URL für die Ressource (HTTPS).                                             |
| `Code`                  | int    | Vom Dienst zurückgegebener HTTP-Statuscode.                                                      |
| `Status`                | string | Textuelle Beschreibung des HTTP-Status.                                                          |

### Fehlerbehandlung

| HTTP-Code | Bedeutung             | Typische Ursache                                 |
| --------- | --------------------- | ------------------------------------------------ |
| 401       | Unauthorized          | Fehlendes oder ungültiges JWT-Token.            |
| 404       | Not Found             | Die angegebene Datei oder das angegebene Arbeitsblatt existiert nicht. |
| 400       | Bad Request           | Ungültige oder fehlerhafte Abfrageparameter.     |
| 500       | Internal Server Error | Unerwarteter Serverzustand.                      |

Überprüfen Sie die Felder `Code` und `Status` in der JSON-Antwort für weitere Details.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit, mit Aspose.Cells Cloud zu entwickeln. Ein SDK abstractiert die niedrigstufigen Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}