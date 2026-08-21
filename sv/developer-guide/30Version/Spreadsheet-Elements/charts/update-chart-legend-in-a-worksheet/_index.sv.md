---
title: "Uppdatera diagramlegend i ett kalkylblad"
type: docs
url: /sv/charts/legend/update/
aliases: [  /sv/update-chart-legend-in-a-worksheet/ ]
weight: 160
keywords: "Aspose.Cells, moln, Excel, diagram, legend, REST API, uppdatera, kalkylblad, cURL, SDK"
description: "Hur man uppdaterar en diagramlegend i ett Excel-kalkylblad med Aspose.Cells Cloud REST API, inklusive exempel på cURL-förfrågningar och SDK-kodfragment för flera programmeringsspråk."
ArticleTitle: "Uppdatera diagramlegend i ett kalkylblad – Aspose.Cells Cloud API-guide"
---

Denna REST API uppdaterar en diagramlegend.

**Förutsättningar:** För att använda detta slutpunkt krävs ett giltigt Aspose Cloud JWT-token, och den måste finnas i ett stöds lagringsområde (standard är Aspose Cloud-lagring). Se till att arbetsbokens namn, kalkylbladsnamn och diagramindex är korrekta.

En diagramlegend visar namnen och symbolerna för dataserierna i ett diagram. Uppdatering av legenden gör det möjligt att anpassa dess utseende, till exempel teckensnittsstil, färg och skugga.

## PostWorksheetChartLegend API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Förfrågningsparametrar

| Parametername   | Typ     | Plats  | Beskrivning                                    |
|-----------------|---------|--------|------------------------------------------------|
| name            | string  | path   | Namn på arbetsboken.                           |
| sheetName       | string  | path   | Namn på kalkylbladet.                          |
| chartIndex      | integer | path   | Index för det diagram som ska ändras.          |
| legend          | object  | body   | JSON-objekt som definierar legendinställningarna. |
| folder          | string  | query  | Mapp som innehåller arbetsboken.               |
| storageName     | string  | query  | Namn på lagringsplatsen.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man anropar moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
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

## Moln-SDK-familj

Att använda en SDK accelererar utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}