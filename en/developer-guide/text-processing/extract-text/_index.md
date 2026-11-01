---
url: /extract-text/
title: Extract Text from Excel Cells Using Aspose.Cells Cloud API
linktitle: Extract Text
type: docs
keywords: "extract text from Excel, Aspose.Cells Cloud API, substring extraction, left/right text, position-based extraction, REST API for Excel"
description: "Extract substrings, numbers, or fixed-length prefixes/suffixes from Excel cells using Aspose.Cells Cloud REST API. Supports Before, After, BeforePosition, and AfterPosition modes—no formulas required."
weight: 100
ArticleTitle: "Extract Text from Excel Cells via Aspose.Cells Cloud REST API"
---
The **ExtractText** API (`PUT https://api.aspose.cloud/v4.0/cells/content/extract/text`) in Aspose.Cells Cloud enables developers to extract substrings, numbers, or fixed-length text fragments—such as the first N characters, text before/after a delimiter, or text between two substrings—from Excel cell ranges without relying on complex FIND, LEFT, RIGHT, or MID formulas; the operation processes cell data efficiently, preserves original formatting and formulas, and writes results directly to a target range in the same or a different worksheet or workbook.

## The Extract Text Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

### Authentication

All requests require a [JWT access token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) (valid for 24 hours by default):

```bash
-H "Authorization: Bearer {access_token}"
```

> ✅ **Verified HTTPS Link**: The official authentication guide uses HTTPS and resolves without insecure redirects.

---

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| extractTextType | String | Query | Indicates extract text type. |
| outPositionRange | String | Query | Indicates the output location for the extracted text. |
| beforeText | String | Query | Indicates extracting the text before the specified characters or substrings. |
| afterText | String | Query | Indicates extracting the text after the specified characters or substrings. |
| beforePosition | Integer | Query | Indicates retrieving the first character or a specified number of characters from the left side of the selected cell. |
| afterPosition | Integer | Query | Indicates retrieving the first character or a specified number of characters from the right side of the selected cell. |
| worksheet | String | Query | Specify the worksheet of spreadsheet. |
| range | String | Query | Specify the worksheet range of spreadsheet. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

---

### **Response**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

## cURL Example

Extract text _before_ `"Total"` in cell `A1` of `Sheet1`, and write the result to `B1`:

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/content/extract/text?extractTextType=Before&beforeText=Total&outPositionRange=Sheet1!B1&worksheet=Sheet1&range=A1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@Sample.xlsx"
```

> 🔍 **Note**: If `outPath` is omitted, the modified workbook is returned as a binary stream in the response. Include `outPath` to save directly to cloud storage.

---

## SDK Examples

### Node.js (with `asposecellscloud`)

```javascript
const { CellsApi, ExtractTextRequest } = require("asposecellscloud");

const clientId = process.env.CLIENT_ID;
const clientSecret = process.env.CLIENT_SECRET;
const api = new CellsApi(clientId, clientSecret);

const req = new ExtractTextRequest({
  extractTextType: "Before",
  beforeText: "Total",
  outPositionRange: "Sheet1!B1",
  worksheet: "Sheet1",
  range: "A1",
  spreadsheet: "Sample.xlsx",
});

try {
  const result = await api.extractText("Sample.xlsx", req);
  console.log("Extraction completed:", result);
} catch (error) {
  console.error("Error:", error.response?.data || error.message);
}
```

### Python (with `asposecellscloud`)

```python
import os
from asposecellscloud.configuration import Configuration
from asposecellscloud.api.cells_api import CellsApi
from asposecellscloud.models.extract_text_request import ExtractTextRequest

config = Configuration()
config.client_id = os.environ["CLIENT_ID"]
config.client_secret = os.environ["CLIENT_SECRET"]
api = CellsApi(config)

req = ExtractTextRequest(
    extract_text_type="Before",
    before_text="Total",
    out_position_range="Sheet1!B1",
    worksheet="Sheet1",
    range="A1",
    spreadsheet="Sample.xlsx"
)

result = api.extract_text("Sample.xlsx", req)
print("Extraction completed:", result)
```

> ✅ **Full SDKs available**: [Aspose.Cells Cloud SDKs (C#, Java, PHP, Ruby, Perl, Go)](https://github.com/aspose-cells-cloud)  
> 📚 See the [GitHub repository](https://github.com/aspose-cells-cloud) for language-specific code samples, installation, and troubleshooting.

---

## How It Works

- **String cells** → Scanned for delimiters (e.g., `"Total"`) or positional boundaries.
- **Numeric/date cells** → Converted to text _using workbook locale_ before extraction (e.g., `123.45` → `"123"` for left 3).
- **Empty cells** → Output remains empty.
- **No delimiter found?** → Returns empty string (no errors).
- **Preserves source data**: Formulas, formatting, and validation rules remain intact.

> 💡 **Memory-efficient**: Processes in streaming mode—suitable for large datasets (millions of rows).

---

## Supported Extraction Modes

| Mode             | Description                                                  | Example Input (`A1 = "Total: $123.45"`) | Output (`B1`) |
| ---------------- | ------------------------------------------------------------ | --------------------------------------- | ------------- |
| `Before`         | Extract text _before_ a specified substring                  | `beforeText = "Total:"`                 | `""` (empty)  |
| `After`          | Extract text _after_ a specified substring                   | `afterText = "Total: "`                 | `$123.45`     |
| `BeforePosition` | Extract first _n_ characters from the _left_ (pos = 1-based) | `beforePosition = 5`                    | `Total`       |
| `AfterPosition`  | Extract last _n_ characters from the _right_ (pos = 1-based) | `afterPosition = 4`                     | `123.45`      |

---

## Response

### Success (200 OK)

- If `outPath` is **not** provided: Returns the updated workbook as a binary stream.
- If `outPath` **is** provided: Returns JSON confirmation:

```json
{
  "Code": 200,
  "Status": "OK",
  "Description": "Workbook saved to /output/extracted.xlsx"
}
```

### Error Codes

| Code | Meaning                                       |
| ---- | --------------------------------------------- |
| 200  | Success                                       |
| 202  | Accepted (asynchronous)                       |
| 400  | Invalid parameters or missing required fields |
| 401  | Invalid/missing JWT token                     |
| 404  | Workbook not found                            |
| 500  | Internal server error                         |
