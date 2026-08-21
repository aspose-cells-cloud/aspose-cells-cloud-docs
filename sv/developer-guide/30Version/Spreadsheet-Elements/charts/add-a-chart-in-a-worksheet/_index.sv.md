---
title: "Lägg till ett diagram i ett kalkylblad"
type: docs
url: /charts/add/
aliases: [/add-a-chart-in-a-worksheet/]
weight: 20
description: "Lär dig hur du lägger till ett diagram i ett Excel-kalkylblad med Aspose.Cells Cloud API v3.0. Inkluderar slutpunkt, parametrar, cURL-exempel och SDK-utdrag."
keywords:
  - "lägg till diagram Aspose.Cells"
  - "Aspose.Cells lägg till diagram API"
  - "diagram API REST"
  - "Aspose.Cells SDK-exempel"
ArticleTitle: "Lägg till ett diagram i ett kalkylblad – Aspose.Cells Cloud API-guide"
---

Denna REST API lägger till ett nytt diagram i ett kalkylblad.

**Förutsättningar**  
Innan du anropar denna åtgärd, skaffa ett giltigt JWT-åtkomsttoken och se till att målarbokshändelsedokumentet lagras i den angivna mappen eller lagringsplatsen.

## PutWorksheetAddChart API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parameter Namn          | Typ     | Plats   | Beskrivning                                                                                                                                                                               |
| ----------------------- | ------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                | string  | path    | Arbetsbokens namn.                                                                                                                                                                        |
| **sheetName**           | string  | path    | Kalkylbladets namn.                                                                                                                                                                       |
| **chartType**           | string  | query   | Diagramtyp (se egenskapen **Type** i diagramresursen). Stödda diagramtyper inkluderar **Bar**, **Column**, **Line**, **Pie**, **Scatter**, **Area**, **Doughnut**, **Radar**, etc.      |
| **upperLeftRow**        | integer | query   | Övre vänstra radindex för diagramområdet (0-baserat).                                                                                                                                     |
| **upperLeftColumn**     | integer | query   | Övre vänstra kolumnindex för diagramområdet (0-baserat).                                                                                                                                  |
| **lowerRightRow**       | integer | query   | Nedre högra radindex för diagramområdet (0-baserat).                                                                                                                                      |
| **lowerRightColumn**    | integer | query   | Nedre högra kolumnindex för diagramområdet (0-baserat).                                                                                                                                   |
| **area**                | string  | query   | Omfattning som innehåller värdena att plotta (t.ex. `A1:B5`).                                                                                                                             |
| **isVertical**          | boolean | query   | Anger om diagrammets orientering är vertikal.                                                                                                                                             |
| **categoryData**        | string  | query   | Omfattning för kategori-axelvärden (t.ex. `D1:E10`).                                                                                                                                      |
| **isAutoGetSerialName** | boolean | query   | Om **true**, genereras serienamn automatiskt.                                                                                                                                             |
| **title**               | string  | query   | Diagrammets rubrik.                                                                                                                                                                       |
| **folder**              | string  | query   | Mappen som innehåller arbetsboken.                                                                                                                                                        |
| **storageName**         | string  | query   | Namnet på lagringsplatsen.                                                                                                                                                                |
| **dataLabels**          | boolean | query   | Visa dataetiketter när **true**.                                                                                                                                                         |
| **dataLabelsPosition**  | string  | query   | Position för dataetiketter (t.ex. `Above`).                                                                                                                                              |
| **pivotTableSheet**     | string  | query   | Namn på kalkylbladet som innehåller pivotdiagrammet.                                                                                                                                      |
| **pivotTableName**      | string  | query   | Namn på pivotdiagrammet.                                                                                                                                                                  |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                 |
|-----|-----------------------------|------------------------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer.     |
| 400 | Bad Request                 | Saknas eller ogiltiga parametrar (t.ex. filtyp som inte stöds).             |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                                             |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.                           |
| 500 | Internal Server Error       | Oväntat serverfel.                                                          |

## Hur du använder PutWorksheetAddChart API med SDK:er

### PutWorksheetAddChart API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetAddChart) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts?chartType=Bar&area=B1:F2&title=SalesState" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
# Ingen begäranbråk krävs för denna åtgärd
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projekttal. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Perl" tabName9="Android" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-AddChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-AddChart-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetAddChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_new_chart_to_worksheet-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddChartToWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-AddChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-AddChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-chart-AddChart-AddChart.jave" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "7fa79c30fca0c594c18c0f3937b6bcc9" >}}

{{< /tab >}}

{{< /tabs >}}
---