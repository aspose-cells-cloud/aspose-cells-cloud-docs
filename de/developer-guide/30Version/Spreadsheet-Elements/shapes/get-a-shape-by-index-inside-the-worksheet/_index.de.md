---
title: "Abrufen einer Form nach Index in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktype: "Abrufen"
type: docs
url: /de/shapes/get/
aliases: [/de/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, Excel-Form-API, Form nach Index abrufen, Arbeitsblattform, REST-API, Formabruf, Aspose.Cells SDK"
description: "Rufen Sie eine Form nach ihrem Index aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API ab. Enthält Anforderungssyntax, Parameter, Antwortdetails und SDK-Beispiele."
weight: 20
ArticleTitle: "Abrufen einer Form nach Index in einem Excel-Arbeitsblatt – Aspose.Cells Cloud-Dokumentation"
---

Diese REST-API ruft eine Form (einschließlich ihrer Bilddaten oder Metadaten) aus einem Excel-Arbeitsblatt ab.

## GetWorksheetShape API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**Voraussetzungen**  
- Ein gültiger Aspose Cloud-Zugriffstoken (Bearer JWT).  
- Die Arbeitsmappe muss sich in Ihrem Aspose Cloud-Speicher oder in einem angegebenen Ordner befinden.  

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername | Typ    | Position | Beschreibung                                               |
| ------------- | ------ | -------- | ---------------------------------------------------------- |
| name          | string | path     | Name des Excel-Dokuments.                                  |
| sheetName     | string | path     | Name des Arbeitsblatts, das die Form enthält.             |
| shapeindex    | integer| path     | Nullbasierter Index der Form innerhalb des Arbeitsblatts. |
| folder        | string | query    | Ordnerpfad, in dem das Dokument gespeichert ist.          |
| storageName   | string | query    | Name des Speicherdiensts.                                  |

**Hinweis:** `shapeindex` ist nullbasiert; die erste Form hat den Index 0. Stellen Sie sicher, dass die Arbeitsmappe im angegebenen `folder` und `storageName` gespeichert ist, sofern Sie nicht den Standardspeicher verwenden.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
# Korrigierter Endpunkt und Pfad
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Mögliche HTTP-Statuscodes**

| Code | Beschreibung |
|------|-------------|
| **200 OK** | Die Form wurde erfolgreich abgerufen. |
| **400 Bad Request** | Die Anforderung ist fehlerhaft formatiert oder erforderliche Parameter fehlen. |
| **401 Unauthorized** | Die Authentifizierung ist fehlgeschlagen oder das Token fehlt/ist ungültig. |
| **404 Not Found** | Die angegebene Arbeitsmappe, das Arbeitsblatt oder der Formindex existiert nicht. |
| **500 Internal Server Error** | Ein unerwarteter Serverfehler ist aufgetreten. |

**Häufige Fehlerquellen:** Die Verwendung einer falschen Basisdomain (`api.aspose.com`) oder des veralteten `/autoshapes/`-Pfads führt zu einem 404-Fehler. Verwenden Sie immer den `/shapes/`-Pfad mit der Domain `api.aspose.cloud`.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details der unteren Schicht und lässt Sie sich auf Ihre Projektziele konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

Für verwandte Vorgänge siehe die Dokumentation zu **[Hinzufügen einer Form](/de/shapes/add/)** und **[Aktualisieren einer Form](/de/shapes/update/)**.