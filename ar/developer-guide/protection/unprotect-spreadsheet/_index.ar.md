---
title: Aspose.Cells Cloud Web API - إلغاء حماية جدول البيانات باستخدام كلمة المرور
second_title: Documen
ArticleTitle: Unprotect the Spreadsheet with passwor
linktitle: إلغاء حماية جدول البيانات
type: docs
url: /ar/unprotect-spreadsheet/
keywords: Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Managemen
description: يزيل بكفاءة حماية كلمة المرور ثنائية الطبقة من جداول البيانات Excel، ويدعم كلمات المرور المفتوحة والمعدلة باستخدام تقنيات التشفير المتقدمة
weight: 100
kwords: Excel، Office Cloud، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، مطابقة جميع الخلايا الفارغة في ورقة عمل Excel
---
ينطبق على جداول البيانات غير المحمية Excel بكلمة مرور، ويدعم كلمات المرور المفتوحة والتعديلية.

## **إلغاء حماية جدول البيانات API**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|جدول بيانات|ملف|بيانات النموذج|قم بتحميل ملف جدول البيانات الذي تريد إلغاء حمايته.|
|كلمة المرور|خيط|استفسار|كلمة مرور التشفير لملف جدول البيانات.|
|تعديل كلمة المرور|خيط|استفسار|كلمة المرور المطلوبة لتعديل الملف المحمي.|
|المسار الخارجي|خيط|استفسار|(اختياري) مسار المجلد الذي سيتم تخزين المصنف غير المحمي فيه. القيمة الافتراضية هي null.|
|اسم التخزين الخارجي|خيط|استفسار|يحدد اسم تخزين ملف الإخراج.|
|منطقة|خيط|استفسار|يحدد إعدادات منطقة جدول البيانات.|

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

## أين يجب علينا استخدام حذف الأعمدة الفارغة في جدول البيانات API؟

عندما تحتاج إلى تحويل البيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام حذف الأعمدة الفارغة في جدول البيانات API؟

- قم بحذف جميع الأعمدة الفارغة التي لا تحتوي على أي بيانات أو كائنات أخرى من جدول البيانات Excel بسرعة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام حذف الأعمدة الفارغة في جدول البيانات API مع مجموعات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يسمح لك ببساطة بحذف الأعمدة الفارغة في جداول البيانات من الخلايا باستخدام الحد الأدنى من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
