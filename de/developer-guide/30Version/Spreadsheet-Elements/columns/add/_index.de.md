---
title: "Fügen Sie eine leere Spalte zu einem Excel-Arbeitsblatt hinzu – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Hinzufügen"
type: docs
url: /de/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "hinzufügen, spalte, excel, api, aspose.cells, cloud, rest, einfügen"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API eine neue Spalte in ein Excel-Arbeitsblatt einfügen. Enthält Anfrage-Syntax, cURL-Beispiel und SDK-Codebeispiele."
weight: 20
ArticleTitle: "Leere Spalte zu Excel-Arbeitsblatt mit Aspose.Cells Cloud API hinzufügen"
---

Diese REST-API fügt eine oder mehrere Spalten in ein Arbeitsblatt ein.

**Voraussetzungen**  
Bevor Sie diesen Endpunkt aufrufen, stellen Sie sicher, dass Sie die folgenden Schritte ausgeführt haben:

- Holen Sie sich ein gültiges OAuth 2.0-Zugriffstoken und fügen Sie es in den `Authorization`-Header ein.  
- Speichern Sie die Ziel-Arbeitsmappe im ausgewählten Speicher (Standard = „Default“) oder geben Sie die entsprechenden Parameter `folder` und `storageName` an.  
- Stellen Sie sicher, dass der in `sheetName` angegebene Arbeitsblattname in der Arbeitsmappe vorhanden ist.

## PutInsertWorksheetColumns API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anfrageparameter

| Parametername       | Typ     | Ort     | Beschreibung                                                                 |
| --------------------|---------|---------|------------------------------------------------------------------------------|
| **name**            | string  | path    | Der Name der Arbeitsmappen-Datei.                                           |
| **sheetName**       | string  | path    | Der Name des Arbeitsblatts.                                                  |
| **columnIndex**     | integer | path    | Nullbasierter Index der Spalte, an der der Einfügvorgang beginnt.           |
| **totalColumns**    | integer | query   | Anzahl der einzufügenden Spalten.                                            |
| **updateReference** | boolean | query   | Wenn **true**, werden Zellbezüge aktualisiert, um die Einfügung widerzuspiegeln. |
| **folder**          | string  | query   | Pfad zum Ordner, der die Arbeitsmappe enthält.                              |
| **storageName**     | string  | query   | Name des Speicherdiensts.                                                    |

**Hinweise**

- Der `columnIndex` muss zwischen 0 und der aktuellen Anzahl der Spalten im Arbeitsblatt liegen. Das Einfügen außerhalb des vorhandenen Bereichs erweitert das Arbeitsblatt automatisch.  
- Das Einfügen mehrerer Spalten (`totalColumns` > 1) verschiebt vorhandene Spalten nach rechts.  
- Der `updateReference`-Flag ist standardmäßig auf `false` gesetzt; setzen Sie ihn auf `true`, um Formeln und benannte Bereiche zu aktualisieren.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices aufzurufen. Das folgende Beispiel zeigt eine vollständige Anfrage einschließlich Authentifizierung und korrekter Pfadparameter.

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Antwortcodes**

| Code | Beschreibung                                          |
|------|-------------------------------------------------------|
| 200  | Spalte(n) erfolgreich eingefügt.                      |
| 400  | Ungültige Anfrage – fehlende oder ungültige Parameter. |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token.   |
| 404  | Arbeitsmappe oder Arbeitsblatt nicht gefunden.        |
| 500  | Interner Serverfehler.                                |

**Beispiel für Fehlerantworten**

```json
// 400 Bad Request – fehlende oder ungültige Parameter
{
  "Code": 400,
  "Message": "Ungültiger Parameter: totalColumns muss eine positive Ganzzahl sein."
}

// 401 Unauthorized – ungültiges oder fehlendes Token
{
  "Code": 401,
  "Message": "Authentifizierung fehlgeschlagen. Zugriffstoken fehlt oder ist ungültig."
}

// 404 Not Found – Arbeitsmappe oder Arbeitsblatt existiert nicht
{
  "Code": 404,
  "Message": "Arbeitsmappe 'test.xlsx' nicht gefunden."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "Auf dem Server ist ein unerwarteter Fehler aufgetreten."
}
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt Details der niedrigen Ebene, sodass Sie sich auf die Logik Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}
---