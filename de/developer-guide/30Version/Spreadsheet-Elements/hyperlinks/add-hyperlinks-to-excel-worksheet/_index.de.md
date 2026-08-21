---
title: "Fügen Sie einen Hyperlink zu einem Arbeitsblatt hinzu"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, Hyperlink hinzufügen, Excel REST API, Cloud SDK"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud v3.0 REST API einen Hyperlink zu einem Excel-Arbeitsblatt hinzufügen. Enthält Endpunkt, vollständige Parameteranleitung, cURL-Beispiel und SDK-Snippets für C#, Java, Python und mehr."
weight: 20
---

Diese REST API fügt einem Excel-Arbeitsblatt einen Hyperlink hinzu.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Anforderungsparameter

| Parametername   | Typ    | Ort    | Beschreibung                                                                                      |
| --------------- | ------ | ------ | ------------------------------------------------------------------------------------------------- |
| name            | string | path   | Name des Dokuments.                                                                              |
| sheetName       | string | path   | Name des Arbeitsblatts.                                                                          |
| firstRow        | integer | query | Nullbasierter Index der ersten Zeile des Bereichs, auf den der Hyperlink angewendet wird.       |
| firstColumn     | integer | query | Nullbasierter Index der ersten Spalte des Bereichs, auf den der Hyperlink angewendet wird.      |
| totalRows       | integer | query | Anzahl der Zeilen, die der Hyperlinkbereich umfasst.                                             |
| totalColumns    | integer | query | Anzahl der Spalten, die der Hyperlinkbereich umfasst.                                            |
| address         | string  | query | Die Ziel-URL, auf die der Hyperlink verweist (URL-kodiert).                                      |
| folder          | string  | query | Der Dokumentordner.                                                                              |
| storageName     | string  | query | Name des Speichers.                                                                               |

Die Anforderung kann auch einen JSON-Body enthalten, der dieselben Felder (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`) enthält. Die Übergabe eines Bodies ist nützlich, wenn Sie einen Payload gegenüber Abfragezeichenkettenparametern bevorzugen.

### Fehlerantworten

| HTTP-Code | Grund                                                | Beispiel-Body                                                      |
| --------- | ---------------------------------------------------- | ------------------------------------------------------------------ |
| **400**   | Bad Request – fehlende oder ungültige Parameter.    | `{ "Code":"400", "Message":"Ungültiger Parameterwert." }`         |
| **401**   | Unauthorized – fehlender oder ungültiger JWT-Token. | `{ "Code":"401", "Message":"Zugriffstoken fehlt oder ist ungültig." }` |
| **404**   | Not Found – Arbeitsmappe oder Arbeitsblatt nicht vorhanden. | `{ "Code":"404", "Message":"Datei nicht gefunden." }`         |
| **500**   | Internal Server Error – unerwarteter Serverfehler.  | `{ "Code":"500", "Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Falls die Anforderung fehlschlägt, gibt die API standardmäßige HTTP-Fehlercodes (z. B. 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error) zusammen mit einer JSON-Payload zurück, die eine Fehlermeldung und einen Code enthält.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}