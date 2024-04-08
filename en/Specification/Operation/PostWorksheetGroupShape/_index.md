---
title: "PostWorksheetGroupShape"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/operation/postworksheetgroupshape/
description: "Group shapes in the worksheet."
weight: 50

---


{{< blocks/products/cells/docs-title titlemsg="PostWorksheetGroupShape" >}}
{{< blocks/products/cells/docs-title titlemsg="Group shapes in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parameter-title="REST API" columns="API,HttpMethod,Description,API reference" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/shapes/group,POST,Group shapes in the worksheet.,<a href='https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetGroupShape'>PostWorksheetGroupShape</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parameter-title="Path Parameter" columns="Parameter Name,Type,Description" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="name,string,The file name." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="sheetName,string,The worksheet name." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parameter-title="Query Parameter" columns="Parameter Name,Type,Description" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="folder,string,The folder where the file is situated." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="storageName,string,The storage name where the file is situated." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parameter-title="Request Body Parameter" columns="Parameter Name,Type,Description" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="listShape,array<integer>,Shape index array." >}} 
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-title titlemsg="The <a href='https://apireference.aspose.cloud/cells/#/ShapesController/PostWorksheetGroupShape'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet6/shapes/group?folder=TestData/In
    -X POST 
    -H "Authorization: Bearer \<jwt token> " \
    -H "accept:application/json"
    -H "Content-Type: application/json"
    -d '' 

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 title-msg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href='https://github.com/aspose-cells-cloud'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP"  tabName17="Python"  tabName18="Ruby"  >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostWorksheetGroupShape.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetGroupShape.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetGroupShape.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetGroupShape.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetGroupShape.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetGroupShape.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetGroupShape.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetGroupShape.rb" >}}
{{< /tab >}}

{{< /tabs >}}
