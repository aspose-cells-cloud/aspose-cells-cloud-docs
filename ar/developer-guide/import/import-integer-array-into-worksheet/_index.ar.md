---
title: استيراد صفيف صحيح إلى Excel Workshee
linktitle: استيراد مجموعة صحيحة
type: docs
url: /ar/import/integer-array/
aliases: [/import-integer-array-into-excel-worksheet/,/import-integer-array-into-worksheet/,/import-data/integer-array/]
keywords: Import integer array data into Excel files
description: Aspose.Cells Cloud REST API يدعم استيراد بيانات صفيف عدد صحيح في ملفات Excel. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 30
---
هذا REST API `import int array data` إلى Excel ورقة العمل.

الطلب عبارة عن طلب HTTP بمحتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات ImportIntegerArrayOption والثاني يحتوي على ملف بيانات.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

يتم وصف المعلمات المهمة في الجدول التالي:


**ImportIntegerArrayOption**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| السطر الاول| int||
| العمود الأول| int||
| عمودي| خيط| خطأ صحيح.|
| بيانات|عدد صحيح[]||
| ورقة عمل الوجهة| خيط| اسم ورقة العمل الوجهة.|
| هو إدراج| خيط| خطأ صحيح.|
| إيمبورداتاتايب| خيط|IntArray / DoubleArray / StringArray / TwoDimensionIntArray / TwoDimensionDoubleArray / TwoDimensionStringArray / BatchData / CSVData.|
| مصدر| مصدر الملف| يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.|



**مثال**

```JSON

{
    "Data": [1, 2, 4],
    "DestinationWorksheet": "Sheet1",
    "FirstRow": 1,
    "FirstColumn": 2,
    "IsVertical": true,
    "IsInsert": true,
    "importDataType": "IntArray"
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

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




