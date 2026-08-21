---
title: "Hintergrund in einem Excel-Arbeitsblatt entfernen"
second_title: "Dokument"
linktitle: "Entfernen"
type: docs
url: /de/worksheets/background/delete/
aliases: [  /delete-background-or-watermark-of-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Hintergrund eines Arbeitsblatts entfernen, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um das Hintergrundbild eines Excel-Arbeitsblatts zu entfernen. SDKs sind für C#, Java, PHP, Ruby, Node.js, Python, Perl und Go verfügbar."
weight: 210
ArticleTitle: "Hintergrund in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API entfernen"
---

Diese REST API entfernt das Hintergrundbild eines Arbeitsblatts.

**Voraussetzungen:** Sie müssen die Arbeitsmappe im Aspose Cloud-Speicher abgelegt haben und über ein gültiges JWT-Access-Token zur Authentifizierung verfügen.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Anforderungsparameter**

| Parametername   | Typ    | Ort    | Beschreibung                                               |
| --------------- | ------ | ------ | ---------------------------------------------------------- |
| name            | string | path   | Der Name der Excel-Datei.                                  |
| sheetName       | string | path   | Der Name des Arbeitsblatts, dessen Hintergrund entfernt wird. |
| folder          | string | query  | Der Ordner im Speicher, in dem sich die Datei befindet.   |
| storageName     | string | query  | Der Name des Speichers (sofern nicht der Standardspeicher). |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach zu nutzen. Alle Anforderungen erfordern ein gültiges JWT-Token. Holen Sie sich das Token über den OAuth2-Token-Endpunkt, wie in der Authentifizierungsanleitung beschrieben.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                   |
|------|-----------------------------|----------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                          |
| 413  | Payload Too Large           | Hochgeladene Datei überschreitet die Größeinschränkung.       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                     |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Sehen Sie sich das [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs an.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}