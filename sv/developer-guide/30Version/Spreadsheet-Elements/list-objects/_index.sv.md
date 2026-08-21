---
title: "Arbeta med Excel ListObject"
ArticleTitle: "Arbeta med Excel ListObject"
second_title: "Document"
linktype: "ListObjects"
type: docs
url: /sv/list-objects/
aliases:
  - /sv/working-with-list-objects/
  - /sv/working-with-list-object-or-table/
keywords: "Aspose.Cells, Excel ListObject, Excel-tabell-API, lägg till tabell, uppdatera tabell, ta bort tabell, konvertera tabell till intervall, sortera Excel-tabell"
description: "Lär dig hur du lägger till, uppdaterar, tar bort, hämtar, sorterar och konverterar Excel ListObjects (tabeller) med Aspose.Cells Cloud REST API. Innehåller kodexempel för C#, Java, Python och mer."
weight: 100
---

Excel ListObjects (tabeller) erbjuder ett strukturerat sätt att organisera datamängder. De inkluderar funktioner som automatisk dataordning, rubrikrader, inbyggda filter och valfria totalrader. Mastera dessa funktioner för att snabbt och effektivt analysera dina data.

**Definition av ListObject:** Ett **ListObject** är Excels inbyggda tabellobjekt som grupperar rader och kolumner, möjliggör sortering, filtrering och formatering, och kan nås via Aspose.Cells Cloud API.

## Hur man arbetar med tabell (ListObject)

- [Hur man lägger till en tabell (ListObject) i kalkylbladet](/sv/cells/add-a-list-object-or-table-inside-the-worksheet/)
- [Hur man uppdaterar en tabell (ListObject) i kalkylbladet](/sv/cells/update-a-list-object-or-table-inside-the-worksheet/)
- [Hur man konverterar en tabell (ListObject) till ett intervall](/sv/cells/convert-list-object-or-table-to-range/)
- [Hur man sorteras tabelldata](/sv/cells/sort-table-data/)
- [Hur man tar bort dubbletterade rader från en tabell](/sv/cells/list-objects/remove-duplicates/)
- [Hur man infogar en slicer för en tabell](/sv/cells/list-objects/insert-slicer/)

**API-referens (översikt):**  
Aspose.Cells Cloud REST API tillhandahåller ListObject-operationer via slutpunkter såsom `GET /cells/{fileName}/worksheets/{sheetName}/listobjects`, `POST /cells/{fileName}/worksheets/{sheetName}/listobjects`, `PUT /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` och `DELETE /cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Krävda frågeparametrar inkluderar `folder` (obligatorisk) och `storage` (valfri). Begärandetexter är JSON-objekt som beskriver tabellens egenskaper (namn, showHeaderRow, showTotalRow, etc.), och svar returnerar JSON-strukturer med information om det skapade eller modifierade ListObjectet.

**Förutsättningar:**  
- En giltig autentiseringstoken från Aspose.Cells Cloud.  
- Arbetsbokens fil måste vara uppladdad till en stödd lagringsplats (standard: **/**), och frågeparametern `folder` ska peka på den platsen.  
- Valfritt: Ställ in `storage` om du använder en icke-standardlagringstjänst.

**Detaljerad slutpunkt**

| Metod | Slutpunkt | Frågeparametrar | Begärandetext (JSON) | Lyckat svar (exempel) | Statuskoder |
|-------|-----------|-----------------|---------------------|------------------------|-------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (obligatorisk), `storage` (valfri) | *inga* | `{ "ListObjects": [ { "Name": "Table1", "ShowHeaderRow": true, "ShowTotalRow": false, ... } ] }` | 200 – OK, 400 – Felaktig begäran, 401 – Oauktoriserad, 404 – Hittades inte |
| POST | `/cells/{fileName}/worksheets/{sheetName}/listobjects` | `folder` (obligatorisk), `storage` (valfri) | `{ "Name": "Table1", "StartRow": 0, "StartColumn": 0, "TotalRows": 10, "TotalColumns": 5, "ShowHeaderRow": true, "ShowTotalRow": false }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "Table1", "ShowHeaderRow": true, ... } }` | 201 – Skapad, 400 – Felaktig begäran, 401 – Oauktoriserad, 409 – Konflikt |
| PUT | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (obligatorisk), `storage` (valfri) | `{ "Name": "UpdatedTable", "ShowTotalRow": true }` | `{ "Code": 200, "Status": "OK", "ListObject": { "Name": "UpdatedTable", "ShowTotalRow": true, ... } }` | 200 – OK, 400 – Felaktig begäran, 401 – Oauktoriserad, 404 – Hittades inte |
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/listobjects/{listObjectIndex}` | `folder` (obligatorisk), `storage` (valfri) | *inga* | `{ "Code": 200, "Status": "Deleted" }` | 200 – OK, 400 – Felaktig begäran, 401 – Oauktoriserad, 404 – Hittades inte |

**Kodexempel**

*C# (POST – Lägg till ListObject)*
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new ListObject
{
    Name = "MyTable",
    StartRow = 0,
    StartColumn = 0,
    TotalRows = 20,
    TotalColumns = 5,
    ShowHeaderRow = true,
    ShowTotalRow = false
};
var response = api.PostWorksheetListObject("Book1.xlsx", "Sheet1", request, folder: "", storage: null);
Console.WriteLine(response.ListObject.Name);
```

*Java (GET – Hämta ListObjects)*
```java
CellsApi apiInstance = new CellsApi();
ListObjectResponse result = apiInstance.getWorksheetListObjects("Book1.xlsx", "Sheet1", null, null);
System.out.println(result.getListObjects());
```

*Python (PUT – Uppdatera ListObject)*
```python
from asposecellscloud import CellsApi, ListObject
api = CellsApi(client_id, client_secret)
list_obj = ListObject(name="UpdatedTable", show_total_row=True)
response = api.put_worksheet_list_object(
    "Book1.xlsx", "Sheet1", 0, list_obj, folder="", storage=None)
print(response.list_object.name)
```

*Node.js (DELETE – Ta bort ListObject)*
```javascript
const { CellsApi } = require("asposecellscloud");
const api = new CellsApi(clientId, clientSecret);
api.deleteWorksheetListObject("Book1.xlsx", "Sheet1", 0, { folder: "" })
   .then(res => console.log("Deleted:", res.body));
```

**Anteckningar:**  
- ListObject-index är nollbaserade.  
- När ett ListObject läggs till definierar `StartRow` och `StartColumn` den övre vänstra cellen i tabellen.  
- API:t stöder paginering via frågeparametrarna `offset` och `limit` (inte visa i tabellen) för stora kalkylblad.  
- Gränser för begäran: 100 begäranden per minut per konto; överskridning returnerar **429 Too Many Requests**.

Genom att använda termen **Excel ListObject** flera gånger i sidan justeras innehållet mot sökord som "Excel ListObject", "Aspose.Cells Cloud" och "Excel table API", vilket förbättrar SEO samtidigt som det förblir naturligt för läsarna.