---
title: "Export Worksheet – Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
date: 2024-05-10T00:00:00Z
lastmod: 2024-06-01T14:30:00Z
linktitle: "Export Worksheet"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, export worksheet, cloud API, PDF, PNG, SVG, CSV, Excel conversion"
description: "Export Excel worksheet to PDF, PNG, SVG, CSV via Aspose.Cells Cloud API using a single GET request."
weight: 100
ArticleTitle: "Export Worksheet to PDF, PNG, SVG, CSV via Aspose.Cells Cloud API"
---

The **ExportWorksheetAsFormat** API (`GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}`) in Aspose.Cells Cloud converts a specific worksheet from a cloud-stored workbook directly into a target format—such as PDF, PNG, or SVG—without requiring local download, enabling efficient, server-side export of structured spreadsheet data.

## **Export Worksheet as Format API**

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Authentication**

The Aspose.Cells Cloud APIs require <a href="https://docs.aspose.cloud/cells/getting-started/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Request Parameters**

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | (Required) The name of the workbook file to be retrieved. |
| worksheet | String | Path | - |
| format | String | Query | (Required) The desired pdf or image format  (e.g., "png", "Pdf", "svg"). |
| folder | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| storageName | String | Query | (Optional) The name of the storage if using custom cloud storage. Use default storage if omitted. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| AutoRowsFit | Boolean | Query | (Optional) Autofits all rows in worksheets. |
| AutoColumnsFit | Boolean | Query | (Optional) Autofits all columns in worksheets. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

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
| 400 | Bad Request | Invalid url. |
| 401 | Unauthorized | Authentication has failed, or no credentials were provided. |
| 404 | Not Found | Source file not accessible. |
| 500 | Server Error | The spreadsheet has encountered an anomaly in obtaining conversion data. |

Returns a binary file stream of the requested format.

### **cURL Example**

```bash
curl -X GET \
  "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf&region=en-US" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: application/octet-stream" \
  --output worksheet.pdf
```

### **Use Cases**

- **Legacy System Migration** – Convert thousands of legacy XLS files to XLSX or CSV for modern systems.
- **Archive Standardization** – Normalize various spreadsheet formats (XLS, XLSM, ODS, CSV) to a single archival format.
- **Office Suite Interoperability** – Generate files compatible with LibreOffice, Google Sheets, or Apple Numbers.
- **Data Source Normalization** – Extract and convert worksheets to CSV or JSON for database ingestion.
- **Web Publishing** – Convert financial models to HTML or PDF for dashboard integration.

### **Key Benefits**

- **Cloud-Native Conversion** – Processes files directly in cloud storage; no local download/upload required.
- **Format Versatility** – Supports PDF, PNG, SVG, CSV, and other common formats.
- **Simplified Workflow** – Direct conversion from cloud-stored workbooks with minimal code.
- **Multi-Language SDK Support** – Client libraries for C#, Java, Python, PHP, Ruby, Node.js, Perl, and Go.

### **SDK Examples**

See the [Export Worksheet as Format API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) for interactive testing.