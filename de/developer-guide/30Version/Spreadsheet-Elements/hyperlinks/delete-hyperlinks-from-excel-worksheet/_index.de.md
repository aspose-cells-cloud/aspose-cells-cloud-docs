---
title: "Hyperlinks löschen"
type: docs
url: /de/hyperlinks/clear/
aliases: [  /de/add-hyperlinks-to-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, Hyperlinks löschen, Hyperlinks entfernen, REST API, Arbeitsblatt, SDK"
description: "Erfahren Sie, wie Sie alle Hyperlinks in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API oder eines beliebigen unterstützten SDKs (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl usw.) entfernen."
weight: 40
ArticleTitle: "Hyperlinks löschen – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST API löscht **alle Hyperlinks** in einem Excel-Arbeitsblatt.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Anforderungsparameter

| Parametername | Typ    | Ort     | Beschreibung                               |
| ------------- | ------ | ------- | ------------------------------------------ |
| name          | string | path    | Der Name der Excel-Datei.                  |
| sheetName     | string | path    | Der Name des Arbeitsblatts.                |
| folder        | string | query   | Der Ordner, der das Dokument enthält.     |
| storageName   | string | query   | Der Name des Speicherdienstes.             |

### Fehlerantworten

| HTTP-Code | Grund                                              | Beispiel-Body                                                       |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400**   | Bad Request – fehlende oder ungültige Parameter.  | `{ "Code":"400", "Message":"Ungültiger Parameterwert." }`          |
| **401**   | Unauthorized – fehlender oder ungültiger JWT-Token. | `{ "Code":"401", "Message":"Zugriffstoken fehlt oder ist ungültig." }` |
| **404**   | Not Found – Arbeitsmappe oder Arbeitsblatt existiert nicht. | `{ "Code":"404", "Message":"Datei nicht gefunden." }`              |
| **500**   | Internal Server Error – unerwarteter Serverfehler. | `{ "Code":"500", "Message":"Ein unerwarteter Fehler ist aufgetreten." }` |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) definiert eine öffentlich zugängliche Programmierschnittstelle, über die Sie REST-Interaktionen direkt aus einem Webbrowser durchführen können.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webservices aufzurufen. Das folgende Beispiel zeigt, wie Sie alle Hyperlinks aus einem Arbeitsblatt löschen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
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

## Cloud SDK-Familie

Die Verwendung eines SDK beschleunigt die Entwicklung, da sie Ihnen die Low-Level-Details abnimmt. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie Arbeitsblatt-Hyperlinks mit verschiedenen SDKs löschen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}