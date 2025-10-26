---
title: احصل على جميع الأشكال في ورقة عمل Excel
second_title: Documen
linktitle: جيت-ال
type: docs
url: /ar/shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: Get all shapes on an Excel workshee
description: يدعم Cloud REST Aspose.Cells الحصول على جميع الأشكال في ورقة عمل Excel. تدعم مجموعة أدوات تطوير البرامج (SDK) أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 10
kwords: Excel، Office Cloud، REST API، جدول بيانات، PDF، CSV، Json، Markdown، الحصول على جميع الأشكال على ورقة عمل Excel
---
يشير هذا REST API إلى الحصول على أشكال ورقة العمل

## RSET API

```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم المستند.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| مجلد| خيط| استفسار| مجلد المستند.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShapes) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash

{

  "Shapes" : {

    "ShapeList" : [

      {

        "link" : {

          "Href" : "/0",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/1",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/2",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/3",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      }

    ],

    "link" : {

      "Href" : "http://api.aspose.com/v1.1/cells/sampleShapes.xlsx/worksheets/Sheet1/shapes",

      "Rel" : "self",

      "Type" : null,

      "Title" : null

    }

  },

  "Code" : 200,

  "Status" : "OK"

}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}
