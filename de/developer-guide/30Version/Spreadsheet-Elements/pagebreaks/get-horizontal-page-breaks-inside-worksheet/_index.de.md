---
title: "Horizontale Umbrüche abrufen"
second_title: "Dokument"
linktitle: "Horizontale Umbrüche abrufen"
type: docs
url: /page-breaks/get-horizontal-page-breaks/
aliases: [/get-horizontal-page-breaks-inside-worksheet/]
keywords: "horizontale Umbrüche, Aspose.Cells Cloud, REST-API, Excel-Arbeitsblatt, SDK"
description: "Rufen Sie horizontale Umbrüche aus einem Excel-Arbeitsblatt über die Aspose.Cells Cloud API ab. Enthält Endpunkt, Parameter, cURL-Beispiel, Antwortformat und SDK-Snippets für C#, Java, Python und mehr."
ArticleTitle: "Horizontale Umbrüche abrufen – Aspose.Cells Cloud API-Dokumentation"
weight: 10
---

**Horizontaler Umbruch** – ein zeilenbasierter Umbruch, der das Arbeitsblatt zwingt, nach der angegebenen Zeile eine neue gedruckte Seite zu beginnen. Diese REST-API ruft diese horizontalen Umbrüche ab.

## Sicherheit und Authentifizierung

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST-API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### Anforderungsparameter

| Parametername   | Typ    | Ort   | Beschreibung                                                       |
| --------------- | ------ | ----- | ------------------------------------------------------------------ |
| name            | string | path  | Der Name der Excel-Datei.                                          |
| sheetName       | string | path  | Der Name des Arbeitsblatts.                                        |
| folder          | string | query | Der Ordnerpfad im Speicher, in dem sich die Datei befindet. _(optional)_ |
| storageName     | string | query | Der Name des Speichers. _(optional)_                               |

Die <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="OpenAPI-Spezifikation für GetHorizontalPageBreaks">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool nutzen, um bequem auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## Fehlerbehandlung

| HTTP-Status | Beschreibung                                                | Beispiel-JSON                                          |
| ----------- | ----------------------------------------------------------- | ------------------------------------------------------ |
| 400         | Ungültige Anforderung – fehlende oder ungültige Parameter. | `{ "Code": 400, "Message": "Invalid parameter." }`     |
| 401         | Nicht autorisiert – JWT-Token fehlt oder ist ungültig.     | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404         | Nicht gefunden – die angegebene Datei oder das angegebene Arbeitsblatt existiert nicht. | `{ "Code": 404, "Message": "Resource not found." }`    |
| 500         | Interner Serverfehler – unerwarteter Zustand auf dem Server. | `{ "Code": 500, "Message": "Server error." }`          |

## Cloud SDK-Familie

Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}