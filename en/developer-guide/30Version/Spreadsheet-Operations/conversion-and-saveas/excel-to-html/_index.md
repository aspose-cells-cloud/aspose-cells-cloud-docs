---
title: "Convert Excel to HTML – Aspose.Cells Cloud API v3.0"
second_title: "Document"
linktitle: "Excel to HTML"
type: docs
url: /convert-excel-file-to-html-file/
aliases: [/convert-excel-file-to-html-in-cloud/,/convert/excel-to-html/]
keywords: "Excel, HTML, Aspose.Cells, Cloud API, spreadsheet conversion, REST, SDK"
description: "Use Aspose.Cells Cloud REST API to convert Excel workbooks to HTML. Includes cURL example, SDK code samples, and a detailed response schema."
weight: 100
---

This REST API converts a spreadsheet file to an HTML‑format file.

### Prerequisites
- An active Aspose.Cloud account with a valid **access token** (OAuth 2.0).  
- API version **v3.0** (released Oct 2023).  
- Sufficient storage space in the selected storage (default is **First Storage**).  
- File size must not exceed the service limit (typically 200 MB).

### Authentication
All requests must contain the **Authorization** header:

```http
Authorization: Bearer <access-token>
```

Obtain the token from the OAuth 2.0 endpoint `/connect/token`. Include the header in every cURL call (or SDK request) as shown in the example below.

## Query Parameters

| Parameter Name        | Type   | Description                                                                      |
|-----------------------|--------|----------------------------------------------------------------------------------|
| password              | string | The password required to open the Excel file.                                   |
| storageName           | string | The name of the storage where the file is located.                               |
| checkExcelRestriction| bool   | Indicates whether to check Excel file restrictions when modifying cells.       |

## Request Body Parameter

| Parameter Name | Type | Description                                                                          |
|----------------|------|--------------------------------------------------------------------------------------|
| **File**       | file | The spreadsheet file to be converted, supplied as the first part of the multipart request. |

## Response

The API returns a **FileInfo** object that contains the generated HTML file.

| Field        | Type   | Description                                            |
|--------------|--------|--------------------------------------------------------|
| **Filename** | string | Name of the HTML file (e.g., `example.html`).         |
| **FileSize** | int    | Size of the file in bytes.                             |
| **FileContent** | string | Base64‑encoded content of the HTML file.               |

[FileInfo](/cells/file-info/)

### Error Responses
| HTTP Status | Description                                 | Error Model |
|-------------|---------------------------------------------|-------------|
| 400         | Bad request – missing file or invalid parameters. | `Error` (`Code`, `Message`) |
| 401         | Unauthorized – invalid or missing access token. | `Error` |
| 404         | File not found – the specified file does not exist in storage. | `Error` |
| 500         | Internal server error – unexpected failure on the server side. | `Error` |

## REST API Specification

| **API**                | **Type** | **Description**                     | **Swagger Link**                                                                 |
|------------------------|----------|-------------------------------------|---------------------------------------------------------------------------------|
| /cells/convert/html    | POST     | Convert a spreadsheet to an HTML file. | [PostConvertWorkbookToHtml](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml) |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "x-aspose-client: curl" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToHtml.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToHtml.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToHtml.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToHtml.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToHtml.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToHtml.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToHtml.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToHtml.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs that Implement This Function

- **POST /cells/{name}/saveAs** – Saves an Excel file as an HTML file with additional settings and stores the result in the specified storage.  
  <https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs>

- **PUT /cells/convert** – Converts an Excel file to HTML with optional settings and returns the result in the response.  
  <https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook>

- **GET /cells/{name}** – Retrieves an Excel file converted to HTML with optional settings.  
  <https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook>

## FAQ

**Q: How do I authenticate when calling the Excel‑to‑HTML conversion API?**  
A: Include an `Authorization: Bearer <access-token>` header obtained from the OAuth 2.0 `/connect/token` endpoint.

**Q: What does the `FileInfo` response contain?**  
A: It returns three fields – `Filename` (string), `FileSize` (integer, bytes), and `FileContent` (Base64‑encoded HTML content).

**Q: Which error codes might I encounter?**  
A: `400` (bad request), `401` (unauthorized), `404` (file not found), and `500` (internal server error). Each response includes an `Error` object with `Code` and `Message`.