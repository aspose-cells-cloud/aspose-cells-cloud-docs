---
title: 获取工作表单元格范围值
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/operation/getworksheetcellsrangevalue/
description: 检索指定范围内的单元格的值
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="GetWorksheetCellsRangeValue" >}}
{{< blocks/products/cells/docs-title titlemsg="Retrieve the values of cells within the specified range." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,描述,API参考" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/ranges/value,GET,检索指定范围内单元格的值。,<a href=\'https://apireference.aspose.cloud/cells/#/Ranges /GetWorksheetCellsRangeValue\'>GetWorksheetCellsRangeValue</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="参数名称、类型、描述" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="名称，字符串，文件名。" >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="sheetName,字符串,工作表名称。" >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="参数名称、类型、描述" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="namerange,字符串,范围名称。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="firstRow,integer,获取范围第一行的索引。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="firstColumn,integer,获取范围第一列的索引。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="rowCount,integer,获取范围内的行数。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="columnCount,integer,获取范围内的列数。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="文件夹，字符串，原始工作簿文件夹。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="存储名称，字符串，存储名称。" >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/RangesController/GetWorksheetCellsRangeValue\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet1/ranges/value?namerange=Name_2&firstRow=0&firstColumn=0&rowCount=3&columnCount=2&folder=TestData/In"
    -X GET 
    -H "Authorization: Bearer \<jwt token> " \

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_GetWorksheetCellsRangeValue.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}
{{< /tab >}}

{{< /tabs >}}
