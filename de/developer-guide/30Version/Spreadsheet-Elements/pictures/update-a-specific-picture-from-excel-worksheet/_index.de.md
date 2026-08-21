---
title: "Bild in einer Excel-Datei aktualisieren"
second_title: "Dokument"
linktitle: "Aktualisieren"
type: docs
url: /de/pictures/update/
aliases: [  /de/update-a-specific-picture-from-excel-workshee/ ]
keywords: "Aspose.Cells Cloud, Excel, Bild aktualisieren, REST API, SDK"
description: "Erfahren Sie, wie Sie ein Bild in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API aktualisieren können. Enthält Anforderungsdetails, ein cURL-Beispiel und SDK-Snippets für mehrere Sprachen."
ArticleTitle: "Bild in einer Excel-Datei mithilfe der Aspose.Cells Cloud REST API aktualisieren"
weight: 70
---

Diese REST API aktualisiert ein Bild, identifiziert anhand seines Indexes, in einem Excel-Arbeitsblatt.

**Voraussetzungen:** Sie benötigen ein gültiges Aspose Cloud JWT-Token, die Ziel-Excel-Datei muss in Ihrem Aspose Cloud-Speicher abgelegt sein, und Sie müssen API-Version 3.0 oder höher verwenden.

## PostWorksheetPicture API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ    | Ort    | Beschreibung                                                  |
| --------------- | ------ | ------ | ------------------------------------------------------------ |
| name            | string | path   | Der Name der Excel-Datei.                                     |
| sheetName       | string | path   | Der Name des Arbeitsblatts, das das Bild enthält.            |
| pictureIndex    | integer| path   | Nullbasierter Index des zu aktualisierenden Bildes.          |
| picture         | object | body   | JSON-Objekt, das die zu aktualisierenden Bildeigenschaften beschreibt. |
| folder          | string | query  | Der Ordner, in dem das Dokument gespeichert ist.             |
| storageName     | string | query  | Der Name des Speicherdienstes.                                |

**Hinweis:** Der Bildindex ist nullbasiert. Unterstützte Bildformate sind JPEG, PNG, BMP und GIF. Die maximale Bildgröße beträgt 10 MB.

### Fehlerantworten

| HTTP-Code | Beschreibung                                                      |
| --------- | ----------------------------------------------------------------- |
| 401       | Nicht autorisiert – fehlendes oder ungültiges Token.             |
| 404       | Nicht gefunden – die angegebene Datei, das angegebene Arbeitsblatt oder der angegebene Bildindex existiert nicht. |
| 400       | Ungültige Anforderung – falsche Syntax oder ungültige Parameter. |
| 500       | Interner Serverfehler – unerwarteter Zustand aufgetreten.        |

Die <a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
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

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*Siehe auch:* Bild hinzufügen, Bild löschen, Bild abrufen, Bilder löschen – andere bildbezogene Vorgänge in der Aspose.Cells Cloud API.