---
title: "استرجاع مخطط من ورقة عمل"
type: docs
url: /ar/charts/get/
aliases: [  /ar/get-chart-from-a-worksheet/ ]
weight: 10
keywords: "Aspose.Cells Cloud, استرجاع المخطط, ورقة العمل, واجهة REST API, Excel, واجهة مخطط, استرجاع المخطط, مخطط Excel"
description: "استرجاع معلومات المخطط، بما في ذلك البيانات الوصفية وتنسيق التصدير، من ورقة عمل باستخدام واجهة Aspose.Cells Cloud REST API."
ArticleTitle: "استرجاع مخطط من ورقة عمل – واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة REST باسترجاع معلومات المخطط.

**المتطلبات المسبقة** – لاستدعاء هذه النقطة النهائية، يجب أن تمتلك حسابًا صالحًا على Aspose.Cells Cloud، وموقع تخزين نشط، ورمز وصول JWT. احصل على الرمز المميز اتباعًا للتعليمات في دليل المصادقة قبل إجراء أي طلبات API.

## واجهة GetWorksheetChart

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}
```

### **الأمان والمصادقة**

واجهات Aspose.Cells Cloud آمنة وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع    | الموقع | الوصف                                     |
|-------------|---------|--------|--------------------------------------------|
| name        | string  | path   | اسم ملف Excel.                             |
| sheetName   | string  | path   | اسم ورقة العمل التي يحتوي المخطط عليها.    |
| chartNumber | integer | path   | المؤشر المبدئي (صفر-الأساس) للمخطط المراد استرجاعه. |
| format      | string  | query  | تنسيق التصدير المطلوب (مثل: png، jpeg).    |
| folder      | string  | query  | مسار المجلد حيث يتم تخزين المستند.         |
| storageName | string  | query  | اسم خدمة التخزين.                          |

### **الاستجابة**

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                                 |
|-------|----------------------------|--------------------------------------------------------|
| 200   | ناجح (OK)                  | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401   | غير مُصادَق (Unauthorized)  | رمز JWT غير صالح أو مفقود.                             |
| 413   | حملة كبيرة جدًا (Payload Too Large) | ملف مُرفع يتجاوز الحد الأقصى للحجم.                |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                         |

## كيفية استخدام واجهة GetWorksheetChart مع حزم تطوير البرمجيات (SDKs)

### مواصفات واجهة GetWorksheetChart

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart) واجهة برمجة تطبيقات قابلة للوصول العام، وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Chart": {
    "Name": "Chart 1",
    "Type": "Bar",
    "Top": 50,
    "Left": 100,
    "Width": 400,
    "Height": 300,
    "DataRange": "A1:B5",
    "ShowLegend": true,
    "Format": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام حزم تطوير البرمجيات Aspose.Cells Cloud

استخدام حزمة تطوير البرمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير. تتعامل SDK مع التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-GetChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_worksheet_charts_info-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetChartAreaFromWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-GetChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-GetChart-get-chart-from-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-GetChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "6fbcaeac3bd9fe1d22319418799757bd" >}}

{{< /tab >}}

{{< /tabs >}}
---