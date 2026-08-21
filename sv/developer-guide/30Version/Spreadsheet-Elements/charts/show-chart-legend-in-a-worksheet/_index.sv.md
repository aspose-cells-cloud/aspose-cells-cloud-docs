---
title: "Visa diagrammetikett i ett kalkylblad"
type: docs
url: /charts/legend/show/
aliases: [/show-chart-legend-in-a-worksheet/]
weight: 100
keywords: "Aspose.Cells Cloud, diagrammetikett-API, Excel-diagrammetikett, REST PUT för diagrammetikett, Aspose API v3.0"
description: "Lär dig hur du visar en diagrammetikett i ett Excel-kalkylblad med Aspose.Cells Cloud REST API (v3.0). Innehåller detaljerad endpointinformation, parametrar, ett cURL-exempel och SDK-utdrag."
---

Denna REST API gör det möjligt att visa **legenden** – den förklarande rutan som identifierar dataserierna – i ett diagram som finns i ett kalkylblad i en Excel-arbetsbok.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Begärparametrar

| Parameternamn   | Typ     | Plats  | Beskrivning                                     |
| --------------- | ------- | ------ | ----------------------------------------------- |
| name            | string  | path   | Arbetsbokens filnamn.                           |
| sheetName       | string  | path   | Kalkylbladets namn som innehåller diagrammet.   |
| chartIndex      | integer | path   | Det nollbaserade indexet för diagrammet.        |
| folder          | string  | query  | Mappen som innehåller arbetsboken.              |
| storageName     | string  | query  | Namnet på lagringstjänsten.                     |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Autentisering sker med ett Bearer JWT-token som anges i **Authorization**-huvudet.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anropet med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
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

API:t kan returnera följande HTTP-statuskoder:

- **200 OK** – Legendet visades framgångsrikt.
- **400 Bad Request** – Ogiltiga parametrar.
- **401 Unauthorized** – Autentisering misslyckades.
- **404 Not Found** – Den angivna arbetsboken, kalkylbladet eller diagrammet finns inte.
- **500 Internal Server Error** – Ett oväntat serverfel uppstod.

{{< /tab >}}

{{< /tabs >}}

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Besök [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:n:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}