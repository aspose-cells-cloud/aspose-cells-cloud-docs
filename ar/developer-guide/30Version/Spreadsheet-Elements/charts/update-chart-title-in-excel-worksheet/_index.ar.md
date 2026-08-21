---
title: "تحديث عنوان المخطط في ورقة عمل إكسل"
type: docs
url: /charts/title/update/
aliases: [/update-chart-title-in-excel-worksheet/]
weight: 160
keywords: Excel, Aspose.Cells, REST API, عنوان المخطط, تحديث, Cloud SDK
description: تعلّم كيفية تحديث عنوان مخطط في ورقة عمل إكسل باستخدام Aspose.Cells Cloud REST API وcURL ومتعدد من SDKs.
ArticleTitle: "تحديث عنوان المخطط في ورقة عمل إكسل – وثائق Aspose.Cells Cloud"
---

يقوم هذا الـ REST API بتحديث عنوان المخطط.

**المتطلبات الأساسية:** يجب أن يكون لديك حساب Aspose Cloud ساري المفعول ورمز مميز JWT للتوثيق. تشمل الخطوات النموذجية ما يلي:

- التسجيل في حساب Aspose Cloud.  
- إنشاء رمز مميز JWT عبر نقطة نهاية المصادقة.  
- التأكد من تخزين ملف العمل المستهدف في تخزين سحابي مدعوم (افتراضي أو مخصص).

## PostWorksheetChartTitle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

يجب إجراء جميع استدعاءات API عبر بروتوكول **HTTPS** لتجنب تحذيرات المحتوى المختلط.

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز مميز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| ------------ | ------- | -------- | ------------------------------ |
| name | string | path | اسم ملف العمل (Workbook). |
| sheetName | string | path | اسم ورقة العمل. |
| chartIndex | integer | path | الفهرس الصفري (zero-based) للمخطط. |
| title | string | body | العنوان الجديد للمخطط. |
| folder | string | query | مجلد ملف العمل. |
| storageName | string | query | اسم التخزين. |

### رموز حالة الاستجابة

| الرمز | الوصف |
| ---- | ---------------------------------------- |
| 200 | نجاح العملية (OK) – تم تحديث عنوان المخطط بنجاح. |
| 400 | طلب غير صالح (Bad Request) – معاملات ناقصة أو غير صحيحة. |
| 401 | غير مخوّل (Unauthorized) – رمز مميز JWT غير صالح أو مفقود. |
| 404 | غير موجود (Not Found) – ملف العمل أو ورقة العمل أو المخطط غير موجود. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) – حالة غير متوقعة في الخادم. |

**ملاحظة:** الفهرس `chartIndex` يبدأ من الصفر (zero-based)، ويُشار إلى أول مخطط في ورقة العمل بالرقم `0`.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChartTitle" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v POST "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
-d '{"title":"Stock exchange"}' \
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

## مجموعة أدوات SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى مجموعة SDK إدارة التفاصيل منخفضة المستوى وتركّز أنت على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء استدعاءات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-UpdateChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-PostWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-update_chart_title-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UpdateChartTitleInExcelWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-UpdateChartTitle-update-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "aab21ae55930321e6eaa46ffe5b8e7bf" >}}

{{< /tab >}}

{{< /tabs >}}