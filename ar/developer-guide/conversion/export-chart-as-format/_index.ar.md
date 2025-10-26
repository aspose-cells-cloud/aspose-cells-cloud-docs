---
title: Aspose.Cells Cloud Web API - تصدير مخطط جدول بيانات كملف تنسيق
second_title: Documen
ArticleTitle: Export a Spreadsheet Chart as a Format fil
linktitle: تصدير الرسم البياني كنموذج
type: docs
url: /ar/export-chart-as-format/
keywords: Export Chart, Aspose.Cells Cloud Web API, Spreadsheet Conversion, PDF Export, Image Export, REST, Excel, CSV, JSO
description: يحول بكفاءة المخططات من جداول البيانات المخزنة في السحابة إلى تنسيقات محددة مثل PDF أو الصورة مباشرة دون تنزيلها
weight: 100
kwords: تصدير المخططات، REST، تحويل جداول البيانات، PDF، CSV، JSON، Markdown، Excel، تنسيق الصورة
---
تصدير جدول بيانات سحابي/مخطط Excel إلى ملف بتنسيق آخر باستخدام Aspose.Cells Cloud Web API.

## **تصدير الرسم البياني بالتنسيق API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| (مطلوب) اسم ملف المصنف الذي سيتم استرجاعه.|
| ورقة عمل| خيط| طريق| اسم ورقة العمل|
| مؤشر الرسم البياني| عدد صحيح| طريق| مؤشر الرسم البياني|
| شكل| خيط| استفسار| (مطلوب) تنسيق الإخراج المطلوب (على سبيل المثال، "png"، "pdf"، "svg").|
| مجلد| خيط| استفسار| (اختياري) مسار المجلد الذي يتم تخزين المصنف فيه؛ الافتراضي هو null.|
| اسم التخزين| خيط| استفسار|(اختياري) اسم التخزين إذا كنت تستخدم تخزينًا سحابيًا مخصصًا؛ استخدم التخزين الافتراضي إذا تم حذفه.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد الذي يتم تخزين المصنف فيه؛ الافتراضي هو null.|
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

## لماذا يجب عليك استخدام مخطط جدول البيانات للتصدير بالتنسيق API؟

- يمكنك تحويل ملفات السحابة إلى تنسيقات مختلفة في أي وقت وفي أي مكان.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام مخطط جدول بيانات التصدير بالتنسيق API مع مجموعات تطوير البرامج (SDKs)؟

### تصدير الرسم البياني بالتنسيق API المواصفات

 ال[تصدير الرسم البياني بالتنسيق API المواصفات](https://reference.aspose.cloud/cells/#/ConversionController/ExportChartAsFormat) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بتصدير بيانات مخطط جدول بيانات إلى ملف تنسيق باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportChartAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportChartAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportChartAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportChartAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportChartAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportChartAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportChartAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportChartAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
