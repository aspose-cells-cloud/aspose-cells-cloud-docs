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

## The Delete Worksheet Conditional Formatting Area Web API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### Security and Authentication

The Aspose.Cells Cloud APIs are secure and require <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer" target="_blank">JWT token-based authentication</a>.

### Request Parameters

| Parameter Name | Type    | Path/Query String/HTTPBody | Description                                  |
| -------------- | ------- | -------------------------- | -------------------------------------------- |
| name           | String  | Path                       | The file name.                               |
| sheetName      | String  | Path                       | The worksheet name.                          |
| startRow       | Integer | Query                      | The start row of the range.                  |
| startColumn    | Integer | Query                      | The start column of the range.               |
| totalRows      | Integer | Query                      | The number of rows of the range.             |
| totalColumns   | Integer | Query                      | The number of columns of the range.          |
| folder         | String  | Query                      | The folder where the file is situated.       |
| storageName    | String  | Query                      | The storage name where the file is situated. |

### Response

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

## How to Use the Delete Worksheet Conditional Formatting Area API with SDKs?

### Delete Worksheet Conditional Formatting Area API Specification

The <a href="https://reference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattingArea" rel="noopener noreferrer">Delete Worksheet Conditional Formatting Area API Specification</a> defines a publicly accessible programming interface and enables you to carry out REST interactions directly from a web browser.

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low‑level details, allowing you to use the API with short code.  
Please check out the <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetConditionalFormattingArea.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetConditionalFormattingArea.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetConditionalFormattingArea.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetConditionalFormattingArea.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetConditionalFormattingArea.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetConditionalFormattingArea.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetConditionalFormattingArea.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetConditionalFormattingArea.go" >}}
{{</tab>}}
{{< /tabs >}}
