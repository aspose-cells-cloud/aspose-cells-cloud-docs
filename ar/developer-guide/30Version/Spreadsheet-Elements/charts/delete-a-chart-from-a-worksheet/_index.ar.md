---
title: "حذف مخطط من ورقة عمل"
type: docs
url: /ar/charts/delete/
aliases: [/delete-a-chart-from-a-worksheet/]
weight: 40
keywords:
  - "Aspose.Cells"
  - "واجهة برمجة التطبيقات REST"
  - "حذف مخطط"
  - "ورقة عمل"
  - "إكسل"
  - "حزمة تطوير البرامج السحابية"
  - "حذف المخططات"
  - "مرجع واجهة برمجة التطبيقات"
description: "يحذف مخططًا من ورقة عمل باستخدام فهرسه الصفري المُعتمد على صفر عبر واجهة Aspose.Cells Cloud REST API."
ArticleTitle: "حذف مخطط من ورقة عمل باستخدام واجهة Aspose.Cells Cloud REST API"
---

تقوم هذه الواجهة البرمجية (REST) بحذف مخطط من ورقة عمل باستخدام فهرسه.

للاطلاع على العمليات ذات الصلة، راجع الصفحتين **[إضافة مخطط](#)** و **[الحصول على مخطط](#)**.

## واجهة برمجة التطبيقات REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### الأمان والمصادقة

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة قائمة على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معاملات الطلب

| اسم المعامل     | النوع    | الموقع | الوصف                                      |
|----------------|---------|--------|--------------------------------------------|
| name           | string  | path   | اسم المصنف.                                |
| sheetName      | string  | path   | اسم ورقة العمل.                            |
| chartIndex     | integer | path   | الفهرس الصفري المُعتمد على صفر للمخطط المراد حذفه. |
| folder         | string  | query  | المجلد الذي يحتوي على المصنف.             |
| storageName    | string  | query  | اسم وحدة التخزين المراد استخدامها.         |


### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                  | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصرّح (Unauthorized)    | رمز JWT غير صالح أو مفقود. |
| 413  | حجم البيانات كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PutWorksheetAddChart مع حزم تطوير البرامج (SDKs)

### مواصفات واجهة PutWorksheetAddChart

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمة لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
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

تعيد الواجهة رموز الحالة التالية:

| الرمز | الوصف                                 |
|------|---------------------------------------------|
| 200  | تم حذف المخطط بنجاح                         |
| 400  | طلب غير صالح (مثل فهرس غير صحيح)          |
| 401  | غير مصرّح (رمز JWT مفقود أو غير صالح)      |
| 404  | لم يتم العثور على المصنف أو ورقة العمل أو المخطط |
| 500  | خطأ في الخادم                                |

**معالجة الأخطاء:** للحصول على معلومات مفصّلة عن الأخطاء، راجع النموذج العام للأخطاء في مواصفات OpenAPI.

### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير، إذ تُجرّدك من التفاصيل منخفضة المستوى وتسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرامج الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام حزم تطوير البرامج المختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}