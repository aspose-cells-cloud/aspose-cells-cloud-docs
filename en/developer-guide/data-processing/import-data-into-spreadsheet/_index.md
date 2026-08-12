---
title: "Aspose.Cells Cloud Data Import API – A cloud solution for automatically importing CSV, JSON, and XML data into Excel spreadsheets."
second_title: "Document"
ArticleTitle: "Multi‑Source Data Integration Excel Platform – Aspose.Cells Cloud Automated Data Import and Transformation API."
linktitle: "Import Data into Spreadsheet"
type: docs
url: /import-data-into-spreadsheet/
keywords: "Aspose Cells, data import API, CSV to Excel, JSON to Excel, XML to Excel, cloud spreadsheet, REST API"
description: "Import CSV, JSON, or XML data into Excel spreadsheets with Aspose.Cells Cloud REST API. Learn request format, parameters, sample SDK code, and error handling."
weight: 100
---

## Core Features

### Multi-Format Data Support

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a> Data Import**: Supports various delimiters and automatically detects encoding.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a> Data Handling**: Flattens complex JSON structures into Excel tables.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a> File Conversion**: Maps node data to Excel row and column structure.

## **Import Data into Spreadsheet API Description**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name     | Type   | Location         | Description                                                              |
| ------------------ | ------ | ---------------- | ------------------------------------------------------------------------ |
| datafile           | File   | FormData         | The data file (CSV, JSON, or XML) to be imported.                        |
| spreadsheet        | File   | FormData         | The target workbook that will receive the imported data.                 |
| worksheet          | string | Query            | Name of the worksheet where data will be placed.                         |
| startCell          | string | Query            | Top‑left cell (e.g., `A1`) that marks the start position for the import. |
| insert             | bool   | Query            | `true` to insert rows; `false` to overwrite existing data.               |
| convertNumericData | bool   | Query            | `true` to convert numeric strings to numbers during import.              |
| splitter           | string | Query            | Single‑character CSV delimiter (default is `,`).                         |
| outPath            | string | Query (optional) | Folder path where the updated workbook will be stored.                   |
| outStorageName     | string | Query (optional) | Name of the storage location for the output file.                        |
| fontsLocation      | string | Query (optional) | Path to a custom fonts folder, if required.                              |
| region             | string | Query (optional) | Spreadsheet region configuration (e.g., `en-US`).                        |
| password           | string | Query (optional) | Password for opening a protected workbook.                               |

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

**HTTP Status Codes**

| Code | Meaning               | Description                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applied successfully; response contains operation details. |
| 400  | Bad Request           | Missing or invalid parameters (e.g., unsupported file type).      |
| 401  | Unauthorized          | Invalid or missing JWT token.                                     |
| 413  | Payload Too Large     | Uploaded file exceeds size limit.                                 |
| 500  | Internal Server Error | Unexpected server error.                                          |

## Why You Should Use This API

- **Efficient data loading** – Enables bulk import of large datasets directly into a workbook without creating intermediate files.
- **Broad SDK support** – Provides client libraries for .NET, Java, PHP, Ruby, Node.js, Python, Go, and Perl, simplifying integration.
- **In‑memory processing** – Performs transformations in memory, which reduces temporary storage requirements.

## How to Use the Import Data into Spreadsheet API with SDKs

**Notes / Limitations:** The API supports up to 1 000 000 rows per import. Only comma is the default CSV delimiter; other single‑character delimiters can be specified via the `splitter` parameter. Large XML files may increase processing time.

For related operations such as exporting data or converting workbook formats, see the **Export Data** and **Convert Workbook** documentation.

### Import Data into Spreadsheet API Specification

The <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">Import Data into Spreadsheet API Specification</a> provides a publicly accessible programming interface, allowing REST interactions directly from your web browser.
You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away low‑level details, allowing you to import data into a spreadsheet worksheet with short code. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
