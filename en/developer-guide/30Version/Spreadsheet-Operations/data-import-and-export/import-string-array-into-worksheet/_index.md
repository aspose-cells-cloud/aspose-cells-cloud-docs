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
keywords: "Aspose.Cells Cloud, import string array, Excel REST API, multipart upload, worksheet data import"
description: "Learn how to import a string array into an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes request format, parameters, and SDK examples."
weight: 40
---

This REST API imports string‑array data into an Excel worksheet.

**Authentication** – All Aspose.Cells Cloud requests require a valid OAuth 2.0 access token. Include it in the `Authorization` header as `Bearer <access_token>`.

The request uses multipart HTTP content (see [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) or [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
The first part of the multipart body contains an **ImportStringArrayOption** payload; the second part contains the source data file.

### Step‑by‑step guide
1. **Obtain an access token** (OAuth 2.0 client credentials flow).  
2. **Prepare the `ImportStringArrayOption`** XML or JSON payload.  
3. **Create a multipart body** – part 1: the payload; part 2: the data file.  
4. **Send a POST request** to the endpoint shown below.  
5. **Check the response** for success or error details.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

The important parameters are described in the following table:

**ImportStringArrayOption**

| Parameter Name       | Type    | Description                                                                                                                                                     |
|----------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FirstRow             | int     | The starting row index (1‑based) where the data will be placed.                                                                                                 |
| FirstColumn          | int     | The starting column index (1‑based) where the data will be placed.                                                                                              |
| IsVertical           | boolean | `true` to insert data vertically; `false` to insert horizontally.                                                                                              |
| Data                 | String[]| The string array to be imported.                                                                                                                                |
| DestinationWorksheet | string  | The name of the worksheet that will receive the data.                                                                                                          |
| IsInsert             | boolean | `true` to insert rows/columns (shifting existing cells); `false` to overwrite existing cells.                                                                   |
| ImportDataType       | string  | Type of data being imported (e.g., `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Describes where the data file resides when **BatchData** is null (e.g., `CloudFileSystem`, `LocalFile`). Required if `BatchData` is not supplied.               |

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

### Common Errors & Troubleshooting

| HTTP Status | Cause                              | Remedy                                                                                         |
|-------------|------------------------------------|------------------------------------------------------------------------------------------------|
| 401         | Missing or invalid access token    | Ensure the `Authorization: Bearer <token>` header is present and the token is still valid.    |
| 400         | Required parameter omitted (`Source` or `FirstRow`) | Verify that all mandatory fields are supplied and correctly typed.                           |
| 415         | Incorrect content‑type for multipart body | Use `multipart/form-data` with proper boundary delimiters.                                     |
| 500         | Server‑side processing error       | Check the payload for malformed XML/JSON and confirm that the file referenced in `Source` exists. |

## Cloud SDK Family

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