---
title: SaveAs Exce
second_title: Aspose.Cells Cloud Documen
linktitle: حفظ
type: docs
url: /ar/saveas-other-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/]
keywords: Save excel files as kinds of format files
description: Aspose.Cells Cloud REST API يدعم حفظ ملفات Excel كأنواع من ملفات التنسيق. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 30
---
يشير هذا REST API إلى `save` ملف excel كملف تنسيق مختلف.

**معامِل الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|اسم جديد|خيط| اسم ملف جديد|
|isAutoFitRows|خيط| خطأ صحيح|
|isAutoFitColumns|خيط| خطأ صحيح|
|مجلد|خيط|مجلد المصنف الأصلي.|
|اسم التخزين|خيط|اسم التخزين.|


## REST API

|**API**|**يكتب**|**وصف**|**رابط الموارد**|
|:- |:- |:- |:- |
|/ الخلايا / {name} / saveAs|بريد|تصدير المصنف إلى تنسيق|[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.

 يمكنك استخدام**cURL** أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.

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

## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:



{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Workbook-ConvertToAnotherFormat-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-ConvertWorkbookToAnotherFormat-convert-workbook-to-different-format.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostDocumentSaveAs-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_document_save_as-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-ConvertToAnotherFormat-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ConvertExcelToVariousFormats.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-ConvertWorkbookToAnotherFormat-convert-workbook-to-different-format.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-ConvertToAnotherFormat-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "ed591112b4a0b4146da679a5b396d577" >}}

{{< /tab >}}

{{< /tabs >}}
