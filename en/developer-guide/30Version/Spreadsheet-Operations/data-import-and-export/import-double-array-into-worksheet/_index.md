---
title: "Import Double Array into Excel Worksheet"
second_title: "Developer Guide"
linktitle: "Import double array"
type: docs
url: /import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, import double array, Excel API, cloud SDK"
description: "Import double array into Excel worksheet via Aspose.Cells Cloud API with multipart request and ImportDoubleArrayOption."
weight: 100
ArticleTitle: "Import Double Array into Excel Worksheet – Aspose.Cells Cloud Guide"
---
The **PostImport** API (`POST https://api.aspose.cloud/v3.0/cells/import`) enables importing double-array data into an Excel worksheet via Aspose.Cells Cloud, supporting output in multiple formats such as XLSX, PDF, CSV, and image types, with optional parameters like password protection and regional settings for flexible data import workflows.

You send an HTTP request with **multipart** content (see [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart body contains the **ImportDoubleArrayOption** data and the second part contains the data file.

## The Post Import Web API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| outFormat | String | Query | The output data file format.(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers) |
| password | String | Query | The password needed to open an Excel file. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |
| region | String | Query | The regional settings for workbook. |

#### **ImportDoubleArrayOption**


#### Example (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### Example (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### Response

```json
[
  {
    "Name": "FilesResult",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FilesResult"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

A successful request returns **HTTP 200** with a JSON payload similar to:


Possible status codes:

| Code | Meaning                                 |
| ---- | --------------------------------------- |
| 200  | Import succeeded                        |
| 400  | Bad request – missing or invalid data   |
| 401  | Unauthorized – invalid or missing token |
| 500  | Internal server error                   |

### Error Handling

When an error occurs the API returns a JSON object containing the error code and a descriptive message. Example for an unauthorized request:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

For more information on related import operations, see the “Import 2‑Dimension Double Array” and “Import Integer Array” documentation pages.

## How to Use the Post Import API with SDKs?

### Post Import API Specification

The <a href="https://reference.aspose.cloud/cells/#/LightCells/PostImport" rel="noopener noreferrer">Post Import API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.
