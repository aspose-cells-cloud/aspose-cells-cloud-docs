---
title: "Lägg till ett pivotfält i en pivottabell"
second_title: "Dokument"
linktitle: "Lägg till pivotfält"
type: docs
url: /sv/pivot-tables/add-pivot-field/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, pivottabell, lägg till pivotfält, REST API, SDK"
description: "Lägg till ett pivotfält i en befintlig pivottabell med Aspose.Cells Cloud REST API. Inkluderar begärandedetaljer, cURL-exempel och SDK-utdrag."
weight: 40
ArticleTitle: "Lägg till ett pivotfält i en pivottabell – Aspose.Cells Cloud-dokumentation"
---

Denna REST API **lägger till** ett pivotfält i en befintlig pivottabell.

> **Förutsättning:** För att anropa denna slutpunkt måste du inkludera en giltig JWT-autentiseringstoken i `Authorization`-headern och se till att arbetsboken är lagrad i den angivna mappen eller standardlagringen.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### Begärparametrar

| Parameternamn   | Typ     | Plats  | Beskrivning                                                         |
| --------------- | ------- | ------ | ------------------------------------------------------------------- |
| name            | string  | path   | Dokumentets namn.                                                   |
| sheetName       | string  | path   | Arbetsbladets namn.                                                 |
| pivotTableIndex | integer | path   | Index för pivottabellen.                                            |
| pivotFieldType  | string  | query  | Typ av fältemne (t.ex. Row, Column).                                |
| request         | object  | body   | DTO som innehåller fältindex som ska läggas till.                  |
| needReCalculate | boolean | query  | Sätt till **true** för att omberäkna pivottabellen efter åtgärden. |
| folder          | string  | query  | Mapp där dokumentet är lagrat.                                      |
| storageName     | string  | query  | Namn på lagringen.                                                  |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells-webbtjänster. Exemplet nedan visar hur du lägger till ett pivotfält med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Ett lyckat svar returnerar ett JSON-objekt med fälten `Code` och `Status`. Exempelschema:

```json
{
  "Code": 0,        // heltal som anger HTTP-statuskoden
  "Status": "OK"    // strängmeddelande
}
```

Möjliga felsvar inkluderar **400 Bad Request** för saknade parametrar, **401 Unauthorized** om token är ogiltig och **500 Internal Server Error** för serverseitiga problem.

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att integrera denna funktionalitet. SDK:er hanterar detaljer på lågnivånivå och låter dig fokusera på din affärslogik. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**Se även:**  
- [Lägg till en pivottabell](https://docs.aspose.cloud/cells/sv/pivot-tables/add-pivot-table/)  
- [Ta bort pivotfält](https://docs.aspose.cloud/cells/sv/pivot-tables/delete-pivot-field/)