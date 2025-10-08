---
title: Aspose.Cells Cloud Web API - البحث عن الروابط المعطلة في جدول بيانات
second_title: Documen
ArticleTitle: Search Spreadsheet Broken Links in a Spreadshee
linktitle: بحث جدول البيانات رابط معطل
type: docs
url: /ar/search-spreadsheet-broken-links/
keywords: search broken links, spreadsheet API, Excel broken links, REST API, Office Cloud integratio
description: ابحث بكفاءة عن الروابط المعطلة في جداول البيانات المحلية باستخدام Excel API
weight: 100
kwords: Excel API، البحث عن الروابط المعطلة، Office السحابة، REST API، إدارة جداول البيانات، PDF، CSV، JSON، Markdown، تحديد الروابط المعطلة، إصلاح الارتباط التشعبي
---
ابحث عن الروابط المعطلة داخل جداول البيانات المحلية.

## **البحث في جدول البيانات الروابط المعطلة API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/broken-links
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|جدول بيانات|ملف|بيانات النموذج|قم بتحميل ملف جدول البيانات المراد تحليله.|
|ورقة عمل|خيط|استفسار|حدد ورقة العمل للامتحان.|
|منطقة الخلية|خيط|استفسار|حدد منطقة الخلية للتحليل.|
|منطقة|خيط|استفسار|تعيين تكوين منطقة جدول البيانات.|
|كلمة المرور|خيط|استفسار|قم بتوفير كلمة المرور للوصول إلى ملف جدول البيانات.|

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

عندما تحتاج إلى البحث عن الروابط المكسورة داخل جدول البيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام البحث عن الروابط المكسورة داخل جدول البيانات API؟

- ابحث بسهولة عن الروابط المكسورة داخل جدول بيانات بعيد باستخدام هذا API.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام البحث عن الروابط المعطلة داخل جدول البيانات API باستخدام مجموعات أدوات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يُتيح لك البحث بسهولة عن الروابط المعطلة داخل جداول البيانات في الخلايا التي تتطلب الحد الأدنى من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{< /tab >}}
{{< /tabs >}}
