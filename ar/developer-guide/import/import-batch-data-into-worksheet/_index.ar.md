---
title: استيراد البيانات الدفعية إلى ورقة عمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد بيانات دفعة
type: docs
url: /ar/import/batch-data/
aliases: [/import-batch-data-into-excel-worksheet/,/import-batch-data-into-worksheet/,/import-data/batch-data/]
keywords: Import batch data into Excel files
description: Aspose.Cells Cloud REST API يدعم استيراد البيانات المجمعة إلى ملفات Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 19
kwords: Excel، Office Cloud، REST API، جدول البيانات، PDF، CSV، Json، Markdwon، استيراد البيانات المجمعة إلى ورقة عمل Excel
---
هذا REST API `import batch data` إلى Excel ورقة العمل.

الطلب هو طلب HTTP بمحتوى متعدد الأجزاء (انظر[آر إف سي 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[آر إف سي 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات ImportBatchDataOption والثاني يحتوي على ملف بيانات.

## رسيت API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

يتم وصف المعلمات الهامة في الجدول التالي:


**ImportBatchDataOption**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| بيانات الدفعة|قائمة<CellValue> | بيانات دفعة|
| ورقة عمل الوجهة| خيط| اسم ورقة العمل الوجهة.|
| IsInsert| خيط| خطأ صحيح.|
| ImportDataType| خيط|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData.|
| مصدر| مصدر الملف| يشير إلى موضع ملف البيانات عندما تكون المعلمة BatchData فارغة.|



**قيمة الخلية**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| RowIndex| كثافة العمليات||
| مؤشر العمود| كثافة العمليات||
| يكتب| خيط|نوع البيانات|
| قيمة| خيط||
| أسلوب| النمط (الكائن)||



**مصدر الملف**
|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| نوع مصدر الملف| خيط| InMemoryFiles/CloudFileSystem/RequestFiles|
| مسار الملف| خيط| موقف الملف|


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

## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:


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
