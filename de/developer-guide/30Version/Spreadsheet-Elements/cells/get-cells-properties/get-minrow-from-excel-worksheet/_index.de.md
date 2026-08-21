---
title: "MinRow aus Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API-Referenz"
type: docs
url: /de/get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, Excel-Arbeitsblatt, REST-API, minimaler Zeilenindex, Cloud-SDK"
description: "Erfahren Sie, wie Sie den minimalen Zeilenindex eines Arbeitsblatts mithilfe der Aspose.Cells Cloud REST API (v3.0) abrufen. Enthält vollständige cURL-Anforderung mit Authentifizierung, Antwortschema und SDK-Beispielen für mehrere Sprachen."
ArticleTitle: "MinRow aus Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API-Referenz"
---

Diese REST-API gibt den minimalen Zeilenindex in einem Excel-Arbeitsblatt zurück, wenn der Parameter `cellOrMethodName` auf `minrow` gesetzt ist. Der Endpunkt kann verwendet werden, um die erste nicht leere Zeile (nullbasiert) in einem angegebenen Arbeitsblatt zu ermitteln.

- **cURL-Beispiel:**

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**Anforderung**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| Eigenschaft         | Typ    | Erforderlich | Beschreibung                                             |
|---------------------|--------|--------------|----------------------------------------------------------|
| `fileName`          | string | Ja           | Name der Arbeitsmappe (z. B. `myWorkbook.xlsx`).         |
| `sheetName`         | string | Ja           | Zielarbeitsblatt (z. B. `Sheet1`).                       |
| `cellOrMethodName`  | string | Ja           | Fester Wert `minrow`.                                     |
| `folder`            | string | Nein         | Pfad des Cloud-Speicherordners.                          |
| `storageName`       | string | Nein         | Speichername, falls ein nicht standardmäßiger Speicher verwendet wird. |

**Antwort**

Der Dienst gibt ein JSON-Objekt zurück, das die Eigenschaft `MinRow` enthält, wobei der Index der ersten nicht leeren Zeile (nullbasiert) angegeben wird.

| HTTP-Status | Bedeutung                                     |
|-------------|-----------------------------------------------|
| 200         | Erfolg – JSON-Payload mit `MinRow`.          |
| 401         | Nicht autorisiert – ungültiges oder fehlendes Token. |
| 404         | Arbeitsmappe oder Arbeitsblatt nicht gefunden. |
| 500         | Interner Serverfehler.                        |

Der Wert `MinRow` ist nützlich, wenn Sie den Startpunkt der Daten in einem Arbeitsblatt schnell ermitteln müssen.

- **Aspose.Cells Cloud SDKs verwenden**

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}