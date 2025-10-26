---
title: Aspose.Cells Cloud Web API - البحث عن الروابط المعطلة للنطاق في جدول بيانات بعيد
second_title: Documen
ArticleTitle: Search Broken Links of Range in Remote a Spreadshee
linktitle: البحث عن النطاق البعيد رابط معطل
type: docs
url: /ar/search-broken-links-in-remote-range/
keywords: broken links, remote spreadsheet, Excel API, REST API, link checker, hyperlink validation, cloud storag
description: البحث بكفاءة عن الروابط المعطلة ضمن نطاق محدد من جدول بيانات بعيد مخزن في وحدة تخزين سحابية
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، الروابط المعطلة، التحقق من صحة الارتباط التشعبي، التخزين السحابي
---
ابحث بكفاءة عن الروابط المعطلة ضمن نطاق محدد من جدول بيانات بعيد مخزن في وحدة تخزين سحابية.

## **البحث عن الروابط المعطلة في النطاق البعيد API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم ملف المصنف الذي سيتم البحث فيه.|
| ورقة عمل| خيط| طريق| حدد ورقة العمل للبحث.|
| منطقة الخلية| خيط| طريق| حدد منطقة الخلية للبحث.|
| مجلد| خيط| استفسار| مسار المجلد الذي يتم تخزين المصنف فيه.|
| اسم التخزين| خيط| استفسار|(اختياري) اسم وحدة التخزين إذا كنت تستخدم تخزينًا سحابيًا مخصصًا. استخدم وحدة التخزين الافتراضية إذا تم حذفها.|
| منطقة| خيط| استفسار| إعداد منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| كلمة المرور لفتح ملف جدول البيانات.|

### **إجابة**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
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

## أين يجب أن نستخدم البحث عن الروابط المكسورة ضمن نطاق جدول البيانات API؟

عندما تحتاج إلى البحث عن الروابط المكسورة ضمن نطاق جدول البيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام البحث عن الروابط المكسورة ضمن نطاق جدول البيانات API؟

- ابحث بسرعة عن الروابط المعطلة ضمن نطاق جدول البيانات.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام البحث عن الروابط المعطلة ضمن نطاق جدول البيانات API باستخدام مجموعات أدوات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchBrokenLinksInRemoteRange) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يسمح لك بسهولة تنفيذ البحث المُجزأ ضمن نطاق جداول البيانات للخلايا باستخدام الحد الأدنى من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
