﻿---
title: ضع ورقة عمل CustomFilte
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/specification/operation/putworksheetcustomfilter/
description: تصفية قائمة بمعايير مخصصة في ورقة العمل
kwords: Excel، Office، جدول البيانات، Cloud REST API، PutWorksheetCustomFilter
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetCustomFilter" >}}
{{< blocks/products/cells/docs-title titlemsg="Filter a list with custom criteria in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API، طريقة المتشعب، الوصف، مرجع API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/autoFilter/custom,PUT,تصفية قائمة بمعايير مخصصة في ورقة العمل.,<a href=\'https://apireference.aspose.cloud/cells/#/AutoFilter /PutWorksheetCustomFilter\'>PutWorksheetCustomFilter</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="اسم المعلمة، النوع، الوصف" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="الاسم، السلسلة، اسم المصنف." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="اسم الورقة، سلسلة، اسم ورقة العمل." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="اسم المعلمة، النوع، الوصف" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="range,string,يمثل النطاق الذي تنطبق عليه عملية التصفية التلقائية المحددة." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="fieldIndex,integer,الإزاحة الصحيحة للحقل الذي تريد إنشاء عامل التصفية عليه (من يسار القائمة؛ الحقل الموجود في أقصى اليسار هو الحقل 0)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="OperatorType1,string,نوع عامل التصفية" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="المعايير 1، سلسلة، المعايير المخصصة." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAnd، منطقية، صحيح/خطأ" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="عامل التشغيلType2، سلسلة،" >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="المعايير 2، سلسلة، المعايير المخصصة." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="matchBlanks,boolean,تطابق كافة الخلايا الفارغة في القائمة." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="تحديث، منطقي، تحديث المرشحات التلقائية لإخفاء الصفوف أو إظهارها." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="المجلد، السلسلة، المجلد الذي يوجد به الملف." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="اسم التخزين، سلسلة، اسم التخزين حيث يوجد الملف." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/AutoFilterController/PutWorksheetCustomFilter\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1&matchBlanks=false&refresh=true&folder=TestData/In"
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
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_PutWorksheetCustomFilter.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}
{{< /tab >}}

{{< /tabs >}}
