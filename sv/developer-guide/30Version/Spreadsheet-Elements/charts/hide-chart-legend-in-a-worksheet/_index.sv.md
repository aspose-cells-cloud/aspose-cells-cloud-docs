---
title: "Dölj diagramlegend i ett Excel-ark – Aspose.Cells Cloud API"
type: docs
url: /sv/charts/legend/hide/
aliases: [/sv/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, dölj diagramlegend, REST API, molntjänst, diagramlegend"
description: "Lär dig hur du döljer en diagramlegend i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller HTTPS-slutpunkt, nödvändig autentisering, begäran syntax, svarsinformation, felhantering och SDK-exempel."
---

Denna REST API döljer legenden i ett diagram. En **diagramlegend** är den ruta som identifierar de dataserier som har ritats upp i diagrammet.

API:et kräver ett giltigt Aspose Cloud JWT-token, arbetsboken måste laddas upp till Aspose Cloud-lagring och den använda API-versionen är **v3.0**.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### Begäran parametrar

| Parameter Name  | Typ     | Plats  | Beskrivning                    |
| --------------- | ------- | ------ | ------------------------------ |
| **name**        | string  | path   | Namn på arbetsboken.           |
| **sheetName**   | string  | path   | Namn på arket.                 |
| **chartIndex**  | integer | path   | Index för diagrammet.          |
| **folder**      | string  | query  | Mapp för arbetsboken (valfritt). |
| **storageName** | string  | query  | Lagringsnamn (valfritt).       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) definierar detta offentligt tillgängliga programmeringsgränssnitt.

Du kan använda kommandoradsverktyget cURL för att enkelt anropa API:et. Exemplet nedan visar en begäran som döljer legenden för diagram 0 i _Sample_Test_Book.xls_.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
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

## Svar

| HTTP-status                   | Beskrivning                                       | Exempel JSON                                                  |
| ----------------------------- | ------------------------------------------------- | ------------------------------------------------------------- |
| **200 OK**                    | Legend har doltts framgångsrikt.                  | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | Saknas eller ogiltigt JWT-token.                 | `{ "Code": 401, "Message": "Invalid access token." }`         |
| **404 Not Found**             | Arbetsbok, ark eller diagram finns inte.         | `{ "Code": 404, "Message": "Chart not found." }`              |
| **500 Internal Server Error** | Oväntat serverfel.                               | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## Vanliga frågor

**Fråga:** _Hur döljer jag en diagramlegend med Aspose.Cells Cloud?_  
**Svar:** Skicka en `DELETE`-begäran till `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` med ett giltigt JWT-token i `Authorization`-huvudet. Ett `200 OK`-svar indikerar framgång.

**Fråga:** _Vilken autentisering krävs för API:et för att dölja diagramlegend?_  
**Svar:** Inkludera ett `Authorization: Bearer <jwt token>`-huvud. Skaffa token via Aspose Cloud OAuth-flödet.

**Fråga:** _Vilket fel svar får jag om diagramindexet är ogiltigt?_  
**Svar:** Tjänsten returnerar `404 Not Found` med ett JSON-svar som innehåller `Code: 404` och ett meddelande som beskriver det saknade diagrammet.

**Fråga:** _Kan jag använda HTTP istället för HTTPS?_  
**Svar:** Nej. Alla Aspose Cloud-slutpunkter kräver HTTPS för säkerhet.

## Molntjänst SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**Kommer snart** – Exempel på Swift SDK kommer att läggas till inom kort.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Dölj diagramlegend i ett Excel-ark – Aspose.Cells Cloud API",
  "description": "Steg-för-steg-guide för att dölja en diagramlegend i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller HTTPS-slutpunkt, autentisering, begäran syntax, svarsinformation, felhantering och SDK-exempel.",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "Hem", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Diagram", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "Dölj diagramlegend", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "Dölj diagramlegend med Aspose.Cells Cloud API"
}
</script>