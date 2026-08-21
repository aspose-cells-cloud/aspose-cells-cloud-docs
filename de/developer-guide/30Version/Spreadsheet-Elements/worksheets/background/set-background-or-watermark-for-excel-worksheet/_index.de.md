---
title: "Hintergrund in einem Excel-Arbeitsblatt festlegen"
ArticleTitle: "Hintergrund in einem Excel-Arbeitsblatt festlegen – Aspose.Cells Cloud API-Anleitung"
second_title: "Dokument"
linktype: "docs"
url: /worksheets/background/add/
aliases: [/set-background-or-watermark-for-excel-worksheet/]
keywords: "Aspose.Cells, Excel, Arbeitsblatt, Hintergrund, REST API, SDK, Bild hinzufügen"
description: "Erfahren Sie, wie Sie ein Hintergrundbild (PNG, JPEG, BMP) mit der Aspose.Cells Cloud REST API zu einem Excel-Arbeitsblatt hinzufügen. Enthält Endpunkt, erforderliche Parameter, Authentifizierungsschritte, cURL-Beispiel und SDK-Codebeispiele."
weight: 180
---

Diese REST API fügt einem Arbeitsblatt ein Hintergrundbild hinzu.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Anforderungsparameter**

| Parametername   | Typ    | Ort    | Beschreibung                                                     |
| --------------- | ------ | ------ | ---------------------------------------------------------------- |
| name            | string | path   | Name der Excel-Arbeitsmappe.                                     |
| sheetName       | string | path   | Name des Arbeitsblatts, dem das Bild hinzugefügt werden soll.   |
| imageFile       | file   | body   | Binäre Bilddatei (PNG, JPEG, BMP usw.) als Hintergrund.          |
| folder          | string | query  | Ordner im Speicher, in dem sich die Arbeitsmappe befindet.      |
| storageName     | string | query  | Name des Aspose Cloud-Speichers.                                 |

**Unterstützte Formate & Grenzwerte**

- Akzeptierte Bildendungen: **PNG, JPEG, BMP, GIF**.
- Maximale Dateigröße: **5 MB**.
- Das Bild wird kachelförmig wiederholt, um den gesamten Hintergrund des Arbeitsblatts zu füllen.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetBackground) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-basierte Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud API mittels cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/background" \
  -X PUT \
  -F "imageFile=@Creative.jpg" \
  -H "Content-Type: multipart/form-data" \
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

*Mögliche Fehlerantworten*

| HTTP-Code | Beschreibung                                               |
| --------- | ---------------------------------------------------------- |
| 400       | Ungültige Anforderung – fehlende oder ungültige Parameter. |
| 401       | Nicht autorisiert – ungültiges oder abgelaufenes JWT-Token.|
| 404       | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht. |
| 500       | Interner Serverfehler – unerwarteter Zustand auf dem Server. |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektziele konzentrieren. Weitere Informationen zu den verfügbaren Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}