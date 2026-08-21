---
title: "MinSpalte aus Excel-Arbeitsblatt abrufen"
type: docs
url: /de/get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, MinSpalte abrufen, Arbeitsblatt, SDK, Cloud API
description: Abrufen des minimalen Spaltenindex mit Daten in einem Arbeitsblatt einer Excel-Datei über die Aspose.Cells Cloud REST API.
ArticleTitle: "MinSpalte aus Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API"
---

Diese REST API gibt den minimalen Spaltenindex zurück, der Daten in einem Excel-Arbeitsblatt enthält, wenn der Parameter `cellOrMethodName` auf `mincolumn` gesetzt ist.

- **cURL-Beispiel**

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <IHR_ZUGRIFFSTOKEN>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**Details zur Anforderung**

| Parameter | Typ | Erforderlich | Beschreibung |
|-----------|------|----------|-------------|
| `cellOrMethodName` | string | Ja | Fester Wert `mincolumn`, um die Operation anzugeben. |
| `folder` | string | Nein | Pfad zum Ordner, der die Arbeitsmappe enthält (sofern nicht das Stammverzeichnis). |
| `storageName` | string | Nein | Name des zu verwendenden Aspose Cloud-Speichers. |

**Details zur Antwort**

Die API gibt ein JSON-Objekt mit einer einzigen Eigenschaft zurück:

```json
{
  "MinColumn": integer   // Nullbasierter Index der am weitesten links stehenden Spalte mit Daten.
}
```

Typische HTTP-Statuscodes:

- **200 OK** – Anforderung erfolgreich, gibt den Wert `MinColumn` zurück.  
- **401 Unauthorized** – Fehlender oder ungültiger Authentifizierungstoken.  
- **404 Not Found** – Die angegebene Arbeitsmappe, das Arbeitsblatt oder der Zellbereich ist nicht vorhanden.  
- **500 Internal Server Error** – Unerwarteter Serverfehler.

- **Verwendung der Aspose.Cells Cloud SDKs**

Die Verwendung eines SDKs ist die effizienteste Methode zur Entwicklung. Ein SDK abstrahiert die low-level-Details und ermöglicht es Ihnen, sich auf die Logik Ihres Projekts zu konzentrieren. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinColumnWorksheet-get-min-column-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "108bf3803d41abd988a29cdbd39aee44" >}}

{{< /tab >}}

{{< /tabs >}}