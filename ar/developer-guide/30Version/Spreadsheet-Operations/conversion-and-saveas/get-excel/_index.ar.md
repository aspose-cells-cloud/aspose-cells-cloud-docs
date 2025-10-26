---
title: يحصل على الملف Excel بتنسيق آخر
second_title: Documen
linktitle: احصل على التميز
type: docs
url: /ar/get different formats files/
aliases: [/export-excel-workbook-to-different-file-formats/, /export-different-formats/]
keywords: Get excel files to kinds of format files
description: يدعم Cloud REST تحويل ملفات Excel إلى أنواع مختلفة من صيغ الملفات. تدعم SDK لغات تطوير متنوعة، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 10
kwords: Excel، Office Cloud، REST API، جدول بيانات، PDF، CSV، Json، Markdown، يحصل على ملف Excel إلى تنسيقات أخرى
---
يشير هذا REST API إلى ملف Excel `get` بتنسيق ملف مختلف.

**معلمة الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|شكل|خيط|تنسيق الملف: csv، xls، html، mhtml، ods، pdf، xml، txt، tiff، xlsb، xlsm، xlsx، xltm، xltx، xps، png، jpg، gif، emf، bmp، md، Numbers، wmf، svg، وما إلى ذلك.|
|كلمة المرور|خيط|كلمة المرور المطلوبة لفتح الملف Excel.|
|isAutoFit|خيط|يُلائم عرض الصفوف والأعمدة تلقائيًا في هذا المصنف. القيمة الافتراضية هي "خطأ".|
|حفظ الجدول فقط|خيط|صواب/خطأ|
|المسار الخارجي|خيط| مسار حفظ النتيجة. إذا كان ملفًا واحدًا، فيجب أن يتضمن الرمز `outPath` اسم الملف وامتداده. أما في حالة وجود ملفات متعددة، فيجب أن يتضمن الرمز `outPath` المجلد فقط.|
|اسم التخزين الخارجي|خيط| اسم التخزين الذي يقع فيه الملف المحفوظ.|
|التحقق من قيود Excel|منطقي| ما إذا كان من الممكن التحقق من تقييد ملف Excel عندما يقوم المستخدم بتعديل الكائنات المرتبطة بالخلايا.|
|منطقة|خيط| الإعدادات الإقليمية للمصنف.|
|ملاءمة الصفحة العريضة لكل ورقة|منطقي| تناسب الصفحة العريضة مع ورقة العمل.|
|طول الصفحة يتناسب مع كل ورقة|منطقي| الصفحة الطويلة تناسب ورقة العمل.|
|صفحة واحدة لكل ورقة|منطقي| عند التحويل إلى تنسيق PDF، صفحة واحدة لكل ورقة.|
|مجلد|خيط|مجلد المصنف الأصلي.|
|اسم التخزين|خيط|اسم التخزين الذي يقع فيه الملف.|

## الباقي API

|**API**|**يكتب**|**وصف**|**رابط سواجر**|
|:- |:- |:- |:- |
|/الخلايا/{الاسم}|يحصل|تصدير المصنف إلى تنسيق آخر.|[احصل على كتاب العمل](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL** أداة سطر أوامر للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
