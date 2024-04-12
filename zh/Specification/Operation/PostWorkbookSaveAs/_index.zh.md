---
title: 后工作簿保存A
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/operation/postworkbooksaveas/
description: 以各种格式保存 Excel 文件
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostWorkbookSaveAs" >}}
{{< blocks/products/cells/docs-title titlemsg="Save an Excel file in various formats." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,描述,API参考" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/SaveAs,POST,以各种格式保存 Excel 文件。,<a href=\'https://apireference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs\'>PostWorkbookSaveAs</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="参数名称、类型、描述" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="名称，字符串，工作簿名称。" >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="参数名称、类型、描述" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="newfilename,string,newfilename 保存结果。“newfilename”应包含文件名和扩展名。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoFitRows,boolean,指示工作簿中是否自动调整行。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoFitColumns,boolean,指示工作簿中是否自动调整列。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="文件夹，字符串，文件所在的文件夹。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName,string,文件所在的存储名称。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outStorageName,string,输出文件所在的存储名称。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction,boolean,用户修改单元格相关对象时是否检查excel文件的限制。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="Region,string,工作簿的区域设置。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pageWideFitOnPerSheet,boolean,页面宽度适合工作表。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pageTallFitOnPerSheet,boolean,页面高度适合工作表。" >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Request Body Parameter" columns="参数名称、类型、描述" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="保存选项，类：保存选项，" >}} 
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/ConversionController/PostWorkbookSaveAs\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/SaveAs?newfilename=OutResult/PostExcelSaveAs.csv&folder=TestData/In"
    -X POST 
    -H "Authorization: Bearer \<jwt token> " \
    -H "accept:application/json"
    -H "Content-Type: application/json"
    -d '' 

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostWorkbookSaveAs.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}
{{< /tab >}}

{{< /tabs >}}
