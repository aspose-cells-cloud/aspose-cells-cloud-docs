---
title: Aspose.Cells Cloud Web API - استيراد بيانات Csv أو JSON أو XML إلى ملف جدول بيانات
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: استيراد البيانات إلى جدول بيانات
type: docs
url: /ar/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: استيراد البيانات بكفاءة إلى جدول بيانات من التنسيقات المدعومة مثل CSV وJSON وXML باستخدام Aspose.Cells Cloud Web API
weight: 100
kwords: Aspose.Cells Cloud Web API، استيراد البيانات، Office Cloud، REST، جدول بيانات، CSV، JSON، XM
---
 استيراد البيانات إلى جدول بيانات. التنسيق المدعوم لملف البيانات المستوردة هو[إكس إم إل](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) أو[ملف CSV](https://docs.fileformat.com/spreadsheet/csv/).

## **استيراد البيانات إلى جدول بيانات API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| ملف البيانات| ملف| بيانات النموذج| قم بتحميل ملف البيانات المراد استيراده.|
| جدول بيانات| ملف| بيانات النموذج| قم بتحميل ملف جدول البيانات المستهدف.|
| ورقة عمل| خيط| استفسار| حدد ورقة العمل لاستيراد البيانات.|
| خلية البداية| خيط| استفسار|حدد موضع البداية لاستيراد البيانات.|
| إدراج| منطقي| استفسار| يشير إلى ما إذا كان سيتم إدراج بيانات الاستيراد المحددة أو الكتابة فوقها.|
| تحويل البيانات الرقمية| منطقي| استفسار| حدد ما إذا كان سيتم تحويل البيانات الرقمية أثناء الاستيراد.|
| الفاصل| خيط| استفسار| حدد الفاصل لتنسيق CSV.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي null.|
|اسم التخزين الخارجي| خيط| استفسار| حدد اسم تخزين ملف الإخراج.|
| الخطوطالموقع| خيط| استفسار| تحديد الخطوط المخصصة التي سيتم استخدامها.|
| العودة| خيط| استفسار| تعيين تكوين منطقة جدول البيانات.|
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

## أين يجب علينا استخدام استيراد البيانات إلى جدول البيانات API؟

- استيراد كميات كبيرة من البيانات إلى ورقة عمل جدول البيانات.
-  تنسيق ملف البيانات المستوردة هو[إكس إم إل](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) و[ملف CSV](https://docs.fileformat.com/spreadsheet/csv/).

## لماذا يجب عليك استخدام استيراد البيانات إلى جدول البيانات API؟

- استيراد كميات كبيرة من البيانات إلى جداول البيانات.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام استيراد البيانات إلى جدول بيانات API باستخدام حزم تطوير البرامج (SDKs)

### استيراد البيانات إلى جدول بيانات API المواصفات

 ال[استيراد البيانات إلى جدول بيانات API المواصفات](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح بالتفاعلات REST مباشرة من متصفح الويب الخاص بك.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك باستيراد البيانات إلى جدول بيانات باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
