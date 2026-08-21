---
title: "Ta bort diagramtitel i ett kalkylblad"
type: docs
url: /sv/charts/delete-chart-title/
aliases: [  /sv/delete-chart-title-in-a-worksheet/ ]
weight: 150
keywords: "Aspose.Cells, molntjänst, ta bort diagramtitel, Excel, REST, SDK"
description: "Lär dig hur du tar bort en diagramtitel från ett Excel-kalkylblad med Aspose.Cells Cloud REST API (v4.0). Inkluderar cURL- och SDK-exempel samt felhantering."
---

Denna REST API tar bort titeln för ett diagram.

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Begärandeparametrar

| Parametername   | Typ    | Plats  | Beskrivning                              |
|-----------------|--------|--------|------------------------------------------|
| name            | string | path   | Namnet på arbetsbokens fil.              |
| sheetName       | string | path   | Namnet på kalkylbladet.                  |
| chartIndex      | integer| path   | Det nollbaserade indexet för diagrammet. |
| folder          | string | query  | Mappen som innehåller arbetsboken.       |
| storageName     | string | query  | Lagringsnamnet.                          |


### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller detaljer om åtgärden. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
## Hur du använder DeleteWorksheetChartTitle API med SDK:er

### DeleteWorksheetChartTitle API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartTitle) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Exemplet nedan visar hur man gör anropet, inklusive den nödvändiga **Bearer JWT**-token för autentisering.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_title_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3898d60ea8f7ea7bb460ffb5d7d29504" >}}

{{< /tab >}}

{{< /tabs >}}