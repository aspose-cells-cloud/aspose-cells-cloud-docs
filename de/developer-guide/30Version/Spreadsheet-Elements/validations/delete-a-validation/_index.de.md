---
title: "Arbeitsblatt-Validierung löschen – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /de/validations/delete/
keywords: "Löschen, Arbeitsblatt-Validierung, Aspose.Cells Cloud, Excel-API"
description: "Erfahren Sie, wie Sie eine Arbeitsblatt-Validierung aus einer Excel-Datei mithilfe der Aspose.Cells Cloud REST-API löschen. Enthält Endpunkt, Parameter, Authentifizierungsdetails, cURL-Beispiel, Fehlerbehandlung und SDK-Code-Snippets."
weight: 10
---

Diese REST-API löscht eine Arbeitsblatt-Validierung anhand ihres nullbasierten Index in einem Excel-Arbeitsblatt.

## REST-API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Anforderungsparameter**

| Parametername     | Typ     | Ort   | Beschreibung                                         |
| ----------------- | ------- | ----- | ---------------------------------------------------- |
| name              | string  | path  | Der Name der Excel-Datei.                            |
| sheetName         | string  | path  | Der Name des Arbeitsblatts.                          |
| validationIndex   | integer | path  | Der nullbasierte Index der zu löschenden Validierung. |
| folder            | string  | query | Der Ordner, der das Dokument enthält.                |
| storageName       | string  | query | Der Name des Speicherdienstes.                       |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/WorksheetValidations/DeleteWorksheetValidation) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um den Aspose.Cells-Webdienst aufzurufen. Das folgende Beispiel zeigt, wie Sie eine Validierung mit cURL löschen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

**HTTP-Statuscodes**

| Code | Bedeutung                 | Beschreibung                                            |
|------|---------------------------|---------------------------------------------------------|
| 200  | OK                        | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request               | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized              | Ungültiges oder fehlendes JWT-Token.                    |
| 413  | Payload Too Large         | Die hochgeladene Datei überschreitet das Größenlimit.   |
| 500  | Internal Server Error     | Unerwarteter Serverfehler.                              |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit, diesen Vorgang in Ihre Anwendung zu integrieren. SDKs übernehmen die Details auf niedriger Ebene, sodass Sie sich auf die Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs eine Arbeitsblatt-Validierung löschen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}