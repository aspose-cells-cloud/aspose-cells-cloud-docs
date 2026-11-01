---
title: "Delete Cell Area – Aspose.Cells Cloud API Documentation"
type: docs
url: /conditional-formattings/delete-cell-area/
aliases: [/remove-cell-area-from-conditional-formatting/]
keywords: "Aspose.Cells Cloud, Delete Cell Area, Conditional Formatting API, Excel REST API"
description: "Delete a cell area from conditional formatting in an Excel worksheet using the Aspose.Cells Cloud REST API."
ArticleTitle: "Delete Cell Area – Aspose.Cells Cloud API Documentation"
weight: 70
linktitle: "Delete Cell Area"
---
The **DeleteWorksheetConditionalFormattingArea** API (`DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area`) in Aspose.Cells Cloud removes a specified rectangular cell area from an existing conditional formatting rule in a worksheet, using required path parameters `name` and `sheetName` plus query parameters `startRow`, `startColumn`, `totalRows`, and `totalColumns` to define the range; this enables precise programmatic control over conditional formatting removal without modifying other rules.

## Security and Authentication
The Aspose.Cells Cloud APIs are secure and require [JWT token-based authentication](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## The Delete Worksheet Conditional Formatting Area Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### **Security and Authentication**

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type | Path/Query String/HTTPBody | Description |
|---|---|---|---|
| name | String | Path | The file name. |
| sheetName | String | Path | The worksheet name. |
| startRow | Integer | Query | The start row of the range. |
| startColumn | Integer | Query | The start column of the range. |
| totalRows | Integer | Query | The number of rows of the range. |
| totalColumns | Integer | Query | The number of columns of the range. |
| folder | String | Query | The folder where the file is situated. |
| storageName | String | Query | The storage name where the file is situated. |

### **Response**

```json
[
  {
    "Name": "CellsCloudResponse",
    "DataType": {
      "Identifier": "Class",
      "Reference": "CellsCloudResponse"
    }
  }
]
```

**Sample response headers**

```http
HTTP/1.1 200 OK
Content-Type: application/json
```

### Error Responses

| HTTP Status | Code            | Description                                           | Sample JSON                                                   |
| ----------- | --------------- | ----------------------------------------------------- | ------------------------------------------------------------- |
| 400         | `BadRequest`    | Missing or invalid parameters.                        | `{ "Code": "400", "Message": "Invalid request parameters." }` |
| 401         | `Unauthorized`  | Missing or invalid JWT token.                         | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404         | `NotFound`      | File, worksheet, or conditional formatting not found. | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500         | `InternalError` | Unexpected server error.                              | `{ "Code": "500", "Message": "Internal server error." }`      |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells Cloud services easily. The following example shows how to call the **Delete Cell Area** endpoint with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/area?startRow=3&startColumn=3&totalRows=1&totalColumns=1" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-remove-cell-area-from-conditional-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formatting_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-RemoveCellAreaFromConditionalFormatting-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2bc4a93409f78b40b6bcf681c6a14bda" >}}

{{< /tab >}}

{{< /tabs >}}