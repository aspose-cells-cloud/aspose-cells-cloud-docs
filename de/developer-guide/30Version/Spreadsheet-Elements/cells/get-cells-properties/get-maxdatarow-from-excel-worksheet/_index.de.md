---
title: "MaxDataRow aus Excel-Arbeitsblatt abrufen"
type: docs
url: /get-maxdatarow-from-excel-worksheet/
weight: 50
keywords: "Excel, Aspose.Cells Cloud, REST-API, MaxDataRow abrufen, Arbeitsblatt"
description: "Ruft den Index der letzten Zeile ab, die Daten in einem angegebenen Arbeitsblatt einer Excel-Arbeitsmappe enthält, mithilfe der Aspose.Cells Cloud REST-API."
ArticleTitle: "Aspose.Cells Cloud API – MaxDataRow aus Excel-Arbeitsblatt abrufen"
---

Diese REST-API gibt den maximalen Datenzeilenindex in einer Excel-Datei zurück, wenn der Parameter `cellOrMethodName` auf `maxdatarow` gesetzt ist.

- **cURL-Beispiel**

{{< tabs tabTotal="2" tabID="11" tabName11="Anfrage" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatarow" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

*Hinweis: Die Anfrage muss über **HTTPS** gesendet werden und einen gültigen OAuth2-Bearer-Token enthalten.*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataRow": 57
}
```

**Mögliche HTTP-Statuscodes**

| Code | Beschreibung |
|------|-------------|
| 200 | Erfolg – gibt den Index der letzten Datenzeile zurück. |
| 401 | Nicht autorisiert – ungültiger oder fehlender Authentifizierungstoken. |
| 403 | Verboten – unzureichende Berechtigungen für den Zugriff auf die Arbeitsmappe. |
| 404 | Nicht gefunden – angegebene Arbeitsmappe oder Arbeitsblatt existiert nicht. |
| 500 | Interner Serverfehler – unerwarteter Serverzustand. |

{{< /tab >}}

{{< /tabs >}}


- **Verwenden der Aspose.Cells Cloud SDKs**

Die Verwendung eines SDKs ist die effizienteste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataRowWorksheet-get-max-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7b834250a25feb5b8a30500cf62cf7a9" >}}

{{< /tab >}}

{{< /tabs >}}

**Siehe auch**

- <a href="https://docs.aspose.cloud/cells/get-maxrow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">MaxRow aus Excel-Arbeitsblatt abrufen</a>  
- <a href="https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">MaxColumn aus Excel-Arbeitsblatt abrufen</a>  
- <a href="https://docs.aspose.cloud/cells/get-mindatarow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">MinDataRow aus Excel-Arbeitsblatt abrufen</a>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Aspose.Cells Cloud Get MaxDataRow",
  "description": "Gibt den Index der letzten Zeile zurück, die Daten in einem angegebenen Arbeitsblatt enthält.",
  "url": "https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatarow",
  "method": "GET",
  "documentation": "https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/",
  "input": [
    {
      "name": "fileName",
      "valueRequired": true,
      "description": "Der Name der Excel-Arbeitsmappe."
    },
    {
      "name": "sheetName",
      "valueRequired": true,
      "description": "Der Name des Arbeitsblatts."
    }
  ],
  "output": {
    "@type": "DataType",
    "name": "MaxDataRow",
    "description": "Nullbasierter Index der letzten Zeile, die Daten enthält."
  }
}
</script>

*Zuletzt aktualisiert: 2026-07-30*