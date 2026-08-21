---
title: "Sortera ListObject-data i ett Excel-ark"
second_title: "Dokument"
linktitle: "Sortera"
type: docs
url: /sv/list-objects/sort-data/
aliases: [  /sv/get-a-list-object-or-table-inside-the-worksheet/ , /sv/tables/sort-data/ ]
keywords: "Aspose.Cells Cloud, Excel, ListObject, Sortera data, REST API, Ark"
description: "Lär dig hur du sorterar ListObject (tabell) data i ett Excel-ark med Aspose.Cells Cloud REST API (v3.0). Inkluderar endpoint, parametrar, exempel på cURL-förfrågan och SDK-exempel."
weight: 40
ArticleTitle: "Sortera ListObject-data i ett Excel-ark – Aspose.Cells Cloud API"
---

**Förutsättningar**  
För att anropa detta API måste du ha ett giltigt Aspose Cloud JWT-åtkomsttoken, och arbetsboken måste ha laddats upp till Aspose Cloud-lagring. Inkludera rubriken `Authorization: Bearer <jwt token>` i varje förfrågan.

Detta REST API sorterar en tabells data i ett Excel-ark.  
För att använda denna åtgärd, ange arbetsbokens namn, arkets namn och indexet för det mål-ListObject, tillsammans med en JSON-kropp `dataSorter` som definierar sorteringskriterierna.

## PostWorksheetListObjectSortTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/sort
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Förfrågningsparametrar**

| Parameternamn   | Typ     | Path/Query String/HTTPBody | Beskrivning                                                                                                     |
| --------------- | ------- | -------------------------- | --------------------------------------------------------------------------------------------------------------- |
| name            | string  | path                       | Namnet på Excel-filen som finns i Aspose Cloud-lagring.                                                         |
| sheetName       | string  | path                       | Namnet på arket som innehåller ListObjectet.                                                                    |
| listObjectIndex | integer | path                       | Nollbaserat index för ListObjectet (tabellen) i arket.                                                          |
| dataSorter      | object  | body                       | JSON-objekt som anger sorteringsalternativ (t.ex. `CaseSensitive`, `HasHeaders`, `KeyList`, `SortLeftToRight`). |
| folder          | string  | query                      | Mappväg i lagringen där Excel-filen finns.                                                                      |
| storageName     | string  | query                      | Namnet på Aspose Cloud-lagringen.                                                                                |

**Anteckningar**  
Förfrågningskroppen måste vara ett giltigt JSON-objekt som matchar `dataSorter`-schemat. Se till att arbetsboken, arket och ListObjectet finns innan du utför sorteringsåtgärden.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSortTable) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet7/listobjects/1/sort" \
  -X POST \
  -d '{
        "CaseSensitive": true,
        "HasHeaders": true,
        "KeyList": [
          {
            "Key": 1,
            "SortOrder": "Ascending",
            "CustomList": "string"
          }
        ],
        "SortLeftToRight": true
      }' \
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

**HTTP-statuskoder**

| Statuskod | Beskrivning                                |
|-----------|--------------------------------------------|
| 200       | OK – sortering slutfördes framgångsrikt.  |
| 400       | Felaktig förfrågan – ogiltiga parametrar. |
| 401       | Obehörig – autentisering misslyckades.     |
| 404       | Hittades inte – arbetsbok, ark eller ListObject hittades inte. |
| 500       | Internt serverfel – serverseitigt problem.|

**Svarsparametrar**

| Parameter | Typ    | Beskrivning                               |
|-----------|--------|-------------------------------------------|
| Code      | integer | HTTP-statuskod som returneras av API:et.  |
| Status    | string  | Textuell beskrivning av resultatet (t.ex. "OK"). |

{{< /tab >}}

{{< /tabs >}}

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObjectSortTable.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObjectSortTable.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObjectSortTable.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObjectSortTable.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObjectSortTable.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObjectSortTable.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObjectSortTable.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObjectSortTable.go" >}}

{{< /tab >}}

{{< /tabs >}}

[Tillbaka till ListObjects-översikten](/list-objects/)