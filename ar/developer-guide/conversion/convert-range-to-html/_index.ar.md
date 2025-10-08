---
title: Aspose.Cells Cloud Web API - تحويل نطاق جدول البيانات إلى HTM
second_title: Documen
ArticleTitle: Converting Spreadsheet Range to Htm
linktitle: تحويل النطاق إلى HTM
type: docs
url: /ar/convert-range-to-html/
keywords: Convert a spreadsheet range data to a html file, Spreadsheet Conversion, Excel Conversio
description: تحويل نطاق من جدول بيانات محلي/ملف Excel إلى ملف html باستخدام Aspose.Cells Cloud Web API
weight: 100
kwords: تحويل النطاق إلى HTML أو جدول بيانات أو Excel
---
تحويل نطاق البيانات من جدول بيانات محلي/ملف Excel إلى ملف html.

## **تحويل النطاق إلى HTML API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/html
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|------------|--|------------------------|-------------------------------------------------|
| جدول بيانات|ملف| بيانات النموذج| تحميل ملف جدول البيانات.|
| ورقة عمل| خيط| استفسار| اسم ورقة العمل داخل جدول البيانات.|
| يتراوح| خيط| استفسار| منطقة الخلية التي سيتم تحويلها، على سبيل المثال، A1:C10.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. الافتراضي هو null.|
| اسم التخزين الخارجي| خيط| استفسار| اسم تخزين ملف الإخراج.|
| الخطوطالموقع| خيط| استفسار| حدد الخطوط المخصصة للاستخدام.|
| منطقة| خيط| استفسار| إعداد منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| كلمة المرور لفتح ملف جدول البيانات.|

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

## لماذا يجب عليك استخدام تحويل النطاق إلى HTML API؟

- لا حاجة للتخزين السحابي، مما يقلل العبء على موارد السحابة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام تحويل النطاق إلى HTML API مع SDKs؟

### تحويل النطاق إلى مواصفات HTML API

 ال[تحويل النطاق إلى مواصفات HTML API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToHtml) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بتحويل بيانات النطاق إلى ملف html باستخدام رمز قصير.
 يرجى زيارة[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة شاملة لـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}
