---
title: Aspose.Cells Cloud Web API - استبدال محتوى النطاق في جدول بيانات بعيد
second_title: Documen
ArticleTitle: Replace Range Content in Remote a Spreadshee
linktitle: استبدال محتوى النطاق البعيد
type: docs
url: /ar/replace-content-in-remote-range/
keywords: API, Excel API, Replace Content, Remote Spreadsheet, Cloud Storage, Text Replacement, REST AP
description: استبدال النص بكفاءة ضمن نطاقات محددة من جداول البيانات البعيدة باستخدام Aspose.Cells Cloud API
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، مطابقة جميع الخلايا الفارغة في ورقة عمل Excel، استبدال النص عن بعد، تكامل التخزين السحابي
---
استبدال النص المحدد بكفاءة ضمن نطاق ملف جدول بيانات بعيد.

## **استبدال المحتوى في النطاق البعيد API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/replace/content
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم ملف المصنف الذي سيتم تعديله.|
| نص البحث| خيط| استفسار| النص الذي تريد البحث عنه داخل جدول البيانات.|
| استبدال النص| خيط| استفسار| النص الذي سيتم استبدال النص الذي تم البحث عنه به.|
| ورقة عمل| خيط| طريق| اسم ورقة العمل التي سيحدث فيها الاستبدال.|
| منطقة الخلية| خيط| طريق| منطقة الخلية المحددة للاستبدال.|
| مجلد| خيط| استفسار| مسار المجلد الذي يتم تخزين المصنف فيه.|
| اسم التخزين| خيط| استفسار|(اختياري) اسم وحدة التخزين إذا كنت تستخدم تخزينًا سحابيًا مخصصًا. استخدم وحدة التخزين الافتراضية إذا تم حذفها.|
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

## أين يجب علينا استخدام محتوى استبدال النطاق في جدول البيانات البعيد API؟

عندما تحتاج إلى استبدال محتوى النطاق في جدول بيانات بعيد، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام استبدال محتوى النطاق في جدول البيانات البعيد API؟

- استبدال محتوى النطاق بسرعة في جداول البيانات البعيدة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام استبدال محتوى النطاق في جدول البيانات البعيد API مع مجموعات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteRange) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام مجموعة أدوات تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يسمح لك بتطبيق استبدال المحتوى في جداول البيانات للخلايا بسهولة وبأقل قدر من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
