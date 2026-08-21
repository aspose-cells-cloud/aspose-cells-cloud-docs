---
title: "احصل على تنسيق ملء منطقة المخطط – واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
type: docs
url: /ar/charts/chart-area/fill-format/get/
aliases: [  /ar/get-fill-format-of-a-chart-area-from-a-worksheet/ ]
weight: 70
keywords:
  - "Aspose.Cells"
  - "Chart Area"
  - "Fill Format"
  - "REST API"
  - "Excel"
description: "استرداد تنسيق الملء (اللون، النمط، التدرج) لمنطقة مخطط داخل ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. يتضمن مثالًا باستخدام cURL، ومقتطفات كود SDK، وخطوات المصادقة، وتفاصيل الاستجابة."
ArticleTitle: "احصل على تنسيق ملء منطقة المخطط باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud الإصدار 3.0"
---

تسترجع هذه الواجهة REST معلومات تنسيق الملء لمنطقة **Chart Area**.

**المتطلبات المسبقة**  
لاستدعاء هذه النقطة النهائية، يجب أن تمتلك رمز وصول OAuth/JWT ساري المفعول. احصل على الرمز باستخدام تدفق المصادقة الخاص بـ Aspose.Cells Cloud، ثم أدخله في رأس `Authorization` على النحو التالي: `Bearer <jwt token>`. وإذا كنت تستخدم أحد SDKs، فتأكد من إعداده بـ `client_id` و`client_secret` قبل استدعاء الدالة.

## واجهة برمجة التطبيقات GetChartAreaFillFormat

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/chartArea/fillFormat
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع    | الموقع | الوصف                               |
|-------------|----------|--------|---------------------------------------|
| name        | string   | path   | اسم ملف العمل (Workbook).             |
| sheetName   | string   | path   | اسم ورقة العمل.                       |
| chartIndex  | integer  | path   | فهرس المخطط.                          |
| folder      | string   | query  | المجلد الذي يحتوي على ملف العمل.      |
| storageName | string   | query  | اسم وحدة التخزين.                     |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/ChartArea/GetChartAreaFillFormat) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية استدعاء الواجهة باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0/chartArea/fillFormat" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "FillFormat": {
    "Type": "Automatic"
  },
  "Code": 200,
  "Status": "OK"
}
```

**ملاحظات**  
- يُرجع الطلب الناجح الرمز HTTP 200 مع تفاصيل تنسيق الملء.  
- يشير الرمز HTTP 401 إلى فشل المصادقة (رمز غير صالح أو مفقود).  
- يُرجع الرمز HTTP 404 عند عدم وجود ملف العمل أو ورقة العمل أو مؤشر المخطط المحدّد.  
- يشير الرمز HTTP 500 إلى خطأ من جانب الخادم؛ حاول إعادة إرسال الطلب أو تواصل مع الدعم إذا استمرت المشكلة.

| الرمز | المعنى                                              |
|-------|------------------------------------------------------|
| 200   | نجاح – تم إرجاع تنسيق الملء                         |
| 401   | غير مُصرّح – رمز غير صالح أو مفقود                 |
| 404   | غير موجود – ملف العمل أو ورقة العمل أو المخطط غير موجود |
| 500   | خطأ داخلي في الخادم                                 |

لعمليات ذات صلة، راجع طرفيّة **Get Chart Area Border** (احصل على حدود منطقة المخطط) و**Get Chart Title** (احصل على عنوان المخطط).

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يُتعامل SDK مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChartFillFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetChartAreaFillFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_area_fill_format_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetFillFormatOfChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChartFillFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChartFillFormat-get-fill-format.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChartFillFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9af13f9a5cf8dee333f8d5e26c32866" >}}

{{< /tab >}}

{{< /tabs >}}
---