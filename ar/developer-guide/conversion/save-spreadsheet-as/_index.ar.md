---
title: Aspose.Cells Cloud Web API - حفظ جدول البيانات كملف تنسيق
second_title: Documen
ArticleTitle: Save Spreadsheet as a Format fil
linktitle: حفظ جدول البيانات أ
type: docs
url: /ar/save-spreadsheet-as/
keywords: spreadsheet conversion, Save as, Excel to PDF, Excel to CSV, RES
description: قم بتحويل جداول البيانات المخزنة في السحابة إلى تنسيقات مختلفة بسهولة، بما في ذلك XLSX وPDF وCSV، باستخدام برنامجنا القوي API
weight: 100
kwords: Excel API، Office السحابة، REST، جدول بيانات، PDF، CSV، JSON، Markdown، تحويل Excel الملفات، حفظ جدول بيانات باسم، Aspose.Cells Cloud Web AP
---
احفظ جدول بيانات سحابي/ملف Excel كملف تنسيق للتخزين السحابي.

## **حفظ جدول البيانات باسم API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| (مطلوب) اسم ملف المصنف المراد تحويله.|
| شكل| خيط| استفسار| (مطلوب) تنسيق الإخراج المطلوب (على سبيل المثال، "Xlsx"، "Pdf"، "Csv").|
| حفظ خيارات البيانات| فصل| جسم| (اختياري) حفظ بيانات الخيارات. القيمة الافتراضية هي null.|
| مجلد| خيط| استفسار| (اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.|
| اسم التخزين| خيط| استفسار|(اختياري) اسم وحدة التخزين إذا كنت تستخدم تخزينًا سحابيًا مخصصًا. استخدم وحدة التخزين الافتراضية إذا تم حذفها.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.|
|اسم التخزين الخارجي| خيط| استفسار| اسم تخزين ملف الإخراج.|
| الخطوطالموقع| خيط| استفسار| استخدم الخطوط المخصصة.|
| منطقة| خيط| استفسار| إعداد منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| كلمة المرور لفتح ملف جدول البيانات.|

### **إجابة**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### رموز الخطأ

- **400 طلب سيء**:عنوان URI الخاص بـ Apose.Cells Cloud API غير صالح.
- **401 غير مصرح به**رمز وصول غير صالح. أو معرف عميل وسر غير صالحين.
- **404 غير موجود**:ملف جدول البيانات غير قابل للوصول.
- **خطأ الخادم 500**:واجهت جدول البيانات خللاً في الحصول على بيانات الحساب.

## لماذا يجب عليك استخدام Save Spread API؟

- يمكنك تحويل ملفات السحابة إلى تنسيقات مختلفة في أي وقت وفي أي مكان.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام تحويل الجدول إلى Json API مع SDKs؟

### حفظ جدول البيانات كمواصفات API

 ال[حفظ جدول البيانات كمواصفات API](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بحفظ جدول بيانات كملف تنسيق مع رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{< /tab >}}
{{< /tabs >}}
