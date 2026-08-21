---
title: "تقسيم ملف Excel إلى ملفات متعددة"
second_title: "Document"
linktitle: "تقسيم ملفات Excel متعددة"
type: docs
url: /ar/split-an-excel-file-to-multi-files/
aliases: [  /ar/split-excel-workbooks/ , /ar/workbook/split/ ]
keywords: "Aspose.Cells, Cloud, Excel, Split, API, PDF, CSV, JSON"
description: "استخدم واجهة Aspose.Cells Cloud REST API لتقسيم ملفات عمل Excel ذات أوراق متعددة إلى ملفات منفصلة. تدعم تنسيقات الإخراج مثل PDF وCSV وJSON، وتتوافر عبر SDKs لـ Android وC# وGo وJava وNode.js وPerl وPHP وPython وRuby وSwift."
weight: 32
ArticleTitle: "تقسيم ملف Excel إلى ملفات متعددة - وثائق Aspose.Cells Cloud"
---

تقوم واجهة Aspose.Cells Cloud REST API بتقسيم ملفات عمل Excel ذات أوراق متعددة إلى ملفات منفصلة.

**المتطلبات الأساسية**  
قبل استدعاء الواجهة البرمجية، يجب عليك الحصول على رمز JWT صالح وتشمله في رأس `Authorization` لكل طلب. راجع [دليل المصادقة](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) للحصول على التفاصيل.

## واجهة PostSplit API

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات Aspose.Cells Cloud آمنة وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع  | الوصف                                                       |
|------------|---------|---------|--------------------------------------------------------------|
| file       | ملف    | formData | ملف عمل Excel المراد تحميله.                                 |
| format     | نص    | query    | تنسيق الإخراج المرغوب (مثل `pdf` أو `csv` أو `json`).        |
| password   | نص    | query    | كلمة المرور لملف العمل المشفر (اختياري).                     |
| from       | عدد صحيح | query    | فهرس الورقة الأولى التي سيتم تضمينها (العد يبدأ من 1).       |
| to         | عدد صحيح | query    | فهرس الورقة الأخيرة التي سيتم تضمينها (بما في ذلك).          |

### **الاستجابة**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[اسم الملف1]",
            "Filesize" : [حجم الملف],
            "FileContent" : "[Base64String]"
        },
        {
            "Filename" : "[اسم الملف2]",
            "Filesize" : [حجم الملف],
            "FileContent" : "[Base64String]"
        },
        {
            "Filename" : "[اسم الملف3]",
            "Filesize" : [حجم الملف],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**رموز حالات HTTP**

| الرمز | المعنى                         | الوصف                                                             |
|-------|---------------------------------|--------------------------------------------------------------------|
| 200   | OK (تمت العملية بنجاح)         | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.      |
| 400   | Bad Request (طلب غير صالح)     | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).            |
| 401   | Unauthorized (غير مخوّل)        | رمز JWT غير صالح أو مفقود.                                       |
| 413   | Payload Too Large (حمولة كبيرة جداً) | تجاوز الملف المرفوع الحد الأقصى للحجم.                          |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | حدث خطأ غير متوقع في جانب الخادم.                              |

## كيفية استخدام واجهة PostSplit API باستخدام SDKs

### مواصفات واجهة PostSplit API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

**رموز حالات HTTP**

| الرمز | المعنى                         | الوصف                                                             |
|-------|---------------------------------|--------------------------------------------------------------------|
| 200   | OK (تمت العملية بنجاح)         | تم تقسيم ملف العمل بنجاح وتحتوي الاستجابة على قائمة الملفات.    |
| 400   | Bad Request (طلب غير صالح)     | معاملات مفقودة أو غير صالحة (مثل تنسيق غير مدعوم).              |
| 401   | Unauthorized (غير مخوّل)        | رمز JWT غير صالح أو مفقود.                                       |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | حدث خطأ غير متوقع في جانب الخادم.                              |

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# استبدل xxxxx1.xlsx وxxxxx2.xlsx بمسارات ملفات Excel الخاصة بك
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64String--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK معالجة التفاصيل من المستوى المنخفض وتركز أنت على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}