---
title: "Zellendaten aus einem Arbeitsblatt abrufen"
type: docs
url: /get-cell-data-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells Cloud, Zellendaten abrufen, Excel-API, REST-API, Zellwert, Arbeitsblatt-API, Aspose-API-Beispiel"
description: "Rufen Sie den Wert, den Typ und den Stil einer einzelnen Zelle aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) ab. Enthält cURL- und SDK-Beispiele, Parameter und Fehlerbehandlung."
---

Diese REST-API ruft eine Zelle aus einem Excel-Arbeitsblatt ab, wenn der Parameter **`cellOrMethodName`** einen Zellennamen angibt (eine A1-Adresse wie `A3`).

- **cURL-Beispiel**

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parameter**

| Parameter          | Type   | Beschreibung                                                | Erforderlich |
|--------------------|--------|-------------------------------------------------------------|--------------|
| `cellOrMethodName` | string | Muss auf `firstcell` gesetzt werden, um die erste Zelle abzurufen. | Ja           |
| `fileName`         | string | Name der Arbeitsmappe (z. B. `myWorkbook.xlsx`).            | Ja           |
| `worksheet`        | string | Name des Arbeitsblatts (z. B. `Sheet1`).                    | Ja           |
| `Authorization`    | header | Bearer-Token zur Authentifizierung.                          | Ja           |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Kategorie",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Kategorie</Font>",
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

{{< /tab >}}

{{< /tabs >}}

- **Verwendung der Aspose.Cells Cloud SDKs**

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