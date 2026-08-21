---
title: "تحديث أسطورة المخطط في ورقة عمل"
type: docs
url: /charts/legend/update/
aliases: [/update-chart-legend-in-a-worksheet/]
weight: 160
keywords: "Aspose.Cells، السحابة، Excel، مخطط، أسطورة، واجهة برمجة التطبيقات REST، تحديث، ورقة عمل، cURL، SDK"
description: "كيفية تحديث أسطورة مخطط في ورقة عمل Excel باستخدام واجهة برمجة التطبيقات REST لـ Aspose.Cells Cloud، مع أمثلة لطلبات cURL وأكواد مقتطفات SDK بلغات برمجة متعددة."
ArticleTitle: "تحديث أسطورة المخطط في ورقة عمل – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية (REST API) بتحديث أسطورة المخطط.

**المتطلبات المسبقة:** لاستخدام هذه النهاية (endpoint)، يجب أن تمتلك رمز JWT صالح لـ Aspose Cloud، ويجب أن يكون الملف المطلوب مخزنًا في موقع دعم للتخزين (الافتراضي هو مستودع Aspose Cloud). تأكد من أن اسم الملف، واسم ورقة العمل، وفهرس المخطط صحيحة.

تعرض أسطورة المخطط أسماء ورموز سلاسل البيانات في المخطط. يسمح لك التحديث بالأسطورة بتخصيص مظهرها، مثل نمط الخط، واللون، والظل.

## واجهة PostWorksheetChartLegend برمجية

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة قائمة على رمز <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a>، وهي آمنة.

### معاملات الطلب

| اسم المعامل      | النوع    | الموقع | الوصف                                        |
| ---------------- | -------- | ------ | --------------------------------------------- |
| name             | string   | path   | اسم ملف العمل (Workbook).                     |
| sheetName        | string   | path   | اسم ورقة العمل.                               |
| chartIndex       | integer  | path   | فهرس المخطط المراد تعديله.                    |
| legend           | object   | body   | كائن JSON يُعرّف إعدادات الأسطورة.             |
| folder           | string   | query  | المجلد الذي يحتوي على ملف العمل.              |
| storageName      | string   | query  | اسم المستودع (Storage).                       |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartLegend) واجهة برمجة تطبيقات عامة قابلة للاستخدام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-d '{"Font":{"Color":{"A":"1","R":"255","G":"0","B":"0"},"DoubleSize":10.0,"IsBold":true,"IsItalic":false,"IsStrikeout":false,"IsSubscript":false,"IsSuperscript":false,"Name":"Arial","Size":15,"Underline":"None"},"Shadow":true}' \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

استخدام SDK يُسرّع عملية التطوير، حيث يتعامل SDK مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

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