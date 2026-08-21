---
title: "Aktualisieren einer Arbeitsblattvalidierung in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Aktualisieren"
type: docs
url: /de/validations/update/
keywords: "Aspose.Cells Cloud, Excel-Validierung aktualisieren, REST-API, Arbeitsblattvalidierung, Excel-API"
description: "Wie Sie eine Arbeitsblattvalidierung in einer Excel-Datei mithilfe der Aspose.Cells Cloud REST-API aktualisieren, mit cURL-Beispielen und SDK-Codeausschnitten für mehrere Programmiersprachen."
weight: 10
ArticleTitle: "Arbeitsblattvalidierung mit der Aspose.Cells Cloud API aktualisieren"
---

Diese REST-API aktualisiert eine Arbeitsblattvalidierung anhand ihres Index in einem Excel-Arbeitsblatt.

Bevor Sie diesen Endpunkt aufrufen, beschaffen Sie ein JWT-Zugriffstoken mit den entsprechenden Berechtigungen (z. B. `Cells.ReadWrite`). Binden Sie das Token wie in den Beispielen gezeigt in den `Authorization`-Header ein.

## REST-API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Anforderungsparameter**

| Parametername   | Typ     | Ort     | Beschreibung                                                   |
| --------------- | ------- | ------- | -------------------------------------------------------------- |
| name            | string  | path    | Der Name der Arbeitsmappe (.xlsx-Datei).                       |
| sheetName       | string  | path    | Der Name des Arbeitsblatts, das die Validierung enthält.      |
| validationIndex | integer | path    | Der nullbasierte Index der zu aktualisierenden Validierung.   |
| validation      | object  | body    | Ein JSON-Objekt, das die aktualisierten Validierungseinstellungen definiert. |
| folder          | string  | query   | Der Ordner im Cloud-Speicher, in dem sich die Arbeitsmappe befindet. |
| storageName     | string  | query   | Der Name des Speicherdienstes (falls ein benutzerdefinierter Speicher verwendet wird). |

Die <a href="https://apireference.aspose.cloud/cells/#/WorksheetValidations/PostWorksheetValidation" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ "AlertStyle":"Warning" }'
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

**Mögliche HTTP-Statuscodes**

| Code | Bedeutung                               | Beschreibung |
|------|-----------------------------------------|-------------|
| 200  | OK                                      | Die Validierung wurde erfolgreich aktualisiert. |
| 400  | Bad Request (Ungültige Anfrage)         | Die Anfrage ist fehlerhaft oder es fehlen erforderliche Parameter. |
| 401  | Unauthorized (Nicht autorisiert)        | Ungültiges oder fehlendes JWT-Token. |
| 403  | Forbidden (Verweigert)                  | Das Token verfügt über nicht ausreichende Berechtigungen. |
| 404  | Not Found (Nicht gefunden)              | Die angegebene Arbeitsmappe, das angegebene Arbeitsblatt oder der angegebene Validierungsindex existiert nicht. |
| 500  | Internal Server Error (Interner Serverfehler) | Auf dem Server ist ein unerwarteter Fehler aufgetreten. |

Weitere Informationen zur Fehlerbehandlung finden Sie in der <a href="https://apireference.aspose.cloud/cells/#/Errors" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud-Fehlerdokumentation</a>.

Sie könnten auch an verwandten Vorgängen interessiert sein, z. B. dem Hinzufügen einer neuen Validierung oder dem Löschen einer bestehenden:

- [Hinzufügen einer Arbeitsblattvalidierung](https://docs.aspose.cloud/cells/validations/add/)
- [Löschen einer Arbeitsblattvalidierung](https://docs.aspose.cloud/cells/validations/delete/)

## Cloud SDK-Familie

Die Verwendung eines SDK ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstractiert niedrigere Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}
---