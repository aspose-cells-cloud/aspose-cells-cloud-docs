---
url: /import-data-into-spreadsheet/
title: "Aspose.Cells Cloud Data Import API: CSV, JSON, XML to Excel"
date: 2024-05-15
secondtitle: "Document"
articletitle: "Multi‑Source Data Integration Excel Platform – Aspose.Cells Cloud Automated Data Import and Transformation API."
linktitle: "Import Data into Spreadsheet"
type: docs
keywords: "Aspose Cells, data import API, CSV to Excel, JSON to Excel, XML to Excel, cloud spreadsheet, REST API"
description: "Import CSV, JSON, and XML data into Excel spreadsheets using the Aspose.Cells Cloud REST API. Includes parameter reference, cURL examples, SDK code for .NET, Java, Python, and more."
weight: 100
---

## Overview

Aspose.Cells Cloud’s **Import Data into Spreadsheet API** enables efficient, secure import of structured data from CSV, JSON, and XML files directly into Excel workbooks—without intermediate file storage. Ideal for ETL pipelines, report generation, and data consolidation, the API handles large datasets (up to 1,000,000 rows), supports flexible positioning, and offers robust locale and formatting controls.

> **Note**: As of May 2024, this documentation covers API v4.0. For the latest version and release updates, see [Aspose.Cells Cloud Release Notes](https://blog.aspose.cloud/cells/).

---

## Core Features

### Multi-Format Data Support

- **[CSV Import](https://docs.fileformat.com/spreadsheet/csv/)**  
  Supports customizable delimiters (single-character), auto-detection of encoding, and optional numeric conversion.

- **[JSON Handling](https://docs.fileformat.com/web/json/)**  
  Automatically flattens nested structures into tabular form, mapping keys to columns and values to rows.

- **[XML Mapping](https://docs.fileformat.com/web/xml/)**  
  Converts XML nodes to Excel rows/columns based on element hierarchy and attribute structure.

---

## API Reference

### Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### Authentication

All requests require a valid [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include in the `Authorization` header as:

```http
Authorization: Bearer {access_token}
```

### Request Parameters

| Parameter Name     | Type   | Location   | Required | Default    | Description |
|--------------------|--------|------------|----------|------------|-------------|
| `datafile`         | File   | FormData   | Yes      | —          | Data file (CSV, JSON, or XML) to import. |
| `spreadsheet`      | File   | FormData   | Yes      | —          | Target Excel workbook. |
| `worksheet`        | string | Query      | Yes      | —          | Name of the worksheet to receive data. |
| `startcell`        | string | Query      | Yes      | `A1`       | Top-left cell for import (e.g., `B3`). |
| `insert`           | bool   | Query      | No       | `true`     | `true`: Insert rows; `false`: Overwrite existing data. |
| `convertNumericData` | bool | Query    | No       | `true`     | `true`: Convert numeric strings to numbers. |
| `splitter`         | string | Query      | No       | `,`        | Single-character CSV delimiter (e.g., `;`, `|`). |
| `outPath`          | string | Query      | No       | `null`     | Folder path for saving the updated workbook. |
| `outStorageName`   | string | Query      | No       | `null`     | Storage name for output file (if using cloud storage). |
| `fontsLocation`    | string | Query      | No       | `null`     | Custom fonts directory path. |
| `region`           | string | Query      | No       | `en-US`    | Locale setting (e.g., `fr-FR`, `de-DE`). Affects date/number formatting. |
| `password`         | string | Query      | No       | `null`     | Password to open password-protected workbooks. |

---

## Response

```json
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "application/vnd.openxmlformats-officedocument.spreadsheetml.sheet",
  "fileDownloadName": "imported-workbook.xlsx"
}
```

### HTTP Status Codes

| Code | Meaning               | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Import successful; workbook returned in response. |
| 400  | Bad Request           | Invalid parameter, unsupported file format, or malformed request. |
| 401  | Unauthorized          | Missing or invalid JWT token. |
| 404  | Not Found             | Source file (data or spreadsheet) not found in storage. |
| 413  | Payload Too Large     | Uploaded file exceeds size limit (50 MB recommended max). |
| 500  | Internal Server Error | Unexpected error during processing. |

---

## Usage Examples

### cURL Request

```bash
curl -X PUT \
  "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A2&insert=true&convertNumericData=true&splitter=," \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/template.xlsx" \
  -o imported-workbook.xlsx
```

> **Tip**: Use `-o` to save the response directly to a file.

### SDK Examples

Using an SDK (e.g., Python) simplifies authentication and file handling. Below is a minimal example for Python:

```python
from asposecellscloud import CellsApi, Configuration
from asposecellscloud.models import ImportDataRequest

config = Configuration(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
api = CellsApi(config)

request = ImportDataRequest(
    data_file="data.csv",
    spreadsheet="workbook.xlsx",
    worksheet="Sheet1",
    start_cell="A1",
    insert=True,
    convert_numeric_data=True
)

response = api.cells_import_data_into_spreadsheet(request)
print("Workbook saved to:", response.file_download_name)
```

> **SDKs Available For**: .NET, Java, PHP, Ruby, Node.js, Python, Go, Perl  
> **GitHub Repository**: [aspose-cells-cloud](https://github.com/aspose-cells-cloud)

---

## Notes & Limitations

- **Row Limit**: Up to 1,000,000 rows per import.
- **CSV Delimiter**: Only single-character delimiters are supported. Use the `splitter` parameter for non-default separators.
- **Large XML Files**: Complex or large XML structures may increase processing time significantly.
- **Memory Use**: All processing occurs in-memory—ensure sufficient memory allocation for large workbooks.
- **File Size**: We recommend keeping individual files under 50 MB for optimal performance.

---

## Related Operations

- **[Export Data](/export-data)**  
  Extract data from Excel to CSV, JSON, or XML.

- **[Convert Workbook](/convert-workbook)**  
  Transform Excel files between formats (XLSX, ODS, PDF, etc.).

---

## Best Practices

- ✅ **Validate data format** before upload (e.g., correct JSON structure, well-formed XML).
- ✅ **Specify `region`** consistently when parsing dates or numbers (e.g., `en-US` for MM/DD/YYYY).
- ✅ **Use `insert=false`** to avoid unintended row expansion when overwriting.
- ✅ **Test with sample files** first—especially for nested JSON or hierarchical XML.

---

*Last updated: May 15, 2024*