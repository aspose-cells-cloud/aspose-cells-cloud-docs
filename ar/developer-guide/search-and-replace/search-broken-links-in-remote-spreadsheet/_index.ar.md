---
title: Aspose.Cells Cloud Web API - البحث عن الروابط المعطلة في جدول البيانات البعيد
second_title: Documen
ArticleTitle: Search for Broken Links in Remote Spreadsheet
linktitle: البحث عن جداول البيانات عن بعد رابط معطل
type: docs
url: /ar/search-broken-links-in-remote-spreadsheet/
keywords: broken links, remote spreadsheet, Excel API, cloud storage, hyperlink checker, dead URL detection, REST AP
description: ابحث بكفاءة عن الروابط المعطلة في جداول البيانات البعيدة المخزنة في بيئات السحابة
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، الروابط المعطلة، التحقق من صحة الارتباط التشعبي، التخزين السحابي
---
ابحث عن الروابط المعطلة في جداول البيانات البعيدة المخزنة في بيئات السحابة.

## **البحث عن الروابط المعطلة في جدول البيانات البعيد API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|اسم|خيط|طريق|اسم ملف المصنف الذي سيتم البحث فيه.|
|ورقة عمل|خيط|استفسار|حدد ورقة العمل للبحث.|
|منطقة الخلية|خيط|استفسار|حدد منطقة الخلية للبحث.|
|مجلد|خيط|استفسار|مسار المجلد الذي يتم تخزين المصنف فيه.|
|اسم التخزين|خيط|استفسار|(اختياري) اسم وحدة التخزين في حال استخدام تخزين سحابي مخصص. سيتم استخدام وحدة التخزين الافتراضية في حال عدم استخدامها.|
|منطقة|خيط|استفسار|إعداد منطقة جدول البيانات.|
|كلمة المرور|خيط|استفسار|كلمة المرور لفتح ملف جدول البيانات.|

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

## أين يجب أن نستخدم البحث عن الروابط المكسورة داخل جدول البيانات API؟

عندما تحتاج إلى البحث عن الروابط المعطلة داخل جدول البيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام البحث عن الروابط المكسورة داخل جدول البيانات API؟

- ابحث بكفاءة عن الروابط المعطلة في جداول البيانات البعيدة المخزنة في بيئات السحابة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام البحث عن الروابط المعطلة داخل جدول البيانات API باستخدام مجموعات أدوات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchBrokenLinksInRemoteSpreadsheet) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يسمح لك بسهولة تنفيذ عمليات البحث المُجزأة داخل جداول البيانات للخلايا باستخدام الحد الأدنى من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

تُظهر أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
