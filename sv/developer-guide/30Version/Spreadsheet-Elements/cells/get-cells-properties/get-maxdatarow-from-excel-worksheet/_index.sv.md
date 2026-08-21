---
title: "Hämta MaxDataRow från Excel-arbetsblad"
type: docs
url: /sv/get-maxdatarow-from-excel-worksheet/
weight: 50
keywords: "Excel, Aspose.Cells Cloud, REST API, Get MaxDataRow, Worksheet"
description: "Hämtar indexet för den sista raden som innehåller data i ett angivet arbetsblad i en Excel-arbetsbok med hjälp av Aspose.Cells Cloud REST API."
ArticleTitle: "Aspose.Cells Cloud API – Get MaxDataRow from Excel Worksheet"
---

Denna REST API returnerar indexet för den sista raden som innehåller data i en Excel-fil när parametern `cellOrMethodName` är inställd på `maxdatarow`.

- **cURL-exempel**

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxdatarow" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

*Obs! Begäran måste skickas över **HTTPS** och innehålla en giltig OAuth2-bärartoken.*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxDataRow": 57
}
```

**Möjliga HTTP-statuskoder**

| Kod | Beskrivning |
|------|-------------|
| 200 | Lyckades – returnerar indexet för den sista data raden. |
| 401 | Auktorisering misslyckades – ogiltig eller saknad auktorisationstoken. |
| 403 | Åtkomst nekad – otillräckliga behörigheter för att komma åt arbetsboken. |
| 404 | Hittades inte – den angivna arbetsboken eller arbetsbladet finns inte. |
| 500 | Internt serverfel – oväntat serverfel. |

{{< /tab >}}

{{< /tabs >}}


- **Använd Aspose.Cells Cloud SDK:er**

Att använda ett SDK är det mest effektiva sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå, så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

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

**Se också**

- <a href="https://docs.aspose.cloud/cells/get-maxrow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">Get MaxRow from Excel Worksheet</a>  
- <a href="https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">Get MaxColumn from Excel Worksheet</a>  
- <a href="https://docs.aspose.cloud/cells/get-mindatarow-from-excel-worksheet/" target="_blank" rel="noopener noreferrer">Get MinDataRow from Excel Worksheet</a>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Aspose.Cells Cloud Get MaxDataRow",
  "description": "Returnerar indexet för den sista rad som innehåller data i ett angivet arbetsblad.",
  "url": "https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/maxdatarow",
  "method": "GET",
  "documentation": "https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/",
  "input": [
    {
      "name": "fileName",
      "valueRequired": true,
      "description": "Namnet på Excel-arbetsboken."
    },
    {
      "name": "sheetName",
      "valueRequired": true,
      "description": "Namnet på arbetsbladet."
    }
  ],
  "output": {
    "@type": "DataType",
    "name": "MaxDataRow",
    "description": "Nollbaserat index för den sista rad som innehåller data."
  }
}
</script>

*Senast uppdaterad: 2026-07-30*