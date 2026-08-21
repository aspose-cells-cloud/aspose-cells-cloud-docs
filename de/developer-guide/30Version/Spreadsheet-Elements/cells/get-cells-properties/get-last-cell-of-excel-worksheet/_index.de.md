---
title: "Letzte Zelle einer Excel-Arbeitsmappe abrufen – Aspose.Cells Cloud API (v4.0)"
type: docs
url: /de/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Excel API, letzte Zelle abrufen, Tabellenkalkulation, Cloud"
description: "Rufen Sie die Adresse der Endzelle einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API v4.0 ab. Enthält Anforderungsdetails, cURL-Beispiel, JSON-Antwort und SDK-Beispiele."
ArticleTitle: "Endzelle einer Excel-Arbeitsmappe abrufen – Aspose.Cells Cloud API v4.0"
---

Diese REST API gibt die **Endzelle** einer Excel-Arbeitsmappe zurück, wenn der Parameter `cellOrMethodName` auf `endcell` gesetzt ist.

**Übersicht**  
Der Vorgang **„Letzte Zelle abrufen“** gibt die Adresse der zuletzt verwendeten Zelle in einer angegebenen Arbeitsmappe zurück. Dies ist nützlich, um den effektiven Datenbereich eines Arbeitsblatts zu ermitteln, ohne das gesamte Dokument durchsuchen zu müssen.

- **cURL-Beispiel.**

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<Weitere Informationen>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<Weitere Informationen>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;Weitere Informationen&gt;</Font>",
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

### Parameter
| Parameter            | Type   | Erforderlich | Beschreibung |
|----------------------|--------|--------------|--------------|
| `fileName`           | string | Ja           | Name der Excel-Datei, die in der Cloud gespeichert ist. |
| `worksheetName`      | string | Ja           | Name des Arbeitsblatts, aus dem die letzte Zelle abgerufen werden soll. |
| `cellOrMethodName`   | string | Ja           | Muss auf **`endcell`** gesetzt sein, um diesen Vorgang auszulösen. |
| `folder` *(optional)*| string | Nein         | Cloud-Ordnerpfad, in dem sich die Arbeitsmappe befindet. |
| `storageName` *(optional)*| string | Nein    | Name des Speichers. Falls weggelassen, wird der Standardspeicher verwendet. |

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größeinschränkung. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

- **Verwenden Sie Aspose.Cells Cloud SDKs**

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_Kommt bald._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

Weitere Vorgänge im Zusammenhang mit der Zellennavigation finden Sie in den Themen **[Erste Zelle abrufen](/de/get-first-cell-of-excel-worksheet/)** und **[Maximale Zeile abrufen](/de/get-max-row-of-worksheet/)**.