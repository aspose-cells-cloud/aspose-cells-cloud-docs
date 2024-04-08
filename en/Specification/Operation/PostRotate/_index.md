---
title: "PostRotate"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/operation/postrotate/
description: "Rotate rows, columns, or other objects in Excel files and save them in various formats."
weight: 50

---


{{< blocks/products/cells/docs-title titlemsg="PostRotate" >}}
{{< blocks/products/cells/docs-title titlemsg="Rotate rows, columns, or other objects in Excel files and save them in various formats." >}}

{{< blocks/products/cells/docs-Parameter parameter-title="REST API" columns="API,HttpMethod,Description,API reference" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/rotate,POST,Rotate rows, columns, or other objects in Excel files and save them in various formats.,<a href='https://apireference.aspose.cloud/cells/#/LightCells/PostRotate'>PostRotate</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parameter-title="Query Parameter" columns="Parameter Name,Type,Description" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="rotateType,string,270/90/row/col/row2col" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outFormat,string,The output data file format.(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/BMP/MD[Markdown]/Numbers)" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="password,string,The password needed to open an Excel file." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction,boolean,Whether check restriction of excel file when user modify cells related objects." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="region,string,The regional settings for workbook." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href='https://apireference.aspose.cloud/cells/#/LightCellsController/PostRotate'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/rotate
    -X POST 
    -H "Authorization: Bearer \<jwt token> " \
 -F '
file=@;filename='
```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 title-msg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href='https://github.com/aspose-cells-cloud'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP"  tabName17="Python"  tabName18="Ruby"  >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostRotate.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRotate.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRotate.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRotate.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRotate.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRotate.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRotate.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRotate.rb" >}}
{{< /tab >}}

{{< /tabs >}}
