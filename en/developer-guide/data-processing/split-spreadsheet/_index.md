---
url: /split-spreadsheet/
title: "Aspose.Cells Cloud Split Excel Web API – Split Excel Locally to Multiple Files & Export to 30+ Formats"
description: "Split Excel workbooks locally using Aspose.Cells Cloud API — no upload required. Export to PDF, CSV, JSON, and 30+ formats. Includes cURL & SDK examples for 8+ languages."
date: 2024-03-15T10:00:00Z
last_modified: 2024-05-22
draft: false
tags:
  - split
  - excel
  - api
  - local-processing
  - sdk
categories:
  - data-processing
  - cloud-api
weight: 5
---

# Split Excel Workbook Locally via Aspose.Cells Cloud API

Split a local Excel workbook into separate files — **entirely on the server side without requiring cloud storage**. Export to 30+ formats (PDF, CSV, JSON, XLSX, HTML, ODS, XPS, and more) using RESTful API or SDKs.

> **Note**: While processing occurs on Aspose’s infrastructure, *no files are persisted to cloud storage*. The operation is fully local to your session — your data remains secure and unuploaded to persistent storage.

## Prerequisites

- Aspose.Cells Cloud account with valid **App SID** and **App Key**
- `curl` installed (for REST examples)
- Optional: SDK for your preferred programming language ([GitHub repository](https://github.com/aspose-cells-cloud))

---

## REST API Endpoint

### PUT `/cells/split/spreadsheet`

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### Authentication

All requests require a valid JWT token. See [Authentication Overview](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

```http
Authorization: Bearer {access_token}
```

---

## Request Parameters

| Parameter Name     | Type     | Location      | Required | Description |
|--------------------|----------|---------------|----------|-------------|
| `Spreadsheet`      | File     | FormData      | ✅ Yes   | Local Excel file to split. Supported formats: XLS, XLSX, ODS, CSV, etc. |
| `from`             | Integer  | Query         | ❌ No    | Zero-based starting worksheet index (e.g., `0` for first sheet). |
| `to`               | Integer  | Query         | ❌ No    | Zero-based ending worksheet index (e.g., `2` splits sheets 0, 1, and 2). |
| `outFormat`        | String   | Query         | ❌ No    | Output format: `PDF`, `CSV`, `JSON`, `XLSX`, `HTML`, `ODS`, `XPS`, etc. Default: `xlsx`. |
| `outPath`          | String   | Query         | ❌ No    | Local folder path for output files. Defaults to a temporary session location. |
| `outStorageName`   | String   | Query         | ❌ No    | Session-based storage identifier (used for organization in local mode). |
| `fontsLocation`    | String   | Query         | ❌ No    | Custom font directory for accurate rendering (especially for PDF/image export). |
| `region`           | String   | Query         | ❌ No    | Locale (e.g., `"en-US"`, `"de-DE"`) for number/date/currency formatting. |
| `password`         | String   | Query         | ❌ No    | Password for encrypted workbooks. |

---

## Example Request (cURL)

Split all worksheets in `myWorkbook.xlsx` to PDF format and save to `./output/`:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF&outPath=./output" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
```

✅ **Response**: ZIP archive containing one file per worksheet (e.g., `Sheet1.pdf`, `Sheet2.pdf`, etc.)

---

## SDK Examples

Using an SDK simplifies integration and handles token management, multipart uploads, and error parsing automatically. Below are verified examples for major languages — all pinned to version `v24.5`.

<details>
<summary><strong>C#</strong> (Click to expand)</summary>

```csharp
// Example40_SplitLocalFile.cs (v24.5)
var cellsApi = new CellsApi(clientId, clientSecret);
var result = await cellsApi.SplitSpreadsheetAsync(
    file: "myWorkbook.xlsx",
    from: 0,
    to: 2,
    outFormat: "PDF",
    outPath: "output"
);
```
</details>

<details>
<summary><strong>Java</strong> (Click to expand)</summary>

```java
// Example40_SplitLocalFile.java (v24.5)
CellsApi api = new CellsApi(clientId, clientSecret);
FilesResult result = api.splitSpreadsheet(
    "myWorkbook.xlsx",
    0,
    2,
    "PDF",
    "output"
);
```
</details>

<details>
<summary><strong>PHP</strong> (Click to expand)</summary>

```php
// Example40_SplitLocalFile.php (v24.5)
$api = new CellsApi($clientId, $clientSecret);
$result = $api->splitSpreadsheet(
    "myWorkbook.xlsx",
    0,
    2,
    "PDF",
    "output"
);
```
</details>

<details>
<summary><strong>Python</strong> (Click to expand)</summary>

```python
# Example40_SplitLocalFile.py (v24.5)
from asposecellscloud.api import CellsApi
api = CellsApi(client_id, client_secret)
result = api.split_spreadsheet(
    file="myWorkbook.xlsx",
    from_=0,
    to=2,
    out_format="PDF",
    out_path="output"
)
```
</details>

<details>
<summary><strong>Node.js / TypeScript</strong> (Click to expand)</summary>

```typescript
// Example40_SplitLocalFile.ts (v24.5)
const api = new CellsApi(clientId, clientSecret);
const result = await api.splitSpreadsheet(
  'myWorkbook.xlsx',
  0,
  2,
  'PDF',
  'output'
);
```
</details>

<details>
<summary><strong>Ruby</strong> (Click to expand)</summary>

```ruby
# Example40_SplitLocalFile.rb (v24.5)
api = AsposeCellsCloud::CellsApi.new(client_id, client_secret)
result = api.split_spreadsheet(
  'myWorkbook.xlsx',
  0,
  2,
  'PDF',
  'output'
)
```
</details>

<details>
<summary><strong>Perl</strong> (Click to expand)</summary>

```perl
# Example40_SplitLocalFile.pl (v24.5)
my $api = AsposeCellsCloud::API->new(
  client_id => $clientId,
  client_secret => $clientSecret
);
my $result = $api->split_spreadsheet(
  'myWorkbook.xlsx',
  0,
  2,
  'PDF',
  'output'
);
```
</details>

<details>
<summary><strong>Go</strong> (Click to expand)</summary>

```go
// Example40_SplitLocalFile.go (v24.5)
api := cells.NewCellsApi(clientId, clientSecret)
result, _, err := api.SplitSpreadsheet(
  context.Background(),
  "myWorkbook.xlsx",
  0,
  2,
  "PDF",
  "output",
)
```
</details>

> 🔗 View full source on GitHub:  
> [`aspose-cells-cloud-gists/Example40_SplitLocalFile.cs@v24.5`](https://github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d/blob/v24.5/Example40_SplitLocalFile.cs)  
> *(Replace `.cs` with `.java`, `.php`, `.py`, etc. for other languages)*

---

## Response

| Status Code | Content-Type         | Description |
|-------------|----------------------|-------------|
| `200 OK`    | `application/zip`    | ZIP archive containing one file per split worksheet. |
| `200 OK`    | `application/octet-stream` | (Legacy) Binary stream — use `outPath` for direct file save. |

✅ **On success**, each worksheet in the range (`from`–`to`) is exported as a separate file in the specified format and packaged into a ZIP archive.  
✅ **File naming**: `Sheet{index}.{ext}` (e.g., `Sheet0.pdf`, `Sheet1.csv`).

---

## Error Handling

| Code | Meaning               | Cause & Resolution |
|------|-----------------------|---------------------|
| `400` | Bad Request           | Invalid `from`/`to` index (e.g., negative, `from > to`), unsupported file type, or missing `Spreadsheet` field. |
| `401` | Unauthorized          | Missing, expired, or invalid JWT token. Re-authenticate and retry. |
| `404` | Not Found             | Source file not found in temporary session (expired upload or malformed FormData). |
| `413` | Payload Too Large     | File exceeds 2 GB limit. Compress or split externally first. |
| `500` | Internal Server Error | Unexpected processing failure (e.g., corrupted file). Verify file integrity. |

---

## Use Cases

| Use Case | Description |
|----------|-------------|
| **Department Distribution** | Split a central HR/Finance workbook into department-specific files (e.g., `Sales.xlsx`, `Engineering.xlsx`). |
| **Regional Reporting** | Generate regional sales reports (e.g., `EMEA_Sales.pdf`, `APAC_Sales.pdf`) from a global master file. |
| **Data Masking & Segmentation** | Split sensitive data into anonymized customer subsets (e.g., `CustomerSetA.csv`, `CustomerSetB.csv`). |
| **Multi-Format Output** | Simultaneously export the same sheets to PDF, CSV, and JSON for downstream systems. |
| **Template-Based Splitting** | Use templates to define split rules (e.g., split by column value → one file per region). |
| **Preprocessing for DB Load** | Split large Excel files into clean CSV chunks ready for bulk database import. |

---

## Why Use Aspose.Cells Cloud Split API?

✅ **Zero Cloud Storage Dependency**  
Files are processed *in-memory* on the server — no need to upload to or configure cloud storage.

✅ **Preserves Complex Formatting**  
Retains formulas, charts, pivot tables, and formatting in PDF/HTML output.

✅ **Developer-Friendly SDKs**  
Supports 8+ languages with minimal boilerplate.

✅ **Scalable & Secure**  
Stateless architecture scales with demand. No data is stored after processing.

✅ **Pay-per-Use Pricing**  
No infrastructure costs — only pay for API calls.

---

## API Diagram

```plaintext
┌──────────────┐
│ Local File   │
│ (e.g., XLSX) │
└──────┬───────┘
       │ Upload via FormData
       ▼
┌──────────────────────────────────────────┐
│ Aspose.Cells Cloud (Local-Processing Mode) │
│  • File processed in-memory              │
│  • No storage required                   │
│  • Split per `from`/`to` & `outFormat`   │
└───────────────┬──────────────────────────┘
                │ Return ZIP of split files
                ▼
┌──────────────────┐
│ Output Files     │
│ (PDF/CSV/JSON,…) │
└──────────────────┘
```

> **Alt text**: *Local-only split flow: No data leaves your environment or cloud storage.*

---

## Related APIs

- [Merge Excel Files](/merge-excel/)  
- [Convert Excel to PDF/HTML/JSON](/convert-excel/)  
- [Protect & Unprotect Workbooks](/protect-excel/)  
- [Extract Worksheet Images](/extract-images/)

---

## References

- [API Reference](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet)  
- [SDK Documentation & Examples](https://github.com/aspose-cells-cloud)  
- [Authentication Guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)