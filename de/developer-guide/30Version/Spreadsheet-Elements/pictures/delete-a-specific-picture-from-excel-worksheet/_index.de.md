---
title: "Ein Bild aus einer Excel-Arbeitsmappe löschen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /pictures/delete/
aliases: [/delete-a-specific-picture-from-excel-worksheet/]
keywords: "Aspose.Cells, Cloud API, Bild löschen, Excel-Arbeitsmappe, REST"
description: "Löschen Sie ein Bild aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API. Erfahren Sie mehr über den DELETE-Endpunkt, die erforderlichen Parameter, die Authentifizierung, Fehlercodes und Beispielcode."
weight: 50
ArticleTitle: "Ein Bild aus einer Excel-Arbeitsmappe löschen – Aspose.Cells Cloud API"
---

Diese REST API löscht ein Bild aus einer Excel-Arbeitsmappe.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Anforderungsparameter

| Parametername | Typ    | Speicherort | Erforderlich | Beschreibung                                              |
| ------------- | ------ | ----------- | ------------ | --------------------------------------------------------- |
| name          | string | path        | Ja           | Der Name der Arbeitsmappe (Datei).                        |
| sheetName     | string | path        | Ja           | Der Name des Arbeitsblatts, das das Bild enthält.        |
| pictureIndex  | integer| path        | Ja           | Der nullbasierte Index des zu löschenden Bildes.         |
| folder        | string | query       | Nein         | Der Ordner, in dem die Arbeitsmappe gespeichert ist.     |
| storageName   | string | query       | Nein         | Der Name des Speicherdienstes (optional).                |

Sie können das cURL-Befehlszeilentool verwenden, um bequem auf die Aspose.Cells-Webdienste zuzugreifen. Im folgenden Beispiel wird gezeigt, wie der Aufruf mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
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

**Beispiel für Antwort-Header**

| Header        | Wert                          |
|---------------|-------------------------------|
| Content-Type  | application/json              |
| Content-Length| (variiert)                    |
| Date          | (Server-Datum)                |

{{< /tab >}}

{{< /tabs >}}

### Fehlerbehandlung

| HTTP-Code | Bedeutung                                                    | Beispiel für Fehlerpayload                                          |
| --------- | ------------------------------------------------------------ | ------------------------------------------------------------------- |
| 200       | Bild erfolgreich gelöscht.                                   | `{ "Code": 200, "Status": "OK" }`                                   |
| 400       | Ungültige Anforderung – ungültige Parameter.                 | `{ "Code": 400, "Message": "Invalid pictureIndex." }`               |
| 401       | Nicht autorisiert – fehlender/ungültiger Token.              | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| 404       | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Bild existiert nicht. | `{ "Code": 404, "Message": "Resource not found." }`                 |
| 500       | Interner Serverfehler.                                       | `{ "Code": 500, "Message": "Unexpected server error." }`            |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihr Projekt konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}