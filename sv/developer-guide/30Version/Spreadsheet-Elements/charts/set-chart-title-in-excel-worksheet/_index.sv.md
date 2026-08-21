---
title: "Aspose.Cells Cloud API – Ställ in diagramrubrik i ett Excel-ark"
type: docs
url: /sv/chart/title/add/
aliases: [  /sv/set-chart-title-in-excel-worksheet/ ]
weight: 30
keywords: "Aspose.Cells Cloud, API för diagramrubrik, Excel-diagramrubrik, REST API, SDK-exempel"
description: "Lär dig hur du lägger till eller uppdaterar en diagramrubrik i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller cURL-kod, SDK-exempel, nödvändiga parametrar, autentiseringssteg och felhantering."
---

Lägger till en diagramrubrik eller gör en befintlig rubrik synlig.

## PutWorksheetChartTitle API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärningsparametrar

| Parameter_name   | Typ    | Plats | Beskrivning                        |
| ---------------- | ------ | ----- | ---------------------------------- |
| name             | string | path  | Arbetsboksnamn.                    |
| sheetName        | string | path  | Arknamn.                           |
| chartIndex       | integer| path  | Index för diagrammet.              |
| title            | string | body  | Text för diagramrubriken.          |
| folder           | string | query | Mapp som innehåller arbetsboken.   |
| storageName      | string | query | Namn på lagringsutrymmet.          |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartTitle) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör en anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
  -d '{"Text":"Sales Chart"}' \
  -X PUT \
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

**Felaktiga svar (error responses)**

| HTTP-kod | Exempelpayload                                                                       | Beskrivning                                             |
| -------- | ------------------------------------------------------------------------------------ | ------------------------------------------------------- |
| 400      | `{ "Code": "400", "Message": "Invalid request payload." }`                          | Begäran har felaktigt format eller saknar nödvändiga fält. |
| 401      | `{ "Code": "401", "Message": "Authentication failed. Invalid or expired JWT token." }`| Bearer-token saknas, är ogiltig eller har löpt ut.      |
| 404      | `{ "Code": "404", "Message": "Workbook, worksheet, or chart not found." }`           | Den angivna resursen finns inte.                        |
| 500      | `{ "Code": "500", "Message": "Internal server error." }`                             | Ett oväntat fel inträffade på servern.                  |

## SDK-familj för molnet

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-SetChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-add_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetChartTitle.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-SetChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-SetChartTitle-set-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-SetChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "728d523e11f8751f5f601bafb04ab86f" >}}

{{< /tab >}}

{{< /tabs >}}