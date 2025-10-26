---
title: Aspose.Cells Cloud Web API - بحث في محتوى جدول البيانات
second_title: Documen
ArticleTitle: Search Spreadsheet Conten
linktitle: البحث في محتوى جدول البيانات
type: docs
url: /ar/search-spreadsheet-content/
keywords: Excel, Office Cloud, REST API, Spreadsheet Search, PDF Export, CSV Handling, JSON Formatting, Markdown Integration, Match Empty Cells in Exce
description: ابحث بكفاءة عن النص داخل ملفات جدول البيانات المحلية باستخدام رقمنا API
weight: 100
kwords: Excel، Office السحابة، REST API، بحث جدول البيانات، PDF التصدير، معالجة CSV، تنسيق JSON، تكامل Markdown، مطابقة فارغة Cells في Excel
---
ابحث عن نص داخل ملفات جدول البيانات المحلية باستخدام رقمنا API.

## **البحث في محتوى جدول البيانات API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/content
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|جدول بيانات|ملف|بيانات النموذج|قم بتحميل ملف جدول البيانات للبحث.|
|نص البحث|خيط|استفسار|النص الذي تريد البحث عنه داخل جدول البيانات.|
|تجاهل الحالة|منطقي|استفسار|حدد ما إذا كان سيتم تجاهل الحالة في البحث.|
|ورقة عمل|خيط|استفسار|حدد ورقة العمل التي تريد البحث داخلها.|
|منطقة الخلية|خيط|استفسار|حدد منطقة الخلايا التي تريد البحث فيها.|
|منطقة|خيط|استفسار|إعداد المنطقة للجدول الإلكتروني.|
|كلمة المرور|خيط|استفسار|كلمة المرور المطلوبة لفتح ملف جدول البيانات.|

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

## أين يجب علينا استخدام محتوى البحث داخل جدول البيانات API؟

عندما تحتاج إلى البحث عن محتوى داخل جدول البيانات، يمكنك استخدام هذا API.

## لماذا يجب عليك استخدام محتوى البحث داخل جدول البيانات API؟

- ابحث بسهولة عن المحتوى داخل جدول بيانات باستخدام هذا الجهاز API.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام البحث عن الروابط المعطلة داخل جدول البيانات API باستخدام مجموعات أدوات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يسمح لك بسهولة تنفيذ محتوى البحث داخل جداول البيانات للخلايا باستخدام الحد الأدنى من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
