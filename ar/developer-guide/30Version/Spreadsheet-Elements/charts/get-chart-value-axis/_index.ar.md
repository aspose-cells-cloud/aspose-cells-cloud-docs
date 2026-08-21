---
title: "الحصول على محور القيمة في المخطط"
type: docs
url: /ar/charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, محور القيمة في المخطط, REST API, Excel, Cloud SDK, الحصول على محور القيمة في المخطط
description: "واجهة برمجة تطبيقات Aspose.Cells Cloud REST API - استرجاع محور القيمة في مخطط ضمن ورقة عمل Excel."
ArticleTitle: "الحصول على محور القيمة في المخطط - Aspose.Cells Cloud REST API"
---

تقوم هذه الواجهة البرمجية REST باسترجاع محور القيمة في مخطط. وهي جزء من **واجهة برمجة تطبيقات Aspose.Cells Cloud REST** وتعمل مع أوراق عمل Excel المخزنة في السحابة.

للاطلاع على العمليات ذات الصلة، راجع نقطة النهاية **[الحصول على محور الفئة في المخطط](/charts/category-axis/get/)**.

## واجهة برمجة التطبيقات GetChartValueAxis

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| name | string | path | اسم ملف Excel (مع امتداد الملف). |
| sheetName | string | path | اسم ورقة العمل التي تحتوي على المخطط. |
| chartIndex | integer | path | المؤشر (بدءًا من الصفر) للمخطط داخل ورقة العمل. |
| folder | string | query | المجلد في تخزين السحابة حيث يقع الملف. |
| storageName | string | query | اسم خدمة التخزين (مثل Aspose Cloud). |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) واجهة برمجة تطبيقات قابلة للوصول بشكل عام، وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاء لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
 -X GET \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "القيم",
    "Format": {
      "NumberFormat": "General",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**رموز حالة HTTP المحتملة**

| الرمز | الوصف |
|-------|--------|
| 200 | نجاح – يتم إرجاع معلومات محور القيمة. |
| 400 | طلب غير صالح – معاملات مطلوبة مفقودة أو غير صالحة. |
| 401 | غير مُصادق – رمز المصادقة مفقود أو غير صالح. |
| 404 | غير موجود – المصنف أو ورقة العمل أو المخطط المحدّد غير موجود. |
| 500 | خطأ داخلي في الخادم – حدث خطأ غير متوقع على الخادم. |

تحتوي الاستجابة على كائن `ValueAxis` مفصّل يحتوي على خصائص مثل `Minimum` و`Maximum` و`MajorUnit` و`MinorUnit` و`Title` و`Format`. وفي حالة التنفيذ الكامل، قد تُقدّم تفاصيل إضافية للتنسيق.

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK إدارة التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء استدعاءات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}