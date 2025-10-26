---
title: Aspose.Cells Cloud Web API - نقل ورقة عمل إلى موضع جديد في جدول البيانات
second_title: Documen
ArticleTitle: Move worksheet to new position in Spreadshee
linktitle: نقل ورقة العمل في جدول البيانات
type: docs
url: /ar/move-worksheet-in-spreadsheet/
keywords: Move Worksheet, Aspose.Cells Cloud Web API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Excel AP
description: يتيح MoveWorksheet API للمستخدمين إعادة وضع ورقة عمل محددة بكفاءة داخل مصنف، وبالتالي تحسين تنظيم بيانات جدول البيانات وإمكانية الوصول إليها
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، نقل ورقة العمل، تنظيم المصنف، PDF، CSV، JSON، Markdown
---
نقل ورقة العمل إلى موضع جديد في جدول البيانات.

## **نقل ورقة العمل من جدول البيانات API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|جدول بيانات|ملف|بيانات النموذج|تحميل ملف جدول البيانات.|
|ورقة عمل|خيط|استفسار|الاسم الحالي للورقة التي سيتم نقلها.|
|موضع|عدد صحيح|استفسار|الموضع الجديد لورقة العمل.|
|المسار الخارجي|خيط|استفسار|(اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.|
|اسم التخزين الخارجي|خيط|استفسار|اسم تخزين ملف الإخراج.|
|منطقة|خيط|استفسار|إعداد منطقة جدول البيانات.|
|كلمة المرور|خيط|استفسار|كلمة المرور لفتح ملف جدول البيانات.|

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

## أين يجب علينا استخدام ورقة العمل المتحركة في جدول البيانات API؟

عندما تحتاج إلى نقل ورقة عمل إلى موضع جديد في جداول البيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام ورقة العمل المتحركة في جدول البيانات API؟

- نقل أوراق العمل بسرعة من جداول البيانات.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام ورقة عمل النقل في جدول البيانات API مع مجموعات تطوير البرامج (SDKs)

### نقل ورقة العمل في جدول بيانات API المواصفات

 ال[نقل ورقة العمل في جدول بيانات API المواصفات](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام لتسهيل تفاعلات REST المباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بنقل ورقة العمل في جدول البيانات باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
تُظهر أمثلة التعليمات البرمجية التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
