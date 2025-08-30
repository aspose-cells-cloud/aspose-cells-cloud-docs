---
title: حفظ باسم إكسل
second_title: Aspose.Cells Cloud Documen
linktitle: احفظ
type: docs
url: /ar/save-an-excel-file-as-other-formats-files/
aliases: [/convert-excel-workbook-to-different-file-formats/, /saveas-other-formats/]
keywords: Save excel files as kinds of format files
description: يدعم Cloud REST حفظ ملفات Excel بصيغ مختلفة. تدعم مجموعة أدوات تطوير البرامج (SDK) لغات تطوير مختلفة، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 30
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، حفظ باسم Excel
---
يشير هذا REST API إلى ملف Excel `save` كملف بتنسيق مختلف.

**معلمة المسار**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|اسم|خيط| اسم الملف.|

**معلمة الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|اسم الملف الجديد|خيط| اسم الملف الجديد|
|isAutoFitRows|خيط| يُلائم جميع الصفوف في هذا المصنف تلقائيًا. القيمة الافتراضية هي خطأ.|
|isAutoFitColumns|خيط| يُلائم عرض الأعمدة في هذا المصنف تلقائيًا. القيمة الافتراضية هي "خطأ".|
|مجلد|خيط|مجلد المصنف الأصلي.|
|اسم التخزين|خيط| اسم التخزين الذي يقع فيه الملف.|
|اسم التخزين الخارجي|خيط| اسم التخزين الذي يقع فيه الملف المحفوظ.|
|التحقق من قيود Excel|منطقي| ما إذا كان من الممكن التحقق من تقييد ملف Excel عندما يقوم المستخدم بتعديل الكائنات المرتبطة بالخلايا.|
|منطقة|خيط| الإعدادات الإقليمية للمصنف.|
|ملاءمة الصفحة العريضة لكل ورقة|منطقي| تناسب الصفحة العريضة مع ورقة العمل.|
|طول الصفحة يتناسب مع كل ورقة|منطقي| الصفحة الطويلة تناسب ورقة العمل.|
|اسم الورقة|خيط| تحويل ورقة العمل المحددة.|
|فهرس الصفحة|خيط| تحويل الصفحة المحددة من ورقة العمل، مطلوب sheetName.|
|صفحة واحدة لكل ورقة|منطقي| عند التحويل إلى تنسيق PDF، صفحة واحدة لكل ورقة.|

**معلمة نص الطلب**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|حفظ الخيارات| هدف|خيار الحفظ حفظ في الجزء الثاني من المحتوى المتعدد الأجزاء.|

## الباقي API

|**API**|**يكتب**|**وصف**|**رابط المورد**|
|:- |:- |:- |:- |
|/الخلايا/{الاسم}/حفظ باسم|بريد|تصدير المصنف إلى التنسيق|[حفظ المستند باسم](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL** أداة سطر أوامر للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" -H "accept: multipart/form-data" 

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
  "SaveResult": {
    "SourceDocument": {
      "Href": "test.xlsx",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "DestDocument": {
      "Href": "test.pdf",
      "Rel": null,
      "Title": null,
      "Type": null
    },
    "AdditionalItems": []
  },
  "Code": 200,
  "Status": "OK"
}

```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}
