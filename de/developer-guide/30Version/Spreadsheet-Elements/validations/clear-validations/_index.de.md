---
title: "Alle Arbeitsblatt-Validierungen löschen – Aspose.Cells Cloud API"
second_title: "Dokumentation"
linktitle: "Löschen"
type: docs
url: /de/validations/clear/
keywords: "Aspose.Cells Cloud, Arbeitsblatt-Validierungen löschen, Excel, REST API, Tabellenkalkulationsvalidierung, API"
description: "Entfernen Sie alle Datenvalidierungsregeln aus einem Arbeitsblatt in einer Excel-Datei mithilfe der Aspose.Cells Cloud REST API. Enthält Authentifizierungsschritte, Anforderungsdetails, cURL-Beispiel, Antwortschema, Fehlerbehandlung und SDK-Snippets."
weight: 10
---

**Voraussetzungen**

- Ein gültiges Aspose Cloud-Konto.
- Ein JWT-Zugriffstoken, das über die Aspose Cloud-Authentifizierungs-API (`/connect/token`) erhalten wurde.
- Die Arbeitsmappe muss in Ihrem Aspose Cloud-Speicher gespeichert sein (oder die entsprechenden Abfrageparameter `folder`/`storageName` müssen angegeben werden).

Diese REST API löscht alle Arbeitsblatt-Validierungen in einem Excel-Arbeitsblatt.

## REST API

```bash
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations
```

### **Anforderungsparameter**

| Parametername   | Typ    | Ort    | Beschreibung                                        |
| --------------- | ------ | ------ | --------------------------------------------------- |
| name            | string | path   | Der Name der Excel-Datei.                          |
| sheetName       | string | path   | Der Name des Arbeitsblatts, das die Validierungen enthält. |
| folder          | string | query  | Der Ordner, in dem das Dokument gespeichert ist.   |
| storageName     | string | query  | Der Name des Speicherdienstes.                     |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL nach dem Erhalt eines JWT-Tokens aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations" \
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

### Fehlerbehandlung

| HTTP-Status | Bedeutung             | Beschreibung                                                |
| ----------- | --------------------- | ----------------------------------------------------------- |
| 400         | Bad Request (Ungültige Anforderung) | Die Anforderung ist fehlerhaft oder erforderliche Parameter fehlen. |
| 401         | Unauthorized (Nicht autorisiert)   | Der JWT-Token fehlt, ist ungültig oder abgelaufen.         |
| 404         | Not Found (Nicht gefunden)         | Die angegebene Arbeitsmappe oder das angegebene Arbeitsblatt existiert nicht. |
| 500         | Internal Server Error (Interner Serverfehler) | Auf Serverseite ist ein unerwarteter Fehler aufgetreten. |

Die Fehlerantwort folgt derselben JSON-Struktur mit den Feldern `Code` und `Message`, beispielsweise:

```json
{
  "Code": 401,
  "Message": "Ungültiger oder abgelaufener Token."
}
```

## Cloud SDK-Familie

Die Verwendung eines SDK ist die schnellste Methode zur Entwicklung. Ein SDK abstractiert niedrigstufige Details, sodass Sie sich auf die Geschäftslogik konzentrieren können. Überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidations.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidations.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidations.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidations.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidations.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidations.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidations.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidations.go" >}}

{{< /tab >}}

{{< /tabs >}}