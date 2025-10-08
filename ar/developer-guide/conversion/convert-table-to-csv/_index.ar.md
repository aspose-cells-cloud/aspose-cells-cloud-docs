---
title: Aspose.Cells Cloud Web API - تحويل بيانات جدول بيانات إلى ملف Csv
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Csv file
linktitle: تحويل الجدول إلى CS
type: docs
url: /ar/convert-table-to-csv/
keywords: convert table to csv, convert spreadsheet to csv, Excel to CSV conversion, cloud conversio
description: يحول جدول بكفاءة من جدول بيانات على محرك الأقراص المحلي الخاص بك إلى ملف CSV باستخدام API
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، جدول إلى CSV، تحويل محلي إلى سحابي
---
تحويل جدول بيانات محلي/Excel إلى ملف csv.

## **تحويل الجدول إلى CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|-------------|-|------------------------|-------------------------------------------|
| جدول بيانات| ملف| بيانات النموذج| تحميل ملف جدول البيانات.|
| ورقة عمل|خيط| استفسار| اسم ورقة العمل الموجودة في جدول البيانات.|
| اسم الجدول|خيط| استفسار|اسم الجدول المراد تحويله.|
| المسار الخارجي|خيط| استفسار| (اختياري) مسار المجلد الذي يتم تخزين المصنف فيه؛ الافتراضي هو null.|
| اسم التخزين الخارجي|خيط| استفسار| اسم تخزين ملف الإخراج.|
| الخطوطالموقع|خيط| استفسار| المسار لاستخدام الخطوط المخصصة.|
| منطقة|خيط| استفسار| يحدد إعداد منطقة جدول البيانات.|
| كلمة المرور|خيط| استفسار| كلمة المرور لفتح ملف جدول البيانات.|

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

## لماذا يجب عليك استخدام تحويل الجدول إلى CSV API؟

- لا حاجة للتخزين السحابي، مما يقلل العبء على موارد السحابة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام تحويل الجدول إلى CSV API مع SDKs؟

### تحويل الجدول إلى مواصفات CSV API

 ال[تحويل الجدول إلى مواصفات CSV API](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToCsv) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح بالتفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بتحويل بيانات جدول بيانات إلى ملف csv باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
