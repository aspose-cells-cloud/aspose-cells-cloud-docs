---
title: "Ein OLE-Objekt in einer Excel-Arbeitsmappe aktualisieren"
second_title: "Dokument"
linktitle: "Aktualisieren"
type: docs
url: /de/oleobjects/update/
aliases: [  /de/update-a-specific-oleobject-from-excel-worksheet/ ]
keywords: "OLE-Objekt aktualisieren, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Erfahren Sie, wie Sie ein OLE-Objekt (Bild, Diagramm usw.) in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API aktualisieren. Enthält cURL- und SDK-Beispiele, Schritte zur Authentifizierung sowie Fehlerbehandlung."
weight: 30
author: "Aspose Cloud Documentation Team"
lastmod: "2024-03-01"
ArticleTitle: "Ein OLE-Objekt in einer Excel-Arbeitsmappe aktualisieren – Aspose.Cells Cloud API-Anleitung"
---

Diese REST API aktualisiert ein **OLE-Objekt** in einer Excel-Arbeitsmappe.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## PostUpdateWorksheetOleObject API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

Die Anfrageparameter sind:

| Parametername      | Typ     | Parameterposition | Beschreibung                                             |
| ------------------ | ------- | ----------------- | -------------------------------------------------------- |
| name               | string  | path              | Der Name der Arbeitsmappe.                               |
| sheetName          | string  | path              | Der Name des Arbeitsblatts.                              |
| oleObjectIndex     | integer | path              | Index des OLE-Objekts innerhalb des Arbeitsblatts.      |
| ole                | object  | body              | JSON-Darstellung des zu aktualisierenden OLE-Objekts.   |
| folder             | string  | query             | Der Ordner, der die Arbeitsmappe enthält.               |
| storageName        | string  | query             | Der Name des Speicherdienstes.                           |

### Felder im Anforderungstext

| Feld                  | Typ      | Erforderlich | Beschreibung                                               |
| --------------------- | -------- | ------------ | ---------------------------------------------------------- |
| ImageSourceFullName   | string   | optional     | Pfad zur Bilddatei, die für das OLE-Objekt verwendet wird.|
| IsAutoSize            | boolean  | optional     | Gibt an, ob das OLE-Objekt automatisch dimensioniert wird.|
| SourceFullName        | string   | erforderlich | Die Quelldatei (z. B. ein Bild oder Diagramm) für das OLE-Objekt. |
| UpperLeftRow          | integer  | erforderlich | Zeilenindex (nullbasiert) der oberen linken Ecke.         |
| UpperLeftColumn       | integer  | erforderlich | Spaltenindex (nullbasiert) der oberen linken Ecke.       |
| Left                  | integer  | optional     | Horizontaler Versatz in Punkten von der oberen linken Ecke. |
| Top                   | integer  | optional     | Vertikaler Versatz in Punkten von der oberen linken Ecke. |
| Width                 | integer  | erforderlich | Breite des OLE-Objekts in Punkten.                        |
| Height                | integer  | erforderlich | Höhe des OLE-Objekts in Punkten.                          |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das Befehlszeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
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
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Fehlerantworten

| HTTP-Status | Code | Nachricht                                                    |
| ----------- | ---- | ------------------------------------------------------------ |
| 400         | 4000 | Bad Request – fehlende oder ungültige Parameter.            |
| 401         | 4010 | Unauthorized – ungültiges oder fehlendes JWT-Token.         |
| 404         | 4040 | Not Found – Arbeitsmappe, Arbeitsblatt oder OLE-Objekt existiert nicht. |
| 500         | 5000 | Internal Server Error – unerwarteter Fehler auf Serverseite. |

Die API gibt im Antworttext auch ein benutzerdefiniertes Feld **Code** zurück, das dem HTTP-Status zugeordnet ist (z. B. 200 → 2000, 400 → 4000 usw.).

## Wann diese API verwenden?

Verwenden Sie diesen Endpunkt, wenn Sie ein vorhandenes OLE-Objekt – beispielsweise ein eingebettetes Bild, Diagramm oder Dokument – ändern möchten, ohne die gesamte Arbeitsmappe erneut hochzuladen. Typische Szenarien sind die Aktualisierung der Bildquelle, das Ändern der Größe des Objekts oder das Ändern seiner Position nach der Erstellung der Arbeitsmappe. Weitere verwandte Vorgänge finden Sie unter [Ein OLE-Objekt hinzufügen](/oleobjects/add/) und [Ein OLE-Objekt löschen](/oleobjects/delete/).

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstractiert Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Im Folgenden finden Sie ein kurzes C#-Beispiel zur Aktualisierung eines OLE-Objekts mithilfe des Aspose.Cells Cloud SDK:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Status: {response.Status}");
```

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}