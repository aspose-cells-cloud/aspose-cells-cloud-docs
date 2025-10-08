---
title: Aspose.Cells Cloud Web API - دمج جداول بيانات متعددة في جدول بيانات واحد
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: دمج جدول البيانات
type: docs
url: /ar/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: دمج ملفات جدول البيانات المحلية بسهولة في تنسيقات مختلفة (XLSX، CSV، PDF) باستخدام Excel API
weight: 100
kwords: Excel API، دمج جداول البيانات، Office السحابة، REST API، دمج جداول البيانات، تنسيق CSV، JSON، Markdow
---
دمج ملفات جدول بيانات محلية متعددة في ملف واحد، مع دعم الإخراج بأكثر من 30 تنسيق ملف.

## **دمج جدول البيانات API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| جدول بيانات| ملف| بيانات النموذج| تحميل ملف جدول البيانات.|
| تنسيق خارجي| خيط| استفسار| حدد تنسيق ملف الإخراج.|
| دمج في ورقة واحدة| منطقي| استفسار| أشر إلى ما إذا كان سيتم دمج كافة البيانات في ورقة عمل واحدة.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد لمصنف العمل الناتج. افتراضيًا، القيمة فارغة.|
|اسم التخزين الخارجي| خيط| استفسار| حدد اسم تخزين ملف الإخراج.|
| الخطوطالموقع| خيط| استفسار| تحديد الخطوط المخصصة التي سيتم استخدامها.|
| منطقة| خيط| استفسار| تعيين منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| قم بتوفير كلمة المرور لفتح ملف جدول البيانات.|

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

## أين يجب علينا استخدام جدول البيانات المحلي الدمج API؟

عندما تحتاج إلى دمج ملفات بيانات متعددة معًا، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام Merge Local Spreadsheet API؟

- لا حاجة لمساحة تخزين سحابية، فقط قم بالدمج مباشرةً.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام دمج جدول البيانات المحلي API مع مجموعات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)يوفر واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح للمستخدمين بإجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بدمج جداول بيانات متعددة في جدول بيانات واحد باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}
