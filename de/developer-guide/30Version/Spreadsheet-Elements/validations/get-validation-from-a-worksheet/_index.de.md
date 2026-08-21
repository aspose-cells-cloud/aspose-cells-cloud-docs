---
title: "Abrufen einer Validierung aus einer Excel-Arbeitsmappe per Index"
second_title: "Dokument"
linktitle: "Abrufen"
type: docs
url: /de/validations/get/
aliases: [  /de/get-validation-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Worksheet-Validierungs-API, Validierung per Index abrufen, Excel REST API, Aspose.Cells SDK"
description: "Rufen Sie eine Validierung aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud API (v3.0) über ihren nullbasierten Index ab. Enthält ein cURL-Beispiel, das Antwortschema, Fehlercodes sowie SDK-Snippets für C#, Java, Python und weitere Sprachen."
weight: 10
---

Diese REST API ruft eine Validierung aus einer Excel-Arbeitsmappe per Index ab.  
Bevor Sie den Endpunkt aufrufen, müssen Sie ein JWT-Token über den `/connect/token`-Endpunkt erhalten und es im `Authorization`-Header als `Bearer <jwt token>` übergeben.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Anfrageparameter**

| Parametername     | Typ      | Ort    | Beschreibung                                                  |
| ----------------- | -------- | ------ | ------------------------------------------------------------- |
| name              | string   | path   | Der Name der Arbeitsmappendatei.                              |
| sheetName         | string   | path   | Der Name des Arbeitsblatts.                                   |
| validationIndex   | integer  | path   | Der nullbasierte Index der abzurufenden Validierung.         |
| folder            | string   | query  | Der Ordner, der die Arbeitsmappe enthält.                     |
| storageName       | string   | query  | Der Name des Speicherdienstes.                                |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen REST-basierte Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Antwortschema**

| Feld             | Typ       | Beschreibung                                                                 |
| ---------------- | --------- | ---------------------------------------------------------------------------- |
| AlertStyle       | string    | Der Stil der dem Benutzer angezeigten Warnung (Stop, Warning, Information). |
| AreaList         | array     | Sammlung von Zellbereichen, auf die die Validierung angewendet wird.        |
| IgnoreBlank      | boolean   | Wenn `true`, werden leere Zellen bei der Validierung ignoriert.             |
| InCellDropDown   | boolean   | Wenn `true`, wird ein Drop-down-Menü in der Zelle angezeigt.                |
| Operator         | string    | Der für die Validierung verwendete Vergleichsoperator (z. B. `None`, `Between`). |
| ShowError        | boolean   | Gibt an, ob eine Fehlermeldung angezeigt wird, wenn die Validierung fehlschlägt. |
| ShowInput        | boolean   | Gibt an, ob eine Eingabemeldung angezeigt wird, wenn die Zelle ausgewählt wird. |
| Type             | string    | Typ der Validierung (z. B. `AnyValue`, `WholeNumber`, `Decimal`, usw.).    |
| link.Href        | string    | Selbstverweis-URL zur Validierungsressource.                                |
| link.Rel         | string    | Beziehungstyp (immer `self`).                                               |

**Mögliche Fehlercodes**

| HTTP-Status | Bedeutung                                                          |
| ----------- | ------------------------------------------------------------------ |
| 200         | Validierung erfolgreich abgerufen.                                |
| 400         | Ungültige Anfrage – fehlende oder ungültige Parameter.           |
| 401         | Nicht autorisiert – ungültiges oder fehlendes JWT-Token.         |
| 404         | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Validierungsindex existiert nicht. |
| 500         | Interner Serverfehler – unerwarteter Zustand.                     |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg, um mit Aspose.Cells Cloud zu entwickeln. Ein SDK abstractiert die Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}