---
title: "Ein OLE-Objekt in einem Excel-Arbeitsblatt hinzufügen"
second_title: "Dokument"
linktitle: "OLE-Objekt hinzufügen"
type: docs
url: /oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "OLE-Objekt hinzufügen, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um OLE-Objekte (z. B. Word-Dokumente, PDFs oder andere Binärdateien) direkt in Excel-Arbeitsblätter einzubetten. Die API kann direkt oder über SDKs für C#, Java, PHP, Ruby, Node.js, Python, Perl und Go aufgerufen werden."
ArticleTitle: "OLE-Objekt mit Aspose.Cells Cloud API zu einem Excel-Arbeitsblatt hinzufügen"
weight: 20
---

Die Aspose.Cells Cloud API ermöglicht die programmatische Bearbeitung von Excel-Arbeitsmappen, einschließlich der Möglichkeit, OLE-Objekte (z. B. Word-Dokumente, PDFs oder andere Binärdateien) direkt in ein Arbeitsblatt einzubetten.

Diese REST API fügt ein **OLE-Objekt** zu einem Excel-Arbeitsblatt hinzu.

**Voraussetzungen** – Sie benötigen ein gültiges JWT-Authentifizierungstoken, und alle Quelldateien, die von `oleFile` oder `imageFile` referenziert werden, müssen vor dem Aufruf des Endpunkts in den angegebenen Speicherort hochgeladen werden.

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername        | Typ    | Ort   | Beschreibung                                           |
|----------------------|--------|-------|--------------------------------------------------------|
| name                 | string | path  | Der Name der Arbeitsmappe.                             |
| sheetName            | string | path  | Der Name des Arbeitsblatts.                            |
| oleObject            | object | body  | Die Definition des OLE-Objekts.                        |
| upperLeftRow         | integer| query | Zeilenindex der oberen linken Ecke (Standardwert 0).  |
| upperLeftColumn      | integer| query | Spaltenindex der oberen linken Ecke (Standardwert 0).|
| height               | integer| query | Höhe des OLE-Objekts (Standardwert 0).                 |
| width                | integer| query | Breite des OLE-Objekts (Standardwert 0).               |
| oleFile              | string | query | Name der OLE-Quelldatei.                               |
| imageFile            | string | query | Name der Vorschaubilddatei.                            |
| folder               | string | query | Der Ordner, der die Arbeitsmappe enthält.              |
| storageName          | string | query | Name des zu verwendenden Speichers.                    |

**Hinweise** – `upperLeftRow` und `upperLeftColumn` verwenden eine nullbasierte Indizierung. Die Dateien `oleFile` (und optional `imageFile`) müssen bereits im Ziel Speicher vorhanden sein; andernfalls gibt die Anforderung einen Fehler zurück.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webservices aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL ein OLE-Objekt hinzufügen. **Für alle Produktionsaufrufe ist HTTPS erforderlich.**

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Screenshot eines in ein Excel-Arbeitsblatt eingebetteten OLE-Objekts](/cells/images/ole-object-example.png)

**Mögliche HTTP-Statuscodes**

| Code | Beschreibung                                               |
|------|------------------------------------------------------------|
| 200  | OLE-Objekt erfolgreich hinzugefügt.                        |
| 400  | Ungültige Anforderung – fehlende oder ungültige Parameter.|
| 401  | Nicht autorisiert – ungültiges oder fehlendes JWT-Token.  |
| 404  | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Quelldatei existiert nicht. |
| 500  | Interner Serverfehler – unerwarteter Fehler.               |

Eine typische erfolgreiche Antwort gibt die folgende JSON-Payload zurück:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Cloud SDK-Familie

Die Verwendung eines SDK beschleunigt die Entwicklung. Ein SDK abstrahiert Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}