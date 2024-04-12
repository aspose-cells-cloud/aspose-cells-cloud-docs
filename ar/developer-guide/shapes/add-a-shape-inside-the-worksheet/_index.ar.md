---
title: إضافة شكل على ورقة عمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: إعلان
type: docs
url: /ar/shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: Add shape on an Excel workshee
description: Aspose.Cells Cloud REST API يدعم إضافة الشكل في ورقة عمل Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 30
---
يشير REST API إلى إضافة شكل في ورقة عمل Excel.
 
## رسيت API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم الملف.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| com.shapeDTO|| جسم||
| drawType| خيط| استفسار| نوع كائن الشكل|
| UpperLeftRow| عدد صحيح| استفسار| مؤشر الصف العلوي الأيسر.|
| UpperLeftColumn| عدد صحيح| استفسار| فهرس العمود الأيسر العلوي.|
| قمة| عدد صحيح| استفسار| يمثل الإزاحة الرأسية لـ Spinner من الصف الأيسر بوحدة البكسل.|
| غادر| عدد صحيح| استفسار| يمثل الإزاحة الأفقية لـ Spinner من العمود الأيسر بوحدة البكسل.|
| عرض| عدد صحيح| استفسار| يمثل ارتفاع Spinner بوحدة البكسل.|
| ارتفاع| عدد صحيح| استفسار| يمثل عرض Spinner بوحدة البكسل.|
| مجلد| خيط| استفسار| مجلد الوثيقة.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## عائلة Cloud SDK
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى الاطلاع على[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:
 
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-PutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "34f478cae8c02848db0e376bd592a087" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-PutWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}
