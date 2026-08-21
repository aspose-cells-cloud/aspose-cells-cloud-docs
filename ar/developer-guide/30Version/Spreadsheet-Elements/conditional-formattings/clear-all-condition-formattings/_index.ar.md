---
title: "مسح التنسيق الشرطي"
type: docs
url: /ar/conditional-formattings/clear/
aliases: [  /ar/clear-all-condition-formattings/ ]
keywords: "Aspose.Cells Cloud, REST API, مسح التنسيق الشرطي, Excel, أوراق العمل, JWT, الإصدار 3.2"
description: "حذف جميع قواعد التنسيق الشرطي من ورقة عمل باستخدام واجهة Aspose.Cells Cloud API (الإصدار 3.2). تعلّم بناء جملة الطلب، والمعلمات المطلوبة، وخطوات المصادقة، وشاهد أمثلة على الشيفرة البرمجية في مكتبات SDK متعددة."
weight: 80
---

تقوم هذه الواجهة البرمجية (REST API) بمسح جميع قواعد التنسيق الشرطي من ورقة عمل.

## واجهة برمجة التطبيقات REST

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### معلمات الطلب

| اسم المعلمة | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| **name** | سلسلة نصية | المسار | اسم ملف المصنف (مثل `Book1.xlsx`). |
| **sheetName** | سلسلة نصية | المسار | اسم ورقة العمل التي سيتم إزالة التنسيق الشرطي منها. |
| **folder** | سلسلة نصية | الاستعلام | _(اختياري)_ مسار المجلد في التخزين حيث يقع المصنف. |
| **storageName** | سلسلة نصية | الاستعلام | _(اختياري)_ اسم خدمة التخزين. |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) واجهة برمجة تطبيقات متاحة للعامة، كما تتيح لك **مواصفات OpenAPI** إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X DELETE \
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

### استجابات الأخطاء

| كود HTTP | السبب | مثال على جسم الاستجابة |
|----------|--------|------------------------|
| **400** | طلب غير صالح – معلمات مفقودة أو غير صالحة. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | غير مصادق عليه – رمز JWT مفقود أو غير صالح. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | غير موجود – ملف المصنف أو ورقة العمل غير موجود. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | خطأ داخلي في الخادم – فشل غير متوقع في الخادم. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## أمثلة لـ SDKs

استخدام SDK يُعد أفضل طريقة لتسريع عملية التطوير، حيث تُدار التفاصيل من المستوى المنخفض تلقائيًا لتمكنك من التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر الأمثلة التالية كيفية إجراء المكالمات إلى خدمات Aspose.Cells عبر الويب باستخدام مكتبات SDK متنوعة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}