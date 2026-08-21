---
title: "Konvertera tabell till pivotdiagram"
second_title: "Dokument"
linktitle: Konvertera
type: docs
url: /sv/pivot-tables/convert-table-to-pivottable/
aliases:
  [
    "/sv/create-a-pivottable-with-table/",
    "/sv/create-new-pivot-table-with-list-object-as-source-data/",
  ]
keywords: "pivotdiagram, listobjekt, Aspose.Cells Cloud, REST API, konvertera tabell till pivotdiagram"
description: "Lär dig hur du skapar ett pivotdiagram från ett listobjekt med Aspose.Cells Cloud REST API. Innehåller begärandedetaljer, cURL-exempel och SDK-referenser."
weight: 60
ArticleTitle: "Konvertera tabell till pivotdiagram – Aspose.Cells Cloud-dokumentation"
---

Denna REST API skapar ett **pivotdiagram** från ett listobjekt.

Ett pivotdiagram sammanfattar data från ett listobjekt, vilket gör att du kan analysera och rapportera om stora dataset direkt i arbetsboken.

**Förutsättningar:**  
- Ett giltigt JWT-bärartoken för autentisering.  
- Arbetsboken måste finnas på den angivna lagringsplatsen.  
- Målbladet måste innehålla det listobjekt som du vill sammanfatta.

## PostWorksheetListObjectSummarizeWithPivotTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| Parameternamn   | Typ     | Plats  | Beskrivning                                |
| --------------- | ------- | ------ | ------------------------------------------ |
| name            | string  | path   | Arbetsbokens filnamn.                      |
| sheetName       | string  | path   | Bladet som innehåller listobjektet.        |
| listObjectIndex | integer | path   | Index för listobjektet i bladet.           |
| destsheetName   | string  | query  | Namn på målbladet.                         |
| request         | object  | body   | JSON-payload som definierar pivotdiagrammet. |
| folder          | string  | query  | Mapp sökväg där arbetsboken finns.         |
| storageName     | string  | query  | Namn på lagringsutrymmet.                  |

Begäran i brödtexten måste följa JSON-schemat som definieras nedan:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Namn på det nya pivotdiagrammet." },
    "DestCellName": { "type": "string", "description": "Övre vänstra cellen i pivotdiagrammet (t.ex. \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Nollbaserade index för fält som ska placeras i rader."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Nollbaserade index för fält som ska placeras i kolumner."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Nollbaserade index för fält som ska användas som datafält."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

<a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*Obs: Använd produktionsändpunkten (`api.aspose.cloud`) i produktionsmiljöer. QA-endpunkten (`api-qa.aspose.cloud`) är endast avsedd för testning. HTTPS krävs för alla produktionsanrop.*

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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                       |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltigt eller saknat JWT-token.                 |
| 413 | Begäran för stor            | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel.                               |

## SDK-familj för moln

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er: