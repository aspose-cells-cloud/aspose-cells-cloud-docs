---
title: استيراد بيانات CSV إلى ورقة العمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد بيانات csv
type: docs
url: /ar/import-csv-data-into-excel/
aliases: [/import-csv-data-into-worksheet/,/import-data/csv-data/,/import/csv-data/]
keywords: Import csv data into Excel files
description: يدعم Cloud REST استيراد بيانات csv إلى ملفات. تدعم حزمة SDK لغات تطوير متنوعة، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 19
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، استيراد بيانات CSV إلى ورقة عمل Excel
---
هذه ورقة عمل REST API `import csv data` في Excel.

الطلب عبارة عن طلب HTTP يحتوي على محتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات ImportCSVDataOption ويحتوي الجزء الثاني على ملف بيانات.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata

```

يتم وصف المعلمات الهامة في الجدول التالي:

**خيار استيراد بيانات CSV**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| سلسلة فاصلة| خيط||
| تحويل البيانات الرقمية| خيط|صواب/خطأ.|
| الصف الأول| عدد صحيح||
| العمود الأول| عدد صحيح||
| ملف المصدر| خيط||
| المحللات المخصصة|قائمة<CustomParserConfig> ||

**تكوين المحلل المخصص**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| فهرس العمود| عدد صحيح||
| طريقة التحليل| خيط||
| نمط مخصص| خيط||

**مثال**

```xml

 <ImportCSVDataOption>
     <DestinationWorksheet>Sheet1</DestinationWorksheet>
     <IsInsert>true</IsInsert>
     <ImportDataType>CSVData</ImportDataType>
     <SeparatorString>;</SeparatorString>
     <ConvertNumericData>true</ConvertNumericData>
     <FirstRow>1</FirstRow>
     <FirstColumn>2</FirstColumn>
     <SourceFile>TestImportDataCSV.csv</SourceFile>
     <CustomParsers>
         <CustomParserConfig>
             <ColumnIndex>0</ColumnIndex>
             <ParseMethod>ToString</ParseMethod>
             <CustomStyle>#</CustomStyle>
         </CustomParserConfig>
     </CustomParsers>
 </ImportCSVDataOption>

```

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="1" tabID="1" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportCSVData.php" >}}

{{< /tab >}}

{{< /tabs >}}
