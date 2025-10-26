---
title: Aspose.Cells Cloud Webb API - إضافة ورقة عمل إلى جدول بيانات
second_title: Documen
ArticleTitle: Add a Worksheet to a Spreadshee
linktitle: إضافة ورقة عمل إلى جدول بيانات
type: docs
url: /ar/add-worksheet-to-spreadsheet/
keywords: Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, RES
description: يتيح الإصدار Aspose.Cells من Cloud Web للمطورين إضافة ورقة عمل جديدة إلى مصنف بكفاءة، مما يوفر لهم التحكم في نوع ورقة العمل وموقعها واسمها. تُحسّن هذه الوظيفة إدارة المصنفات ومرونتها.
weight: 100
kwords: Excel، Office السحابة، REST، جدول بيانات، PDF، CSV، JSON، Markdown، إدارة Excel أوراق العمل، إنشاء جدول بيانات ديناميكي
---
إضافة ورقة عمل إلى جدول البيانات، وتحديد نوع وموقع ورقة العمل.

|**نوع ورقة العمل** | وصف|
|:- |:- |
|**في بي** | وحدة Visual Basic|
|**ورقة عمل** | ورقة عمل|
|**جدول** | ورقة الرسم البياني|
|**بيف4ماكرو** | ورقة ماكرو BIFF4|
|**الماكرو الدولي** | ورقة الماكرو الدولية|
|**آخر** | ورقة الماكرو الدولية|
|**الحوار** | ورقة عمل الحوار|

## **إضافة ورقة عمل إلى جدول بيانات API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|جدول بيانات|ملف|بيانات النموذج|تحميل ملف جدول البيانات.|
|نوع الورقة|خيط|استفسار|يُحدد اسم ورقة العمل الجديدة. في حال عدم تحديده، سيتم تعيين اسم افتراضي.|
|موضع|عدد صحيح|استفسار|يُحدد موضع إدراج ورقة العمل الجديدة. في حال عدم تحديده، ستُضاف ورقة العمل إلى نهاية المصنف.|
|اسم الورقة|خيط|استفسار|يُحدد نوع ورقة العمل المراد إضافتها. في حال عدم تحديده، سيتم استخدام نوع ورقة العمل الافتراضي.|
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

## أين يجب علينا استخدام إضافة ورقة العمل إلى جدول البيانات API؟

عندما تحتاج إلى إضافة ورقة عمل إلى جدول بيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام إضافة ورقة العمل إلى جدول البيانات API؟

- أضف ورقة عمل إلى جدول البيانات، مع تحديد نوع وموقع ورقة العمل.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام إضافة ورقة عمل إلى جدول بيانات API مع مجموعات تطوير البرامج (SDKs)

### إضافة ورقة عمل إلى جدول بيانات API المواصفات

 ال[إضافة ورقة عمل إلى جدول بيانات API المواصفات](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بإضافة ورقة عمل إلى جدول بيانات باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات API إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
