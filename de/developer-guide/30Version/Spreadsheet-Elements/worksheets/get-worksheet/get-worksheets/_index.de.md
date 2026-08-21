---
title: "Alle Arbeitsblätter abrufen"
second_title: "Dokument"
linktitle: "Alle"
type: docs
url: /worksheets/get-all/
aliases: [/get-worksheet-count/]
keywords: "Aspose.Cells, Cloud API, Arbeitsblätter abrufen, Excel, REST, SDK"
description: "Rufen Sie die Liste der Arbeitsblätter in einer Excel-Arbeitsmappe über die Aspose.Cells Cloud REST API (v3.0) ab. Enthält cURL-Beispiel, SDK-Snippets und Antwortformat."
weight: 10
---

Diese REST API gibt Informationen über die Arbeitsblätter in einer Arbeitsmappe zurück.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Anfrageparameter**

| Parametername   | Typ    | Ort    | Beschreibung                              |
| --------------- | ------ | ------ | ----------------------------------------- |
| name            | string | path   | Der Name der Excel-Datei.                 |
| folder          | string | query  | Der Ordner, der das Dokument enthält.     |
| storageName     | string | query  | Der Name des zu verwendenden Speichers.   |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um auf Aspose.Cells Cloud-Dienste zuzugreifen. Das folgende Beispiel zeigt eine GET-Anfrage zum Abrufen der Arbeitsblätter.

{{< tabs tabTotal="2" tabID="1" tabName1="Anfrage" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Fehlerbehandlung

Typische HTTP-Statuscodes, die von diesem Endpunkt zurückgegeben werden:

| Code | Bedeutung             | Beschreibung                                 |
| ---- | --------------------- | -------------------------------------------- |
| 400  | Bad Request           | Erforderlicher Parameter fehlt (z. B. `name`). |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.         |
| 404  | Not Found             | Angegebene Arbeitsmappe existiert nicht.     |
| 500  | Internal Server Error | Unerwarteter Serverzustand.                  |

Fehlerantworten werden im JSON-Format zurückgegeben, z. B.:

```json
{
  "Code": "401",
  "Message": "Ungültiges Zugriffstoken."
}
```

## Cloud SDK Family

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}