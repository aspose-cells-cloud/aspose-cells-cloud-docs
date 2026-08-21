---
title: "Aspose.Cells Cloud API – Hämta MaxDataColumn från ett Excel-ark (v3.0)"
type: docs
url: /get-maxdatacolumn-from-excel-worksheet/
weight: 70
keywords: "Aspose.Cells Cloud, hämta MaxDataColumn, Excel-ark, REST API, v3.0, SDK"
description: "Hämta det högsta kolumnindexet som innehåller data i ett angivet ark med Aspose.Cells Cloud REST API (v3.0). Inkluderar begärandedetaljer, exempel på svar och SDK-exempel."
ArticleTitle: "Aspose.Cells Cloud API – Hämta MaxDataColumn från ett Excel-ark (v3.0)"
---

Denna REST API returnerar det maximala datakolumnindexet i ett Excel-ark när parametern `cellOrMethodName` är inställd på `maxdatacolumn`.

## **cURL-exempel**

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

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

**Begärandedetaljer**  
- **HTTP-metod:** `GET`  
- **Endpoint-mönster:** `https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatacolumn`  
- **Sökvägsparametrar:**  
  - `fileName` – Namn på Excel-filen (t.ex. `myWorkbook.xlsx`).  
  - `sheetName` – Namn på arbetsarket (t.ex. `Sheet1`).  
- **Headrar:**  
  - `Authorization: Bearer <access_token>` (obligatorisk)  
  - `Accept: application/json` (rekommenderas)  

**Parametrar**

| Parameter | Plats | Typ   | Obligatorisk | Beskrivning |
|-----------|-------|-------|--------------|-------------|
| `fileName` | Sökväg | string | Ja | Namnet på Excel-filen som lagras i molnlagringen. |
| `sheetName` | Sökväg | string | Ja | Arbetsarket vars maximala datakolumn ska hämtas. |
| `cellOrMethodName` | Sökväg | string | Ja | Måste vara inställt på `maxdatacolumn` för att aktivera denna åtgärd. |

**Svar**

| Statuskod | Beskrivning | Exempelpayload |
|-----------|-------------|----------------|
| 200 | Lyckades – returnerar indexet för maximala datakolumnen. | `{ "MaxDataColumn": 12 }` |
| 401 | Obehörig – ogiltig eller saknad åtkomsttoken. | `{ "error": "Invalid authentication." }` |
| 404 | Inte hittad – filen eller arbetsarket finns inte. | `{ "error": "Resource not found." }` |
| 500 | Internt serverfel – oväntat tillstånd. | `{ "error": "Server error." }` |

**Felhantering**  
Om begäran misslyckas, undersök HTTP-statuskoden och felmeddelandet `error` i svarsbrödet. Se till att åtkomsttoken är giltig och att den angivna filen och arbetsarket finns i din Aspose Cloud-lagring.

- **Använd Aspose.Cells Cloud SDK:n**

Att använda en SDK är det mest effektiva sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå, så att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagret</a> för en fullständig lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:n:

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