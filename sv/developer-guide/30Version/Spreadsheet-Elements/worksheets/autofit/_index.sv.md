---
title: "Arbeta med autofit på ett Excel-ark"
second_title: "Document"
linktype: "Autofit"
type: docs
url: /sv/worksheets/autofit/
aliases: [  /sv/autofit-rows-and-columns-of-worksheet/ ]
keywords: "autofit, kolumn, rad, Aspose.Cells, moln, Excel, API, storlek"
description: "Lär dig hur du automatiskt anpassar rad- och kolumnstorlek i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller exempel i cURL, .NET, Java och Python."
weight: 20
ArticleTitle: "Arbeta med autofit på ett Excel-ark – Aspose.Cells Cloud API"
---

## Arbeta med autofit på ett Excel-ark

- [Hur man autofitar en kolumn i ett Excel-ark.](/cells/worksheets/autofit/column/)
- [Hur man autofitar kolumner i ett Excel-ark.](/cells/worksheets/autofit/columns/)
- [Hur man autofitar en rad i ett Excel-ark.](/cells/worksheets/autofit/row/)
- [Hur man autofitar rader i ett Excel-ark.](/cells/worksheets/autofit/rows/)

**Förutsättningar**  
Innan du använder autofit-åtgärderna måste du ha:

1. Ett Aspose.Cells Cloud-konto med giltigt **Client Id** och **Client Secret**.  
2. En arbetsbok uppladdad till Aspose Cloud-lagring (eller tillgänglig via en offentlig URL).  
3. Namnet på det ark du planerar att ändra.

**API-referens**  

| Åtgärd | HTTP-metod | Slutpunkt | Nödvändiga parametrar | Begärandetext | Exempelsvar | Statuskoder |
|--------|------------|-----------|----------------------|---------------|----------------|--------------|
| Autofita en **kolumn** | POST | `/cells/worksheets/{sheetName}/autofit/column` | `sheetName` (sökväg) <br> `columnIndex` (frågeparameter) | *inga* | `{ "code": 200, "status": "OK", "message": "Kolumnen autofitad." }` | 200, 400, 401, 404, 500 |
| Autofita **kolumner** | POST | `/cells/worksheets/{sheetName}/autofit/columns` | `sheetName` (sökväg) <br> `startColumn`, `endColumn` (frågeparameter) | *inga* | `{ "code": 200, "status": "OK", "message": "Kolumnerna autofitade." }` | 200, 400, 401, 404, 500 |
| Autofita en **rad** | POST | `/cells/worksheets/{sheetName}/autofit/row` | `sheetName` (sökväg) <br> `rowIndex` (frågeparameter) | *inga* | `{ "code": 200, "status": "OK", "message": "Raden autofitad." }` | 200, 400, 401, 404, 500 |
| Autofita **rader** | POST | `/cells/worksheets/{sheetName}/autofit/rows` | `sheetName` (sökväg) <br> `startRow`, `endRow` (frågeparameter) | *inga* | `{ "code": 200, "status": "OK", "message": "Raderna autofitade." }` | 200, 400, 401, 404, 500 |

**Kodexempel**

*cURL*

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/worksheets/MySheet/autofit/columns?startColumn=0&endColumn=5" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json"
```

*.NET (C#)*

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Autentisera
var apiInstance = new CellsApi("{client_id}", "{client_secret}");

// Anropa autofit för kolumner
var response = apiInstance.PostWorksheetAutofitColumns(
    name: "Workbook.xlsx",
    sheetName: "Sheet1",
    startColumn: 0,
    endColumn: 5,
    folder: "",
    storageName: ""
);
Console.WriteLine(response.Status);
```

*Java*

```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.*;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Autofita rader
PostWorksheetAutofitRowsResponse resp = api.postWorksheetAutofitRows(
    "Workbook.xlsx",
    "Sheet1",
    0,   // startRow
    10,  // endRow
    "",  // folder
    ""   // storageName
);
System.out.println(resp.getStatus());
```

*Python*

```python
from asposecellscloud import CellsApi, ApiClient, Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api_client = ApiClient(configuration=config)
api = CellsApi(api_client)

# Autofita en enskild kolumn
response = api.post_worksheet_autofit_column(
    name="Workbook.xlsx",
    sheet_name="Sheet1",
    column_index=2,
    folder="",
    storage_name=""
)
print(response.status)
```

Dessa kodstycken visar hur man:

1. Autentiserar med Aspose.Cells Cloud med hjälp av sitt **Client Id** och **Client Secret**.  
2. Anropar rätt autofit-slutpunkt för kolumner eller rader.  
3. Bearbetar svaret, som bekräftar att åtgärden lyckades.

**Nästa steg**

När autofit-åtgärden är klar kan du ladda ner den uppdaterade arbetsboken:

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Workbook.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -o UpdatedWorkbook.xlsx
```

Du kan fritt justera parametrarna `startColumn`, `endColumn`, `startRow` och `endRow` för att rikta in dig på specifika intervall.
---