---
title: "Hämta MinColumn från Excel-arket"
type: docs
url: /sv/get-mincolumn-from-excel-worksheet/
weight: 100
keywords: Excel, Aspose.Cells Cloud, REST API, Hämta MinColumn, Ark, SDK, Molntjänst
description: Hämta det minsta kolumnindexet som innehåller data i ett ark i en Excel-fil via Aspose.Cells Cloud REST API.
ArticleTitle: "Hämta MinColumn från Excel-ark - Aspose.Cells Cloud API"
---

Denna REST API returnerar det minsta kolumnindexet som innehåller data i ett Excel-ark när parametern `cellOrMethodName` är inställd på `mincolumn`.

- **cURL-exempel**

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mincolumn" \
     -H "Authorization: Bearer <DIN_AKTIVERINGS_TOKEN>" \
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

**Detaljer för begäran**

| Parameter | Typ | Obligatoriskt | Beskrivning |
|-----------|-----|---------------|-------------|
| `cellOrMethodName` | sträng | Ja | Fast värde `mincolumn` för att ange åtgärden. |
| `folder` | sträng | Nej | Sökväg till mappen som innehåller arbetsboken (om det inte är rotmappen). |
| `storageName` | sträng | Nej | Namn på Aspose Cloud-lagringen som ska användas. |

**Detaljer för svar**

API:et returnerar ett JSON-objekt med en enda egenskap:

```json
{
  "MinColumn": heltal   // Nollbaserat index för den vänstraste kolumnen som innehåller data.
}
```

Typiska HTTP-statuskoder:

- **200 OK** – Lyckad begäran, returnerar värdet `MinColumn`.  
- **401 Oauktoriserad** – Saknar eller har ogiltig autentiseringstoken.  
- **404 Inte hittad** – Den angivna arbetsboken, arket eller cellintervallet finns inte.  
- **500 Internt serverfel** – Oväntat serverfel.

- **Använd Aspose.Cells Cloud SDK:er**

Att använda en SDK är det mest effektiva sättet att utveckla. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på din projektlogik. Ta en titt på <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

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
---