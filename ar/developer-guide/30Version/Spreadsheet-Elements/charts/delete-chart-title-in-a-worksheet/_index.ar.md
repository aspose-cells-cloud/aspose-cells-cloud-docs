---
title: "حذف عنوان المخطط في ورقة عمل"
type: docs
url: /ar/charts/delete-chart-title/
aliases: [  /ar/delete-chart-title-in-a-worksheet/ ]
weight: 150
keywords: "Aspose.Cells، واجهة برمجة التطبيقات السحابية، حذف عنوان المخطط، إكسل، REST، SDK"
description: "تعرّف على كيفية إزالة عنوان مخطط من ورقة عمل إكسل باستخدام واجهة Aspose.Cells Cloud REST API (النسخة 4.0). يتضمن أمثلة لـ cURL وSDKs، وإدارة الأخطاء."
---

تقوم هذه الواجهة REST بحذف عنوان المخطط.

## واجهة برمجة التطبيقات (REST API)

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/title
```

### الأمان والمصادقة

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud المصادقة باستخدام [رمز مميز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) (JWT token-based authentication).

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف                                    |
|-------------|---------|--------|-------------------------------------------|
| name        | string  | path   | اسم ملف المصنف.                           |
| sheetName   | string  | path   | اسم ورقة العمل.                           |
| chartIndex  | integer | path   | المؤشر (الصفر-مبني) للمخطط.               |
| folder      | string  | query  | المجلد الذي يحتوي على المصنف.            |
| storageName | string  | query  | اسم وحدة التخزين.                         |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الكود | المعنى                     | الوصف                                              |
|-------|----------------------------|-----------------------------------------------------|
| 200   | OK (تم بنجاح)             | تم تطبيق العامل بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب غير صحيح) | معاملات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401   | Unauthorized (غير مُAUTH)   | رمز مميز JWT غير صالح أو مفقود.                     |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به.         |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | حدث خطأ غير متوقع في الخادم.                  |

## كيفية استخدام واجهة DeleteWorksheetChartTitle باستخدام SDKs

### مواصفات واجهة DeleteWorksheetChartTitle API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetChartTitle) واجهة برمجة قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة cURL لاستخدام خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء الطلب، بما في ذلك رمز **Bearer JWT** المطلوب للمصادقة.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/title" \
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

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع التطوير. فتتولى SDK معالجة التفاصيل منخفضة المستوى وتسمح لك بالتركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChartTitle-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetChartTitle-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-hide_title_in_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChartTitle-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteChartTitle-delete-chart-title.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChartTitle-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3898d60ea8f7ea7bb460ffb5d7d29504" >}}

{{< /tab >}}

{{< /tabs >}}