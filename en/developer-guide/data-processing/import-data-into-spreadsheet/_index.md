---
url: /import-data-into-spreadsheet/
title: "Aspose.Cells Cloud Data Import API: CSV, JSON, XML to Excel"
secondtitle: "Document"
articletitle: "Multi‑Source Data Integration Excel Platform – Aspose.Cells Cloud Automated Data Import and Transformation API."
linktitle: "Import Data into Spreadsheet"
type: docs
keywords: "Aspose Cells, data import API, CSV to Excel, JSON to Excel, XML to Excel, cloud spreadsheet, REST API"
description: "Import CSV, JSON, XML into Excel using Aspose.Cells Cloud REST API with large dataset support and flexible positioning."
weight: 100
---
The **ImportDataIntoSpreadsheet** API (`PUT https://api.aspose.cloud/v4.0/cells/import/data`) in Aspose.Cells Cloud enables secure, direct import of structured data from CSV, JSON, or XML files into Excel workbooks without intermediate storage, supporting large datasets and precise placement via `worksheet` and `startcell` parameters to streamline ETL, reporting, and data consolidation workflows.

## Overview

Aspose.Cells Cloud’s **Import Data into Spreadsheet API** enables efficient, secure import of structured data from CSV, JSON, and XML files directly into Excel workbooks—without intermediate file storage. Ideal for ETL pipelines, report generation, and data consolidation, the API handles large datasets (up to 1,000,000 rows), supports flexible positioning, and offers robust locale and formatting controls.

> **Note**: As of May 2024, this documentation covers API v4.0. For the latest version and release updates, see [Aspose.Cells Cloud Release Notes](https://blog.aspose.cloud/cells/).

---

## Core Features

- **[CSV Import](https://docs.fileformat.com/spreadsheet/csv/)**  
  Supports customizable delimiters (single-character), auto-detection of encoding, and optional numeric conversion.

- **[JSON Handling](https://docs.fileformat.com/web/json/)**  
  Automatically flattens nested structures into tabular form, mapping keys to columns and values to rows.

- **[XML Mapping](https://docs.fileformat.com/web/xml/)**  
  Converts XML nodes to Excel rows/columns based on element hierarchy and attribute structure.

---

## The Import Data Into Spreadsheet Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### Authentication

All requests require a valid [JWT token](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/). Include in the `Authorization` header as:

```http
Authorization: Bearer {access_token}
```

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| datafile | File | FormData | Upload data file. |
| Spreadsheet | File | FormData | Upload spreadsheet file. |
| worksheet | String | Query | Specify the worksheet for importing data |
| startcell | String | Query | Specify the starting position for importing data |
| insert | Boolean | Query | The specified import data is for insertion and overwrite. |
| convertNumericData | Boolean | Query | Specify whether to convert numerical data |
| splitter | String | Query | Specify the delimiter for the CSV format. |
| outPath | String | Query | (Optional) The folder path where the workbook is stored. The default is null. |
| outStorageName | String | Query | Output file Storage Name. |
| fontsLocation | String | Query | Use Custom fonts. |
| region | String | Query | Spreadsheet region/language setting (e.g., `en-US`, `fr-FR`). Influences number formatting, date parsing, and locale‑specific behavior. |
| password | String | Query | The password for opening spreadsheet file. |

---

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

### HTTP Status Codes

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Import successful; workbook returned in response.                 |
| 400  | Bad Request           | Invalid parameter, unsupported file format, or malformed request. |
| 401  | Unauthorized          | Missing or invalid JWT token.                                     |
| 404  | Not Found             | Source file (data or spreadsheet) not found in storage.           |
| 413  | Payload Too Large     | Uploaded file exceeds size limit (50 MB recommended max).         |
| 500  | Internal Server Error | Unexpected error during processing.                               |

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
