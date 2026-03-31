---  
title: "Unmerge Cells in a Range"  
second_title: "Document"  
linktitle: "Unmerge"  
type: docs  
url: /ranges/unmerge/  
aliases: [/unmerge-merged-cells-of-the-range/]  
keywords: "Aspose.Cells Cloud, unmerge cells, Excel API, worksheet range, REST API"  
description: "Learn how to use the Aspose.Cells Cloud API to unmerge merged cells in a specific worksheet range. Includes endpoint, parameters, sample cURL, and SDK code snippets for C#, Java, Python, and more."  
weight: 20  
---  

This REST API unmerges merged cells within a specified range on an Excel worksheet.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/unmerge
```  

The request parameters are:

| Parameter Name | Type   | Location | Required | Description                                   |
|----------------|--------|----------|----------|-----------------------------------------------|
| name           | string | path     | Yes      | Workbook name.                                |
| sheetName      | string | path     | Yes      | Worksheet name.                               |
| range          | object | body     | Yes      | Range object that defines the cells to unmerge. |
| folder         | string | query    | No       | Folder that contains the workbook.            |
| storageName    | string | query    | No       | Storage name.                                 |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeUnmerge) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make calls to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/unmerge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "ColumnCount": 7,
    "ColumnWidth": 19,
    "FirstColumn": 0,
    "FirstRow": 9,
    "Name": "string",
    "RefersTo": "string",
    "RowCount": 1,
    "RowHeight": 15,
    "Worksheet": "Sheet1"
}'
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

Using an SDK is the best way to accelerate development. An SDK handles low‑level details so you can focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to call Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeUnMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeUnMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeUnMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeUnMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeUnMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeUnMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeUnMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeUnMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}