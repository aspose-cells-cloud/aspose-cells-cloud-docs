---
title: PostRevers
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/specification/operation/postreverse/
description: عكس الصفوف أو الأعمدة في ملفات Excel وإنشاء ملفات الإخراج بتنسيقات مختلفة
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PostReverse" >}}
{{< blocks/products/cells/docs-title titlemsg="Reverse rows or columns in Excel files and create output files in various formats." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API، طريقة المتشعب، الوصف، مرجع API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/reverse,POST,عكس الصفوف أو الأعمدة في ملفات Excel وإنشاء ملفات الإخراج بتنسيقات مختلفة.,<a href=\'https://apireference.aspose.cloud/cells/#/LightCells/PostReverse\'>PostReverse</ أ>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="اسم المعلمة، النوع، الوصف" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="نوع التدوير، السلسلة، الصفوف/الأعمدة/كلاهما" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outFormat,string,تنسيق ملف بيانات الإخراج.(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF /BMP/MD[تخفيض السعر]/الأرقام)" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="كلمة المرور، سلسلة، كلمة المرور اللازمة لفتح ملف Excel." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction,boolean,ما إذا كان يتم التحقق من تقييد ملف Excel عندما يقوم المستخدم بتعديل الكائنات ذات الصلة بالخلايا." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="المنطقة، سلسلة، الإعدادات الإقليمية للمصنف." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/LightCellsController/PostReverse\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/reverse?rotateType=rows&outFormat=pdf"
    -X POST 
    -H "Authorization: Bearer \<jwt token> " \
 -F '
file=@Book1.xlsx;filename=Book1.xlsx'
```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PostReverse.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReverse.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReverse.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReverse.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReverse.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReverse.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReverse.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReverse.rb" >}}
{{< /tab >}}

{{< /tabs >}}
