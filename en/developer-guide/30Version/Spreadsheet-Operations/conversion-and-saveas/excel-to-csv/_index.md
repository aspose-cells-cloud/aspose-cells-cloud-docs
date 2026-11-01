---
title: "Excel to CSV"
second_title: "Developer Guide"
linktitle: "Excel to CSV"
type: docs
url: convert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel to CSV, Aspose.Cells Cloud, REST API, spreadsheet conversion, CSV file, file conversion"
description: "Convert Excel spreadsheets to CSV using the Aspose.Cells Cloud REST API. Supports multiple SDKs and programming languages for easy integration."
weight: 90
ArticleTitle: "Convert Excel to CSV using Aspose.Cells Cloud REST API"
---
The **PostConvertWorkbookToCSV** API (`POST https://api.aspose.cloud/v3.0/cells/convert/csv`) converts Excel files to CSV format using Aspose.Cells Cloud, supporting password-protected workbooks and optional parameters such as regional settings and Excel restriction checks; it accepts a file upload via multipart form data and returns detailed file information upon successful conversion.

## The Post Convert Workbook to CSV Web API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Query Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| File | File | FormData | File to upload |
| password | String | Query | The password needed to open an Excel file. |
| checkExcelRestriction | Boolean | Query | Whether check restriction of excel file when user modify cells related objects. |
| region | String | Query | The regional settings for workbook. |

### Response

```json
[
  {
    "Name": "FileInfo",
    "DataType": {
      "Identifier": "Class",
      "Reference": "FileInfo"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

**HTTP Status Codes**

| Code | Meaning | Description |
|---|---|---|
| 200 | OK | The request completed successfully. |
| 400 | Bad Request | The request is malformed or one or more parameters are invalid. |
| 401 | Unauthorized | Authentication failed, or the JWT token is missing or expired. |
| 404 | Not Found | The requested workbook, worksheet, or resource was not found. |
| 413 | Payload Too Large | The uploaded file exceeds the allowed size limit. |
| 500 | Internal Server Error | The server encountered an unexpected error while processing the request. |

The API returns a **FileInfo** object that contains the generated CSV file.

| Field           | Type   | Description                                 |
| --------------- | ------ | ------------------------------------------- |
| **Filename**    | string | Name of the CSV file (e.g., `example.csv`). |
| **FileSize**    | int    | Size of the file in bytes.                  |
| **FileContent** | string | Base64‑encoded content of the CSV file.     |

[FileInfo](/cells/file-info/)

### Request Body Parameter

| Parameter Name | Type      | Description                                                             |
| -------------- | --------- | ----------------------------------------------------------------------- |
| `datafile`     | data file | The data file included in the first part of the multipart request body. |

## How to Use the PostConvertWorkbookToCSV API with SDKs

### PostConvertWorkbookToCSV API Specification

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services. The example below shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your project. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services with various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}
