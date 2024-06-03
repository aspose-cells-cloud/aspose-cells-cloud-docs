---
title: 放置工作表字符
second_title: Aspose.Cells Cloud Documen
type: docs
url: /zh/specification/operation/putworksheetchart/
description: 在工作表中添加新图表
kwords: Excel，Office，电子表格，云 REST API，PutWorksheetChart
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetChart" >}}
{{< blocks/products/cells/docs-title titlemsg="Add a new chart in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,描述,API 参考" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/charts,PUT,在工作表中添加新图表。,<a href=\'https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChart\'>PutWorksheetChart</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="参数名称、类型、描述" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="name，string，文件名。" >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="sheetName，string，工作表名称。" >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="参数名称、类型、描述" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="chartType，string，图表类型，请参考图表资源中的属性Type。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="upperLeftRow，integer，新图表的左上行。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="upperLeftColumn，integer，新图表的左上列。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="lowerRightRow，整数，新图表的左下行。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="lowerRightColumn，integer，新图表的左下列。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="区域，字符串，指定绘制数据系列的值。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns=" isVertical，boolean，指定是否按行还是按列绘制单元格值范围的系列。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="categoryData,string,获取或设置分类轴值的范围，可以是单元格区域（例如：\'D1:E10\'）。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoGetSerialName,boolean,指定是否自动更新序列名称。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="title，string，指定图表标题名称。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="文件夹，字符串，文件所在的文件夹。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabels,boolean,表示指定图表的数据标签值的显示行为。True 表示显示值，False 表示隐藏值。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabelsPosition，string，表示数据标签位置（Center/InsideBase/InsideEnd/OutsideEnd/Above/Below/Left/Right/BestFit/Moved）。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pivotTableSheet,string,源为pivotTable的数据，若PivotSource不为空，则图表为PivotChart。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pivotTableName，string，数据透视表名称。" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName，string，文件所在的存储名称。" >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/ChartsController/PutWorksheetChart\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet4/charts?chartType=Pie&upperLeftRow=5&upperLeftColumn=5&lowerRightRow=10&lowerRightColumn=10&area=C7:D11&isVertical=true&title=Aspose Chart&folder=TestData/In"
    -X PUT 
    -H "Authorization: Bearer \<jwt token> " \

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PutWorksheetChart.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetChart.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetChart.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetChart.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetChart.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetChart.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetChart.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetChart.rb" >}}
{{< /tab >}}

{{< /tabs >}}
