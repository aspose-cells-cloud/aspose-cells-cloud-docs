---
title: Aspose.Cells Cloud Web API - تصدير بيانات نطاق جدول بيانات كملف تنسيق
second_title: Documen
ArticleTitle: Export a Spreadsheet Range data as a Format file
linktitle: تصدير النطاق كصيغة
type: docs
url: /ar/export-range-as-format/
keywords: Aspose.Cells Cloud Web API, Export range, Spreadsheet conversion, REST API, PDF, CSV, JSON, Markdown, Excel workshee
description: تحويل نطاق محدد من جدول بيانات في التخزين السحابي إلى تنسيقات مختلفة مثل PDF أو CSV أو تنسيقات الصور دون تنزيل الملف
weight: 100
kwords: تحويل جداول البيانات، REST API، PDF، CSV، JSON، Markdown، ورقة عمل Excel
---
تصدير جدول بيانات سحابي/نطاق Excel إلى ملف بتنسيق. يمكن حفظ ملف التنسيق في السحابة أو تصديره إلى وحدة التخزين المحلية.

## **تصدير النطاق بالتنسيق API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|اسم|خيط|طريق|(مطلوب) اسم ملف المصنف الذي سيتم استرجاعه.|
|ورقة عمل|خيط|طريق|اسم ورقة العمل Spreadsheet/Excel|
|يتراوح|خيط|طريق|النطاق الذي سيتم تحويله (على سبيل المثال، A1:C12).|
|شكل|خيط|استفسار|(مطلوب) تنسيق الإخراج المطلوب (على سبيل المثال، "png"، "pdf"، "svg").|
|مجلد|خيط|استفسار|(اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.|
|اسم التخزين|خيط|استفسار|(اختياري) اسم وحدة التخزين في حال استخدام تخزين سحابي مخصص. يُضبط افتراضيًا على وحدة التخزين الافتراضية في حال حذفه.|
|المسار الخارجي|خيط|استفسار|(اختياري) مسار المجلد لملف الإخراج. افتراضيًا، القيمة فارغة.|
|اسم التخزين الخارجي|خيط|استفسار|اسم تخزين ملف الإخراج.|
|الخطوطالموقع|خيط|استفسار|موقع الخطوط المخصصة.|
|منطقة|خيط|استفسار|إعداد المنطقة في جدول البيانات.|
|كلمة المرور|خيط|استفسار|كلمة المرور المطلوبة لفتح ملف جدول البيانات.|

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

## لماذا يجب عليك استخدام نطاق جدول البيانات المصدر بالتنسيق API؟

- يمكنك تحويل ملفات السحابة إلى تنسيقات مختلفة في أي وقت وفي أي مكان.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام نطاق جدول بيانات التصدير بالتنسيق API مع مجموعات تطوير البرامج (SDKs)؟

### تصدير النطاق كمواصفات تنسيق API

 ال[تصدير النطاق كمواصفات تنسيق API](https://reference.aspose.cloud/cells/#/ConversionController/ExportRangeAsFormat) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بتصدير بيانات نطاق جدول بيانات إلى ملف تنسيق باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

تُظهر أمثلة التعليمات البرمجية التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
