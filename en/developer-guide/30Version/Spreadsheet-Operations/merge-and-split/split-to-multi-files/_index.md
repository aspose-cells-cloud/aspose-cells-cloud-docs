---
title: "Split an Excel file into multiple files"
second_title: "Document"
linktitle: "Split Multi Excel files"
type: docs
url: /split-an-excel-file-to-multi-files/
aliases: [/split-excel-workbooks/,/workbook/split/]
keywords: "Aspose.Cells, Cloud, Excel, Split, API, PDF, CSV, JSON"
description: "Use the Aspose.Cells Cloud REST API to split multi‑sheet Excel workbooks into separate files. Supports output formats such as PDF, CSV, and JSON, and is available through SDKs for Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, and Swift."
weight: 32
ArticleTitle: "Split an Excel file into multiple files - Aspose.Cells Cloud Documentation"
---

The Aspose.Cells Cloud REST API splits multi‑sheet Excel workbooks into separate files.

**Prerequisites**  
Before calling the API you must obtain a valid JWT token and include it in the `Authorization` header of each request. See the [authentication guide](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) for details.

## PostSplit API

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.


### Request parameters

| Parameter Name | Type   | Location  | Description                                                       |
|----------------|--------|-----------|-------------------------------------------------------------------|
| file           | file   | formData  | The Excel workbook to upload.                                     |
| format         | string | query     | Desired output format (e.g., `pdf`, `csv`, `json`).               |
| password       | string | query     | Password for an encrypted workbook (optional).                   |
| from           | integer| query     | Index of the first sheet to include (1‑based).                    |
| to             | integer| query     | Index of the last sheet to include (inclusive).                  |

### **Response**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[file1 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[file2 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[file3 name]",
            "Filesize" : [file size],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**HTTP Status Codes**

| Code | Meaning                     | Description                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter applied successfully; response contains operation details. |
| 400  | Bad Request                 | Missing or invalid parameters (e.g., unsupported file type). |
| 401  | Unauthorized                | Invalid or missing JWT token. |
| 413  | Payload Too Large           | Uploaded file exceeds size limit. |
| 500  | Internal Server Error       | Unexpected server error. |
## How to Use the PostSplit API with SDKs

### PostSplit API Specification

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

**HTTP status codes**

| Code | Meaning                         | Description                                                                      |
|------|---------------------------------|----------------------------------------------------------------------------------|
| 200  | OK                              | The workbook was split successfully and the response contains the file list.   |
| 400  | Bad Request                     | Missing or invalid parameters (e.g., unsupported format).                     |
| 401  | Unauthorized                    | Invalid or missing JWT token.                                                    |
| 500  | Internal Server Error           | An unexpected error occurred on the server side.                                 |

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# Replace xxxxx1.xlsx and xxxxx2.xlsx with the paths to your Excel files
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Use Aspose.Cells Cloud SDKs

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}