---
title: "How to Get Range Content from an Excel Worksheet"
second_title: "Document"
linktitle: "Get"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel API, get range, spreadsheet range content, REST API, Java SDK, Python SDK"
description: "Learn how to retrieve the content of a specific range in an Excel worksheet using Aspose.Cells Cloud REST API. Includes request syntax, sample code in C#, Java, Python, and error handling tips."
weight: 20
---

## Working with retrieving range content in an Excel worksheet

- [How to get cell data based on a named range](/cells/ranges/get/values/)
- [How to get a named range from an Excel workbook](/cells/ranges/get/name/)

### Overview
The **Get Range** endpoint returns the complete content of a named range (values, formulas, and formatting) from a worksheet in an Excel file stored in Aspose.Cloud. Use this operation when you need to read a block of cells without downloading the whole workbook.

### Prerequisites
- An active **Aspose.Cloud** account.  
- `client_id` and `client_secret` generated in the Aspose Cloud dashboard.  
- An OAuth 2.0 access token obtained via the */connect/token* endpoint.  
- The target workbook must already be uploaded to Aspose Cloud storage.  

### Request
#### Endpoint URL
```http
GET https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}
```
- `v3.0` – current API version.  

#### Path / Query Parameters
| Parameter | Type   | Required | Description |
|-----------|--------|----------|-------------|
| `fileName` | string | Yes | Name of the Excel file (including extension). |
| `sheetName`| string | Yes | Worksheet that contains the range. |
| `rangeName`| string | Yes | Name of the range to retrieve (e.g., `A1:C5`). |

#### Headers
| Header | Value | Required | Description |
|--------|-------|----------|-------------|
| `Authorization` | `Bearer {access_token}` | Yes | OAuth 2.0 token. |
| `Accept` | `application/json` *(default)* or `application/xml` | No | Desired response format. |

### Response
A successful call returns **HTTP 200** with a JSON payload that describes the range.

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "Name": "MyRange",
    "RowCount": 3,
    "ColumnCount": 3,
    "Values": [
      ["A1", "B1", "C1"],
      ["A2", "B2", "C2"],
      ["A3", "B3", "C3"]
    ],
    "Formulas": [
      [null, null, null],
      [null, null, null],
      [null, null, null]
    ],
    "Style": {
      "Font": "Calibri",
      "Size": 11,
      "Color": "#000000"
    }
  }
}
```

### Error Handling
| HTTP Status | Description                              | Sample Error Body |
|-------------|------------------------------------------|-------------------|
| 400         | Bad request – missing/invalid parameters | `{"Code":400,"Message":"Invalid range name."}` |
| 401         | Unauthorized – token missing or expired   | `{"Code":401,"Message":"Access token is invalid."}` |
| 404         | Not found – file, sheet, or range absent  | `{"Code":404,"Message":"Resource not found."}` |
| 500         | Server error – unexpected condition       | `{"Code":500,"Message":"Internal server error."}` |

### Step‑by‑Step Usage
1. **Generate an access token** using your `client_id` and `client_secret`.  
2. **Upload** the workbook to Aspose Cloud storage (if not already present).  
3. **Compose the request URL** by replacing `{fileName}`, `{sheetName}`, and `{rangeName}`.  
4. **Send the GET request** with the `Authorization` header.  
5. **Parse the JSON response** to obtain `Range.Values`, `Range.Formulas`, or style information.  

### Code Samples
#### C# (.NET SDK)
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};

var api = new CellsApi(config);
var token = api.OAuth2GetToken(new OAuth2GetTokenRequest
{
    GrantType = "client_credentials"
});

var response = api.CellsRanges_GetRange(
    new CellsRanges_GetRangeRequest(
        name: "Sample.xlsx",
        sheetName: "Sheet1",
        name: "A1:C3",
        folder: null,
        storageName: null,
        token: token.AccessToken));

Console.WriteLine(response.Range.Values);
```

#### Java (Java SDK)
```java
import com.aspose.cloud.cells.api.*;
import com.aspose.cloud.cells.model.*;

ApiClient client = new ApiClient();
client.setAppSid("<your_client_id>");
client.setAppKey("<your_client_secret>");

CellsApi api = new CellsApi(client);
String accessToken = api.oauth2GetToken("client_credentials").getAccessToken();

RangeResponse result = api.cellsRangesGetRange(
        "Sample.xlsx",
        "Sheet1",
        "A1:C3",
        null,
        null,
        accessToken);

System.out.println(result.getRange().getValues());
```

#### Python (Python SDK)
```python
from asposecellscloud import CellsApi, ApiClient, GetRangeRequest

api_client = ApiClient(app_sid='<your_client_id>', app_key='<your_client_secret>')
cells_api = CellsApi(api_client)

# Get access token
token = cells_api.oauth2_get_token(grant_type='client_credentials')
access_token = token.access_token

request = GetRangeRequest(
    name='Sample.xlsx',
    sheet_name='Sheet1',
    range_name='A1:C3',
    folder=None,
    storage_name=None,
    token=access_token
)

response = cells_api.cells_ranges_get_range(request)
print(response.range.values)
```

### Next Steps / Related Operations
- **[Get Range Values](/cells/ranges/get/values/)** – Retrieve only the values of a range.  
- **[Get Named Range](/cells/ranges/get/name/)** – Access a named range definition.  
- **[Update Range](/cells/ranges/put/)** – Modify the content of an existing range.  

### FAQ
**Q:** *How do I authenticate when calling the Get Range endpoint?*  
**A:** Obtain an OAuth 2.0 token via the `/connect/token` endpoint and include it in the `Authorization: Bearer {token}` header.

**Q:** *What response formats are available?*  
**A:** JSON is the default (`Accept: application/json`). Set `Accept: application/xml` to receive XML.

**Q:** *Which SDKs provide ready‑made examples for this operation?*  
**A:** Aspose offers SDKs for C#, Java, Python, Go, Node.js, Perl, PHP, Ruby, and Swift. Sample snippets above illustrate C#, Java, and Python.

---  