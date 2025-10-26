---
title: تحويل ملف Excel إلى تنسيق مختلف
second_title: Documen
linktitle: تحويل Excel
type: docs
url: /ar/convert-an-excel-file-to-different-formats/
aliases: [/convert-excel-workbook-to-different-file-formats/,/convert/excel-to-different-formats/]
keywords: Convert excel files to kinds of format files
description: يدعم Cloud REST تحويل ملفات إكسل إلى أنواع مختلفة من صيغ الملفات. تدعم مجموعة أدوات تطوير البرامج (SDK) لغات تطوير مختلفة، بما في ذلك أندرويد، وغو، ونود جي إس، وروبي، وسويفت.
weight: 10
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، تحويل Excel
---
يشير هذا REST API إلى ملف Excel `convert` بتنسيق ملف مختلف.

الطلب عبارة عن طلب HTTP يحتوي على محتوى متعدد الأجزاء (انظر[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)أو[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)يحتوي الجزء الأول من المحتوى المتعدد الأجزاء على ملف البيانات، ويحتوي الجزء الثاني على خيارات الحفظ.

**معلمة الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|شكل|خيط| تنسيق الملف: csv، xls، html، mhtml، ods، pdf، xml، txt، tiff، xlsb، xlsm، xlsx، xltm، xltx، xps، png، jpg، gif، emf، bmp، md، Numbers، wmf، svg، وما إلى ذلك.|
|كلمة المرور|خيط| كلمة المرور المطلوبة لفتح الملف Excel.|
|المسار الخارجي|خيط| مسار حفظ النتيجة. إذا كان ملفًا واحدًا، فيجب أن يتضمن الرمز `outPath` اسم الملف وامتداده. أما في حالة وجود ملفات متعددة، فيجب أن يتضمن الرمز `outPath` المجلد فقط.|
|اسم التخزين|خيط| اسم التخزين الذي يقع فيه الملف.|
|التحقق من قيود Excel|منطقي| ما إذا كان من الممكن التحقق من تقييد ملف Excel عندما يقوم المستخدم بتعديل الكائنات المرتبطة بالخلايا.|
|تنسيق التدفق|خيط| تنسيق تدفق ملف الإدخال.|
|منطقة|خيط| الإعدادات الإقليمية للمصنف.|
|ملاءمة الصفحة العريضة لكل ورقة|منطقي| تناسب الصفحة العريضة مع ورقة العمل.|
|طول الصفحة يتناسب مع كل ورقة|منطقي| الصفحة الطويلة تناسب ورقة العمل.|
|اسم الورقة|خيط| تحويل ورقة العمل المحددة.|
|فهرس الصفحة|خيط| تحويل الصفحة المحددة من ورقة العمل، مطلوب sheetName.|
|صفحة واحدة لكل ورقة|منطقي| عند التحويل إلى تنسيق PDF، صفحة واحدة لكل ورقة.|
|صفوف تلقائية|منطقي| يتناسب تلقائيًا مع جميع الصفوف في هذا المصنف.|
|ملاءمة الأعمدة التلقائية|منطقي| يتناسب عرض الأعمدة في هذا المصنف تلقائيًا.|

**معلمة نص الطلب**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|ملف البيانات| ملف البيانات|يتم حفظ ملف البيانات في الجزء الأول من المحتوى المتعدد الأجزاء.|
|حفظ الخيارات| هدف|خيار الحفظ حفظ في الجزء الثاني من المحتوى المتعدد الأجزاء.|

## الباقي API

|**API**|**يكتب**|**وصف**|**رابط سواجر**|
|:- |:- |:- |:- |
|/خلايا/تحويل|يضع|تحويل المصنف من محتوى الطلب إلى تنسيق ما|[ضع كتاب العمل المحول](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL** أداة سطر أوامر للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

{{< /tab >}}

{{< /tabs >}}

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
