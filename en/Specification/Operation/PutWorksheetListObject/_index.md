---
title: "PutWorksheetListObject"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/operation/putworksheetlistobject/
description: ""
kwords: Excel, Office, Spreadsheet, Cloud REST API, PutWorksheetListObject
weight: 50

---


{{< blocks/products/cells/docs-title titlemsg="PutWorksheetListObject" >}}
{{< blocks/products/cells/docs-title titlemsg="" >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Description,API reference" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/listobjects,PUT,,<a href='https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject'>PutWorksheetListObject</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Parameter Name,Type,Description" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="name,string,The file name." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="sheetName,string,The worksheet name." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Parameter Name,Type,Description" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="startRow,integer,The start row of the list range." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="startColumn,integer,The start column of the list range." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="endRow,integer,The start row of the list range." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="endColumn,integer,The start column of the list range." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="folder,string,The folder where the file is situated." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="hasHeaders,boolean,Indicate whether the range has headers." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="displayName,string,Indicate whether display name." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="showTotals,boolean,Indicate whether show totals." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName,string,The storage name where the file is situated." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href='https://apireference.aspose.cloud/cells/#/ListObjectsController/PutWorksheetListObject'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet7/listobjects?startRow=1&startColumn=1&endRow=6&endColumn=6&folder=TestData/In&hasHeaders=true&displayName=true&showTotals=false"
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
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PutWorksheetListObject.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}
{{< /tab >}}

{{< /tabs >}}
