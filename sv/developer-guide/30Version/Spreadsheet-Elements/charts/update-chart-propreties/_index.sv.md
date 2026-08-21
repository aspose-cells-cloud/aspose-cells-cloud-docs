---
title: "Uppdatera diagramegenskaper"
type: docs
url: /sv/charts/properties/update/
aliases: [  /sv/update-chart-properties/ ]
weight: 160
keywords: "Aspose.Cells, diagram, uppdatera, Excel, REST API, SDK"
description: "Lär dig hur du uppdaterar diagramegenskaper (typ, titel, legend etc.) i en Excel-arbetsbok med Aspose.Cells Cloud REST API (v3.0). Inkluderar slutpunkt, parametrar, cURL-exempel och SDK-utdrag för C#, Java, PHP, Ruby, Node.js, Perl och Go."
ArticleTitle: "Uppdatera diagramegenskaper – Aspose.Cells Cloud REST API"
---

Denna REST API uppdaterar diagramegenskaper.

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## PostWorksheetChart API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Begärparametrar

| Parameternamn | Typ    | Path/Query String/HTTPBody | Beskrivning                                                   |
| ------------- | ------ | -------------------------- | ------------------------------------------------------------- |
| name          | string | path                       | Namnet på Excel-filen.                                        |
| sheetName     | string | path                       | Namnet på kalkylbladet som innehåller diagrammet.             |
| chartIndex    | integer| path                       | Nollbaserat index för det diagram som ska uppdateras.          |
| chart         | object | body                       | JSON-objekt som definierar diagramegenskaperna som ska ändras.|
| folder        | string | query                      | Mappen i lagringen där filen finns.                           |
| storageName   | string | query                      | Namnet på lagringstjänsten.                                   |

### Schemat för begärandetexten

**`chart`**-objektet innehåller de egenskaper du kan ändra. Nedan finns ett typiskt JSON-exempel med flera vanligt använda fält:

```json
{
  "Title": {
    "Text": "Kvartalsvis försäljning"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **Obs:** Endast de fält du behöver ändra behöver anges. Överhoppade egenskaper behåller sina befintliga värden.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
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

## Svar

API:et returnerar ett JSON-objekt som anger åtgärdens resultat. En lyckad uppdatering ger:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Statuskoder för lyckade åtgärder**

| HTTP-status | Beskrivning |
| ----------- | ----------- |
| 200         | OK – diagramegenskaperna uppdaterades framgångsrikt. |

**Svarshuvuden**

| Header | Beskrivning |
| ------ | ----------- |
| `Content-Type` | `application/json` – anger att svarsbodyn är JSON-formaterad. |
| `X-RequestId` | Unik identifierare för begäran (användbar vid felsökning). |

Möjliga felsvar inkluderar:

| HTTP-status | Beskrivning                                     |
| ----------- | ----------------------------------------------- |
| 400         | Ogiltig begäran – ogiltiga parametrar eller body |
| 401         | Autentisering misslyckades – token saknas eller är ogiltig |
| 404         | Hittades inte – fil, kalkylblad eller diagram hittades inte |
| 500         | Internt serverfel                               |

För andra diagramrelaterade åtgärder, se relaterade ämnen såsom [Uppdatera diagramtitel](/charts/title/update/) och [Uppdatera diagramlegend](/charts/legend/update/).

## Molnsdk-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Besök <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-arkivet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}