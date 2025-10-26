---
title: Aspose.Cells Cloud Web API - استبدال محتوى جدول البيانات
second_title: Documen
ArticleTitle: Replace Spreadsheet Conten
linktitle: استبدال محتوى جدول البيانات
type: docs
url: /ar/replace-spreadsheet-content/
keywords: Excel API, Spreadsheet manipulation, Replace text, Office Cloud integration, REST AP
description: استبدال النص بكفاءة في ملفات جدول البيانات المحلية باستخدام Aspose.Cells API
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، استبدال النص في Excel، مطابقة الخلايا الفارغة في ورقة العمل Excel
---
استبدال النص المحدد بكفاءة داخل ملفات جدول البيانات المحلية.

## **استبدال محتوى جدول البيانات API**

```
PUT http://api.aspose.cloud/v4.0/cells/replace/content
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| جدول بيانات| ملف| بيانات النموذج| تحميل ملف جدول البيانات.|
| نص البحث| خيط| استفسار|النص الذي تريد البحث عنه.|
| استبدال النص| خيط| استفسار| النص الذي سيتم استبداله به.|
| ورقة عمل| خيط| استفسار| حدد ورقة العمل للاستبدال.|
| منطقة الخلية| خيط| استفسار| حدد منطقة الخلية للاستبدال.|
| منطقة| خيط| استفسار| إعداد منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| كلمة المرور لفتح ملف جدول البيانات.|

### **إجابة**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### رموز الخطأ

- **400 طلب سيء**:عنوان URI الخاص بـ Apose.Cells Cloud API غير صالح.
- **401 غير مصرح به**رمز وصول غير صالح. أو معرف عميل وسر غير صالحين.
- **404 غير موجود**:ملف جدول البيانات غير قابل للوصول.
- **خطأ الخادم 500**:واجهت جدول البيانات خللاً في الحصول على بيانات الحساب.

## أين يجب علينا استخدام محتوى الاستبدال في جدول البيانات API؟

عندما تحتاج إلى استبدال المحتوى في جدول البيانات بكلمة مرور، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام استبدال المحتوى في جدول البيانات API؟

- استبدال المحتوى في جداول البيانات بسرعة باستخدام كلمة المرور.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام استبدال المحتوى في جدول البيانات API باستخدام مجموعات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceSpreadsheetContent) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام مجموعة أدوات تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يسمح لك بتطبيق استبدال المحتوى في جداول البيانات للخلايا بسهولة وبأقل قدر من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

تُظهر أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
