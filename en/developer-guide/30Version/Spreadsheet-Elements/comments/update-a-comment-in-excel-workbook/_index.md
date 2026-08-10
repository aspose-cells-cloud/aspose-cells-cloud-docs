---
title: "Update a Worksheet Cell Comment"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, REST API, Excel, worksheet, cell comment, update worksheet comment, comment object"
description: "Use Aspose.Cells Cloud REST API to update a worksheet comment on a cell in an Excel workbook, including request details, response codes, and SDK examples."
weight: 30
ArticleTitle: "Update Worksheet Cell Comment – Aspose.Cells Cloud API"
---

This REST API updates a comment on a worksheet cell. Use this endpoint to **update a worksheet comment** in an Excel file.  

**Prerequisites:**  
- A valid OAuth/JWT access token must be included in the `Authorization` header.  
- The workbook must be stored in a supported cloud storage location (specify `folder` and optionally `storageName`).  

## PostWorksheetComment API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type   | Location | Description                                                           |
| -------------- | ------ | -------- | --------------------------------------------------------------------- |
| name           | string | path     | The name of the Excel document.                                       |
| sheetName      | string | path     | The name of the worksheet that contains the cell.                     |
| cellName       | string | path     | The address of the cell (e.g., **A1**).                               |
| comment        | object | body     | A **Comment** object that defines the comment to be added or updated. |
| folder         | string | query    | The folder where the document is stored.                              |
| storageName    | string | query    | The name of the storage service.                                      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment) defines a publicly accessible programming interface and lets you perform REST interactions directly from a web browser.

You can use the **cURL** command-line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Possible response status codes:

| Code | Description                                   |
|------|-----------------------------------------------|
| 200  | Comment updated successfully.                |
| 400  | Bad request – missing or invalid parameters. |
| 401  | Unauthorized – authentication failed.        |
| 404  | Not found – workbook, worksheet, or comment does not exist. |
| 500  | Internal server error.                       |

**Notes / Tips:**  
- Maximum comment length is 1024 characters.  
- Supported characters are UTF‑8; avoid control characters.  

## Cloud SDK Family

Using an SDK is the fastest way to develop with Aspose.Cells Cloud. An SDK handles low‑level details so you can focus on your project. Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

Related Operations:  
- [Get Worksheet Comment](/comments/get/)  
- [Add Worksheet Comment](/comments/add/)  
- [Delete Worksheet Comment](/comments/delete/)