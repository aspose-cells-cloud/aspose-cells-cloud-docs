---
title: "Export Excel Range to PDF, PNG, CSV – Aspose.Cells Cloud API"
date: 2024-05-15
lastmod: 2024-05-15
description: "Export Excel ranges to PDF, PNG, SVG, CSV, and more via Aspose.Cells Cloud API—no local download needed."
linktitle: "Export Range as Format"
type: docs
url: /export-range-as-format/
keywords: "Aspose.Cells Cloud, export Excel range, PDF, PNG, CSV, SVG, cloud API, spreadsheet conversion, range to format"
weight: 100
ArticleTitle: "Export Excel Range to PDF, PNG, CSV, SVG via Aspose.Cells Cloud API"
---
The **ExportRangeAsFormat** API (`GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}`) in Aspose.Cells Cloud converts a specified range of a cloud-hosted Excel workbook—such as A1:C12 in a given worksheet—to a target format (e.g., PDF, PNG, SVG, CSV) without downloading the file locally, enabling efficient, server-side conversion directly from cloud storage.

## The Export Range as Format Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### Security & Authentication

All API requests require [JWT token–based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include the token in the `Authorization` header:

```http
Authorization: Bearer <access_token>
```

---

### **Request Parameters:**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | (Required) The name of the workbook file to be retrieved. |
| worksheet | String | Path | worksheet name |
| range | String | Path | range: A1:C12 |
| format | String | Query | (Required) The desired format  (e.g., "png", "Pdf", "svg"). |
| folder | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

### Response

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
Content-Length: 0
```

The API returns a binary stream of the converted file (MIME type matches the requested format). When `outPath` is provided, the file is saved directly to cloud storage, and the response body is empty with HTTP status `200 OK`.

#### Example Response (Stream Output)

| Field                 | Type   | Description                                                        |
| :-------------------- | :----- | :----------------------------------------------------------------- |
| `Content-Type`        | string | MIME type (e.g., `application/pdf`, `image/png`)                   |
| `Content-Disposition` | string | Inline or attachment with filename (e.g., `filename="A1_C12.pdf"`) |
| Body                  | binary | File content as byte stream                                        |

#### Example Response (Cloud Storage Save)

When `outPath` is used and the operation succeeds, the response is:


---

Convert a specific range within a cloud-hosted Excel or spreadsheet workbook to another format—PDF, PNG, SVG, CSV, and more—without downloading the file locally. The output can be saved to cloud storage or returned as a binary stream.

### REST API Endpoint
#### Path Parameters

| Parameter   | Type   | Required | Description                                              |
| :---------- | :----- | :------- | :------------------------------------------------------- |
| `name`      | string | Yes      | Name of the workbook file in cloud storage.              |
| `worksheet` | string | Yes      | Name of the worksheet containing the range.              |
| `range`     | string | Yes      | Cell range identifier (e.g., `A1:C12`, `Sheet2!B2:D20`). |

#### Query Parameters

| Parameter        | Type    | Required | Description                                                                                                                                                            |
| :--------------- | :------ | :------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `format`         | string  | Yes      | Target output format (e.g., `pdf`, `png`, `svg`, `csv`, `xlsx`). Case-insensitive.                                                                                     |
| `folder`         | string  | No       | Folder path containing the workbook. Defaults to root.                                                                                                                 |
| `storageName`    | string  | No       | Cloud storage name. Omit to use default storage.                                                                                                                       |
| `outPath`        | string  | No       | Absolute path in cloud storage where the output file will be saved. Requires `outStorageName` if non-default storage is used.                                          |
| `outStorageName` | string  | No       | Storage name for the output file. Required when `outPath` specifies a non-default storage.                                                                             |
| `fontsLocation`  | string  | No       | Custom folder path for fonts used during rendering.                                                                                                                    |
| `AutoRowsFit`    | boolean | No       | Whether to auto-fit rows in the range before conversion. Default: `false`.                                                                                             |
| `AutoColumnsFit` | boolean | No       | Whether to auto-fit columns in the range before conversion. Default: `false`.                                                                                          |
| `region`         | string  | No       | Locale setting (e.g., `en-US`, `fr-FR`). Mirrors Excel’s **File > Options > Advanced > International** setting. Affects number, date, and formula evaluation behavior. |
| `password`       | string  | No       | Password to open the protected workbook.                                                                                                                               |

> **Note**: If `outPath` is specified, `outStorageName` must be provided when the output should reside in a non-default storage.

---

### HTTP Status Codes

| Code  | Meaning               | Description                                                                     |
| :---- | :-------------------- | :------------------------------------------------------------------------------ |
| `200` | OK                    | Conversion successful.                                                          |
| `400` | Bad Request           | Invalid or missing parameters (e.g., unsupported `format`, malformed range).    |
| `401` | Unauthorized          | Invalid, expired, or missing JWT token.                                         |
| `403` | Forbidden             | Access denied to the workbook (e.g., wrong password, insufficient permissions). |
| `404` | Not Found             | Workbook, worksheet, or range not found.                                        |
| `500` | Internal Server Error | Unexpected error during conversion (e.g., unsupported feature in range).        |

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

## How to Use the Export Range as Format API with SDKs?

### Export Range as Format API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">Export Range as Format API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

SDKs for 8+ languages simplify integration, handle authentication, and manage serialization. See the [Aspose.Cells Cloud GitHub organization](https://github.com/aspose-cells-cloud) for official SDKs.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="2" tabID="1" tabName1="PHP" tabName2="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
