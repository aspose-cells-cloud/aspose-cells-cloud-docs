---
title: الحصول على قائمة الملفات - Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: الحصول على قائمة الملفات
type: docs
url: /ar/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: تعرف على كيفية استرداد قائمة الملفات من مجلد محدد باستخدام Aspose.Cells API. يوفر هذا الدليل تفاصيل حول معلمات الطلب وبنية الاستجابة وأمثلة التعليمات البرمجية بلغات البرمجة المختلفة
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، إدارة الملفات السحابية، الحصول على قائمة الملفات
---
## **Excel API: الحصول على قائمة الملفات**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **وصف الوظيفة**

 ال**الحصول على قائمة الملفات**يتيح API للمستخدمين استرجاع قائمة شاملة بالملفات والمجلدات الموجودة ضمن مجلد محدد في خدمة التخزين السحابي Aspose.Cells. تُعد هذه النقطة النهائية أساسية لإدارة الملفات بكفاءة، كما أنها تدعم تنسيقات ملفات متنوعة.

###  معلمات الطلب**الحصول على قائمة الملفات** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| طريق| خيط| طريق| المسار إلى المجلد في التخزين السحابي الذي تريد استرداد قائمة الملفات منه.|
| اسم التخزين| خيط| استفسار| اسم التخزين الذي سيتم الوصول إليه.|

### **وصف الاستجابة**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام تتيح التفاعلات REST مباشرة من متصفح الويب، مما يسهل التكامل والاختبار.

## Excel API مجموعة تطوير البرامج

 يُعد استخدام حزمة تطوير برمجيات (SDK) الطريقة الأمثل لتسريع عملية التطوير. تُدير هذه الحزمة التفاصيل البسيطة، مما يُتيح لك التركيز على مهام مشروعك. للاطلاع على قائمة كاملة بمجموعات تطوير البرمجيات السحابية (Aspose.Cells)، يُرجى زيارة[مستودع GitHub](https://github.com/aspose-cells-cloud).

توضح أمثلة التعليمات البرمجية التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}
