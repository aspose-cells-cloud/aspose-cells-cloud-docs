---
title: "Import String Array into Excel Worksheet – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Import string array"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, import string array, Excel REST API, multipart upload, worksheet data import, cloud SDK"
description: "Learn how to import a string array into an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes request format, parameters, and SDK examples."
weight: 40
ArticleTitle: "Import String Array into Excel Worksheet – Aspose.Cells Cloud"
---

Importing a string array into an Excel worksheet is a common task when populating spreadsheets with list‑based data. This operation is useful for scenarios such as loading configuration values, transferring data from external sources, or initializing worksheets with predefined string collections.

## REST API

**Prerequisites:**  
- A valid JWT token obtained via the Aspose.Cells Cloud authentication flow.  
- An existing workbook (or the ability to create one) in your Aspose Cloud storage.  
- The appropriate SDK version that supports the `ImportStringArrayOption` model.

This REST API imports string‑array data into an Excel worksheet.

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### **Request Parameters**

The request uses multipart HTTP content (see [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart body contains an **ImportStringArrayOption** payload; the second part contains the source data file.

The important parameters are described in the following table:

<caption>ImportStringArrayOption parameters</caption>
### **ImportStringArrayOption**

| Parameter Name       | Type       | Description                                                                                                                                                                         |
| -------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | The starting row index (1‑based) where the data will be placed.                                                                                                                     |
| FirstColumn          | int        | The starting column index (1‑based) where the data will be placed.                                                                                                                  |
| IsVertical           | boolean    | `true` to insert data vertically; `false` to insert horizontally.                                                                                                                   |
| Data                 | String[]   | The string array to be imported.                                                                                                                                                    |
| DestinationWorksheet | string     | The name of the worksheet that will receive the data.                                                                                                                               |
| IsInsert             | boolean    | `true` to insert rows/columns (shifting existing cells); `false` to overwrite existing cells.                                                                                       |
| ImportDataType       | string     | Type of data being imported (e.g., `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Describes where the data file resides when **BatchData** is null (e.g., `CloudFileSystem`, `LocalFile`). Required if `BatchData` is not supplied.                                   |

### Example

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
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

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}