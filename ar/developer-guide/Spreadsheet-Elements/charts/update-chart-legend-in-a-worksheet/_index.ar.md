﻿---
title: تحديث أسطورة الرسم البياني في ورقة العمل
type: docs
url: /ar/charts/legend/update/
aliases: [/update-chart-legend-in-a-worksheet/]
weight: 160
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، تحديث أسطورة الرسم البياني في ورقة عمل
---
يشير هذا REST API إلى أسطورة مخطط التحديث
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم المصنف.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| مؤشر الرسم البياني| عدد صحيح| طريق| مؤشر الرسم البياني.|
| أسطورة|| جسم||
| مجلد| خيط| استفسار| مجلد المصنف.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|

 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v  "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" 
-d '{"Font":{"Color":{"A":"1", "R":"255", "G":"0", "B":"0"}, "DoubleSize":10.0, "IsBold":true, "IsItalic":false, "IsStrikeout":false, "IsSubscript":false, "IsSuperscript":false, "Name":"Arial", "Size":15, "Underline":"None"}, "Shadow":true}' 
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{

  "Code": "200",

  "Status": "OK"

} 

```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية
 
 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:
 

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_legend-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartLegendInWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartLegend-update-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "74fffa317bc5ba65dc6536005e5bb683" >}}

{{< /tab >}}

{{< /tabs >}}
