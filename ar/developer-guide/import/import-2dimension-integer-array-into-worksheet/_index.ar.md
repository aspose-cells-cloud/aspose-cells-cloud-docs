---
title: قم باستيراد صفيف عدد صحيح ثنائي الأبعاد إلى Excel Workshee
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد 2 بعد مصفوفة عدد صحيح
type: docs
url: /ar/import/2dimension-integer-array/
aliases: [/import-2dimension-integer-array-into-excel-worksheet/,/import-2dimension-integer-array-into-worksheet/, /import-data/2dimension-integer-array/]
keywords: Import 2 dimension integer array data into Excel files
description: Aspose.Cells Cloud REST API يدعم استيراد بيانات مصفوفة ذات أبعاد صحيحة في ملفات Excel. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 20
---
هذا REST API `import 2 dimension integer array data` إلى Excel ورقة العمل.

الطلب عبارة عن طلب HTTP بمحتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات Import2DimensionIntegerArrayOption والثاني يحتوي على ملف بيانات.

يتم وصف المعلمات المهمة في الجدول التالي:

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

**Import2DimensionIntegerArrayOption**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| السطر الاول| int||
| العمود الأول| int||
| بيانات|عدد صحيح[،]||
| ورقة عمل الوجهة| خيط| اسم ورقة العمل الوجهة.|
| هو إدراج| خيط| خطأ صحيح.|
| إيمبورداتاتايب| خيط|IntArray / DoubleArray / StringArray / TwoDimensionIntArray / TwoDimensionDoubleArray / TwoDimensionStringArray / BatchData / CSVData.|
| مصدر| مصدر الملف| يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.|



**مثال**

```json
{
    "Data": [
        [1, 2],
        [3, 4]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 4,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionIntArray"
}

```
## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




