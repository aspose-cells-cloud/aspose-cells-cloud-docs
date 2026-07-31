---
title: "Delete metadata from Excel files"
second_title: "Document"
linktitle: "Delete without using storage"
type: docs
url: /metadata/delete/
keywords: "Aspose.Cells, delete metadata, Excel API, workbook properties"
description: "Delete workbook metadata (author, title, custom) via Aspose.Cells Cloud API. Includes endpoint, authentication, parameters, cURL and SDK samples."
weight: 55
ArticleTitle: "Delete metadata from Excel files – Aspose.Cells Cloud Documentation"
---

**Overview**  
The Delete Metadata operation permanently removes all workbook properties (standard and custom) from the uploaded Excel file(s) and returns the processed file(s) in the response.

**Prerequisites**  
- A valid Aspose.Cells Cloud JWT token (obtainable via the OAuth 2.0 authentication flow).  
- API version **v3.0** (the endpoint used in this example).  
- For SDK usage, install the appropriate Aspose.Cells Cloud SDK for your language (e.g., via NuGet, Maven, npm, pip, CPAN, or Go modules).

This REST API deletes **metadata** from one or more Excel files. It removes workbook properties such as author, title, and custom data, and returns the cleaned files.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **Request parameters**

| Parameter Name | Type   | Location | Description                                               |
| -------------- | ------ | -------- | --------------------------------------------------------- |
| file           | file   | formData | Excel file to upload for **metadata** deletion            |
| type           | string | query    | Operation type; set to **all** to delete all **metadata** |

The <a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Error responses** may include:

- **400 Bad Request** – missing file or invalid `type` value.
- **401 Unauthorized** – invalid or missing JWT token.
- **500 Internal Server Error** – server‑side processing error.

The API returns a JSON object containing an `Error` field with details for each case.

| Code | Meaning | Description |
|------|---------|-------------|
| 200 | OK | Metadata deleted, file returned |
| 400 | Bad Request | Missing file or invalid `type` |
| 401 | Unauthorized | Invalid or missing JWT |
| 500 | Internal Server Error | Server processing failure |

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}