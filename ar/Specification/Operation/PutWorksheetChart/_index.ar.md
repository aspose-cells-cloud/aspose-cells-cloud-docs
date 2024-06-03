---
title: PutWorksheetChar
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/specification/operation/putworksheetchart/
description: إضافة مخطط جديد في ورقة العمل
kwords: Excel، Office، جدول البيانات، Cloud REST API، PutWorksheetChart
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="PutWorksheetChart" >}}
{{< blocks/products/cells/docs-title titlemsg="Add a new chart in the worksheet." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API، طريقة المتشعب، الوصف، مرجع API" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name}/worksheets/{sheetName}/charts,PUT,أضف مخططًا جديدًا في ورقة العمل.,<a href=\'https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChart\'> وضع ورقة عمل الرسم البياني</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="اسم المعلمة، النوع، الوصف" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="الاسم، السلسلة، اسم الملف." >}} 
     {{< blocks/products/cells/docs-Parameter-content columns="اسم الورقة، سلسلة، اسم ورقة العمل." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="اسم المعلمة، النوع، الوصف" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="مخطط نوع، سلسلة، نوع المخطط، يرجى الرجوع إلى الخاصية اكتب في مورد المخطط." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="UpperLeftRow،عدد صحيح،الصف العلوي الأيسر للمخطط الجديد." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="UpperLeftColumn,integer,العمود العلوي الأيسر للمخطط الجديد." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="LowerRightRow,integer,الصف السفلي الأيسر للمخطط الجديد." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="LowerRightColumn,integer,العمود السفلي الأيسر للمخطط الجديد." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="منطقة، سلسلة، حدد القيم التي سيتم من خلالها رسم سلسلة البيانات." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns=" isVertical,boolean,حدد ما إذا كنت تريد رسم السلسلة من نطاق من قيم الخلايا حسب الصف أو حسب العمود." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="فئة البيانات، سلسلة، الحصول على أو تعيين نطاق قيم محور الفئة. يمكن أن يكون نطاقًا من الخلايا (على سبيل المثال، \'D1:E10\')." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoGetSerialName,boolean,حدد ما إذا كنت تريد التحديث التلقائي للاسم التسلسلي." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="عنوان، سلسلة، حدد اسم عنوان المخطط." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="المجلد، السلسلة، المجلد الذي يوجد به الملف." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabels,boolean,يمثل سلوك عرض قيم تسمية بيانات المخطط المحدد. صحيح لعرض القيم، وخطأ لإخفائها." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="dataLabelsPosition,string,يمثل موضع تسمية البيانات (مركز/InsideBase/InsideEnd/OutsideEnd/أعلى/أسفل/يسار/يمين/BestFit/منقول)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="PivotTableSheet,string,المصدر هو بيانات PivotTable. إذا لم يكن PivotSource فارغاً، فهذا يعني أن المخطط هو PivotChart." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="PivotTableName,string,اسم الجدول المحوري." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="اسم التخزين، سلسلة، اسم التخزين حيث يوجد الملف." >}} 
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
