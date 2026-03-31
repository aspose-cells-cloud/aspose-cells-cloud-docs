---  
title: "Add CellArea to Conditional Formatting"  
type: docs  
url: /conditional-formattings/add-cell-area/  
aliases: [/add-a-cell-area-for-format-condition/]  
keywords: "Aspose.Cells Cloud, conditional formatting, add cell area, REST API, Excel, SDK"  
description: "Learn how to add a cell area to a conditional formatting rule in an Excel worksheet using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL example, SDK snippets, and error handling."  
weight: 30  
---  

This REST API adds a cell area to a format condition.

## REST API  

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}/area
```  

**Quick‑Start**  

1️⃣ Obtain a JWT token via the Aspose Cloud OAuth 2.0 flow.  
2️⃣ Replace `{name}`, `{sheetName}` and `{index}` with your file name, worksheet name, and rule index.  
3️⃣ Supply the `cellArea` query parameter (e.g., `A1:C3`).  
4️⃣ Send the **PUT** request with the `Authorization: Bearer <jwt token>` header.  

The API accepts the following parameters:

<table>  
<caption>Parameters for Add CellArea API</caption>  
<thead>  
<tr>  
<th scope="col">Parameter Name</th>  
<th scope="col">Type</th>  
<th scope="col">Location</th>  
<th scope="col">Description</th>  
</tr>  
</thead>  
<tbody>  
<tr>  
<td>name</td>  
<td>string</td>  
<td>path</td>  
<td>The name of the Excel file.</td>  
</tr>  
<tr>  
<td>sheetName</td>  
<td>string</td>  
<td>path</td>  
<td>The name of the worksheet that contains the condition.</td>  
</tr>  
<tr>  
<td>index</td>  
<td>integer</td>  
<td>path</td>  
<td>The zero‑based index of the conditional formatting rule.</td>  
</tr>  
<tr>  
<td>cellArea</td>  
<td>string</td>  
<td>query</td>  
<td>The cell range to add, expressed in A1 notation (e.g., <code>A1:C3</code>).</td>  
</tr>  
<tr>  
<td>folder</td>  
<td>string</td>  
<td>query</td>  
<td>The folder where the file is stored.</td>  
</tr>  
<tr>  
<td>storageName</td>  
<td>string</td>  
<td>query</td>  
<td>The name of the storage service.</td>  
</tr>  
</tbody>  
</table>  

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatConditionArea) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0/area?cellArea=A1:C3" \
  -X PUT \
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

*Successful response* – a JSON object containing `Code` `200` and `Status` `OK`. The body may also include the updated `CellArea` object.

*Common error responses*  

- **400 Bad Request** – `{ "Code":"400", "Message":"Invalid cellArea format." }`  
- **401 Unauthorized** – `{ "Code":"401", "Message":"Invalid or missing JWT token." }`  
- **404 Not Found** – `{ "Code":"404", "Message":"Worksheet or conditional formatting rule not found." }`

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family  

Using an SDK is the best way to speed up development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-FormatConditionArea-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition_area-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-FormatConditionArea-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-FormatConditionArea-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "597f99e44a3ac676ca8273b28f088ad2" >}}

{{< /tab >}}

{{< /tabs >}}