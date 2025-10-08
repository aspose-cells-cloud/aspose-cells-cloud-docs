---
title: Aspose.Cells Cloud Web API - دمج جدول بيانات واحد في آخر.
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: دمج جدول البيانات عن بعد
type: docs
url: /ar/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: يمكنك دمج ملف جدول بيانات مخزن في وحدة تخزين سحابية في جدول بيانات آخر، ومن ثم تحديد تنسيق وموقع إخراج البيانات.
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، دمج الخلايا الفارغة، المعالجة السحابية
---
يمكنك دمج ملف جدول بيانات مخزن في وحدة تخزين سحابية في جدول بيانات آخر، ومن ثم تحديد تنسيق وموقع إخراج البيانات.

## **دمج جدول البيانات عن بعد API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|اسم|خيط|طريق|اسم ملف المصنف الذي سيتم دمجه.|
|جدول بيانات مدمج|خيط|استفسار|قائمة ملفات جدول البيانات المراد دمجها.|
|مجلد|خيط|استفسار|مسار المجلد الذي يتم تخزين المصنف فيه.|
|تنسيق خارجي|خيط|استفسار|تنسيق ملف الإخراج (على سبيل المثال، XLSX، PDF).|
|دمج في ورقة واحدة|منطقي|استفسار|ما إذا كان سيتم دمج كافة البيانات في ورقة عمل واحدة.|
|اسم التخزين|خيط|استفسار|(اختياري) اسم وحدة التخزين في حال استخدام تخزين سحابي مخصص. يُضبط افتراضيًا على وحدة التخزين الافتراضية في حال حذفه.|
|المسار الخارجي|خيط|استفسار|(اختياري) مسار المجلد للمصنف المدمج. افتراضيًا، القيمة فارغة.|
|اسم التخزين الخارجي|خيط|استفسار|اسم التخزين لملف الإخراج.|
|الخطوطالموقع|خيط|استفسار|موقع الخط المخصص.|
|منطقة|خيط|استفسار|إعداد منطقة جدول البيانات.|
|كلمة المرور|خيط|استفسار|كلمة المرور للوصول إلى ملف جدول البيانات.|

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

## أين يجب علينا استخدام Merge Remote Spreadsheet API؟

- عندما تحتاج إلى دمج ملفات بيانات متعددة معًا في التخزين السحابي.


## لماذا يجب عليك استخدام Merge Remote Spreadsheet API؟

- لا تحتاج ملفات التخزين السحابي إلى التنزيل، ويمكن دمجها مباشرة في السحابة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام دمج جدول البيانات عن بُعد API مع مجموعات تطوير البرامج (SDKs)

### مواصفات دمج جدول البيانات عن بُعد API

 ال[مواصفات دمج جدول البيانات عن بُعد API](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) يوفر واجهة برمجة يمكن الوصول إليها بشكل عام لتنفيذ تفاعلات REST مباشرة من متصفح الويب.

## Excel API مجموعة تطوير البرامج

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث إنه يجرد التفاصيل منخفضة المستوى، مما يسمح لك بدمج جدول بيانات في جدول بيانات آخر باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
تُظهر أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
