---
title: "Hur man hämtar innehåll från ett intervall i ett Excel-ark"
second_title: "Dokument"
linktitle: "Hämta"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel, API, hämta, intervall, kalkylark, REST"
description: "Lär dig hur du hämtar innehåll från ett intervall i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller begärsyntax och exempelkod."
weight: 20
ArticleTitle: "Hur man hämtar innehåll från ett intervall i ett Excel-ark – Aspose.Cells Cloud API"
---

## Arbeta med hämtning av intervallinnehåll i ett Excel-ark

- [Hur man hämtar celldata baserat på ett namngivet intervall](/cells/ranges/get/values/)
- [Hur man hämtar ett namngivet intervall från en Excel-arbetsbok](/cells/ranges/get/name/)

**Förutsättningar**

- En giltig Aspose Cloud-åtkomsttoken (eller `client_id`/`client_secret` för OAuth).
- Excel-filen måste ha laddats upp till målmappen i lagringen.
- Aspose.Cells Cloud SDK version 3.0 eller senare.

**Get Range**-åtgärden returnerar innehållet i ett angivet intervall i ett ark.  
Det är en enkel `GET`-begäran som returnerar intervalldata i JSON-format (eller andra format om så önskas).

**Översikt över begäran**

| Element | Värde |
|---------|-------|
| **HTTP-metod** | `GET` |
| **Endpoint** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **Sökvägsparametrar** | `fileName` – namn på Excel-filen (inklusive filtillägg) <br> `sheetName` – namn på arket <br> `rangeName` – namn på intervallet (t.ex. `A1:B10`) |
| **Frågeparametrar** (valfria) | `folder` – lagringsmapp <br> `storage` – lagringsnamn <br> `outFormat` – svarssformat (t.ex. `json`, `xml`) |
| **Headers** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**Exempel med cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**Exempel i C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**Exempel i Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**Exempel i Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**Svarschema (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsinformation. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

- `200 OK` – Intervallet hämtades framgångsrikt.  
- `400 Bad Request` – Saknade eller ogiltiga parametrar.  
- `401 Unauthorized` – Ogiltig eller saknad åtkomsttoken.  
- `404 Not Found` – Den angivna filen, arket eller intervallet kunde inte hittas.  
- `500 Internal Server Error` – Oväntat serverfel.

**Exempel på fel-svar**

```json
// 400 Bad Request
{
  "Code": 400,
  "Message": "Begärans parametrar är ogiltiga eller saknas."
}
```

```json
// 401 Unauthorized
{
  "Code": 401,
  "Message": "Ogiltig eller saknad åtkomsttoken."
}
```

```json
// 404 Not Found
{
  "Code": 404,
  "Message": "Den angivna filen, arket eller intervallet kunde inte hittas."
}
```

**Se även**

- [Hur man hämtar celldata baserat på ett namngivet intervall](/cells/ranges/get/values/)  
- [Hur man hämtar ett namngivet intervall från en Excel-arbetsbok](/cells/ranges/get/name/)  
- [Uppdatera intervallinnehåll](/cells/ranges/update/)  
- [Ta bort ett intervall](/cells/ranges/delete/)  
---