---
title: تحويل ملف Excel إلى تنسيق مختلف
second_title: Aspose.Cells Cloud Documen
linktitle: تحويل جدول البيانات
type: docs
url: /ar/convert-a-spread-file-to-different-formats/
keywords: Convert excel files to kinds of format files
description: يدعم Cloud REST تحويل ملفات إكسل إلى أنواع مختلفة من صيغ الملفات. تدعم مجموعة أدوات تطوير البرامج (SDK) لغات تطوير مختلفة، بما في ذلك أندرويد، وغو، ونود جي إس، وروبي، وسويفت.
weight: 10
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، تحويل Excel
---
يشير هذا الرمز REST API إلى الملف `convert` والملف Excel بتنسيق مختلف. يدعم هذا الرمز تنسيقات مختلفة، كما يمكنه ضبط إعدادات الصفحة وخيارات الحفظ قبل التحويل.

**معلمة نص الطلب**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|[خيارات تحويل مصنف العمل](/cells/ar/convert-workbook-options/)| هدف| خيارات تحويل المصنف.|

**إجابة**

[معلومات الملف](/cells/ar/file-info/)

## الباقي API

|**API**|**يكتب**|**وصف**|**رابط سواجر**|
|:- |:- |:- |:- |
|/خلايا/تحويل|بريد|تحويل المصنف من محتوى الطلب إلى تنسيق ما|[كتاب عمل PostConvert](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL** أداة سطر أوامر للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "filename",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
