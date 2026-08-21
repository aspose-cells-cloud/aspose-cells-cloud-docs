---
title: "Aspose.Cells Cloud API – Ermitteln des MaxDataColumn einer Excel-Arbeitsmappe (v3.0)"
type: docs
url: /de/get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, MaxDataColumn ermitteln, Excel-Arbeitsblatt, REST API, v3.0, SDK"
description: "Rufen Sie den höchsten Spaltenindex ab, der Daten in einem angegebenen Arbeitsblatt enthält, mithilfe der Aspose.Cells Cloud REST API (v3.0). Enthält Anforderungsdetails, eine Beispielantwort und SDK-Beispiele."
ArticleTitle: "Aspose.Cells Cloud API – Ermitteln des MaxDataColumn einer Excel-Arbeitsmappe (v3.0)"
---

Diese REST API gibt den höchsten Daten-Spaltenindex in einem Excel-Arbeitsblatt zurück, wenn der Parameter `cellOrMethodName` auf `maxdatacolumn` gesetzt ist.

## **cURL-Beispiel**

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatacolumn" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataColumn": 12
}
```

{{< /tab >}}

{{< /tabs >}}

**Anforderungsdetails**  
- **HTTP-Methode:** `GET`  
- **Endpunkt-Muster:** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **Pfadparameter:**  
  - `fileName` – Name der Excel-Datei (z. B. `myWorkbook.xlsx`).  
  - `sheetName` – Name des Arbeitsblatts (z. B. `Sheet1`).  
- **Header:**  
  - `Authorization: Bearer <access_token>` (erforderlich)  
  - `Accept: application/json` (empfohlen)  

**Parameter**

| Parameter | Ort     | Typ    | Erforderlich | Beschreibung |
|-----------|---------|--------|--------------|--------------|
| `fileName` | Pfad    | string | Ja           | Der Name der Excel-Datei, die im Cloud-Speicher gespeichert ist. |
| `sheetName` | Pfad  | string | Ja           | Das Arbeitsblatt, aus dem der höchste Daten-Spaltenindex abgerufen werden soll. |
| `cellOrMethodName` | Pfad | string | Ja | Muss auf `maxdatacolumn` gesetzt werden, um diesen Vorgang auszulösen. |

**Antworten**

| Statuscode | Beschreibung                                      | Beispiel-Payload |
|------------|---------------------------------------------------|------------------|
| 200        | Erfolg – gibt den höchsten Daten-Spaltenindex zurück. | `{ "MaxDataColumn": 12 }` |
| 401        | Nicht autorisiert – ungültiges oder fehlendes Zugriffstoken. | `{ "error": "Invalid authentication." }` |
| 404        | Nicht gefunden – Datei oder Arbeitsblatt existiert nicht. | `{ "error": "Resource not found." }` |
| 500        | Interner Serverfehler – unerwarteter Zustand.     | `{ "error": "Server error." }` |

**Fehlerbehandlung**  
Falls die Anforderung fehlschlägt, überprüfen Sie den HTTP-Statuscode sowie die `error`-Nachricht im Antworttext. Stellen Sie sicher, dass das Zugriffstoken gültig ist und die angegebene Datei sowie das Arbeitsblatt in Ihrem Aspose Cloud-Speicher vorhanden sind.

- **Verwenden Sie Aspose.Cells Cloud SDKs**

Die Verwendung eines SDKs ist der effizienteste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxDataColumnWorksheet-get-max-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "126f68818f671a2f6087ee334726c454" >}}

{{< /tab >}}

{{< /tabs >}}