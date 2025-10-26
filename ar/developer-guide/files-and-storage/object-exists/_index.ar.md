---
title: وجود الكائن
second_title: Documen
linktitle: وجود الكائن
type: docs
url: /ar/object-exists/
keywords: Excel API, Object Exists, REST API, Aspose, File Management, Excel, Office Cloud, Spreadsheet, PDF, CSV, JSON, Markdow
description: يتحقق الأمر The Object Exists API من وجود ملف أو مجلد محدد في وحدة التخزين السحابية Aspose.Cells
weight: 100
kwords: Excel API، وجود الكائن، REST API، Aspose، Office السحابة، إدارة الملفات، جدول بيانات، PDF، CSV، JSON، Markdown، التحقق من وجود الملف في Excel
---
## **Excel API: الكائن موجود**

```
GET http://api.aspose.cloud/v4.0/cells/storage/exist/{path}
```

### **وصف الوظيفة**

يتيح `objectExists` API للمطورين التحقق من وجود ملف أو مجلد محدد ضمن التخزين السحابي Aspose.Cells.

###  معلمات الطلب**الكائن موجود** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|طريق|خيط|طريق|المسار إلى الملف أو المجلد في التخزين السحابي.|
|اسم التخزين|خيط|استفسار|اسم التخزين الذي يوجد به الملف.|
|معرف الإصدار|خيط|استفسار|معرف إصدار الملف (إن أمكن).|

### **وصف الاستجابة**

```json
{
  "Name": "ObjectExist",
  "Description": [
    "Object exists"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates that the file or folder exists."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    },
    {
      "Name": "IsFolder",
      "Description": [
        "True if it is a folder, false if it is a file."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/ObjectExists) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

## Excel API مجموعة تطوير البرامج

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ObjectExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ObjectExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ObjectExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ObjectExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ObjectExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ObjectExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ObjectExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ObjectExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
