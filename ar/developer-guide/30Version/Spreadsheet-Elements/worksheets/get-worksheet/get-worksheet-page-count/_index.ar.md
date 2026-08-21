---
title: "الحصول على عدد الصفحات لورقة عمل Excel"
second_title: "مستند"
linktitle: "عددالصفحات"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, API Excel, عدد صفحات ورقة العمل, REST, SDK السحابي, ترقيم الصفحات في Excel"
description: "استرجاع عدد الصفحات القابلة للطباعة في ورقة عمل Excel باستخدام REST API الخاص بـ Aspose.Cells Cloud (الإصدار 3.0). يشمل تنسيق طلب HTTPS، خطوات المصادقة، مثال باستخدام cURL، استجابة JSON كاملة، رموز الحالة، وأكواد الأمثلة الخاصة بـ SDK."
weight: 10
ArticleTitle: "الحصول على عدد الصفحات لورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تُعيد هذه الواجهة البرمجية REST **عدد الصفحات** لورقة العمل.

**المصادقة:** تتطلب جميع نقاط نهاية Aspose.Cells Cloud رمز Bearer يُحصل عليه عبر تدفق OAuth2. يجب تضمين الرمز في رأس `Authorization` كما هو موضح في مثال cURL أدناه.

## واجهة برمجة التطبيقات REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### معاملات الطلب

| المعامل     | النوع   | الموقع   | الوصف                              |
| ----------- | ------- | -------- | ---------------------------------- |
| name        | string  | path     | اسم المستند.                        |
| sheetName   | string  | path     | اسم ورقة العمل.                     |
| folder      | string  | query    | المجلد الذي يحتوي على المستند.     |
| storageName | string  | query    | اسم مساحة التخزين.                 |

تعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) على واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء الواجهة البرمجية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### تفاصيل الاستجابة

| رمز الحالة HTTP | المعنى                                              |
| --------------- | ---------------------------------------------------- |
| **200**         | نجاح – يُعيد حمولة JSON كما هو موضح أعلاه.          |
| **401**         | غير مصرّح – نقص أو عدم صلاحية الرمز.               |
| **404**         | غير موجود – الملف أو ورقة العمل غير موجودين.       |
| **500**         | خطأ داخلي في الخادم – ظرف غير متوقع في الخادم.     |

### تاريخ الإصدارات

**إصدار الواجهة v3.0** (أُصدر في 2025). إذا كنت تستخدم إصدارًا أحدث، فراجع وثائق نقطة النهاية المحدّثة.

## عائلة SDK السحابية

استخدام SDK هو أسرع طريقة لتطوير البرمجيات. فتقوم SDK بإخفاء التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على منطق أعمالك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKات مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### ملاحظات

- يعكس عدد الصفحات التخطيط القابل للطباعة، مع أخذ فواصل الصفحات، الهوامش، والتحجيم في الاعتبار. وقد تؤثر الصفوف أو الأعمدة المخفية على النتيجة.
- تأكد من وجود ورقة العمل المستهدفة، وتخزين الملف في المجلد المحدد `folder` و `storageName` قبل إرسال الطلب.