---
title: "Ta bort ett diagram från ett kalkylblad"
type: docs
url: /sv/charts/delete/
aliases: [  /sv/delete-a-chart-from-a-worksheet/ ]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Ta bort diagram"
  - "Kalkylblad"
  - "Excel"
  - "Cloud SDK"
  - "Diagramborttagning"
  - "API-referens"
description: "Tar bort ett diagram från ett kalkylblad med hjälp av dess nollbaserade index via Aspose.Cells Cloud REST API."
ArticleTitle: "Ta bort ett diagram från ett kalkylblad med Aspose.Cells Cloud REST API"
---

Denna REST API tar bort ett diagram från ett kalkylblad med hjälp av dess index.

Se **[Lägg till ett diagram](#)** och **[Hämta diagram](#)** för relaterade åtgärder.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Begärandeparametrar

| Parameternamn | Typ    | Plats  | Beskrivning                                     |
| ------------- | ------ | ------ | ----------------------------------------------- |
| name          | string | path   | Namnet på arbetsboken.                          |
| sheetName     | string | path   | Namnet på kalkylbladet.                         |
| chartIndex    | integer | path  | Det nollbaserade indexet för diagrammet som ska tas bort. |
| folder        | string | query  | Mappen som innehåller arbetsboken.              |
| storageName   | string | query  | Namnet på det lagringsutrymme som ska användas. |


### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PutWorksheetAddChart API med SDK:er

### PutWorksheetAddChart API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
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

API:et returnerar följande statuskoder:

| Kod | Beskrivning                                 |
|-----|---------------------------------------------|
| 200 | Diagrammet togs bort framgångsrikt          |
| 400 | Felaktig begäran (t.ex. ogiltigt index)     |
| 401 | Inte auktoriserad (saknad eller ogiltig JWT)|
| 404 | Arbetsbok, kalkylblad eller diagram hittades inte |
| 500 | Serverfel                                   |

**Felhantering:** För detaljerad felinformation, se den generella felmodellen i OpenAPI-specifikationen.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}