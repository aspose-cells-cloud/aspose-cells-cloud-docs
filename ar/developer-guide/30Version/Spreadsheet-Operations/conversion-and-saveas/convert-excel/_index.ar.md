---
title: "تحويل ملف إكسل إلى تنسيقات مختلفة"
ArticleTitle: "تحويل ملف إكسل إلى تنسيقات مختلفة"
second_title: "مستند"
linktype: "تحويل إكسل"
type: docs
url: /convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud، تحويل إكسل، تحويل تنسيق الملف، واجهة REST API، واجهة برمجة التطبيقات SDK، CSV، PDF، HTML، JSON، Markdown"
description: "قم بتحويل كتب عمل إكسل إلى تنسيقات مختلفة مثل CSV وPDF وHTML وJSON وMarkdown وغيرها باستخدام واجهة Aspose.Cells Cloud REST API."
weight: 10
---

قبل استدعاء هذه النقطة النهائية (endpoint)، تأكد من حصولك على رمز JWT صالح، ومن وجود ملف المصنف المصدر في موقع تخزين مدعوم (مثل: Aspose Cloud Storage). ضع الرمز في رأس `Authorization`، وحدّد معلمة الاستعلام `storageName` إن لزم الأمر.

تقوم هذه الواجهة REST API بتحويل ملف إكسل إلى تنسيقات إخراج مختلفة.

## PutConvertWorkBook API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

يكون الطلب عبارة عن طلب HTTP **PUT** بمحتوى متعدد الأجزاء (انظر [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
يحتوي الجزء الأول من جسم الطلب متعدد الأجزاء على **ملف البيانات**، بينما يحتوي الجزء الثاني على **خيارات الحفظ**.

### **الأمان والمصادقة**

تُعدّ واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الاستعلام (Query Parameters)

| اسم المعلمة            | النوع   | الوصف                                                                                                                |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | تنسيق ملف الإخراج المستهدف (مثل: CSV، XLS، HTML، PDF، XML، TXT، TIFF، PNG، JPG، GIF، EMF، BMP، MD، Numbers، WMF، SVG، إلخ). |
| `password`              | string | كلمة المرور المطلوبة لفتح ملف الإكسل المصدر.                                                                           |
| `outPath`               | string | المسار الكامل (بما في ذلك اسم الملف وامتداده) لملف إخراج واحد، أو مسار مجلد عند توليد ملفات متعددة. |
| `storageName`           | string | اسم مساحة التخزين التي يقع فيها ملف المصدر.                                                                         |
| `checkExcelRestriction` | bool   | عند القيمة **true**، يتحقق من قيود إكسل قبل تعديل الخلايا أو الكائنات المرتبطة بها.                                     |
| `streamFormat`          | string | تنسيق تدفق ملف الإدخال.                                                                                           |
| `region`                | string | الإعدادات الإقليمية المطبّقة على مصنف العمل.                                                                                 |
| `pageWideFitOnPerSheet` | bool   | ضبط عرض الصفحة لتناسب كل ورقة عمل عند التحويل إلى PDF.                                                           |
| `pageTallFitOnPerSheet` | bool   | ضبط ارتفاع الصفحة لتناسب كل ورقة عمل عند التحويل إلى PDF.                                                          |
| `sheetName`             | string | اسم ورقة العمل المراد تحويلها.                                                                                          |
| `pageIndex`             | string | فهرس الصفحة المراد تحويلها (يتطلب `sheetName`).                                                                       |
| `onePagePerSheet`       | bool   | عند القيمة **true**، يُولّد صفحة PDF واحدة لكل ورقة عمل.                                                                       |
| `AutoRowsFit`           | bool   | ضبط ارتفاع جميع الصفوف في مصنف العمل تلقائيًا.                                                                                        |
| `AutoColumnsFit`        | bool   | ضبط عرض الأعمدة في مصنف العمل تلقائيًا.                                                                                   |

### معلمات جسم الطلب (Request Body Parameters)

| اسم المعلمة | النوع      | الوصف                                                    |
| -------------- | --------- | -------------------------------------------------------------- |
| `datafile`     | data file | ملف الإكسل الموضّع في الجزء الأول من جسم الطلب متعدد الأجزاء. |
| `SaveOptions`  | object    | خيارات الحفظ الموضّحة في الجزء الثاني من جسم الطلب متعدد الأجزاء.  |

### **الاستجابة**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**رموز حالة HTTP**

| الكود | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | نجاح (OK)                          | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | معلمات مفقودة أو غير صحيحة (مثل: نوع ملف غير مدعوم). |
| 401  | غير مصادق عليه (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large)           | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |

## كيفية استخدام PutConvertWorkBook API مع واجهات برمجة التطبيقات SDK

### مواصفات PutConvertWorkBook API

تُحدّد [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) واجهة قابلة للوصول بشكل عام تتيح التفاعل المباشر مع REST من متصفح ويب.

### مثال باستخدام cURL

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### استخدام واجهات برمجة التطبيقات SDK لـ Aspose.Cells Cloud

استخدام واجهات SDK يُسرّع عملية التطوير من خلال التعامل مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على المنطق التجاري. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بواجهات Aspose.Cells Cloud SDK.

تُظهر الأمثلة التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}