﻿---
title: تصدير الصورة
second_title: Aspose.Cells Cloud Documen
linktitle: صورة
type: docs
url: /ar/export-excel-picture-to-different-formats/
aliases: [ /export/excel-picture-to-different-formats/]
keywords: Export Excel picture to kinds of format files
description: يدعم Cloud REST تصدير الصور إلى أنواع مختلفة من ملفات التنسيق. تدعم حزمة SDK لغات تطوير متنوعة، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 20
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، تصدير الصورة
---
 يمكنك تصدير التنسيقات:[PNG](https://docs.fileformat.com/Image/png/), [صورة متحركة](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/),  [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [مؤسسة ويكيميديا](https://docs.fileformat.com/image/Wmf/).

- **الباقي API**

|**API**|**يكتب**|**وصف**|**رابط سواجر**|
|:- |:- |:- |:- |
|/الخلايا/التصدير|بريد|تصدير كائنات Excel من محتوى الطلب إلى بعض التنسيقات|[ما بعد التصدير](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL** أداة سطر أوامر للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

- **طلب**

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **إجابة**

```bash
{
    "Files": [{
        "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
        "FileSize": 21680,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
        "FileSize": 21286,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
        "FileSize": 130084,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
        "FileSize": 120062,
        "FileContent": "-----Base64String--------"
    }]
}
```

- **عائلة SDK السحابية**

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

