---
url: /extract-text/
title: Extract Text from Excel Cells Using Aspose.Cells Cloud API
date: 2024-03-15
lastmod: 2024-05-22
sitemap:
  priority: 0.8
canonical: https://reference.aspose.cloud/cells/extract-text/
keywords: "extract text from Excel, Aspose.Cells Cloud API, substring extraction, left/right text, position-based extraction, REST API for Excel"
description: "Extract substrings, numbers, or fixed-length prefixes/suffixes from Excel cells using Aspose.Cells Cloud REST API. Supports Before, After, BeforePosition, and AfterPosition modes—no formulas required."
weight: 100
---

Extract substrings, numbers, or fixed-length text fragments from Excel cells—without using complex `FIND`, `LEFT`, `RIGHT`, or `MID` formulas. Aspose.Cells Cloud’s **Extract Text** API processes cell data efficiently, preserving original formatting and formulas, and writes results directly to a target range in the same or different worksheet/workbook.

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/content/extract/text
```

## Authentication

All requests require a [JWT access token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) (valid for 24 hours by default):

```bash
-H "Authorization: Bearer {access_token}"
```

> ✅ **Verified HTTPS Link**: The official authentication guide uses HTTPS and resolves without insecure redirects.

---

## Request Parameters

| Parameter         | Type    | Location   | Required | Description |
|-------------------|---------|------------|----------|-------------|
| `Spreadsheet`     | File    | FormData   | ✅ Yes   | Upload the Excel workbook (`.xlsx`, `.xls`, `.csv`, etc.). |
| `extractTextType` | String  | Query      | ✅ Yes   | Extraction mode. Valid values: `Before`, `After`, `BeforePosition`, `AfterPosition`. |
| `outPositionRange`| String  | Query      | ✅ Yes   | Target cell/range for output (e.g., `Sheet1!B1:B10`). |
| `beforeText`      | String  | Query      | ❌ No    | Extract text *before* this substring (used with `Before`). |
| `afterText`       | String  | Query      | ❌ No    | Extract text *after* this substring (used with `After`). |
| `beforePosition`  | Integer | Query      | ❌ No    | Number of characters from the *left* (used with `BeforePosition`). |
| `afterPosition`   | Integer | Query      | ❌ No    | Number of characters from the *right* (used with `AfterPosition`). |
| `worksheet`       | String  | Query      | ❌ No    | Source worksheet name. Defaults to first sheet if omitted. |
| `range`           | String  | Query      | ❌ No    | Source cell/range (e.g., `A1`, `A1:A100`). |
| `outPath`         | String  | Query      | ❌ No    | Storage folder path for saving the result workbook. If omitted, the updated file is returned in the response body. |
| `outStorageName`  | String  | Query      | ❌ No    | Name of the cloud storage to use for `outPath`. |
| `region`          | String  | Query      | ❌ No    | Locale setting (e.g., `en-US`, `fr-FR`). Affects numeric/date parsing. |
| `password`        | String  | Query      | ❌ No    | Password for protected workbooks. |

---

## cURL Example

Extract text *before* `"Total"` in cell `A1` of `Sheet1`, and write the result to `B1`:

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
  spreadsheet: "Sample.xlsx"
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
- **Numeric/date cells** → Converted to text *using workbook locale* before extraction (e.g., `123.45` → `"123"` for left 3).
- **Empty cells** → Output remains empty.
- **No delimiter found?** → Returns empty string (no errors).
- **Preserves source data**: Formulas, formatting, and validation rules remain intact.

> 💡 **Memory-efficient**: Processes in streaming mode—suitable for large datasets (millions of rows).

---

## Supported Extraction Modes

| Mode             | Description                                                                 | Example Input (`A1 = "Total: $123.45"`) | Output (`B1`) |
|------------------|-----------------------------------------------------------------------------|------------------------------------------|---------------|
| `Before`         | Extract text *before* a specified substring                                | `beforeText = "Total:"`                 | `""` (empty)  |
| `After`          | Extract text *after* a specified substring                                 | `afterText = "Total: "`                 | `$123.45`     |
| `BeforePosition` | Extract first *n* characters from the *left* (pos = 1-based)               | `beforePosition = 5`                    | `Total`       |
| `AfterPosition`  | Extract last *n* characters from the *right* (pos = 1-based)               | `afterPosition = 4`                     | `123.45`      |

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

| Code | Meaning                         |
|------|---------------------------------|
| 200  | Success                         |
| 202  | Accepted (asynchronous)         |
| 400  | Invalid parameters or missing required fields |
| 401  | Invalid/missing JWT token       |
| 404  | Workbook not found              |
| 500  | Internal server error           |

---

## Best Practices & Tips

- 🔁 **Batch processing**: Use `range=A1:A1000` to extract text across many rows at once.
- 🌐 **Locale-awareness**: Set `region` to match your data’s format (e.g., `de-DE` for comma decimals).
- 🗂️ **Storage management**: Use `outPath` + `outStorageName` to avoid large response payloads.
- 🔄 **Idempotent**: Re-running with the same inputs overwrites the target range predictably.

---

## See Also

- [Upload Spreadsheet](/upload-spreadsheet/)  
- [Save Workbook to Cloud Storage](/storage-management/)  
- [Convert Excel to PDF](/convert-excel-to-pdf/)  
- [Working with Formulas](/formula-support/)  

---

> 📄 **Last updated**: 2024-05-22  
> 📚 [OpenAPI Specification (v4.0)](https://raw.githubusercontent.com/aspose-cells-cloud/aspose-cells-cloud-openapi-spec/main/specs/cells-cloud-openapi-spec.yaml)  
> 🛡️ All endpoints enforce HTTPS and support CORS for browser-based clients.