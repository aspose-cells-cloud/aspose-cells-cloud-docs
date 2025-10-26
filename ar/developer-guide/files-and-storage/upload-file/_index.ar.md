---
title: تحميل الملف إلى الجوال Aspose
second_title: Developer Guide for File Uploa
linktitle: تحميل الملف
type: docs
url: /ar/upload-file/
keywords: Aspose, file upload, Excel API, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, upload Excel files, match blank cell
description: دليل شامل حول كيفية تحميل الملفات باستخدام Aspose Cells API، بما في ذلك المعلمات وبنية الاستجابة
weight: 100
kwords: Excel، Office Cloud، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، مطابقة جميع الخلايا الفارغة في ورقة عمل Excel، تحميل الملف
---
## **Aspose Cells API: تحميل الملف**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **وصف الوظيفة**

 ال**تحميل الملف** يتيح API للمطورين تحميل الملفات مباشرة إلى التخزين السحابي للمعالجة باستخدام Aspose Cells.

###  معلمات الطلب**تحميل الملف** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| تحميل الملفات| ملف| بيانات النموذج|تحميل الملفات إلى التخزين السحابي.|
| طريق| خيط| طريق| مسار الوجهة في التخزين السحابي. حدد المسار الذي سيتم تحميل الملف إليه.|
| اسم التخزين| خيط| استفسار| اسم التخزين الذي سيتم تحميل الملف عليه.|

### **وصف الاستجابة**

```json
{
  "Name": "FilesUploadResult",
  "Description": [
    "File upload result"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": [
        "List of uploaded file names"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": [
        "List of errors."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FileController/UploadFile) يوفر وصفًا تفصيليًا لـ API، مما يتيح للمطورين إجراء تفاعلات REST مباشرة من متصفح الويب.

## Aspose Cells API مجموعة تطوير البرامج

 يُحسّن استخدام مجموعة أدوات تطوير البرامج (SDK) كفاءة التطوير من خلال إدارة التفاصيل البسيطة، مما يسمح للمطورين بالتركيز على مهام المشروع. تفضل بزيارة[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة شاملة لـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
