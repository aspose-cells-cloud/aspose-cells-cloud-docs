---
title: "Erste Zelle (A1) aus einem Excel-Arbeitsblatt abrufen"
type: docs
url: /de/get-first-cell-from-excel-worksheet/
weight: 20
keywords: "Aspose.Cells Cloud, Excel, REST API, Erste Zelle abrufen, Arbeitsblatt, A1, API v3"
description: "Erfahren Sie, wie Sie die erste Zelle (A1) eines Excel-Arbeitsblatts mithilfe der Aspose.Cells Cloud REST API v3.0 abrufen. Enthält cURL-Anforderung, JSON-Antwort, Fehlerbeispiele und SDK-Beispiele für C#, Java, PHP, Python und weitere Sprachen."
ArticleTitle: "Erste Zelle (A1) aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API abrufen"
---

Diese REST API zeigt, wie Sie die **erste Zelle** in einer Excel-Datei abrufen, wenn der Parameter `cellOrMethodName` auf `firstcell` gesetzt ist.

**Endpoint**  
`GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{worksheet}/cells/firstcell`

- **cURL-Beispiel**

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/firstcell" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parameter**

| Parameter          | Typ    | Beschreibung                                               | Erforderlich |
|--------------------|--------|-----------------------------------------------------------|-------------|
| `cellOrMethodName` | string | Muss auf `firstcell` gesetzt werden, um die erste Zelle abzurufen. | Ja          |
| `fileName`         | string | Name der Arbeitsmappe (z. B. `myWorkbook.xlsx`).          | Ja          |
| `worksheet`        | string | Name des Arbeitsblatts (z. B. `Sheet1`).                 | Ja          |
| `Authorization`    | header | Bearer-Token zur Authentifizierung.                       | Ja          |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A1",
    "Row": 0,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**Fehlerantworten**

- **401 Unauthorized**

```json
{
  "Code": "401",
  "Message": "Ungültiges Access-Token."
}
```

- **404 Not Found**

```json
{
  "Code": "404",
  "Message": "Die angegebene Arbeitsmappe, das angegebene Arbeitsblatt oder die angegebene Zelle existiert nicht."
}
```

- **500 Internal Server Error**

```json
{
  "Code": "500",
  "Message": "Auf dem Server ist ein unerwarteter Fehler aufgetreten."
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.            |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                      |

{{< /tab >}}

{{< /tabs >}}

- **Cloud SDK-Familie**

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}
---