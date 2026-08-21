---
title: "تحويل مخطط Excel إلى صورة – واجهة Aspose.Cells Cloud REST API"
type: docs
url: /ar/charts/to-image/
aliases: [  /ar/convert-charts-to-image/ ]
weight: 50
keywords: "Aspose.Cells Cloud، تحويل المخطط إلى صورة، تحويل مخططات Excel، واجهة REST API، تنسيق الصورة، PNG، JPEG، BMP، TIFF، GIF"
description: "تعلم كيفية تحويل كائنات المخططات في Excel إلى صور بتنسيقات PNG أو JPEG أو BMP أو TIFF أو GIF باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن تفاصيل نقطة النهاية، المعلمات، مثال باستخدام cURL، مقاطع كود لواجهات برمجة التطبيقات (SDK)، مثال على الاستجابة، ومعالجة الأخطاء."
ArticleTitle: "تحويل مخطط Excel إلى صورة – واجهة Aspose.Cells Cloud REST API"
---

توضح واجهة REST هذه كيفية تحويل **مخطط Excel** إلى صورة باستخدام **Aspose.Cells Cloud**.

## واجهة PutWorksheetAddChart API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartNumber}?format={format}
```

تشمل تنسيقات الصور المدعومة `png` و `jpeg` و `bmp` و `tiff` و `gif`.

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة | النوع    | الموقع | الوصف                     |
|------------|---------|--------|---------------------------|
| name       | string  | path   | اسم المستند.              |
| sheetName  | string  | path   | اسم ورقة العمل.           |
| chartNumber| integer | path   | رقم المخطط.               |
| format     | string  | query  | تنسيق الملف المصدر.       |
| folder     | string  | query  | مجلد المستند.             |
| storageName| string  | query  | اسم وحدة التخزين.         |

### **الاستجابة**

تُرجع نقطة النهاية ملف الصورة بالتنسيق المطلوب كدفق ثنائي (مثل `byte[]`). يتطابق رأس `Content-Type` في الاستجابة مع تنسيق الصورة المحدد، مثل `image/png` أو `image/jpeg` وما إلى ذلك.

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                           |
|------|----------------------------|------------------------------------------------|
| 200  | OK (تم بنجاح)              | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request (طلب خاطئ)     | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized (غير مخوّل)    | رمز JWT غير صالح أو مفقود.                     |
| 413  | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PutWorksheetAddChart API باستخدام واجهات برمجة التطبيقات (SDKs)

### مواصفات واجهة PutWorksheetAddChart API

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/Charts/GetWorksheetChart" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0?format=jpg" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```text
byte[]
```

{{< /tab >}}

{{< /tabs >}}

### استخدام واجهات برمجة تطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام واجهة برمجة التطبيقات (SDK) هو أفضل طريقة لتسريع عملية التطوير. فواجهات برمجة التطبيقات (SDKs) تتعامل مع التفاصيل منخفضة المستوى وتسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بواجهات برمجة التطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات (SDKs) مختلفة:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Python" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-ConvertChartToImage-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-GetWorksheetChartWithFormat-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-get_chart_in_specified_format-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-ConvertChartToImage-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertChartToImage.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-ConvertChartToImage-convert-chart-to-image.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

مثال قادم قريبًا.

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-ConvertChartToImage-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d22256010a610e1351ab15969a7adeef" >}}

{{< /tab >}}

{{< /tabs >}}
---