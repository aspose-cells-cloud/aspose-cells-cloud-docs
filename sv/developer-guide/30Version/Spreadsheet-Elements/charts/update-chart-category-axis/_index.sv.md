---
title: "Uppdatera diagrammets kategoriaxel"
type: docs
url: /sv/charts/category-axis/update/
weight: 160
keywords: "Aspose.Cells, diagram, kategoriaxel, REST API, Excel, molntjänst SDK"
description: "Uppdaterar kategoriaxeln i ett diagram i ett Excel-ark med Aspose.Cells Cloud REST API."
ArticleTitle: "Uppdatera diagrammets kategoriaxel – Aspose.Cells Cloud API"
---

Denna REST API uppdaterar ett diagrams kategoriaxel.

## PostChartCategoryAxis API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parametername    | Typ    | Plats  | Beskrivning |
| ---------------- | ------ | ------ | ----------- |
| name             | string | path   | Namn på Excel-filen. |
| sheetName        | string | path   | Namn på det kalkylblad som innehåller diagrammet. |
| chartIndex       | integer | path  | Nollbaserat index för det diagram som ska uppdateras. |
| axis             | object | body   | JSON-objekt som definierar egenskaperna för kategoriaxeln. |
| folder           | string | query  | Mapp i molnlagring där filen finns (valfritt). |
| storageName      | string | query  | Namn på lagringsutrymmet (valfritt). |

**Schemat för begärandetexten – `axis`-objektet**

| Egenskap                | Typ      | Beskrivning |
|-------------------------|----------|-------------|
| IsAutomaticMajorUnit    | boolean  | Bestämmer om huvudenheten beräknas automatiskt. |
| MajorUnit               | number   | Värdet för huvudenheten när `IsAutomaticMajorUnit` är `false`. |
| IsAutomaticMinorUnit    | boolean  | Bestämmer om minnenheten beräknas automatiskt. |
| MinorUnit               | number   | Värdet för minnenheten när `IsAutomaticMinorUnit` är `false`. |
| Title                   | object   | Titelinställningar för axeln (t.ex. `Text`, `Font`, `Visible`). |
| TickLabelPosition       | string   | Position för ticketiketterna (t.ex. `Low`, `High`, `NextToAxis`). |
| ...                     | ...      | Ytterligare axelegenskaper enligt API-specifikationen. |

**HTTP-statuskoder**

| Kod  | Betydelse                 | Beskrivning |
|------|---------------------------|-------------|
| 200  | OK                        | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Oautentiserad             | Ogiltig eller saknad JWT-token. |
| 413  | För stor nyttolast        | Den uppladdade filen överskrider storleksgränsen. |
| 500  | Internt serverfel         | Oväntat serverfel. |

**Förutsättningar / Autentisering**

För att anropa denna slutpunkt måste du skaffa en JWT-åtkomsttoken från Aspose.Cells Cloud-autentiseringstjänsten (`/connect/token`). Inkludera token i `Authorization`-headern enligt exemplet nedan.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/categoryaxis?folder={folder}&storageName={storageName}" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "axis": {
          "IsAutomaticMajorUnit": true,
          "IsAutomaticMinorUnit": true,
          "Title": {
            "Text": "Kategoriaxel",
            "Visible": true
          }
        }
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Exempelsvar**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/PostChartCategoryAxis) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Anteckningar

* Slutpunkten kräver HTTPS; användning av HTTP kan orsaka varningar om blandat innehåll i webbläsare.
* Alla platshållarvärden (`{name}`, `{sheetName}`, `{chartIndex}`, `{folder}`, `{storageName}`) måste ersättas med faktiska identifierare.
* Diagramtyper som stöds för uppdatering av kategoriaxel anges i API-referensen.

## Molntjänst SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med diverse SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Post-ChartCategoryAxis.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< /tab >}}

{{< /tabs >}}
---