---
title: Aspose.Cells Cloud Web API - تصدير جدول بيانات كملف تنسيق
second_title: Documen
ArticleTitle: Export a Spreadsheet as a Format fil
linktitle: تصدير جدول بيانات كنموذج
type: docs
url: /ar/export-spreadsheet-as-format/
keywords: Export spreadsheet, Aspose.Cells Cloud Web API, Convert spreadsheet, Spreadsheet formats, XLSX, PDF, CSV, JSON, Markdow
description: يحول بكفاءة جداول البيانات المخزنة في التخزين السحابي إلى تنسيقات مختلفة مثل XLSX وPDF وCSV
weight: 100
kwords: Excel، Office السحابة، REST، تحويل جداول البيانات، PDF، CSV، JSON، Markdow
---
تصدير جدول بيانات سحابي/Excel إلى ملف بتنسيق آخر.

## **تصدير جدول البيانات بالتنسيق API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| (مطلوب) اسم ملف المصنف الذي سيتم استرجاعه.|
| شكل| خيط| استفسار| (مطلوب) تنسيق الإخراج المطلوب (على سبيل المثال، "Xlsx"، "Pdf"، "Csv").|
| مجلد| خيط| استفسار| (اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.|
| اسم التخزين| خيط| استفسار|(اختياري) اسم وحدة التخزين إذا كنت تستخدم تخزينًا سحابيًا مخصصًا. استخدم وحدة التخزين الافتراضية إذا تم حذفها.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد الذي سيتم تخزين المصنف فيه. الافتراضي هو null.|
|اسم التخزين الخارجي| خيط| استفسار| اسم تخزين ملف الإخراج.|
| الخطوطالموقع| خيط| استفسار| استخدم الخطوط المخصصة.|
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

## لماذا يجب عليك استخدام جدول بيانات التصدير بالتنسيق API؟

- يمكنك تحويل ملفات السحابة إلى تنسيقات مختلفة في أي وقت وفي أي مكان.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام جدول بيانات التصدير بالتنسيق API مع مجموعات تطوير البرامج (SDKs)؟

### تصدير جدول بيانات بالتنسيق API المواصفات

 ال[تصدير جدول بيانات بالتنسيق API المواصفات](https://reference.aspose.cloud/cells/#/ConversionController/ExportSpreadsheetAsFormat) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام لأداء تفاعلات REST بسلاسة.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بتصدير جدول بيانات إلى ملف تنسيق باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells ومجموعات SDK المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
