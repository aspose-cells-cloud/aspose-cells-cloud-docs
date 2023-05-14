---
title: استيراد صورة إلى Excel Workshee
second_title: Aspose.Cells Cloud Documen
linktitle: استيراد الصورة
type: docs
url: /ar/import/picture/
aliases: [/import-picture-into-excel-worksheet/,/import-picture-into-worksheet/,/import-data/picture/]
keywords: Import picture into Excel files
description: Aspose.Cells Cloud REST API يدعم استيراد الصورة إلى ملفات Excel. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 19
---
هذا REST API `import picture data` إلى Excel ورقة العمل.

الطلب عبارة عن طلب HTTP بمحتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات ImportPictureOption والثاني يحتوي على ملف بيانات.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/import-data

```


يتم وصف المعلمات المهمة في الجدول التالي:


**ImportPictureOption**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| UpperLeftRow| int||
|UpperLeftColumn| int||
| LowerRightRow| int||
| LowerRightColumn| int||
| اسم الملف| خيط||
| بيانات| خيط||
| ورقة عمل الوجهة| خيط| اسم ورقة العمل الوجهة.|
| هو إدراج| خيط| خطأ صحيح.|
| إيمبورداتاتايب| خيط|IntArray / DoubleArray / StringArray / TwoDimensionIntArray / TwoDimensionDoubleArray / TwoDimensionStringArray / BatchData / CSVData / Picture.|
| مصدر| مصدر الملف| يشير إلى موضع ملف البيانات عندما تكون معلمة BatchData خالية.|


**مثال**


## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:


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

