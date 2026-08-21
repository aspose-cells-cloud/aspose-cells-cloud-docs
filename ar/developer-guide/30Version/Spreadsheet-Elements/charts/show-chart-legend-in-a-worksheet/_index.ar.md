---
title: "عرض أسطورة المخطط في ورقة عمل"
type: docs
url: /ar/charts/legend/show/
aliases: [  /ar/show-chart-legend-in-a-worksheet/ ]
weight: 100
keywords: "Aspose.Cells Cloud, API أسطورة المخطط, أسطورة مخطط Excel, REST PUT لأسطورة المخطط, Aspose API v3.0"
description: "تعرّف على كيفية عرض أسطورة المخطط في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن تفاصيل نقطة النهاية، والمعاملات، ومثال cURL، ومقتطفات SDK."
---

تتيح لك هذه واجهة REST API عرض **أسطورة المخطط**—المربع التفسيري الذي يُعرّف سلاسل البيانات—في مخطط موجود في ورقة عمل من ملف Excel.

## واجهة REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### معاملات الطلب

| اسم المعامل      | النوع    | الموقع  | الوصف                                                |
| ---------------- | -------- | ------- | ---------------------------------------------------- |
| name             | string   | path    | اسم ملف المصنف.                                      |
| sheetName        | string   | path    | اسم ورقة العمل التي يحتوي المخطط عليها.             |
| chartIndex       | integer  | path    | الفهرس (الصفر-الأساسي) للمخطط.                      |
| folder           | string   | query   | المجلد الذي يحتوي على المصنف.                       |
| storageName      | string   | query   | اسم خدمة التخزين.                                    |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/PutWorksheetChartLegend) واجهة برمجة تطبيق متاحة عمومًا، ويتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يتم تنفيذ المصادقة باستخدام رمز JWT من نوع Bearer يُزوَّد في رأس **Authorization**.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء الاستدعاء باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

يمكن أن تُعيد الواجهة رموز حالة HTTP التالية:

- **200 OK** – تم عرض الأسطورة بنجاح.
- **400 Bad Request** – معاملات غير صالحة.
- **401 Unauthorized** – فشلت المصادقة.
- **404 Not Found** – المصنف أو الورقة أو المخطط المحدد غير موجود.
- **500 Internal Server Error** – حدث خطأ غير متوقع في الخادم.

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير، فهو يتعامل مع التفاصيل منخفضة المستوى ويُمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء استدعاءات إلى خدمات Aspose.Cells باستخدام مكتبات SDK متنوعة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ShowChartLegend-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PutWorksheetChartLegend-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-show_legend_in_chart-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ShowChartLegendInAWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ShowChartLegend-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ShowChartLegend-show-chart-legend.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ShowChartLegend-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "f9f1d14e3b6985c0a44ec7acdd4f56b2" >}}
{{< /tab >}}

{{< /tabs >}}