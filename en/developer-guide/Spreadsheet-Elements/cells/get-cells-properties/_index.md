---
title: "Get Cells Properties"
type: docs
url: /get-cells-properties/
weight: 130
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, Get Cells Properties
---

This REST API indicates shows how to `get a specific cell` in an Excel file.

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```

The request parameters are:

| Parameter Name | Type | Path/Query String/HTTPBody | Description|
| :- | :- | :- |:- |
| name | string | path | Document name. |
| sheetName | string | path | Worksheet name. |
| cellOrMethodName | string | path | The cell's or method name. (Method name value : firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn and cellName.) |
| folder | string | query | Document's folder. |
| storageName | string | query | storage name. |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

### **Cloud SDK Family**

Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### **How to get specific cell**

- [Get Cell Data from a Worksheet](/cells/get-cell-data-from-a-worksheet/)
- [Get First Cell from Excel Worksheet](/cells/get-first-cell-from-excel-worksheet/)
- [Get Last Cell of Excel Worksheet](/cells/get-last-cell-of-excel-worksheet/)
- [Get MaxRow from Excel Worksheet](/cells/get-maxrow-from-excel-worksheet/)
- [Get MaxDataRow from Excel Worksheet](/cells/get-maxdatarow-from-excel-worksheet/)
- [Get MaxColumn from Excel Worksheet](/cells/get-maxcolumn-from-excel-worksheet/)
- [Get MaxDataColumn from Excel Worksheet](/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Get MinRow from Excel Worksheet](/cells/get-minrow-from-excel-worksheet/)
- [Get MinDataRow from Excel Worksheet](/cells/get-mindatarow-from-excel-worksheet/)
- [Get MinColumn from Excel Worksheet](/cells/get-mincolumn-from-excel-worksheet/)
- [Get MinDataColumn from Excel Worksheet](/cells/get-mindatacolumn-from-excel-worksheet/)
