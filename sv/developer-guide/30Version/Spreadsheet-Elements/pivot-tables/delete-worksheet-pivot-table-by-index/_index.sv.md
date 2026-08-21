---
title: "Ta bort en pivotdatabas i ett Excel-ark"
second_title: "Document"
linktitle: Delete
type: docs
url: /pivot-tables/delete/
aliases: [/delete-worksheet-pivot-table-by-index/]
keywords: "Aspose.Cells, pivotdatabas, ta bort, Excel, REST API"
description: "Ta bort en pivotdatabas från ett Excel-ark med Aspose.Cells Cloud REST API (v3.0). Inkluderar begäranformat, cURL-exempel, felkoder och SDK-utdrag för C#, Java, Python och Node.js."
weight: 70
ArticleTitle: "Hur man tar bort en pivotdatabas i ett Excel-ark med Aspose.Cells Cloud"
---

Denna REST API tar bort en pivotdatabas från ett ark enligt dess index.

**Förutsättningar** – Du måste ha en giltig JWT-åtkomsttoken för Aspose.Cells Cloud och den mål-Excel-filen lagrad på en stödd lagringsplats. Se till att filnamnet, arkets namn och lagringsuppgifter anges korrekt innan du anropar API:et.

Pivotdatabaser är ett kraftfullt sätt att sammanfatta data i ett **Excel-ark**. Med Aspose.Cells Cloud kan du programmatiskt ta bort en onödig pivotdatabas med ett enda HTTP DELETE-anrop. Denna åtgärd är idealisk när du behöver rensa upp ark, automatisera rapportgenerering eller integrera Excel-manipulation i dina applikationer.

## DeleteWorksheetPivotTable API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäransparametrar**

| Parameter Name  | Typ     | Position | Beskrivning                                            |
| --------------- | ------- | -------- | ------------------------------------------------------ |
| name            | sträng  | path     | Namn på Excel-dokumentet.                              |
| sheetName       | sträng  | path     | Namn på arket som innehåller pivotdatabasen.           |
| pivotTableIndex | heltal  | path     | Nollbaserat index för pivotdatabasen som ska tas bort. |
| folder          | sträng  | query    | Sökväg till mappen där dokumentet lagras.              |
| storageName     | sträng  | query    | Namn på lagringstjänsten.                              |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable) definierar ett offentligt tillgängligt programmeringsgränssnitt och tillåter dig att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Exempel på svar**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Svaret följer ett enkelt JSON-schema:

```json
{
  "Code": heltal,    // HTTP-liknande statuskod för åtgärden
  "Status": sträng   // Textuell beskrivning, t.ex. "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Felhantering

Vanliga svarsstatuskoder är listade nedan:

| HTTP-status | Beskrivning                                                             |
| ----------- | ----------------------------------------------------------------------- |
| 400         | Felaktig begäran – saknade eller ogiltiga parametrar.                  |
| 401         | Otillåten – ogiltig eller saknad JWT-token.                             |
| 404         | Inte hittad – filen, arket eller pivotdatabasen finns inte.            |
| 500         | Internt serverfel – ett oväntat tillstånd inträffade på servern.       |

## Cloud SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med diverse SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}