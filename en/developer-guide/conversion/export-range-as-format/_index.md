---
title: "Export Excel Range to PDF, PNG, CSV – Aspose.Cells Cloud API"
date: 2024-05-15
lastmod: 2024-05-15
description: "Export specific Excel ranges to PDF, PNG, SVG, CSV, and other formats via Aspose.Cells Cloud API. Includes cURL, SDK examples (C#, Java, Python, PHP, Node.js, Ruby, Perl, Go), parameter reference, error handling, and use cases."
linktitle: "Export Range as Format"
type: docs
url: /export-range-as-format/
keywords: "Aspose.Cells Cloud, export Excel range, PDF, PNG, CSV, SVG, cloud API, spreadsheet conversion, range to format"
weight: 100
---

## Export Range as Format API

Convert a specific range within a cloud-hosted Excel or spreadsheet workbook to another format—PDF, PNG, SVG, CSV, and more—without downloading the file locally. The output can be saved to cloud storage or returned as a binary stream.

### REST API Endpoint

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

#### Path Parameters

| Parameter | Type   | Required | Description                          |
|:----------|:-------|:---------|:-------------------------------------|
| `name`    | string | Yes      | Name of the workbook file in cloud storage. |
| `worksheet` | string | Yes    | Name of the worksheet containing the range. |
| `range`   | string | Yes      | Cell range identifier (e.g., `A1:C12`, `Sheet2!B2:D20`). |

#### Query Parameters

| Parameter         | Type    | Required | Description |
|:------------------|:--------|:---------|:------------|
| `format`          | string  | Yes      | Target output format (e.g., `pdf`, `png`, `svg`, `csv`, `xlsx`). Case-insensitive. |
| `folder`          | string  | No       | Folder path containing the workbook. Defaults to root. |
| `storageName`     | string  | No       | Cloud storage name. Omit to use default storage. |
| `outPath`         | string  | No       | Absolute path in cloud storage where the output file will be saved. Requires `outStorageName` if non-default storage is used. |
| `outStorageName`  | string  | No       | Storage name for the output file. Required when `outPath` specifies a non-default storage. |
| `fontsLocation`   | string  | No       | Custom folder path for fonts used during rendering. |
| `AutoRowsFit`     | boolean | No       | Whether to auto-fit rows in the range before conversion. Default: `false`. |
| `AutoColumnsFit`  | boolean | No       | Whether to auto-fit columns in the range before conversion. Default: `false`. |
| `region`          | string  | No       | Locale setting (e.g., `en-US`, `fr-FR`). Mirrors Excel’s **File > Options > Advanced > International** setting. Affects number, date, and formula evaluation behavior. |
| `password`        | string  | No       | Password to open the protected workbook. |

> **Note**: If `outPath` is specified, `outStorageName` must be provided when the output should reside in a non-default storage.

---

### Security & Authentication

All API requests require [JWT token–based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include the token in the `Authorization` header:

```http
Authorization: Bearer <access_token>
```

---

### Response

The API returns a binary stream of the converted file (MIME type matches the requested format). When `outPath` is provided, the file is saved directly to cloud storage, and the response body is empty with HTTP status `200 OK`.

#### Example Response (Stream Output)

| Field | Type | Description |
|:------|:-----|:------------|
| `Content-Type` | string | MIME type (e.g., `application/pdf`, `image/png`) |
| `Content-Disposition` | string | Inline or attachment with filename (e.g., `filename="A1_C12.pdf"`) |
| Body | binary | File content as byte stream |

#### Example Response (Cloud Storage Save)

When `outPath` is used and the operation succeeds, the response is:

```http
HTTP/1.1 200 OK
Content-Length: 0
```

---

### HTTP Status Codes

| Code | Meaning | Description |
|:-----|:--------|:------------|
| `200` | OK | Conversion successful. |
| `400` | Bad Request | Invalid or missing parameters (e.g., unsupported `format`, malformed range). |
| `401` | Unauthorized | Invalid, expired, or missing JWT token. |
| `403` | Forbidden | Access denied to the workbook (e.g., wrong password, insufficient permissions). |
| `404` | Not Found | Workbook, worksheet, or range not found. |
| `500` | Internal Server Error | Unexpected error during conversion (e.g., unsupported feature in range). |

---

### Example: Export Range with cURL

Export range `A1:C12` from `Sheet1` of `MyWorkbook.xlsx` to PDF:

```bash
curl -X GET \
  "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
  -H "Authorization: Bearer eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCJ9..." \
  -H "Accept: application/octet-stream" \
  --output range_export.pdf
```

---

### Using Aspose.Cells Cloud SDKs

SDKs for 8+ languages simplify integration, handle authentication, and manage serialization. See the [Aspose.Cells Cloud GitHub organization](https://github.com/aspose-cells-cloud) for official SDKs.

#### C# (.NET)

```csharp
var api = new CellsApi(clientId, clientSecret);
var response = api.CellsRangesGetRangesWorksheet(
    name: "MyWorkbook.xlsx",
    worksheet: "Sheet1",
    range: "A1:C12",
    format: "pdf",
    folder: null,
    storageName: null
);
File.WriteAllBytes("range_export.pdf", response);
```

#### Java

```java
CellsApi api = new CellsApi(System.getenv("CELLS_CLOUD_CLIENT_ID"), 
                            System.getenv("CELLS_CLOUD_CLIENT_SECRET"));
ResponseStream response = api.cellsRangesGetRangesWorksheet(
    "MyWorkbook.xlsx", "Sheet1", "A1:C12", "pdf", null, null);
Files.write(Paths.get("range_export.pdf"), response.getBytes());
```

#### Python

```python
from asposecellscloud.api import CellsApi
from asposecellscloud.configuration import Configuration

config = Configuration()
config.client_id = "YOUR_CLIENT_ID"
config.client_secret = "YOUR_CLIENT_SECRET"
api = CellsApi(config)

response = api.cells_ranges_get_ranges_worksheet(
    name="MyWorkbook.xlsx",
    worksheet="Sheet1",
    range="A1:C12",
    format="pdf"
)
with open("range_export.pdf", "wb") as f:
    f.write(response)
```

> Full examples for PHP, Ruby, Node.js, Perl, and Go are available in the [SDK repository](https://github.com/aspose-cells-cloud).

---

### Use Cases

#### Data Export & Migration
- **Database Integration**: Export ranges directly to database staging tables.
- **Application Integration**: Push selected ranges into SaaS tools (e.g., CRM, analytics).
- **Legacy-to-Modern Migration**: Convert legacy Excel ranges to open formats (CSV, JSON).
- **Cross-Platform Sharing**: Distribute only relevant data subsets across teams or platforms.

#### Reporting & Analytics
- **Targeted Reporting**: Export report sections (e.g., Q3 KPIs) to PDF for stakeholder review.
- **Dashboard Feeds**: Generate CSV/JSON for BI tools (Power BI, Tableau).
- **Financial Reporting**: Extract ledger ranges for audit compliance (e.g., balance sheet, P&L).
- **Performance Tracking**: Pull KPI ranges into monitoring systems.

#### Development & Testing
- **Test Data Generation**: Create CSV or Excel test datasets from production ranges.
- **API Prototyping**: Quickly validate data flows using real range exports.
- **Dev/QA Collaboration**: Share specific data scenarios with minimal overhead.

#### Business Operations
- **Selective Data Sharing**: Send only approved ranges to external partners.
- **Partial Backups**: Backup critical ranges without full workbook duplication.
- **Compliance Submissions**: Export regulatory data (e.g., tax, ESG) in required formats.
- **Inter-Department Sharing**: Distribute sales or inventory ranges to relevant teams.

#### Automation Workflows
- **Scheduled Exports**: Run nightly exports of range data using cron or workflow engines (e.g., Apache Airflow).
- **Event-Triggered Exports**: Export upon sales order creation, inventory threshold, or report completion.
- **Batch Processing**: Export multiple ranges across workbooks in parallel.
- **Pipeline Integration**: Embed range export in CI/CD (e.g., generate test reports as PDF).

---

### Benefits

- **Cloud-Native Workflow**: Process spreadsheets directly in cloud storage—no local file I/O needed.
- **Format Versatility**: Support for PDF, PNG, SVG, CSV, XLSX, and other common formats.
- **Reduced Infrastructure Overhead**: Hosted service eliminates server provisioning, scaling, and maintenance.
- **Consistent Formatting**: Preserves Excel styling, formulas, and layout in output.
- **Scalable Performance**: Optimized for large workbooks and high-throughput scenarios.

---

### Related Documentation

- [Authentication Guide](/getting-started/authentication/)  
- [Export Entire Workbook to PDF](/export-workbook-to-pdf/)  
- [Cloud Storage Integration](/cloud-storage-integration/)  
- [Aspose.Cells Cloud SDK Overview](/sdks/)

---