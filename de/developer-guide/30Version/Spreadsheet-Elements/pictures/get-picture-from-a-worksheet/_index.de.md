---
title: "Alle Bilder in einem Excel-Arbeitsblatt abrufen"
second_title: "Dokument"
linktitle: "Alle abrufen"
type: docs
url: /de/pictures/get-all/
aliases: [  /de/get-picture-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel-Arbeitsblatt, Bilder-API, alle Bilder abrufen, REST-API, SDK"
description: "Rufen Sie alle Bildobjekte über die Aspose.Cells Cloud REST-API aus einem Excel-Arbeitsblatt ab."
ArticleTitle: "Alle Bilder in einem Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API"
weight: 10
---

Diese REST-API ruft alle Bildinformationen aus einem Excel-Arbeitsblatt ab.

**Voraussetzungen**  
Bevor Sie diesen Endpunkt aufrufen, stellen Sie sicher, dass Folgendes vorliegt:

- Ein gültiges Aspose Cloud JWT-Access-Token.  
- Die Ziel-Excel-Datei ist im ausgewählten Speicher hochgeladen.  
- Der korrekte Speichername (sofern ein benutzerdefinierter Speicher verwendet wird).  
- Der Name des Arbeitsblatts, das die Bilder enthält.

## GetWorksheetPictures API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

**Hinweis:** Nutzen Sie HTTPS (TLS 1.2 oder höher) beim Aufruf der API und fügen Sie ein gültiges JWT-Token in den `Authorization`-Header ein.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anfrageparameter**

| Parametername | Typ   | Ort    | Beschreibung                                   |
| ------------- | ----- | ------ | ---------------------------------------------- |
| name          | string | path   | Der Name der Excel-Datei.                      |
| sheetName     | string | path   | Der Name des Arbeitsblatts, das Bilder enthält. |
| folder        | string | query  | Der Pfad des Ordners, in dem die Datei gespeichert ist. |
| storageName   | string | query  | Der Name des Speicherdienstes.                 |

### Fehlerantworten

| HTTP-Code | Beschreibung                                                                 |
| --------- | ---------------------------------------------------------------------------- |
| 401       | Nicht autorisiert – fehlendes oder ungültiges Token.                         |
| 404       | Nicht gefunden – die angegebene Datei, das Arbeitsblatt oder der Seitenumbruchindex existiert nicht. |
| 400       | Ungültige Anfrage – falsche Anfragesyntax oder ungültige Parameter.          |
| 500       | Interner Serverfehler – eine unerwartete Bedingung ist aufgetreten.         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPictures) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Pictures": {
    "PictureList": [
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
      }
    ],
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet2/pictures",
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

**Erfolgsantwort** – Ein erfolgreicher Aufruf gibt HTTP 200 mit einer JSON-Payload zurück, die ein `Pictures`-Objekt enthält, das den Ressourcenlink jedes Bilds auflistet.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}

Sie können die SDKs direkt über ihre jeweiligen Paketmanager herunterladen (z. B. NuGet für .NET, Maven Central für Java, Composer für PHP, npm für Node.js, PyPI für Python, CPAN für Perl und Go-Module für Go).

*Siehe auch:* Ein Bild hinzufügen, Ein Bild löschen, Bild-Eigenschaften aktualisieren.