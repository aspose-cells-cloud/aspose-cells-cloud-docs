---
title: احصل على البيانات الوصفية من ملف Excel
second_title: Aspose.Cells Cloud Documen
linktitle: احصل عليه دون استخدام storag
type: docs
url: /ar/metadata/get/
keywords: Get properties from Excel files
description: Aspose.Cells Cloud REST API يدعم الحصول على الخصائص من ملفات الاكسل. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 23
kwords: Excel، Office Cloud، REST API، Spreadsheet، PDF، CSV، Json، Markdwon، احصل على البيانات الوصفية من Excel ملف
---
يشير REST API إلى الحصول على `metadata` من ملفات Excel المتعددة.

```bash

POST https://api.aspose.cloud/v3.0/cells/metadata/get

```

- **معلمة الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| يكتب| خيط| الكل/مدمج/مخصص|


- **طلب معلمة الجسم**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|ملف اكسل| ملف البيانات|يتم حفظ ملف البيانات في الجزء الأول من المحتوى متعدد الأجزاء.|

- **إجابة**

```bash
{
    [
        { 
            "Name":"test1",
            "Value":"test1",
            ...
        },
        { 
            "Name":"test2",
            "Value":"test3",
            ...
        }
    ]
}
```
- **عائلة Cloud SDK**

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Metadata-Get.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-MetaData-Get.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Metadata-Get.php" >}}

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

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMetadata-Get.py" >}}
{{< /tab >}}
{{< /tabs >}}
