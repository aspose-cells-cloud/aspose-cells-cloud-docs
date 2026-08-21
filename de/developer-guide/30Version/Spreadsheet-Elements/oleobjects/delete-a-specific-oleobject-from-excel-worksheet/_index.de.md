---
title: "Ein OLE-Objekt in einem Excel-Arbeitsblatt löschen"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /de/oleobjects/delete/
aliases: [/de/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells, Cloud, Löschen, OLE, Objekt, Excel, Arbeitsblatt, REST, API, SDK"
description: "Erfahren Sie, wie Sie ein OLE-Objekt aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v4.0) löschen. Enthält HTTPS-Endpunkt, Authentifizierungsschritte, cURL-Beispiel, SDK-Snippets, Fehlerbehandlungshinweise und Links zu nächsten Schritten."
weight: 50
ArticleTitle: "OLE-Objekt aus Excel-Arbeitsblatt mit Aspose.Cells Cloud API löschen"
---

Diese Seite erklärt, wie Sie ein bestimmtes OLE-Objekt aus einem Arbeitsblatt in einer Excel-Arbeitsmappe mithilfe von **Aspose.Cells Cloud** löschen. Ein OLE-Objekt kann ein verknüpftes Bild, ein Diagramm oder ein beliebiges eingebettetes Objekt sein, das Excel als eigenständige Entität speichert.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### Anforderungsparameter

| Parametername     | Typ    | Ort   | Beschreibung                                                |
| ----------------- | ------ | ----- | ----------------------------------------------------------- |
| name              | string | path  | Der Name der Arbeitsmappe.                                  |
| sheetName         | string | path  | Der Name des Arbeitsblatts.                                 |
| oleObjectIndex    | integer| path  | Der Index des zu löschenden OLE-Objekts.                    |
| folder            | string | query | Der Ordner, der die Arbeitsmappe enthält. (optional)        |
| storageName       | string | query | Der Name des Speicherdienstes. (optional)                   |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das **cURL-Befehlszeilentool** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie der Aufruf mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
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

### Antwortdetails

| HTTP-Status          | Beschreibung                                                             | Beispiel-JSON                                                       |
| -------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------- |
| **200 OK**           | Das OLE-Objekt wurde erfolgreich gelöscht.                               | `{ "Code": 200, "Status": "OK" }`                                   |
| **401 Unauthorized** | Fehlender oder ungültiger JWT-Token.                                    | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404 Not Found**    | Die angegebene Arbeitsmappe, das Arbeitsblatt oder der OLE-Objektindex existiert nicht. | `{ "Code": 404, "Message": "OLE object index out of range." }`      |
| **400 Bad Request**  | Erforderliche Parameter fehlen oder sind fehlerhaft.                    | `{ "Code": 400, "Message": "Invalid request parameters." }`         |

Fangen Sie diese Antworten in Ihrer Anwendung ab, indem Sie den HTTP-Statuscode prüfen und die zugehörige Meldung anzeigen.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---