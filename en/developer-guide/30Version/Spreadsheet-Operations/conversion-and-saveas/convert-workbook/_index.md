---
title: "Convert an Excel File to Different Formats"
second_title: "Document"
linktitle: "Convert Spreadsheet"
type: docs
url: /convert-a-spread-file-to-different-formats/
keywords: "Excel conversion, spreadsheet conversion, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, Markdown, file format conversion"
description: "Use Aspose.Cells Cloud REST API to convert Excel workbooks to various formats such as PDF, CSV, JSON, and Markdown. The API supports multiple SDKs for languages like C#, Java, Python, and more."
weight: 10
ArticleTitle: "Convert an Excel File to Different Formats – Aspose.Cells Cloud API Guide"
---

This REST API converts an Excel file to a different format. It supports a wide range of output formats and allows you to set page‑setup and save options before conversion.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

Before using this API, ensure you have a valid JWT token and have installed the appropriate Aspose.Cells Cloud SDK for your programming language.

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.


**Request Body Parameter**

| Parameter Name                                                                          | Type   | Description                          |
| --------------------------------------------------------------------------------------- | ------ | ------------------------------------ |
| `ConvertWorkbookOptions`<br/>[ConvertWorkbookOptions](/cells/convert-workbook-options/) | object | Options for converting the workbook. |

**Response**

The API returns a **FileInfo** object that contains the generated Spreadsheet file.

| Field           | Type   | Description                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Name of the Spreadsheet file (e.g., `example.xlsx`). |
| **FileSize**    | int    | Size of the file in bytes.                    |
| **FileContent** | string | Base64‑encoded content of the Spreadsheet file.      |

[FileInfo](/cells/file-info/)



**Response Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Conversion succeeded; response contains converted file details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |


## How to Use the PostConvertWorkBook API with SDKs

### PostConvertWorkBook API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the fastest way to develop. An SDK abstracts low‑level details so you can focus on your project. Check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}