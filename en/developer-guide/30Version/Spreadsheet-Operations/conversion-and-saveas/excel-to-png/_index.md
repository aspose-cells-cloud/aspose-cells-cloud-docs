---
title: "Excel to PNG"
second_title: "Document"
linktitle: "Excel to PNG"
type: docs
url: convert-excel-file-to-png-file/
keywords: "Excel to PNG, Aspose.Cells Cloud, REST API, spreadsheet conversion, PNG format"
description: "Convert Excel spreadsheets to PNG images using Aspose.Cells Cloud REST API. Supports multiple SDKs and provides detailed examples for various programming languages."
weight: 90
---

This REST API converts a spreadsheet file to PNG format.

**Query Parameter**

| Parameter Name          | Type   | Description                                                                                         |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------|
| password                 | string | The password required to open the Excel file.                                                       |
| storageName              | string | The name of the storage where the file is located.                                                  |
| checkExcelRestriction    | bool   | Determines whether to check Excel file restrictions when modifying cells or related objects.      |

**Request Body Parameter**

| Parameter Name | Type      | Description                                                                 |
|----------------|-----------|-----------------------------------------------------------------------------|
| datafile       | data file | The spreadsheet file included in the first part of the multipart request. |

**Response**

[FileInfo](/cells/file-info/)

## REST API Specification

| **API**                | **Type** | **Description**                     | **Swagger Link** |
|------------------------|----------|-------------------------------------|------------------|
| /cells/convert/png     | POST     | Convert a spreadsheet to a PNG file.| [PostConvertWorkbookToPNG](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs Implementing Similar Functions

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Saves an Excel file as CSV (or other formats) with additional settings and stores the result.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converts an Excel file to CSV (or other formats) with optional parameters and returns the result in the response.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Retrieves an Excel file and can convert it to CSV (or other formats) on the fly.