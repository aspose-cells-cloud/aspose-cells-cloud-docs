---
title: Aspose.Cells Cloud WEb API - تقسيم جدول البيانات إلى ملفات منفصلة
second_title: Documen
ArticleTitle: Split the Spreadsheet into separate files
linktitle: تقسيم جدول البيانات
type: docs
url: /ar/split-spreadsheet/
keywords: Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdow
description: تقسيم جدول بيانات محلي إلى ملفات متعددة بتنسيقات مختلفة دون الحاجة إلى تخزين سحابي
weight: 100
kwords: Excel API، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، تقسيم جدول بيانات محلي، معالجة سحابية، إدارة الملفات، معالجة الأخطاء
---
قم بتقسيم جدول البيانات المحلي إلى ملفات منفصلة باستخدام 30 تنسيق ملف إخراج دون الحاجة إلى تخزين سحابي.

## **جدول بيانات مقسم API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| جدول بيانات| ملف| بيانات النموذج| قم بتحميل ملف جدول البيانات الذي تريد تقسيمه.|
| من| عدد صحيح| استفسار| حدد فهرس ورقة العمل الأولية.|
| ل| عدد صحيح| استفسار| حدد فهرس ورقة العمل النهائية.|
| تنسيق خارجي| خيط| استفسار| تحديد تنسيق ملف الإخراج.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد لتخزين مصنف الإخراج. القيمة الافتراضية هي null.|
|اسم التخزين الخارجي| خيط| استفسار| قم بتحديد اسم تخزين ملف الإخراج.|
| الخطوطالموقع| خيط| استفسار| حدد الخطوط المخصصة إذا لزم الأمر.|
| العودة| خيط| استفسار| تعيين منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| قم بتوفير كلمة المرور للوصول إلى ملف جدول البيانات.|

## **إجابة**

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

## أين يجب علينا استخدام جدول البيانات المنقسم API؟

عندما تحتاج إلى تقسيم جدول بيانات إلى المزيد من الملفات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام جدول البيانات المنقسم API؟

- لا حاجة لمساحة تخزين سحابية، فقط قم بتقسيمها مباشرة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام جدول البيانات المنقسم API مع مجموعات تطوير البرامج (SDKs)

### مواصفات جدول البيانات المنقسم API

 ال[مواصفات جدول البيانات المنقسم API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام لإجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، لأنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بتقسيم جدول البيانات إلى ملفات منفصلة باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مجموعات SDK مختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
