---
title: Aspose.Cells Cloud Web API - تحويل جدول بيانات إلى Pd
second_title: Documen
ArticleTitle: Convert Spreadsheet Worksheet to Pd
linktitle: تحويل ورقة العمل إلى Pd
type: docs
url: /ar/convert-worksheet-to-pdf/
keywords: worksheet to pdf, Excel PDF conversion, REST API, cloud-based conversion, spreadsheet to PD
description: تحويل ورقة عمل من جدول بيانات على محرك الأقراص المحلي الخاص بك إلى ملف PDF باستخدام برنامجنا السحابي API
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، تحويل ورقة العمل إلى PDF، تحويل السحابة، تحويل الملف المحلي
---
تحويل جدول بيانات محلي/ورقة عمل Excel إلى ملف pdf باستخدام Aspose.Cells Cloud Web API.

## **تحويل ورقة العمل إلى PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|-----------------|-|-----------------------|------------------------------------|
| جدول بيانات| ملف| بيانات النموذج| تحميل ملف جدول البيانات.|
| ورقة عمل|خيط| استفسار|اسم ورقة العمل الموجودة في جدول البيانات.|
| المسار الخارجي|خيط| استفسار|(اختياري) مسار المجلد لتخزين المصنف؛ الافتراضي هو null.|
| اسم التخزين الخارجي|خيط| استفسار| اسم تخزين ملف الإخراج.|
| الخطوطالموقع|خيط| استفسار| تحديد الخطوط المخصصة.|
| منطقة|خيط| استفسار| قم بتحديد إعدادات منطقة جدول البيانات.|
|كلمة المرور|خيط| استفسار|كلمة المرور المطلوبة لفتح ملف جدول البيانات.|

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

## لماذا يجب عليك استخدام Convert Table to Pdf API؟

- لا حاجة للتخزين السحابي، مما يقلل العبء على موارد السحابة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام تحويل الجدول إلى PDF API مع SDKs؟

### تحويل الجدول إلى PDF API المواصفات

 ال[تحويل الجدول إلى PDF API المواصفات](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToPdf) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام ويمكّن من التفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بتحويل بيانات جدول بيانات إلى ملف pdf باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
