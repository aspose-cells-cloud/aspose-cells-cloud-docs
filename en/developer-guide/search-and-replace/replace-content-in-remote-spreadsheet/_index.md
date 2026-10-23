---
url: /replace-content-in-remote-spreadsheet/
title: "Bulk Text Replacement in Remote Excel Files – Find & Replace API"
linktitle: "Replace content in Remote Spreadsheet"
type: docs
keywords: "Aspose.Cells Cloud, replace content, remote spreadsheet, find and replace API, cloud Excel, bulk text replacement"
description: "Aspose.Cells Cloud Find & Replace API enables secure, programmatic bulk text replacement in Excel workbooks hosted in the cloud. Supports OAuth2, multiple SDKs, and preserves cell formatting, formulas, and charts."
weight: 100
ArticleTitle: "Aspose.Cells Cloud API: Bulk Replace Text in Remote Excel Ranges"
---

Perform bulk text replacement across remote Excel files stored in cloud storage such as AWS S3 or Azure Blob. Use this REST API endpoint to efficiently locate and update text across an entire workbook or specific ranges—without downloading or manually editing files.

> **Prerequisites**
>
> - An Aspose.Cells Cloud account with valid `AppSID` and `AppKey`.
> - A valid OAuth2 access token (see [Authentication Guide](/cells-cloud/authentication/)).
> - A workbook file uploaded to your cloud storage.

---

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

> **Note**: For _workbook-wide_ replacement (all worksheets), use the simplified endpoint:  
> `PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content`  
> This document covers the **range-specific** operation per the latest API specification.

---

## Request Parameters

| Parameter     | Type   | Location | Description                                                                                                                          |
| ------------- | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `name`        | String | Path     | The name of the workbook file stored in cloud storage (e.g., `"report.xlsx"`).                                                       |
| `worksheet`   | String | Path     | The name of the worksheet where the replacement occurs (e.g., `"Sheet1"`).                                                           |
| `cellArea`    | String | Path     | The cell range (e.g., `"A1:D20"`, `"B2:F"`). Supports full-column/row references.                                                    |
| `searchText`  | String | Query    | The text string to locate. Search is case-sensitive unless modified by locale settings.                                              |
| `replaceText` | String | Query    | The replacement text.                                                                                                                |
| `folder`      | String | Query    | Cloud storage folder path containing the workbook (e.g., `"/documents/quarterly/"`).                                                 |
| `storageName` | String | Query    | _(Optional)_ Custom cloud storage name (e.g., `"MyS3Bucket"`). Omit to use the default storage.                                      |
| `region`      | String | Query    | _(Optional)_ Locale identifier (e.g., `"en-US"`, `"fr-FR"`). Affects number/date formatting and language-specific matching behavior. |
| `password`    | String | Query    | _(Optional)_ Password to open a protected workbook.                                                                                  |

---

## Example Request

```bash
curl -X PUT \
  'https://api.aspose.cloud/v4.0/cells/report.xlsx/worksheets/Sheet1/ranges/A1:D20/replace/content?searchText=Q1&replaceText=Q2&folder=documents/quarterly&region=en-US' \
  -H 'Authorization: Bearer <your_access_token>' \
  -H 'Content-Type: application/json'
```

---

## Response

A successful response returns the `CellsCloudResponse` object with operation status:

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "ReplacedCount": 5,
    "ReplacedRanges": ["A3", "A7", "B12", "C4", "D19"]
  }
}
```

| Field            | Type    | Description                                            |
| ---------------- | ------- | ------------------------------------------------------ |
| `ReplacedCount`  | Integer | Total number of text replacements performed.           |
| `ReplacedRanges` | Array   | Array of cell coordinates where replacements occurred. |

---

## Error Codes

| Status Code | Description                                                                |
| ----------- | -------------------------------------------------------------------------- |
| `400`       | Bad Request — Invalid URL, missing parameters, or malformed range syntax.  |
| `401`       | Unauthorized — Missing, expired, or invalid OAuth2 token.                  |
| `404`       | Not Found — Workbook, worksheet, or specified range does not exist.        |
| `500`       | Server Error — Internal failure (e.g., file corruption, permission error). |

---

## When to Use This API

- **Targeted Range Updates** – Replace text only within a defined cell range (e.g., update Q1 values in a financial model without affecting headers or totals).
- **Template Personalization** – Inject region-specific values (e.g., currency, date format) into cloud-based templates.
- **Cross-Environment Sync** – Maintain consistency across regional deployments (e.g., replace `"USD"` with `"EUR"` in EU-based workbooks).
- **Data Validation Cleanup** – Standardize inconsistent entries (e.g., replace `"N/A"`, `"n/a"`, `"NA"` with `"Missing"` in a region-agnostic way using `region=en-US`).

---

## Why Use Aspose.Cells Cloud for Text Replacement?

- **Zero Latency** – All processing occurs in the cloud; no local file I/O required.
- **Formatting Preservation** – Cell styles, formulas, charts, and conditional formatting remain intact.
- **Scalable** – Replace text across hundreds of workbooks in parallel via API orchestration.
- **Developer-Friendly** – Use native SDKs for rapid integration.
- **Secure** – OAuth2 authentication and encrypted data-in-transit (TLS 1.2+).
- **Pay-Per-Use** – No infrastructure costs or maintenance overhead.

---

## Code Examples

### Python (Aspose.Cells Cloud SDK)

```python
from asposecellscloud.api import CellsApi
from asposecellscloud.models import ReplaceTextOptions

# Initialize API
cells_api = CellsApi(client_id, client_secret)

# Replace "Q1" with "Q2" in range A1:D20 of Sheet1
response = cells_api.cells_replace_content(
    name="report.xlsx",
    search_text="Q1",
    replace_text="Q2",
    worksheet="Sheet1",
    cell_area="A1:D20",
    folder="documents/quarterly",
    region="en-US"
)

print(f"Replaced {response.body.replaced_count} occurrences.")
```

### Node.js (Aspose.Cells Cloud SDK)

```javascript
const { CellsApi } = require("asposecellscloud");

const cellsApi = new CellsApi(
  process.env.ASPOSE_CLOUD_CLIENT_ID,
  process.env.ASPOSE_CLOUD_CLIENT_SECRET,
);

const response = await cellsApi.cellsReplaceContent("report.xlsx", "Q1", "Q2", {
  worksheet: "Sheet1",
  cellArea: "A1:D20",
  folder: "documents/quarterly",
  region: "en-US",
});

console.log(`Replaced ${response.body.replacedCount} occurrences.`);
```
