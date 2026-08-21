---
---
title: "Hämta en enskild rad från ett Excel-arbetsblad med Aspose.Cells Cloud API"
description: "Lär dig hur du hämtar en specifik rad från ett Excel-arbetsblad som är lagrat i Aspose Cloud-lagring med Aspose.Cells Cloud REST API. Inkluderar begäransyntax, parametrar, svarschema, exempel på cURL och SDK-kod (C#, Java, Python)."
keywords: "Aspose.Cells Cloud, hämta rad, Excel API, kalkylblad REST, C# SDK, Java SDK, Python SDK"
date: 2026-07-30
api_version: "v3.0"
---

# Hämta en enskild rad från ett Excel-arbetsblad

**Endpoint**: `GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/rows/{rowIndex}`  

Hämta en rad från ett arbetsblad som är lagrat i Aspose Cloud-lagring. Åtgärden kräver en giltig OAuth 2.0-åtkomsttoken med **Read**-omfattningen.

---

## Innehållsförteckning
1. [Förutsättningar](#prerequisites)  
2. [HTTP-begäran](#http-request)  
3. [Parametrar](#parameters)  
   - [Sökvägsparametrar](#path-parameters)  
   - [Frågeparametrar](#query-parameters)  
4. [cURL-exempel](#curl-example)  
5. [Svar](#response)  
   - [Lyckat svarschema](#success-schema)  
   - [Statuskoder](#status-codes)  
6. [SDK-kodexempel](#sdk-code-samples)  
   - [C#](#c)  
   - [Java](#java)  
   - [Python](#python)  
7. [Relaterade operationer](#related-operations)  
8. [Anteckningar & begränsningar](#notes--limits)  

---

## Förutsättningar
- **Aspose Cloud-konto** med aktiv prenumeration.  
- **OAuth 2.0-åtkomsttoken** som inkluderar **Read**-omfattningen.  
- Målarbetsboken måste redan finnas i Aspose Cloud-lagring.  

---

## HTTP-begäran
```http
GET /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}?folder={folder}&storageName={storageName} HTTP/1.1
Host: api.aspose.cloud
Authorization: Bearer {access_token}
Accept: application/json
```

*Bas-URL*: `https://api.aspose.cloud/v3.0`

---

## Parametrar

### Sökvägsparametrar
| Namn        | Typ     | Krävs    | Beskrivning                                  |
|-------------|---------|----------|----------------------------------------------|
| `name`      | string  | ✅       | Namn på arbetsboksfilen (t.ex. `MyWorkbook.xlsx`). |
| `sheetName` | string  | ✅       | Namn på arbetsbladet (t.ex. `Sheet1`).       |
| `rowIndex`  | integer | ✅       | Nollbaserat index för raden som ska hämtas.  |

### Frågeparametrar *(valfria)*
| Namn          | Typ    | Krävs    | Beskrivning                                           |
|---------------|--------|----------|-------------------------------------------------------|
| `folder`      | string | ❌       | Sökväg till mappen i molnlagring där arbetsboken finns. |
| `storageName` | string | ❌       | Namn på lagringstjänsten (om du använder en anpassad lagring). |

---

## cURL-exempel
```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/rows/5?folder=Docs&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## Svar

### Lyckat svarschema (`200 OK`)
```json
{
  "Code": 200,
  "Status": "OK",
  "Row": {
    "Index": 5,
    "Height": 15.0,
    "Style": { /* stilobjekt */ },
    "Cells": [
      { "ColumnIndex": 0, "Value": "A6", "DataType": "String" },
      { "ColumnIndex": 1, "Value": 123, "DataType": "Number" }
      /* ...ytterligare celler... */
    ]
  }
}
```

### Statuskoder
| Kod | Betydelse |
|-----|-----------|
| **200** | Raden har hämtats utan fel. |
| **401** | Oauktorisering – saknad eller ogiltig åtkomsttoken. |
| **404** | Arbetsbok, arbetsblad eller rad hittades inte. |
| **500** | Internt serverfel. |

### Felexempel (`401 Unauthorized`)
```json
{
  "Code": 401,
  "Message": "Åtkomsttoken saknas eller är ogiltig."
}
```

---

## SDK-kodexempel

### C#  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var clientId = "YOUR_CLIENT_ID";
var clientSecret = "YOUR_CLIENT_SECRET";

var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRows_GetWorksheetRow(
    name: "MyWorkbook.xlsx",
    sheetName: "Sheet1",
    rowIndex: 5,
    folder: "Docs",
    storageName: null   // valfritt
);

Console.WriteLine($"Rad {response.Row.Index} hämtad med {response.Row.Cells.Count} celler.");
```

### Java  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.RowResponse;

CellsApi api = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
RowResponse response = api.cellsRowsGetWorksheetRow(
    "MyWorkbook.xlsx",
    "Sheet1",
    5,
    "Docs",
    null   // storageName – valfritt
);

System.out.println("Radindex: " + response.getRow().getIndex());
System.out.println("Antal celler: " + response.getRow().getCells().size());
```

### Python  
```python
from asposecellscloud import CellsApi, ApiException
from asposecellscloud.models import RowResponse

client_id = "YOUR_CLIENT_ID"
client_secret = "YOUR_CLIENT_SECRET"

api = CellsApi(client_id, client_secret)

try:
    response = api.cells_rows_get_worksheet_row(
        name="MyWorkbook.xlsx",
        sheet_name="Sheet1",
        row_index=5,
        folder="Docs",
        storage_name=None
    )
    print(f"Rad {response.row.index} hämtad med {len(response.row.cells)} celler.")
except ApiException as e:
    print("Undantag vid anrop till CellsApi->cells_rows_get_worksheet_row:", e)
```

---

## Relaterade operationer
| Operation | Beskrivning |
|-----------|-------------|
| **Lägg till rad** | `POST /cells/{name}/worksheets/{sheetName}/rows` – Infoga en ny rad i ett arbetsblad. |
| **Ta bort rad** | `DELETE /cells/{name}/worksheets/{sheetName}/rows/{rowIndex}` – Ta bort en befintlig rad. |
| **Hämta flera rader** | `GET /cells/{name}/worksheets/{sheetName}/rows` – Hämta en samling rader. |
| **Översikt över rader** | `/cells/rows/` – Allmän dokumentation för radrelaterade endpointar. |

---

## Anteckningar & begränsningar
- **Begränsning av frekvens**: 100 begäranden per minut per konto.  
- **Stödda format**: XLS, XLSX, CSV, ODS.  
- Radindex är **nollbaserat**; den första raden är `0`.  
- Se till att arbetsboken har laddats upp till den angivna `folder` innan du anropar denna endpoint.  

---