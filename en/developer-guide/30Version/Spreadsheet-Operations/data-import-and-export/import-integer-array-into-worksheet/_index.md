---
title: "Import Integer Array into Excel Worksheet"
linktitle: "Import integer array"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, import integer array, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "Learn how to import an integer array into an Excel worksheet using Aspose.Cells Cloud REST API. Includes request syntax, parameters, sample code for multiple SDKs, and response details."
weight: 30
ArticleTitle: "Import Integer Array into Excel Worksheet – Aspose.Cells Cloud API"
---

This REST API imports an integer array into an Excel worksheet.

The request must be an HTTP **POST** with multipart content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). The first part of the multipart body contains the **ImportIntegerArrayOption** JSON payload, and the second part contains the source data file (e.g., a CSV or binary Excel file).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

Both endpoints accept the same multipart payload. The first endpoint works with a generic import operation, while the second targets a specific workbook identified by `{name}`.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

### ImportIntegerArrayOption

| Parameter Name           | Type       | Description                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | Zero‑based index of the first row where the data will be placed.                                                                                                                               |
| **FirstColumn**          | int        | Zero‑based index of the first column where the data will be placed.                                                                                                                            |
| **IsVertical**           | boolean    | `true` to insert the array vertically (down a column); `false` to insert it horizontally (across a row).                                                                                       |
| **Data**                 | Integer[]  | The integer array to be imported.                                                                                                                                                              |
| **DestinationWorksheet** | string     | Name of the worksheet that will receive the data.                                                                                                                                              |
| **IsInsert**             | boolean    | `true` to insert rows/columns before writing the data; `false` to overwrite existing cells.                                                                                                    |
| **ImportDataType**       | string     | Type of the data being imported. Valid values: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | Indicates the position of the data file when the **BatchData** parameter is `null`.                                                                                                            |

#### Example Request Body

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
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


## How to Use the PostImportData API with SDKs

### PostImportData API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to integrate this functionality. SDKs abstract low‑level details, letting you focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}