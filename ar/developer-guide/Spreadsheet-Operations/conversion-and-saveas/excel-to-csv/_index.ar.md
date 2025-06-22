---
title: Excel إلى CS
second_title: Aspose.Cells Cloud Documen
linktitle: Excel إلى CS
type: docs
url: /arconvert-excel-file-to-csv-file/
aliases: [/convert-excel-file-to-csv-in-cloud/,/convert/excel-to-csv/,/convert-excel-file-to-csv-file/]
keywords: Convert excel files to csv files
description: يدعم Cloud REST تحويل ملفات Excel إلى ملفات csv. تدعم مجموعة أدوات تطوير البرامج (SDK) أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 90
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، Excel إلى CSV
---
يشير هذا REST API إلى `convert` ملف جدول بيانات إلى ملف بتنسيق csv.

**معلمة الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|كلمة المرور|خيط| كلمة المرور المطلوبة لفتح الملف Excel.|
|اسم التخزين|خيط| اسم التخزين الذي يوجد فيه الملف.|
|التحقق من قيود Excel|منطقي| ما إذا كان يتم التحقق من تقييد ملف Excel عندما يقوم المستخدم بتعديل الكائنات المرتبطة بالخلايا.|

**معلمة نص الطلب**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|ملف البيانات| ملف البيانات|يتم حفظ ملف البيانات في الجزء الأول من المحتوى المتعدد الأجزاء.|

**إجابة**

[معلومات الملف](/cells/ar/file-info/)

## مواصفات REST API

|**API**|**يكتب**|**وصف**|**رابط سواجر**|
|:- |:- |:- |:- |
|/خلايا/تحويل/csv|بريد|تحويل جدول بيانات إلى ملف csv.|[تحويل مصنف العمل إلى CSV](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV)|

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL** أداة سطر أوامر للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.csv",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPdf.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPdf.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPdf.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPdf.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPdf.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPdf.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPdf.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPdf.go" >}}

{{< /tab >}}

{{< /tabs >}}

## تنفذ واجهات برمجة التطبيقات الأخرى هذه الوظيفة

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)يتيح لك البرنامج API حفظ ملف MS Excel كملف CSV مع إعدادات إضافية وحفظ النتيجة في وحدة التخزين.

هذا الملف REST API `convert` excel إلى CSV.

[ضع /الخلايا/تحويل](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) يتيح لك البرنامج API تحويل ملف MS Excel إلى ملف CSV مع إعدادات إضافية وحفظ النتيجة في الاستجابة.

هذا الملف REST API `export` excel إلى CSV.

[احصل على /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) يتيح لك البرنامج API تحويل ملف MS Excel إلى ملف CSV مع إعدادات إضافية وحفظ النتيجة في الاستجابة.
