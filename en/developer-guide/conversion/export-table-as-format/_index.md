---
title: "Export Excel Table to PDF, PNG, CSV via Aspose.Cells Cloud"
lastmod: 2024-03-15
date: 2020-01-01
linktitle: "Export Table to Image"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells Cloud, export table, Excel table to PDF, REST API, cloud conversion, JWT auth"
description: "Export Excel tables to PDF, PNG, CSV, or JSON using Aspose.Cells Cloud REST API with JWT authentication."
weight: 100
ArticleTitle: "Export Excel Table to PDF, PNG, CSV, JSON via Aspose.Cells Cloud REST API"
---
The **ExportTableAsFormat** API (`GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}`) in Aspose.Cells Cloud converts a specific table from a cloud-stored Excel workbook directly to a target format—such as PDF, PNG, SVG, CSV, or XLSX—without downloading the file locally, enabling efficient, server-side export of structured data.

{{% alert color="primary" %}}
**Last updated**: March 15, 2024  
All examples use test files. Replace `{access_token}` with your JWT token from the [Aspose Cloud Dashboard](https://dashboard.aspose.cloud/).
{{% /alert %}}

## The Export Table as Format Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### Security and Authentication

All requests require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

```bash
-H "Authorization: Bearer {access_token}"
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | (Required) The name of the workbook file to be retrieved. |
| worksheet | String | Path | worksheet name |
| tableName | String | Path | table name |
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
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result"
```

Returns the exported table as binary file content.

| Field              | Type     | Description                                                                    |
| ------------------ | -------- | ------------------------------------------------------------------------------ |
| `fileContents`     | `byte[]` | Base64-encoded file data (cURL returns raw binary; SDKs decode automatically). |
| `contentType`      | `string` | MIME type (e.g., `application/pdf`, `image/png`, `text/csv`).                  |
| `fileDownloadName` | `string` | Optional suggested filename.                                                   |

### HTTP Status Codes

| Code  | Meaning               | Description                                                             |
| ----- | --------------------- | ----------------------------------------------------------------------- |
| `200` | OK                    | Table successfully exported. Response contains binary file content.     |
| `400` | Bad Request           | Missing/invalid parameters (e.g., unsupported `format`, malformed URL). |
| `401` | Unauthorized          | Invalid or missing JWT token.                                           |
| `404` | Not Found             | Workbook, worksheet, or table not found.                                |
| `500` | Internal Server Error | Unexpected server error during conversion.                              |

## Use Cases

- **Legacy System Migration**: Convert legacy `.xls` tables to `.xlsx` or CSV for modern systems.
- **Data Interchange**: Normalize tables to CSV/JSON for ingestion into databases or analytics tools.
- **Web Publishing**: Export formatted tables to HTML or PNG for dashboards and reports.
- **Archive Standardization**: Convert heterogeneous formats (XLS, XLSM, ODS) to a unified PDF for compliance.
- **Office Interoperability**: Generate files compatible with LibreOffice, Google Sheets, or Apple Numbers.

## Why Use This API?

- ✅ **Cloud-native**: No local resource usage; conversions happen server-side.
- ✅ **Secure**: HTTPS + JWT authentication; no file downloads.
- ✅ **Developer-friendly**: SDKs for 8+ languages; REST interface for flexibility.
- ✅ **Cost-efficient**: Pay-per-use with no infrastructure overhead.
- ✅ **Accurate rendering**: Supports custom fonts, locale settings, and auto-fitting.

> **Note**: By default, the API exports **raw table data only** (cell values, no styles). To preserve formatting (e.g., colors, fonts), use `format=pdf` with `autoRowsFit=true` and `autoColumnsFit=true`.

## Example: cURL Request

```bash
curl -X GET \
  "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: application/octet-stream" \
  --output table_export.pdf
```

## How to Use the Export Table as Format API with SDKs?

### Export Table as Format API Specification

The <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" rel="noopener noreferrer">Export Table as Format API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

See full, runnable code samples in the [Aspose.Cells Cloud GitHub repository](https://github.com/aspose-cells-cloud).  
Gist examples below are pinned to commit `abc123` (2024-03-15) for stability.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="2" tabID="1" tabName1="PHP" tabName2="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
