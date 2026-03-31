---  
title: "Get Worksheet Comment – Aspose.Cells Cloud API Documentation"  
type: docs  
url: /comments/get/  
aliases: [/get-comment-from-a-worksheet/]  
keywords: "Aspose.Cells Cloud Get Worksheet Comment, REST API, Excel, worksheet comment"  
description: "Learn how to retrieve a worksheet comment by cell name using Aspose.Cells Cloud API (v3.0). Includes request URL, parameters, cURL sample, and SDK code snippets."  
weight: 10  
---  

This REST API retrieves a worksheet comment by cell name using **Aspose.Cells Cloud**.

## Authentication  

Obtain a JWT token by calling the `/connect/token` endpoint with your client ID and client secret. Include the token in the request header:

```http
Authorization: Bearer <jwt token>
```

## REST API  

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

The following table lists all request parameters required to retrieve a comment.

| Parameter Name | Type   | Location (URL Path / Query String) | Description |
|----------------|--------|------------------------------------|-------------|
| name           | string | URL Path                           | The name of the Excel file. |
| sheetName      | string | URL Path                           | The name of the worksheet that contains the comment. |
| cellName       | string | URL Path                           | The cell address (e.g., **A1**) whose comment is being retrieved. |
| folder         | string | Query String                       | The folder path where the document is stored. |
| storageName    | string | Query String                       | The name of the storage service. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Common Errors  

- **401 Unauthorized** – Verify that the JWT token is valid, not expired, and correctly placed in the `Authorization` header.  
- **404 Not Found** – Ensure the file name, worksheet name, and cell address are correct and that the file exists in the specified folder/storage.  
- **500 Internal Server Error** – Check the request payload for malformed data and confirm that the service is operational.

## Next Steps  

1. Obtain a JWT token (see **Authentication**).  
2. Replace placeholder values (`{name}`, `{sheetName}`, `{cellName}`, `<jwt token>`) in the request URL and header.  
3. Execute the cURL command or use one of the SDK examples below.  
4. Parse the JSON response to access comment details.

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}