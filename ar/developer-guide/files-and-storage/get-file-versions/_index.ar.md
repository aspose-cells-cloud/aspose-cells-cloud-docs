---
title: الحصول على إصدار الملف
second_title: Documen
linktitle: الحصول على إصدار الملف
type: docs
url: /ar/get-file-versions/
keywords: file versions, Excel API, Office Cloud, REST API, spreadsheet management, document histor
description: استرداد وإدارة إصدارات الملفات المخزنة في السحابة Aspose.Cells، مما يعزز إدارة المستندات والتعاون
weight: 100
kwords: الحصول على إصدارات الملفات، Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، إدارة المستندات
---
## **Excel API: الحصول على إصدارات الملف**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **وصف الوظيفة**

 ال**الحصول على إصدارات الملفات** يتيح API للمستخدمين استرجاع إصدارات مختلفة من ملف مُحدد مُخزّن في السحابة Aspose.Cells. تُعد هذه الوظيفة أساسية للحفاظ على سلامة المستندات وتتبّع التغييرات بمرور الوقت.

###  معلمات الطلب**الحصول على إصدارات الملفات** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| المسار إلى الملف الذي سيتم استرجاع الإصدارات الخاصة به.|
| اسم التخزين| خيط| استفسار| اسم التخزين الذي يوجد به الملف.|

### **وصف الاستجابة**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)يوفر واجهة برمجة شاملة لتنفيذ تفاعلات REST مباشرة من متصفح الويب.

## Excel API مجموعة تطوير البرامج

 يُسهّل استخدام مجموعة تطوير البرامج (SDK) عملية التطوير من خلال تبسيط التعقيدات البسيطة، مما يسمح للمطورين بالتركيز على الوظائف الأساسية. استكشف[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells عبر لغات البرمجة المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{< /tab >}}
{{< /tabs >}}
