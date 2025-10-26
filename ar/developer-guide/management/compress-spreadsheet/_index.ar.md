---
title: Aspose.Cells Cloud Web API - ضغط حجم جدول البيانات
second_title: Documen
ArticleTitle: Compress the size of the Spreadshee
linktitle: ضغط جدول البيانات
type: docs
url: /ar/compress-spreadsheet/
keywords: Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web AP
description: يتيح Compress Spreadsheet API للمستخدمين تقليل حجم ملفات جداول البيانات بكفاءة من خلال تطبيق مستويات ضغط محددة وتحسين التخزين وتعزيز الأداء
weight: 100
kwords: Excel، Office السحابة، REST، ضغط جداول البيانات، تحسين حجم الملفات، PDF، CSV، Json، Markdow
---
ضغط حجم جدول البيانات.

## **ضغط جدول البيانات API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|جدول بيانات|ملف|بيانات النموذج|قم بتحميل ملف جدول البيانات المراد ضغطه.|
|مستوى|عدد صحيح|استفسار|يقوم بتحديد مستوى الضغط الذي سيتم تطبيقه، ويتراوح من 0 (بدون ضغط) إلى 9 (الحد الأقصى للضغط).|
|المسار الخارجي|خيط|استفسار|(اختياري) مسار المجلد الذي سيتم تخزين المصنف المضغوط فيه. الافتراضي هو null.|
|اسم التخزين الخارجي|خيط|استفسار|اسم تخزين ملف الإخراج.|
|منطقة|خيط|استفسار|إعداد منطقة جدول البيانات.|
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

## أين يجب علينا استخدام جدول البيانات المضغوط API؟

عندما تحتاج إلى تقليل حجم جداول البيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام Compress Spreadsheet API؟

- حجم جدول البيانات كبير جدًا ويجب تقليل حجم الملف.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام Compress Spreadsheet API مع SDKs

### مواصفات ضغط جدول البيانات API

 ال[مواصفات ضغط جدول البيانات API](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) يوفر واجهة يمكن الوصول إليها بشكل عام لتفاعلات REST، مما يسمح بإجراء مكالمات مباشرة API من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتلخيص التفاصيل منخفضة المستوى، مما يسمح لك بضغط حجم جدول البيانات باستخدام الكود القصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

تُظهر أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
