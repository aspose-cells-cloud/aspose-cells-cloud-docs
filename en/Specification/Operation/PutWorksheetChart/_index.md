---
title: "PutWorksheetChart"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/operation/putworksheetchart/
description: ""
kwords: Excel, Office, Spreadsheet, Cloud REST API, PutWorksheetChart
weight: 50

---


{{< blocks/products/cells/docs-title titlemsg="PutWorksheetChart" >}}
{{< blocks/products/cells/docs-title titlemsg="" >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Description,API reference" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/charts,PUT,,<a href='https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChart'>PutWorksheetChart</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Parameter Name,Type,Description" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="name,string,The file name." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="sheetName,string,The worksheet name." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Parameter Name,Type,Description" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="chartType,string,Chart type, please refer property Type in chart resource." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="upperLeftRow,integer,Upper-left row for the new chart." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="upperLeftColumn,integer,Upper-left column for the new chart." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="lowerRightRow,integer,Lower-left row for the new chart." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="lowerRightColumn,integer,Lower-left column for the new chart." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="area,string,Specify the values from which to plot the data series." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isVertical,boolean,Specify whether to plot the series from a range of cell values by row or by column. " >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="categoryData,string,Get or set the range of category axis values. It can be a range of cells (e.g., 'D1:E10')." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoGetSerialName,boolean,Specify whether to auto-update the serial name." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="title,string,Specify the chart title name." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="folder,string,The folder where the file is situated." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabels,boolean,Represents the specified chart's data label values display behavior. True to display the values, False to hide them." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabelsPosition,string,Represents data label position (Center/InsideBase/InsideEnd/OutsideEnd/Above/Below/Left/Right/BestFit/Moved)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pivotTableSheet,string,The source is the data of the pivotTable. If PivotSource is not empty, the chart is a PivotChart." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pivotTableName,string,The pivot table name." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName,string,The storage name where the file is situated." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href='https://apireference.aspose.cloud/cells/#/ChartsController/PutWorksheetChart'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
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

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href='https://github.com/aspose-cells-cloud'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP"  tabName17="Python"  tabName18="Ruby"  >}}

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
