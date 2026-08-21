---
title: "Ermitteln der MaxRow aus einem Excel-Arbeitsblatt"
type: docs
url: /de/get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "Höchste Zeilennummer in einem Excel-Arbeitsblatt abrufen – Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel, MaxRow, REST API, Cloud SDK, Tabellenkalkulation, Arbeitsblatt, GetMaxRow"
description: "Erfahren Sie, wie Sie die höchste Zeilennummer eines Arbeitsblatts in einer Excel-Datei mithilfe der Aspose.Cells Cloud REST API abrufen. Enthält Anforderungssyntax, Antwortschema, SDK-Beispiele und Nutzungshinweise."
---

Diese REST-API gibt die **höchste Zeilennummer** in einem Excel-Arbeitsblatt zurück, wenn der Parameter `cellOrMethodName` auf `maxrow` gesetzt ist.

- **cURL-Beispiel**

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Verwenden der Aspose.Cells Cloud SDKs**

Die Verwendung eines SDKs ist die effizienteste Methode zur Beschleunigung der Entwicklung. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf die Logik Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**API-Referenz**

| Element | Details |
|--------|---------|
| **Methode** | `GET` |
| **Endpunkt** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **Pfadparameter** | `fileName` – Name der Excel-Datei (erforderlich) <br> `sheetName` – Name des Arbeitsblatts (erforderlich) |
| **Abfrageparameter** | `folder` – Pfad zum Ordner im Speicher (optional) <br> `storageName` – Name des Speichers (optional) |
| **Erfolgsantwort** | `200 OK` <br> ```json { "MaxRow": Ganzzahl } ``` |
| **Fehlerantworten** | `400 Bad Request` – ungültige Parameter <br> `401 Unauthorized` – Authentifizierungsfehler <br> `404 Not Found` – Datei oder Arbeitsblatt nicht gefunden |

**Voraussetzungen**

- Ein gültiges Aspose Cloud Authentifizierungstoken.  
- Die Zielarbeitsmappe muss in den Aspose Cloud-Speicher hochgeladen oder über eine öffentliche URL erreichbar sein.  

**Hinweise**

- Der Vorgang ist ab API-Version **v3.0** verfügbar.  
- Der zurückgegebene `MaxRow`-Wert entspricht dem höchsten verwendeten Zeilenindex (1-basiert). Bei einem leeren Arbeitsblatt beträgt der Wert typischerweise `1`.  

Die folgenden SDK-Beispiele veranschaulichen den Aufruf des Vorgangs in verschiedenen Programmiersprachen.