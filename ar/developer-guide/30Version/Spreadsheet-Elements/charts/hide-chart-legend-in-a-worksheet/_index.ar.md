---
title: "إخفاء أسطورة المخطط في ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
type: docs
url: /charts/legend/hide/
aliases: [/hide-chart-legend-in-a-worksheet/]
weight: 110
keywords: "Aspose.Cells, Excel, إخفاء أسطورة المخطط, واجهة برمجة تطبيقات REST, واجهة برمجة التطبيقات السحابية, أسطورة المخطط"
description: "تعرّف على كيفية إخفاء أسطورة مخطط في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. تتضمن الرابط (Endpoint) باستخدام HTTPS، ومصادقة مطلوبة، وبنية الطلب، وتفاصيل الاستجابة، ومعالجة الأخطاء، وأمثلة لواجهات برمجة التطبيقات (SDKs)."
---

تقوم هذه الواجهة بـإخفاء أسطورة المخطط. تُعد **أسطورة المخطط** هي المربع الذي يُعرّف سلاسل البيانات المُرسَمة في المخطط.

تتطلب الواجهة رمزًا صالحًا لـ Aspose Cloud JWT، ويجب تحميل المصنف إلى تخزين Aspose Cloud، وتستخدم الإصدار **v3.0** من الواجهة.

## الأمان والمصادقة
واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة تطبيقات REST

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend
```

### معلمات الطلب

| اسم المعلمة   | النوع   | الموقع | الوصف                                    |
| ------------- | ------- | ------ | ----------------------------------------- |
| **name**      | نص (string) | path   | اسم المصنف.                              |
| **sheetName** | نص (string) | path   | اسم ورقة العمل.                           |
| **chartIndex**| عدد صحيح (integer) | path   | فهرس المخطط.                             |
| **folder**    | نص (string) | query  | مجلد المصنف (اختياري).                   |
| **storageName**| نص (string) | query  | اسم التخزين (اختياري).                    |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartLegend) هذه الواجهة البرمجية المتاحة علنًا.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء الواجهة بسهولة. يُظهر المثال أدناه طلبًا لإخفاء أسطورة المخطط رقم 0 في ملف _Sample_Test_Book.xls_.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/legend" \
  -X DELETE \
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

{{< /tab >}}

{{< /tabs >}}

## الاستجابات

| حالة HTTP                     | الوصف                                      | مثال JSON                                                     |
| ----------------------------- | ------------------------------------------- | ------------------------------------------------------------- |
| **200 OK**                    | تم إخفاء أسطورة المخطط بنجاح.               | `{ "Code": 200, "Status": "OK" }`                             |
| **401 Unauthorized**          | رمز JWT مفقود أو غير صالح.                 | `{ "Code": 401, "Message": "Invalid access token." }`         |
| **404 Not Found**             | المصنف أو ورقة العمل أو المخطط غير موجود.  | `{ "Code": 404, "Message": "Chart not found." }`              |
| **500 Internal Server Error** | خطأ غير متوقع في الخادم.                   | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

## الأسئلة الشائعة (FAQ)

**س:** كيف يمكنني إخفاء أسطورة المخطط باستخدام Aspose.Cells Cloud؟  
**ج:** أرسل طلب `DELETE` إلى الرابط `https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/legend` مع رمز JWT صالح في رأس `Authorization`. استجابة `200 OK` تشير إلى نجاح العملية.

**س:** ما نوع المصادقة المطلوبة لواجهة إخفاء أسطورة المخطط؟  
**ج:** تضمن رأس `Authorization: Bearer <jwt token>`. احصل على الرمز عبر تدفق مصادقة OAuth في Aspose Cloud.

**س:** ما الاستجابة الخطأ التي سأحصل عليها إذا كان فهرس المخطط غير صالح؟  
**ج:** تعيد الخدمة `404 Not Found` مع جسم JSON يحتوي على `Code: 404` ورسالة تصف المخطط المفقود.

**س:** هل يمكنني استخدام HTTP بدلاً من HTTPS؟  
**ج:** لا. جميع نقاط نهاية Aspose Cloud تتطلب HTTPS لأغراض الأمان.

## عائلة واجهات برمجة التطبيقات السحابية (Cloud SDK Family)

استخدام واجهات برمجة التطبيقات (SDK) هو أسرع طريقة لتطوير التطبيقات. فواجهات SDK تُجرّد التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بواجهات برمجة التطبيقات السحابية لـ Aspose.Cells.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-HideChartLegend-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartLegend-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_legend_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideChartLegendInWorkSheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-HideChartLegend-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-HideChartLegend-hide-chart-legend.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
**قريبًا** – سيتم إضافة مثال لواجهة SDK الخاصة بـ Swift قريبًا.  
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-HideChartLegend-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3eb15aa10e3d2cd8931e60f8d001fd1c" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "إخفاء أسطورة المخطط في ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud",
  "description": "دليل خطوة بخطوة لإخفاء أسطورة المخطط في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. تتضمن الرابط باستخدام HTTPS، والمصادقة، وبنية الطلب، وتفاصيل الاستجابة، ومعالجة الأخطاء، وأمثلة لواجهات برمجة التطبيقات (SDKs).",
  "breadcrumb": {
    "@type": "BreadcrumbList",
    "itemListElement": [
      { "@type": "ListItem", "position": 1, "name": "الصفحة الرئيسية", "item": "https://docs.aspose.cloud/" },
      { "@type": "ListItem", "position": 2, "name": "Cells", "item": "https://docs.aspose.cloud/cells/" },
      { "@type": "ListItem", "position": 3, "name": "Charts", "item": "https://docs.aspose.cloud/cells/charts/" },
      { "@type": "ListItem", "position": 4, "name": "إخفاء أسطورة المخطط", "item": "https://docs.aspose.cloud/cells/charts/legend/hide/" }
    ]
  },
  "about": "إخفاء أسطورة المخطط باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
}
</script>