---
title: "Import Batch Data into Excel Worksheet"
second_title: "Document"
linktitle: "Import batch data"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, Cloud API, import batch data, Excel"
description: "Learn how to import batch data (CSV, JSON, XML, arrays) into an Excel worksheet using Aspose.Cells Cloud REST API. Includes authentication, request/response examples, SDK snippets, and error handling."
weight: 19
ArticleTitle: "Import Batch Data into Excel Worksheet – Aspose.Cells Cloud Documentation"
---

This REST API **imports batch data** into an Excel worksheet.

The operation uses an HTTP request with multipart content (see [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart payload contains the **ImportBatchDataOption** object, and the second part carries the data file.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

**Prerequisites**  
- A valid OAuth2 access token (see the authentication guide).  
- The target workbook must already exist in the cloud storage.  
- The `{name}` placeholder represents the workbook file name, including its extension (e.g., `Report.xlsx`).  

**Request parameters**  
| Parameter | Location | Description |
|-----------|----------|-------------|
| `name` | Path | Name of the workbook to which the data will be imported. |
| `importBatchDataOption` | Body (first part) | JSON or XML representation of the `ImportBatchDataOption` object. |
| `file` | Body (second part) | The data file (CSV, JSON, XML, etc.) to be imported. |
| `folder` | Query (optional) | Cloud folder path where the workbook resides. |
| `storageName` | Query (optional) | Name of the storage to use. |

**Response schema**  
| Field | Type | Description |
|-------|------|-------------|
| `code` | `int` | HTTP status code of the operation. |
| `status` | `string` | Short description of the result (`OK`, `Error`, etc.). |
| `data` | `object` | Details of the import operation, including the number of rows/columns affected. |
| `error` | `object` (optional) | Error information when the request fails. |

**Status‑code table**

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Batch data imported successfully. |
| 202 | Accepted | Request accepted for processing (asynchronous). |
| 400 | Bad Request | Invalid parameters or malformed request body. |
| 401 | Unauthorized | Authentication failed or token missing. |
| 404 | Not Found | Specified workbook or file not found. |
| 500 | Internal Server Error | Unexpected server error. |

**Multipart request example**

```http
POST https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/importdata HTTP/1.1
Authorization: Bearer {access_token}
Content-Type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW

------WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="importBatchDataOption"
Content-Type: application/xml

<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>

------WebKitFormBoundary7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="file"; filename="Array_int_xml.txt"
Content-Type: text/plain

1,2,3,4,5
6,7,8,9,10

------WebKitFormBoundary7MA4YWxkTrZu0gW--
```

**Response example (JSON)**

```json
{
  "code": 200,
  "status": "OK",
  "data": {
    "importedRows": 2,
    "importedColumns": 5,
    "worksheet": "Sheet1"
  }
}
```

The important parameters are described in the tables below.

### ImportBatchDataOption

| Parameter Name           | Type              | Description                                                                                                                                                                                   |
| ------------------------ | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**            | `List<CellValue>` | Collection of cell values to be written directly.                                                                                                                                             |
| **DestinationWorksheet** | `string`          | Name of the worksheet where the data will be imported.                                                                                                                                        |
| **IsInsert**             | `bool`            | When `true`, the data is inserted and existing cells are shifted; when `false`, the data overwrites existing cells.                                                                           |
| **ImportDataType**       | `string`          | Format of the data to import. Allowed values: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | `FileSource`      | Specifies the location of the data file when **BatchData** is `null`.                                                                                                                         |

### CellValue

| Parameter Name  | Type     | Description                                               |
| --------------- | -------- | --------------------------------------------------------- |
| **rowIndex**    | `int`    | Zero‑based row index of the target cell.                  |
| **columnIndex** | `int`    | Zero‑based column index of the target cell.               |
| **type**        | `string` | Data type of the value (e.g., `int`, `double`, `string`). |
| **value**       | `string` | The actual value to write into the cell.                  |
| **style**       | `Style`  | Optional styling information for the cell.                |

### FileSource

| Parameter Name     | Type     | Description                                                                |
| ------------------ | -------- | -------------------------------------------------------------------------- |
| **FileSourceType** | `string` | Source of the file: `InMemoryFiles`, `CloudFileSystem`, or `RequestFiles`. |
| **FilePath**       | `string` | Path or identifier of the file within the chosen source.                   |

### Example (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

**Notes**  
- Maximum batch size is 10 MB per request.  
- Supported data types depend on the chosen `ImportDataType`.  

## Cloud SDK Family

Using an SDK is the fastest way to integrate this functionality. SDKs handle low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with different SDKs:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}