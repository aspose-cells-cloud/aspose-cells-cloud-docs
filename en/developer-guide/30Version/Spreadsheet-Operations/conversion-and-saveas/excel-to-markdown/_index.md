---  
title: "Convert Excel to Markdown"  
second_title: "Document"  
linktitle: "Excel to Markdown"  
type: docs  
url: /convert-excel-file-to-markdown-file/  
keywords: "Excel, Markdown, conversion, Aspose.Cells Cloud, REST API, excel to markdown conversion, aspose cells markdown api, excel markdown export"  
description: "Learn how to convert Excel worksheets to Markdown using Aspose.Cells Cloud REST API. Includes curl example, SDK snippets, required parameters and authentication."  
weight: 100  
---  

This REST API converts a spreadsheet file to a Markdown-format file.

### Prerequisites  

- A valid Aspose Cloud account with an API key.  
- OAuth 2.0 access token (see **Authentication** below).

### Authentication  

All requests must include an `Authorization` header with a bearer token:

```http
Authorization: Bearer <access_token>
```

Obtain the token from the Aspose Cloud OAuth endpoint using your client ID and secret.

### Parameters  

| Parameter Name | Type   | Location | Description                                                                 |
|----------------|--------|----------|-----------------------------------------------------------------------------|
| password       | string | query    | Password required to open the Excel file.                                   |
| storageName    | string | query    | Name of the storage where the file is located.                               |
| checkExcelRestriction | bool   | query    | Indicates whether to enforce Excel‑specific restrictions when modifying cells or related objects. |
| datafile       | file   | body     | The Excel file to be uploaded as the first part of the multipart content.   |

### Response  

The API returns a JSON object of type **FileInfo**:

- **FileInfo** – object containing the name, size, and base‑64‑encoded content of the generated Markdown file.  

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### Error Responses  

| HTTP Code | Description                               | Example JSON Body |
|----------|-------------------------------------------|-------------------|
| 401      | Unauthorized – missing or invalid token. | `{"error":"Invalid access token."}` |
| 400      | Bad Request – missing required parameters or invalid file format. | `{"error":"The 'datafile' field is required."}` |
| 500      | Internal Server Error – unexpected server problem. | `{"error":"An unexpected error occurred."}` |

## REST API Specification  

| API                         | Type | Description                              | Swagger Link |
|-----------------------------|------|------------------------------------------|--------------|
| /cells/convert/markdown     | POST | Convert a spreadsheet to a Markdown file.| [PostConvertWorkbookToMarkdown](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) |

The [OpenAPI Specification](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command‑line tool to access Aspose.Cells web services easily. The example below shows how to call the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family  

Using an SDK is the fastest way to develop. An SDK handles low‑level details so you can focus on your business logic. See the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Other APIs that Implement This Function  

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Saves an Excel file as HTML with additional settings and stores the result.  
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Converts an Excel file to HTML with extra options and returns the result in the response.  
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Retrieves an Excel file and can convert it to HTML with optional settings.  