---
title: "Export Worksheet – Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
date: 2024-05-10T00:00:00Z
lastmod: 2024-06-01T14:30:00Z
linktitle: "Export Worksheet"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, export worksheet, cloud API, PDF, PNG, SVG, CSV, Excel conversion"
description: "Convert a worksheet stored in Aspose.Cells Cloud to PDF, PNG, SVG, CSV, or other formats via a single GET request. Includes code samples for C#, Java, Python, and more."
weight: 100
---

Export a cloud spreadsheet/Excel worksheet to another format file using the Aspose.Cells Cloud Web API.

## **Export Worksheet as Format API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Authentication**

The Aspose.Cells Cloud APIs require <a href="https://docs.aspose.cloud/cells/getting-started/" rel="noopener noreferrer">JWT token-based authentication</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Request Parameters**

| Parameter Name     | Type      | Location           | Description                                                                             |
| :----------------- | :-------- | :----------------- | :-------------------------------------------------------------------------------------- |
| **name**           | `string`  | Path _(required)_  | The name of the workbook file to be retrieved.                                          |
| **worksheet**      | `string`  | Path _(required)_  | The name of the worksheet to convert.                                                   |
| **format**         | `string`  | Query _(required)_ | The desired output format (e.g., `"png"`, `"pdf"`, `"svg"`, `"csv"`). Case-insensitive. |
| **folder**         | `string`  | Query _(optional)_ | The folder path where the workbook is stored. Defaults to `null` (root).                |
| **storageName**    | `string`  | Query _(optional)_ | The name of the custom cloud storage. Uses default storage if omitted.                  |
| **outPath**        | `string`  | Query _(optional)_ | The folder path where the output file will be saved. Defaults to `null`.                |
| **outStorageName** | `string`  | Query _(optional)_ | The name of the storage for the output file.                                            |
| **fontsLocation**  | `string`  | Query _(optional)_ | Path to custom fonts for rendering.                                                     |
| **region**         | `string`  | Query _(optional)_ | Spreadsheet region/locale (e.g., `"en-US"`, `"fr-FR"`). Affects number/date formatting. |
| **password**       | `string`  | Query _(optional)_ | Password to open the protected spreadsheet.                                             |
| **AutoRowsFit**    | `boolean` | Query _(optional)_ | Whether to autofit all rows before conversion.                                          |
| **AutoColumnsFit** | `boolean` | Query _(optional)_ | Whether to autofit all columns before conversion.                                       |

### **Response**

Returns a binary file stream of the requested format.

| Status Code | Meaning               | Description                                                       |
| :---------- | :-------------------- | :---------------------------------------------------------------- |
| `200`       | OK                    | Conversion successful; response body contains the converted file. |
| `400`       | Bad Request           | Invalid or missing parameters (e.g., unsupported format).         |
| `401`       | Unauthorized          | Invalid or missing JWT token.                                     |
| `404`       | Not Found             | Workbook or worksheet not found in storage.                       |
| `500`       | Internal Server Error | Unexpected server error during conversion.                        |

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
