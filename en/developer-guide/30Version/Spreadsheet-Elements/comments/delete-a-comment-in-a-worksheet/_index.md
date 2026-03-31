---  
title: "Delete a Worksheet Comment"  
type: docs  
url: /comments/delete/  
aliases: [/delete-a-comment-in-a-worksheet/]  
keywords: "Aspose.Cells delete comment, Excel comment API, REST delete worksheet comment, Aspose Cloud SDK, Excel comment removal"  
description: "Learn how to delete a specific cell comment in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL example, SDK snippets, and error handling."  
weight: 40  
---  

A **comment** is a text note attached to a specific cell in an Excel worksheet. This REST API deletes such a comment from a worksheet cell.  

**Version:** v3.0  

## REST API  

### Prerequisites  

- The Excel file must already exist in the selected storage.  
- The target worksheet must contain the comment you intend to delete.  
- If the file is not stored in the root folder, provide the `folder` query parameter.  

### Authentication  

The endpoint requires **OAuth 2.0 Bearer tokens**. Obtain a token from the Aspose Cloud authentication service and include it in the request header:

```http
Authorization: Bearer <access_token>
```  

### Endpoint  

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```  

### Parameters  

The endpoint accepts the following parameters:

| Parameter Name | Type   | Location | Required | Description                              |
|----------------|--------|----------|----------|------------------------------------------|
| name           | string | path     | Yes      | The name of the Excel document.          |
| sheetName      | string | path     | Yes      | The name of the worksheet.               |
| cellName       | string | path     | Yes      | The address of the cell (e.g., `A1`).    |
| folder         | string | query    | No       | The folder that contains the document.   |
| storageName    | string | query    | No       | The name of the storage service.         |

### Request Example  

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Error Responses  

| HTTP Code | Description                              | Example Response |
|-----------|------------------------------------------|------------------|
| 400       | Bad request – missing or malformed parameters. | `{ "Code": 400, "Message": "Invalid parameters." }` |
| 401       | Unauthorized – invalid or missing token. | `{ "Code": 401, "Message": "Authentication required." }` |
| 404       | Not found – the file, worksheet, or comment does not exist. | `{ "Code": 404, "Message": "Resource not found." }` |
| 500       | Internal server error – unexpected condition on the server. | `{ "Code": 500, "Message": "Server error." }` |

For a complete list of status codes, refer to the **Error Responses** section above.  

The [OpenAPI Specification for DeleteWorksheetComment](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetComment) provides a machine‑readable description of this endpoint.  

## Cloud SDK Family  

Using an SDK can speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository for Aspose.Cells Cloud SDKs](https://github.com/aspose-cells-cloud) for a complete list.  

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}