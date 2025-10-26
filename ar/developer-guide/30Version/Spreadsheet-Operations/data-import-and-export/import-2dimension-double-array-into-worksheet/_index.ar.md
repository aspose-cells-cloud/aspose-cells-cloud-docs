---
title: استيراد مصفوفة ثنائية الأبعاد إلى ورقة العمل Excel
second_title: Documen
linktitle: استيراد ترتيب مزدوج ثنائي الأبعاد
type: docs
url: /ar/import-a-2D-double-array-into-excel-worksheet/
aliases: [/import-2dimension-double-array-into-excel-worksheet/,/import-2dimension-double-array-into-worksheet/, /import-data/2dimension-double-array/, /import/2dimension-double-array/]
keywords: Import 2 dimension double array data into Excel files
description: يدعم Cloud REST استيراد بيانات مصفوفة ثنائية الأبعاد إلى ملفات. تدعم حزمة SDK لغات تطوير متنوعة، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 20
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، استيراد مصفوفة مزدوجة ثنائية الأبعاد إلى ورقة عمل Excel
---
هذه ورقة عمل REST API `import 2 dimension double array data` في Excel.

الطلب عبارة عن طلب HTTP يحتوي على محتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات Import2DimensionDoubleArrayOption ويحتوي الجزء الثاني على ملف بيانات.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

يتم وصف المعلمات الهامة في الجدول التالي:

**خيار استيراد مصفوفة مزدوجة الأبعاد**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| الصف الأول| عدد صحيح||
| العمود الأول| عدد صحيح||
| بيانات|مزدوج[،]||
|ورقة عمل الوجهة| خيط| اسم ورقة عمل الوجهة.|
| هل تم إدراجه| خيط| صواب/خطأ.|
| نوع بيانات الاستيراد| خيط|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| مصدر| مصدر الملف| يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.|

**مثال**

```json

{
    "Data": [
        [1.0, 2.9, 3.1],
        [2.0, 2.1, 3.1]
    ],
    "DestinationWorksheet": "Sheet2",
    "FirstRow": 4,
    "FirstColumn": 1,
    "importDataType": "TwoDimensionDoubleArray"
}

```

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
