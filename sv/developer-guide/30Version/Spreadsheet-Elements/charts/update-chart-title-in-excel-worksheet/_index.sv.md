---
title: "Uppdatera diagramrubrik i Excel-ark"
type: docs
url: /sv/charts/title/update/
aliases: [  /sv/update-chart-title-in-excel-worksheet/ ]
weight: 160
keywords: Excel, Aspose.Cells, REST API, Diagramrubrik, Uppdatera, Molntjänst SDK
description: Lär dig hur du uppdaterar en diagramrubrik i ett Excel-ark med Aspose.Cells Cloud REST API, cURL och diverse SDK:er.
ArticleTitle: "Uppdatera diagramrubrik i Excel-ark – Aspose.Cells Cloud-dokumentation"
---

Denna REST API uppdaterar diagramrubriken.

**Förutsättningar:** Du måste ha ett giltigt Aspose Cloud-konto och en JWT-token för auktorisering. Typiska steg inkluderar:

- Registrera dig för ett Aspose Cloud-konto.  
- Generera en JWT-token via autentiseringsslutpunkten.  
- Se till att målarbokshanteraren är lagrad i ett stödt molnlagringssystem (standard eller anpassad).

## PostWorksheetChartTitle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

Alla API-anrop måste göras över **HTTPS** för att undvika varningar om blandat innehåll.

### **Säkerhet och auktorisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad auktorisering</a>.

### Begäranparametrar

| Parameternamn | Typ    | Plats  | Beskrivning                          |
| ------------- | ------ | ------ | ------------------------------------ |
| name          | string | path   | Arbetsbokens namn.                   |
| sheetName     | string | path   | Arkets namn.                         |
| chartIndex    | integer | path  | Nollbaserat index för diagrammet.    |
| title         | string | body  | Ny diagramrubrik.                    |
| folder        | string | query | Mappen för arbetsboken.              |
| storageName   | string | query | Lagringsnamn.                        |

### Svarsstatuskoder

| Kod | Beskrivning                                         |
| --- | --------------------------------------------------- |
| 200 | OK – Diagramrubriken uppdaterades framgångsrikt.   |
| 400 | Bad Request – Saknade eller ogiltiga parametrar.   |
| 401 | Unauthorized – Ogiltig eller saknad JWT-token.     |
| 404 | Not Found – Arbetsbok, ark eller diagram hittades inte. |
| 500 | Internal Server Error – Oväntat serverfel.         |

**Obs:** `chartIndex` är nollbaserat; det första diagrammet i ett ark refereras med `0`.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Stock exchange"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

## Molntjänst SDK-familj

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projekts uppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av diverse SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}