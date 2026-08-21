---
title: "Alle Bilder in einem Excel-Arbeitsblatt löschen"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /de/pictures/clear/
aliases: [  /delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, alle Bilder löschen, Arbeitsblatt, REST API, Bilder löschen"
description: "Erfahren Sie, wie Sie alle Bilder aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API mit cURL- und SDK-Beispielen löschen."
weight: 60
ArticleTitle: "So löschen Sie alle Bilder in einem Excel-Arbeitsblatt mit Aspose.Cells Cloud"
---

Diese REST API löscht **alle** Bilder in einem Arbeitsblatt.

**Voraussetzungen**  
- Ein aktives Aspose.Cells Cloud-Konto mit einem gültigen OAuth 2.0-Zugriffstoken.  
- API-Version 3.0 (oder neuer) ist erforderlich; frühere Versionen sind veraltet.  
- Die Ziel-Excel-Datei muss an einem unterstützten Speicherort gespeichert sein (Standard oder benutzerdefiniert).

**Versionskompatibilität**  
Der Endpunkt folgt der Cells Cloud 3.0-API-Spezifikation. Stellen Sie sicher, dass Ihre Client-Bibliotheken und Anforderungs-URLs `api.aspose.cloud/v3.0` verwenden.

## DeleteWorksheetPictures API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud-APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername | Typ    | Ort   | Beschreibung                                |
| ------------- | ------ | ----- | ------------------------------------------- |
| name          | string | Path  | Name der Excel-Datei.                       |
| sheetName     | string | Path  | Name des Arbeitsblatts, das die Bilder enthält. |
| folder        | string | Query | Ordner, in dem die Datei gespeichert ist.   |
| storageName   | string | Query | Name des Speicherdienstes.                  |

### Fehlerantworten

| HTTP-Code | Beschreibung                                                                   |
| --------- | ------------------------------------------------------------------------------ |
| 401       | Nicht autorisiert – fehlendes oder ungültiges Token.                          |
| 404       | Nicht gefunden – die angegebene Datei, das Arbeitsblatt oder der Seitenumbruchindex existiert nicht. |
| 400       | Ungültige Anforderung – fehlerhafte Anforderungssyntax oder ungültige Parameter. |
| 500       | Interner Serverfehler – unerwarteter Zustand ist aufgetreten.                 |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
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

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Hinweise:** Der DELETE-Vorgang unterstützt keine Paginierung und unterliegt den Standard-Rate-Limits der Aspose.Cells Cloud API (standardmäßig 100 Anfragen pro Minute). Passen Sie Ihre Client-Logik entsprechend an.

**Siehe auch**:  
- [/pictures/delete/](../delete/) – Löschen eines bestimmten Bilds aus einem Arbeitsblatt.  
- [/pictures/add/](../add/) – Hinzufügen eines Bilds zu einem Arbeitsblatt.  
---