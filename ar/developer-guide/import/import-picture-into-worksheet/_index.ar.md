---
title: استيراد الصورة إلى ورقة عمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد الصورة
type: docs
url: /ar/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API يدعم استيراد الصور إلى ملفات Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 19
kwords: Excel، Office السحابة، REST API، جدول البيانات، PDF، CSV، Json، Markdwon، استيراد الصورة إلى ورقة عمل Excel
---
هذا REST API `import picture data` إلى Excel ورقة العمل.

الطلب هو طلب HTTP بمحتوى متعدد الأجزاء (انظر[آر إف سي 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[آر إف سي 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات ImportPictureOption والثاني يحتوي على ملف بيانات.

## رسيت API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```


يتم وصف المعلمات الهامة في الجدول التالي:


**ImportPictureOption**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| UpperLeftRow| كثافة العمليات||
| UpperLeftColumn| كثافة العمليات||
| الصف السفلي لليمين| كثافة العمليات||
| LowerRightColumn| كثافة العمليات||
| اسم الملف| خيط||
| بيانات| خيط||
| ورقة عمل الوجهة| خيط| اسم ورقة العمل الوجهة.|
| IsInsert| خيط| خطأ صحيح.|
| ImportDataType| خيط|IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture.|
| مصدر| مصدر الملف| يشير إلى موضع ملف البيانات عندما تكون المعلمة BatchData فارغة.|


**مثال**


## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< /tabs >}}

