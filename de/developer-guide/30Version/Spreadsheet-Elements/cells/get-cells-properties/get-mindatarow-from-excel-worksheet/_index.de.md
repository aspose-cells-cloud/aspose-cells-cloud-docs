---
title: "MinDataRow aus Excel-Arbeitsblatt abrufen"
type: docs
url: /de/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel-API, Cloud SDK"
description: "Abrufen des Index der ersten Datenzeile eines Arbeitsblatts mithilfe der Aspose.Cells Cloud API v3.0. Enthält Anforderungsmuster, Parameter, Beispiel-cURL, Antwortbeispiel, HTTP-Statuscodes und SDK-Snippets."
ArticleTitle: "MinDataRow aus Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API"
---

Der Endpunkt **Get MinDataRow** der **Aspose.Cells Cloud API v3.0** gibt den Index der ersten Zeile zurück, die Daten in einem angegebenen Arbeitsblatt enthält. Der Vorgang erfordert ein gültiges Zugriffstoken (Bearer-Authentifizierung) und den Abfrageparameter `cellOrMethodName` mit dem Wert `mindatarow`.

**API-Version: 3.0**

### cURL-Beispiel

Die Anfrage verwendet die HTTP-Methode GET. Ersetzen Sie die Platzhalter `{fileName}` und `{sheetName}` durch den tatsächlichen Namen der Arbeitsmappe und des Arbeitsblatts.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Anforderungsparameter**

| Parameter          | Ort    | Typ    | Erforderlich | Beschreibung                                                   |
|--------------------|--------|--------|--------------|----------------------------------------------------------------|
| `fileName`         | Pfad   | string | Ja           | Name der Excel-Arbeitsmappe (einschließlich Dateierweiterung). |
| `sheetName`        | Pfad   | string | Ja           | Name des Arbeitsblatts innerhalb der Arbeitsmappe.             |
| `cellOrMethodName` | Abfrage| string | Ja           | Muss auf `mindatarow` gesetzt werden, um diesen Vorgang auszulösen. |

**Antwortbeispiel**

```json
{
  "MinDataRow": 5
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                    |
|------|-----------------------------|-----------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                           |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.          |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                      |

### SDK-Beispiele

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Logik Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**Siehe auch**

- [Get MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [Get MinColumn](https://docs.aspose.cloud/cells/get-mincolumn-from-excel-worksheet/)
- [Get MaxColumn](https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/)