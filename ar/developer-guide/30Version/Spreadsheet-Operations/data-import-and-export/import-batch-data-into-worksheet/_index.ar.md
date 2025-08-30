---
title: استيراد بيانات الدفعة إلى ورقة العمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد بيانات الدفعة
type: docs
url: /ar/import-batch-data-into-excel/
aliases: [/import-batch-data-into-worksheet/,/import-data/batch-data/,/import/batch-data/]
keywords: Import batch data into Excel files
description: يدعم Cloud REST استيراد بيانات الدفعات إلى ملفات SDK. تدعم SDK أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 19
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، استيراد بيانات الدفعة إلى ورقة عمل Excel
---
هذه ورقة عمل REST API `import batch data` في Excel.

الطلب عبارة عن طلب HTTP يحتوي على محتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات ImportBatchDataOption ويحتوي الجزء الثاني على ملف بيانات.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

يتم وصف المعلمات الهامة في الجدول التالي:

**خيار استيراد بيانات الدفعة**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| بيانات الدفعة|قائمة<CellValue> | بيانات الدفعة|
| ورقة عمل الوجهة| خيط| اسم ورقة عمل الوجهة.|
| هل تم إدراجه| خيط| صواب/خطأ.|
| نوع بيانات الاستيراد| خيط|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| مصدر| مصدر الملف| يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData فارغة.|

**قيمة الخلية**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| فهرس الصف| عدد صحيح||
| فهرس العمود| عدد صحيح||
| يكتب| خيط| نوع البيانات|
| قيمة| خيط||
| أسلوب| النمط (الكائن)||

**مصدر الملف**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| نوع مصدر الملف| خيط| ملفات في الذاكرة/نظام ملفات السحابة/ملفات الطلب|
| مسار الملف| خيط| موضع الملف|

**مثال**

```xml
<ImportIntArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportIntArrayOption>

```

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
