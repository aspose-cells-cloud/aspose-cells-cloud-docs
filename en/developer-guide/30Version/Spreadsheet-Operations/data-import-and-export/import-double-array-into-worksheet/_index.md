---
title: "Import Double Array into Excel Worksheet"
second_title: "Document"
linktitle: "Import double array"
type: docs
url: /import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, import double array, Excel API, cloud SDK"
description: "Learn how to import a double‑array into an Excel worksheet using Aspose.Cells Cloud REST API. Includes authentication, request format, parameters, sample XML/JSON, and response details."
weight: 20
ArticleTitle: "Import Double Array into Excel Worksheet – Aspose.Cells Cloud Guide"
---

This REST API **imports double‑array data** into an Excel worksheet.

> **Prerequisites:** You must have a valid JWT token before calling this API. See the authentication guide for details.

You send an HTTP request with **multipart** content (see [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart body contains the **ImportDoubleArrayOption** data and the second part contains the data file.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

#### **ImportDoubleArrayOption**

| Parameter Name       | Type       | Description                                                                                                |
| -------------------- | ---------- | ---------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Zero‑based index of the first row where the data will be placed.                                           |
| FirstColumn          | int        | Zero‑based index of the first column where the data will be placed.                                        |
| IsVertical           | boolean    | `true` / `false` – determines whether the array is inserted vertically (`true`) or horizontally (`false`). |
| Data                 | Double[]   | Array of double values to import.                                                                          |
| DestinationWorksheet | string     | Name of the target worksheet.                                                                              |
| IsInsert             | boolean    | `true` / `false` – if `true`, data is inserted; if `false`, existing cells are overwritten.                |
| ImportDataType       | string     | Type of data being imported (e.g., `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`).      |
| Source               | FileSource | Specifies the data file location when the `BatchData` parameter is null.                                   |

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

A successful request returns **HTTP 200** with a JSON payload similar to:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

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

## How to Use the PostImportData API with SDKs

### PostImportData API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}