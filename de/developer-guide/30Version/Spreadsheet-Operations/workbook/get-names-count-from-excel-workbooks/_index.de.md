---
title: "Namen aus einer Excel-Arbeitsmappe abrufen"
second_title: "Dokument"
linktitle: "Namen"
type: docs
url: /get-names-from-an-excel-file/
aliases:
  [
    /get-names-count-from-excel-workbooks/,
    /workbook/names/,
    /workbook/get/names/,
  ]
keywords: "Aspose.Cells, Cloud, Excel, Arbeitsmappe, Namen, REST-API, SDK"
description: "Rufen Sie alle definierten Namen aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API ab. Enthält Anleitungen zur Authentifizierung, ein cURL-Beispiel, das Antwortschema, Fehlerbehandlung und SDK-Beispiele."
weight: 120
ArticleTitle: "Namen aus einer Excel-Arbeitsmappe abrufen – Aspose.Cells Cloud API"
---

Diese REST API ruft die definierten Namen aus einer Excel-Arbeitsmappe ab.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

## GetWorkbookNames API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

Die Anforderungsparameter sind:

| Parametername | Typ   | Ort     | Beschreibung                               |
| ------------- | ----- | ------- | ------------------------------------------ |
| name          | string | Pfad    | Der Name der Arbeitsmappe-Datei.           |
| folder        | string | Abfrage | Der Ordner, der die Arbeitsmappe enthält.  |
| storageName   | string | Abfrage | Der Name des zu verwendenden Speichers.    |

Die Anforderung muss die folgenden HTTP-Header enthalten:

| Header        | Typ    | Beschreibung                                    |
|---------------|--------|-------------------------------------------------|
| Authorization | string | Bearer JWT-Token (erforderlich)                |
| Accept        | string | `application/json`                             |
| Content-Type  | string | `application/json` (für Anforderungen mit Body) |

**Authentifizierung** – Die API erfordert ein OAuth2/JWT Bearer-Token. Holen Sie sich ein Token von `https://api.aspose.cloud/connect/token` mithilfe Ihrer client-id und client-secret und fügen Sie den Header `Authorization: Bearer <jwt token>` in jede Anforderung ein.

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Aspose.Cells Cloud API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

_Antwortfelder_

- **Status** _(string)_ – Statusmeldung des Vorgangs.
- **Names.link** _(object)_ – Hyperlink-Informationen für die Sammlung.
- **Names.Count** _(integer)_ – Gesamtanzahl der zurückgegebenen definierten Namen.
- **Names.NameList** _(array)_ – Liste von Namensobjekten; jedes Objekt enthält ein **link**-Objekt mit Navigationsdetails.

**Fehlerbehandlung** – Der Dienst kann die folgenden HTTP-Statuscodes zurückgeben:

| Code | Bedeutung             | Empfohlene Aktion                                            |
| ---- | --------------------- | ------------------------------------------------------------ |
| 401  | Nicht autorisiert     | Stellen Sie sicher, dass ein gültiges JWT-Token übermittelt wird. |
| 404  | Nicht gefunden        | Überprüfen Sie, ob der Name der Arbeitsmappe, der Ordner und der Speicher korrekt sind. |
| 500  | Interner Serverfehler | Versuchen Sie es später erneut oder kontaktieren Sie den Aspose-Support, falls das Problem weiterhin besteht. |

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Die Verwendung eines SDKs ist die schnellste Methode zur Entwicklung. Ein SDK übernimmt Details auf niedriger Ebene, sodass Sie sich auf Ihr Projekt konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}
---