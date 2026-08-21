---
title: "Get MinDataColumn – Aspose.Cells Cloud API Referenz (v3.0)"
type: docs
url: /get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, Excel-Arbeitsblatt, REST-API, API-Referenz, v3.0, Datenspalte, Cloud-API"
description: "Rufen Sie die am weitesten links liegende Spalte ab, die Daten in einem Excel-Arbeitsblatt enthält, über die Aspose.Cells Cloud REST-API (v3.0). Enthält Authentifizierungsdetails, Anforderungssyntax, JSON-Antwortbeispiel, Fehlercodes und SDK-Snippets."
ArticleTitle: "Get MinDataColumn – Aspose.Cells Cloud API Referenz (v3.0)"
---

Der **`mindatacolumn`**-Endpunkt gibt den nullbasierten Index der am weitesten links liegenden Spalte zurück, die mindestens eine Zellendaten enthält, in einem angegebenen Arbeitsblatt.  
Mit anderen Worten: Er gibt an, welche Spalte die erste ist, die tatsächlich Daten enthält.

> **Definition** – `mindatacolumn`: Der Index (beginnend bei 0) der ersten Spalte, die Daten im Arbeitsblatt enthält.

**Voraussetzungen**  
- Ein gültiges OAuth2-Zugriffstoken ist erforderlich.  
- Die Excel-Datei muss in den Aspose-Cloud-Speicher hochgeladen worden sein.

**Anforderungsparameter**

| Parameter                    | Typ    | Erforderlich | Beschreibung                                           |
|------------------------------|--------|--------------|--------------------------------------------------------|
| `fileName`                   | string | Ja           | Name der Excel-Datei im Cloud-Speicher.               |
| `sheetName`                  | string | Ja           | Name des Arbeitsblatts, aus dem der Spaltenindex abgerufen werden soll. |
| `Authorization` (Header)     | string | Ja           | Bearer-Token zur OAuth2-Authentifizierung.             |

- **cURL-Beispiel**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                             |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | Filter wurde erfolgreich angewendet; Antwort enthält Details zur Operation. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                    |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.   |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                               |
---

- Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf die Logik Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}
---