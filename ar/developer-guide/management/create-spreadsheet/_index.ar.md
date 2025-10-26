---
title: Aspose.Cells Cloud Web API - إنشاء جدول بيانات جديد باستخدام قالب جدول بيانات
second_title: Documen
ArticleTitle: Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc
linktitle: إنشاء جدول بيانات
type: docs
url: /ar/create-spreadsheet/
keywords: Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancemen
description: يتيح Excel API للمستخدمين إنشاء جدول بيانات جديد باسم محدد، ودعم قوالب اختيارية للمحتوى أو التنسيق المحدد مسبقًا، مما يعزز إنتاجية المستخدم
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، مطابقة جميع الخلايا الفارغة في ورقة عمل Excel، إنشاء جدول بيانات، دعم القالب، تحسين الإنتاجية
---
قم بإنشاء جدول بيانات جديد، والذي يمكن أن يكون جدول بيانات فارغًا أو جدول بيانات قابل للاستخدام تم إنشاؤه استنادًا إلى القالب المحدد.

## **إنشاء جدول بيانات API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|---------- ||----------------------- |----- |
|شكل| خيط| استفسار| يُحدِّد اسم جدول البيانات الجديد. سيُستخدَم هذا الاسم لتحديد جدول البيانات في النظام.|
| نموذج| خيط| استفسار| اختياري. في حال توفره، سيتم إنشاء جدول البيانات الجديد بناءً على القالب المحدد. قد يكون هذا مفيدًا لتطبيق التخطيطات والأنماط المحددة مسبقًا.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.|
| اسم التخزين الخارجي| خيط| استفسار| اسم تخزين ملف الإخراج.|
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

## أين يجب علينا استخدام Create Spreadsheet API؟

عندما تحتاج إلى إنشاء جدول بيانات جديد، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام Create Spreadsheet API؟

- لا يمكنك فقط إنشاء جدول بيانات فارغ، بل يمكنك أيضًا إنشاء جدول بيانات محدد استنادًا إلى قالب.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام إنشاء جدول بيانات API مع مجموعات تطوير البرامج (SDKs)

### إنشاء جدول بيانات API المواصفات

 ال[إنشاء جدول بيانات API المواصفات](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويمكّن تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك ببناء جدول بيانات باستخدام كود قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
