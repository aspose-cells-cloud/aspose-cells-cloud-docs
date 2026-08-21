---
title: "Fügen Sie eine Form in ein Excel-Arbeitsblatt ein"
second_title: "Dokument"
linktitle: "Hinzufügen"
type: docs
url: /de/shapes/add/
aliases: [  /de/add-a-shape-inside-the-worksheet/ ]
keywords: "Aspose.Cells, Form hinzufügen, Excel, REST-API, Cloud-SDK, shapeDTO, Zeichnungstyp"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API v3.0 Formen (Bogen, Linie, Rechteck usw.) in ein Excel-Arbeitsblatt einfügen. Enthält die Anforderungssyntax, erforderliche Parameter, Authentifizierungsschritte und Beispiel-SDK-Code."
weight: 30
ArticleTitle: "Fügen Sie eine Form mithilfe der Aspose.Cells Cloud-API in ein Excel-Arbeitsblatt ein"
---

Diese REST-API fügt eine Form in ein Excel-Arbeitsblatt ein.  
Der Endpunkt gehört zur **API-Version v3.0**. Stellen Sie sicher, dass Sie ein JWT-Zugriffstoken verwenden, das über den Aspose Cloud OAuth2-Flow (client-id/client-secret) erhalten wurde, und fügen Sie es in den Header `Authorization: Bearer <token>` ein.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## PutWorksheetShape API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Anforderungsparameter**

| Parametername      | Typ    | Speicherort | Beschreibung                                                                                           |
|--------------------|--------|-------------|--------------------------------------------------------------------------------------------------------|
| name               | string | path        | Name des Dokuments.                                                                                    |
| sheetName          | string | path        | Name des Arbeitsblatts.                                                                                |
| shapeDTO           | object | body        | JSON-Objekt, das die einzufügende Form beschreibt (siehe OpenAPI-Spezifikation für das vollständige Schema). |
| drawingType        | string | query       | Typ des Formobjekts (z. B. `arc`, `line`, `rectangle`).                                                |
| upperLeftRow       | integer| query       | Zeilenindex der oberen linken Ecke der Form.                                                           |
| upperLeftColumn    | integer| query       | Spaltenindex der oberen linken Ecke der Form.                                                          |
| top                | integer| query       | Vertikaler Versatz der Form ab ihrem oberen Rand, in Pixel.                                            |
| left               | integer| query       | Horizontaler Versatz der Form ab ihrem linken Rand, in Pixel.                                          |
| width              | integer| query       | Breite der Form, in Pixel.                                                                             |
| height             | integer| query       | Höhe der Form, in Pixel.                                                                               |
| folder             | string | query       | Ordner, der das Dokument enthält.                                                                      |
| storageName        | string | query       | Name des Speichers.                                                                                    |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ShapeId": 5
}
```

_Die erfolgreiche Antwort gibt den HTTP-Statuscode, einen textuellen Status und die Kennung der neu erstellten Form (`ShapeId`) zurück._

{{< /tab >}}

{{< /tabs >}}

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

Typische Fehlerantworten umfassen:

- **400 Bad Request** – fehlende oder ungültige Parameter.  
- **401 Unauthorized** – ungültiges oder fehlendes JWT-Token.  
- **404 Not Found** – das angegebene Arbeitsblatt oder Dokument ist nicht vorhanden.

Jeder Fehler wird als JSON-Objekt mit den Feldern `Code` und `Message` zurückgegeben.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs anzuzeigen.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}