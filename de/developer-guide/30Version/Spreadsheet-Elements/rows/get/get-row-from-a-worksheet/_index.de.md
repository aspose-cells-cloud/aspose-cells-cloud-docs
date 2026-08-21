---
title: "Zeilenbeschreibung aus einem Excel-Arbeitsblatt abrufen"
second_title: "Document"
linktitle: "Row"
type: docs
url: /rows/get/row/
aliases: [/get-row-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel-Zeilen-API, Arbeitsblattzeile abrufen, REST-API, .NET SDK, Java SDK, Python SDK"
description: "Abrufen detaillierter Informationen (Höhe, Stil, ausgeblendeter Status usw.) für eine bestimmte Zeile in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. Enthält cURL-Beispiel, SDK-Snippets und Fehlerbehandlung."
weight: 10
ArticleTitle: "Zeilenbeschreibung aus einem Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API"
---

**Voraussetzungen:**  
- Holen Sie sich ein gültiges JWT-Zugriffstoken und fügen Sie es in den Header `Authorization: Bearer <jwt token>` ein.  
- Stellen Sie sicher, dass die Arbeitsmappe im Aspose Cloud-Speicher gespeichert ist, oder geben Sie den Pfad des Ordners an, in dem sie sich befindet.  
- Verwenden Sie API-Version **v3.0**, wie in der Endpunkt-URL gezeigt.

Diese REST-API ruft Zeilendaten anhand ihres Index in einem Excel-Arbeitsblatt ab.

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Ort     | Beschreibung                                        |
| --------------- | ------- | ------- | --------------------------------------------------- |
| name            | string  | path    | Der Name der Arbeitsmappen-Datei.                  |
| sheetName       | string  | path    | Der Name des Arbeitsblatts innerhalb der Arbeitsmappe. |
| rowIndex        | integer | path    | Nullbasierter Index der abzurufenden Zeile.        |
| folder          | string  | query   | Der Ordner, der die Arbeitsmappe enthält.          |
| storageName     | string  | query   | Der Name des Speichers, in dem sich die Arbeitsmappe befindet. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen. Fügen Sie den Header `Authorization: Bearer <jwt token>` hinzu, um die Anfrage zu authentifizieren.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Antwort-Schema**

| Eigenschaft       | Typ     | Beschreibung                                                         |
|-------------------|---------|----------------------------------------------------------------------|
| `GroupLevel`      | integer | Gliederungsebene der Zeile (wird für Gruppierung verwendet).       |
| `Height`          | number  | Höhe der Zeile in Punkten.                                           |
| `Index`           | integer | Nullbasierter Index der zurückgegebenen Zeile.                      |
| `IsBlank`         | boolean | Gibt an, ob die Zeile Daten enthält.                                 |
| `IsHeightMatched`| boolean | `true`, wenn die Zeilenhöhe mit der Standardzeilenhöhe übereinstimmt. |
| `IsHidden`        | boolean | `true`, wenn die Zeile ausgeblendet ist.                             |
| `Style`           | object  | Objekt mit Stilinformationen für die Zeile.                         |
| `link`            | object  | Hyperlink-Verweis auf die Zeilenressource.                          |
| `Code`            | integer | HTTP-Statuscode der Antwort.                                         |
| `Status`          | string  | Textuelle Beschreibung des Status (z. B. „OK“).                    |

{{< /tab >}}

{{< /tabs >}}

**Hinweise / Fehlerbehandlung:** Die API kann die folgenden HTTP-Statuscodes zurückgeben:

- **200** – Erfolg; die Zeilendaten werden zurückgegeben.  
- **401** – Nicht autorisiert; das JWT-Token fehlt oder ist ungültig.  
- **404** – Nicht gefunden; die angegebene Arbeitsmappe, das Arbeitsblatt oder die Zeile existiert nicht.  
- **500** – Interner Serverfehler; es ist eine unerwartete Bedingung aufgetreten.

| Code | Beschreibung                                  | Behebung                                 |
|------|-----------------------------------------------|------------------------------------------|
| 200  | Erfolg – Zeilendaten wurden zurückgegeben.   | –                                        |
| 401  | Nicht autorisiert – fehlendes oder ungültiges JWT-Token. | Geben Sie ein gültiges JWT-Token an.     |
| 404  | Nicht gefunden – Arbeitsmappe, Arbeitsblatt oder Zeile fehlt. | Überprüfen Sie Namen und Zeilenindex.   |
| 500  | Interner Serverfehler – unerwartete Bedingung. | Wenden Sie sich an den Aspose-Support.   |

Eine vollständige Liste der Fehlercodes finden Sie in der Aspose.Cells Cloud [Dokumentation zu Fehlercodes](https://docs.aspose.cloud/cells/).

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Bitte überprüfen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}