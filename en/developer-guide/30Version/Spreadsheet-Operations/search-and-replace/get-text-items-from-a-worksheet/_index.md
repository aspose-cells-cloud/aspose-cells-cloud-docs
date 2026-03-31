---  
title: "Get Text Items from an Excel Worksheet"  
second_title: "Document"  
linktitle: "Get Text Items in Worksheet"  
type: docs  
url: /worksheets/get-text-items/  
aliases: [/get-text-items-from-a-worksheet/]  
weight: 20  
keywords: "Aspose.Cells, Cloud API, Excel, worksheet, text items, REST"  
description: "Retrieve all text items from a specific worksheet in an Excel file using Aspose.Cells Cloud REST API. Includes sample cURL, SDK code, authentication steps, and response schema."  
---  

This REST API reads a worksheet’s text items in an Excel file.

## REST API  

### Authentication  

The endpoint requires an OAuth 2.0 Bearer token. Obtain the token from the Aspose Cloud authentication service and include it in the `Authorization` header:

```bash
-H "Authorization: Bearer <access_token>"
```

### Request  

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/textItems
```

### Parameters  

The request parameters are as follows:

| Parameter Name | Type   | Location | Required | Description |
|----------------|--------|----------|----------|-------------|
| name           | string | path     | Yes      | Workbook file name. |
| sheetName      | string | path     | Yes      | Name of the worksheet. |
| folder         | string | query    | No       | Path to the folder that contains the workbook. |
| storageName    | string | query    | No       | Name of the Aspose Cloud storage. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Error Handling  

The API can return the following HTTP status codes:

* **400 Bad Request** – Missing or invalid parameters.  
* **401 Unauthorized** – Access token is absent, expired, or invalid.  
* **404 Not Found** – The specified workbook or worksheet does not exist.  
* **500 Internal Server Error** – An unexpected server‑side error occurred.

Error responses are returned in JSON format, for example:

```json
{
  "Error": {
    "Code": "InvalidToken",
    "Message": "The access token is invalid or has expired."
  }
}
```

### Pagination / Limits  

The endpoint returns all text items in a single response. If a future version supports pagination, the documentation will be updated accordingly.

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}