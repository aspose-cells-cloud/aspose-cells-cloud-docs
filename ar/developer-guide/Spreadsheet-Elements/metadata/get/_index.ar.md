---
title: الحصول على البيانات الوصفية من الملف Excel
second_title: Aspose.Cells Cloud Documen
linktitle: احصل عليه دون استخدام التخزين
type: docs
url: /ar/metadata/get/
keywords: Get properties from Excel files
description: يدعم Cloud REST Aspose.Cells الحصول على خصائص من ملفات Excel. تدعم SDK أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 23
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، الحصول على البيانات الوصفية من ملفات Excel
---
يشير هذا REST API إلى الحصول على `metadata` من ملفات Excel المتعددة.

```bash

POST https://api.aspose.cloud/v3.0/cells/metadata/get

```

- **معلمة الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
| يكتب| خيط| الكل/مدمج/مخصص|

- **معلمة نص الطلب**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|ملف إكسل| ملف البيانات|يتم حفظ ملف البيانات في الجزء الأول من المحتوى المتعدد الأجزاء.|

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

- **عائلة SDK السحابية**

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
