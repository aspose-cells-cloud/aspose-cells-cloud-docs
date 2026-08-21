---
title: "Spalten in einem Excel-Arbeitsblatt ausblenden"
second_title: "Dokument"
linktitle: "Ausblenden"
type: docs
url: /de/columns/hide/
aliases:
  - /de/hide-columns-in-excel-worksheet/
  - /de/hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, API zum Ausblenden von Spalten, Excel-Spalte ausblenden, REST-API zum Ausblenden von Spalten, Aspose.Cells SDK, Automatisierung von Tabellenkalkulationen"
description: "Erfahren Sie, wie Sie eine oder mehrere Spalten in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API (v3.0) ausblenden. Enthält Endpunkt, Parameter, cURL-Beispiel, SDK-Codebeispiele und Fehlerbehandlung."
weight: 40
---

Diese REST-API blendet Spalten in einem Arbeitsblatt aus.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### Anforderungsparameter

| Parametername   | Typ     | Ort    | Beschreibung                                                                 |
| --------------- | ------- | ------ | ---------------------------------------------------------------------------- |
| name            | string  | path   | Der Name der Arbeitsmappen-Datei.                                            |
| sheetName       | string  | path   | Der Name des Arbeitsblatts, in dem die Spalten ausgeblendet werden sollen.   |
| startColumn     | integer | query  | Nullbasierter Index der ersten auszublendenden Spalte.                      |
| totalColumns    | integer | query  | Anzahl der aufeinanderfolgenden Spalten, die ab **startColumn** ausgeblendet werden sollen. |
| folder          | string  | query  | Pfad zum Ordner, der die Arbeitsmappe enthält.                               |
| storageName     | string  | query  | Name des Speicherdiensts, in dem sich die Datei befindet.                    |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das Kommandozeilen-Tool **cURL** verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie eine Spalte mit cURL ausgeblendet wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Mögliche Antwortcodes**

| HTTP-Code | Bedeutung                                     | Beispiel-JSON (Fehler)                                 |
| --------- | --------------------------------------------- | ------------------------------------------------------ |
| 200       | Erfolg                                        | `{ "Code": 200, "Status": "OK" }`                      |
| 400       | Ungültige Anforderung (z. B. ungültige Parameter) | `{ "Code": 400, "Message": "Ungültiger Spaltenbereich." }` |
| 401       | Nicht autorisiert (fehlender/ungültiger Token) | `{ "Code": 401, "Message": "Ungültiger Zugriffstoken." }` |
| 404       | Nicht gefunden (Arbeitsmappe oder Arbeitsblatt) | `{ "Code": 404, "Message": "Datei nicht gefunden." }` |
| 500       | Interner Serverfehler                         | `{ "Code": 500, "Message": "Unerwarteter Fehler." }`   |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK abstractiert Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}