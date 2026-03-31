---  
title: "Delete Cell Area – Aspose.Cells Cloud API Documentation"  
type: docs  
url: /conditional-formattings/delete-cell-area/  
aliases: [/remove-cell-area-from-conditional-formatting/]  
keywords: "Aspose.Cells Cloud, Delete Cell Area, Conditional Formatting API, Excel REST API"  
description: "Use the Aspose.Cells Cloud REST API to delete a specific cell area from conditional formatting in an Excel worksheet. Includes ASP.NET, Java, and Python examples."  
weight: 70  
---  

This REST API removes a cell area from a conditional‑formatting rule.

## REST API  

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/area
```

### Request Parameters  

| Parameter Name | Type    | Location | Description |
|----------------|---------|----------|-------------|
| `name`         | string  | path     | The name of the Excel file. |
| `sheetName`    | string  | path     | The name of the worksheet that contains the conditional formatting. |
| `startRow`     | integer | query    | Zero‑based index of the first row of the area to be removed. |
| `startColumn`  | integer | query    | Zero‑based index of the first column of the area to be removed. |
| `totalRows`    | integer | query    | Number of rows in the area to be removed. |
| `totalColumns`| integer | query    | Number of columns in the area to be removed. |
| `folder`       | string  | query    | Folder in cloud storage where the file is located (optional). |
| `storageName`  | string  | query    | Name of the storage service (optional). |

### Error Responses  

| HTTP Status | Code | Description | Sample JSON |
|-------------|------|-------------|-------------|
| 400 | `BadRequest` | Missing or invalid parameters. | `{ "Code": "400", "Message": "Invalid request parameters." }` |
| 401 | `Unauthorized` | Missing or invalid JWT token. | `{ "Code": "401", "Message": "Authentication failed." }` |
| 404 | `NotFound` | File, worksheet, or conditional formatting not found. | `{ "Code": "404", "Message": "Resource not found." }` |
| 500 | `InternalError` | Unexpected server error. | `{ "Code": "500", "Message": "Internal server error." }` |

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

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

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