---
title: استيراد صفيف سلسلة البعد 2 إلى ورقة عمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد 2 سلسلة البعد
type: docs
url: /ar/import/2dimension-string-array/
aliases: [/import-2dimension-string-array-into-excel-worksheet/,/import-2dimension-string-array-into-worksheet/,/import-data/-2dimension-string-array/,/import-data/2dimension-string-array/]
keywords: Import 2 dimension string array data into Excel files
description: Aspose.Cells Cloud REST API يدعم استيراد بيانات صفيف سلسلة ذات بعدين إلى ملفات Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 20
kwords: Excel، Office السحابة، REST API، جدول البيانات، PDF، CSV، Json، Markdwon، استيراد مصفوفة سلسلة ثنائية الأبعاد إلى ورقة عمل Excel
---
هذا REST API `import 2 dimension string array data` إلى Excel ورقة العمل.

الطلب هو طلب HTTP بمحتوى متعدد الأجزاء (انظر[آر إف سي 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[آر إف سي 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات Import2DimensionStringArrayOption والثاني يحتوي على ملف بيانات.

## رسيت API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```

يتم وصف المعلمات الهامة في الجدول التالي:

**Import2DimensionStringArrayOption**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| السطر الاول| كثافة العمليات||
| العمود الأول| كثافة العمليات||
| بيانات|خيط[،]||
| ورقة عمل الوجهة| خيط| اسم ورقة العمل الوجهة.|
| IsInsert| خيط| خطأ صحيح.|
| ImportDataType| خيط|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| مصدر| مصدر الملف| يشير إلى موضع ملف البيانات عندما تكون المعلمة BatchData فارغة.|



**مثال**

```json

{
    "Data": [
        ["1.0", "2.9"],
        ["2.0", "2.1"]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 1,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionStringArray"
}

```

## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}




