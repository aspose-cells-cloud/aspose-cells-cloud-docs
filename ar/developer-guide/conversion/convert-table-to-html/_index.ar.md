---
title: Aspose.Cells Cloud Web API - تحويل بيانات جدول بيانات إلى ملف HTML
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Html fil
linktitle: تحويل الجدول إلى HTM
type: docs
url: /ar/convert-table-to-html/
keywords: Excel Table to HTML, Spreadsheet Conversion, Aspose.Cells Cloud Web API, REST, Convert Excel to HTML, Table to HTML, Document Conversion, Cloud Service
description: يمكنك بسهولة تحويل الجداول من ملفات جداول البيانات المحلية إلى تنسيق HTML باستخدام نظامنا السحابي API
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، HTML، PDF، CSV، JSON، Markdown، مطابقة الخلايا الفارغة في Excel
---
تحويل جدول بيانات محلي/Excel إلى ملف HTML.

## **تحويل الجدول إلى HTML API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| جدول بيانات| ملف| بيانات النموذج| قم بتحميل ملف جدول البيانات المراد تحويله.|
| ورقة عمل| خيط| استفسار| اسم ورقة العمل Spreadsheet/Excel|
| اسم الجدول| خيط| استفسار| اسم الجدول المراد تحويله.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد الذي سيتم تخزين الملف المُحوَّل فيه. القيمة الافتراضية هي null.|
|اسم التخزين الخارجي| خيط| استفسار| اسم التخزين المخصص لملف الإخراج.|
| الخطوطالموقع| خيط| استفسار| حدد الخطوط المخصصة للتحويل.|
| منطقة| خيط| استفسار| تحديد إعدادات منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| كلمة المرور المطلوبة للوصول إلى ملف جدول البيانات.|

### **إجابة**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### رموز الخطأ

- **400 طلب سيء**:عنوان URI الخاص بـ Apose.Cells Cloud API غير صالح.
- **401 غير مصرح به**رمز وصول غير صالح. أو معرف عميل وسر غير صالحين.
- **404 غير موجود**:ملف جدول البيانات غير قابل للوصول.
- **خطأ الخادم 500**:واجهت جدول البيانات خللاً في الحصول على بيانات الحساب.

## لماذا يجب عليك استخدام تحويل الجدول إلى HTML API؟

- لا حاجة للتخزين السحابي، مما يقلل العبء على موارد السحابة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام تحويل الجدول إلى HTML API مع SDKs؟

### تحويل الجدول إلى مواصفات HTML API

 ال[تحويل الجدول إلى مواصفات HTML API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToHtml) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب الخاص بك.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بتحويل بيانات جدول بيانات إلى ملف HTML باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}
