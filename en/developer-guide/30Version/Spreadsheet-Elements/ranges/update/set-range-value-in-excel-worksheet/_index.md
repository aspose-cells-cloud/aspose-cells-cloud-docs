---
title: "Set Range Value in an Excel Worksheet"
second_title: "Document"
linktitle: "Set values"
type: docs
url: /ranges/update/values/
aliases: [/set-range-value-in-excel-worksheet/]
keywords: "Aspose.Cells, Excel API, set range value, REST API, cloud SDK, worksheet update"
description: "Learn how to set a cell or range value in an Excel workbook using Aspose.Cells Cloud REST API (v3.0). Includes endpoint, parameters, cURL example, SDK code samples, and error handling."
weight: 72
---

Use this REST API to set a value in the specified range. When appropriate, the value is converted to another data type and the cell’s number format is reset.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

The request parameters are:

| Parameter Name | Type    | Location | Description                                                |
|----------------|---------|----------|------------------------------------------------------------|
| name           | string  | path     | Workbook name                                              |
| sheetName      | string  | path     | Worksheet name                                             |
| value          | string  | query    | Input value                                                |
| range          | object  | body     | Range object in the worksheet                              |
| isConverted    | boolean | query    | Indicates whether the input value should be converted      |
| setStyle       | boolean | query    | Indicates whether to apply style to the target cells       |
| folder         | string  | query    | Workbook folder                                            |
| storageName    | string  | query    | Storage name                                               |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to call the Cloud API with cURL. **Include a valid JWT token in the `Authorization` header.**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details, allowing you to focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}