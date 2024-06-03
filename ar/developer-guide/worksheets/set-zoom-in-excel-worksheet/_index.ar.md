﻿---
title: اضبط التكبير/التصغير لورقة العمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: حديقة حيوان
type: docs
url: /ar/worksheets/zoom/
aliases: [/set-zoom-in-excel-worksheet/]
keywords: Set zoom for an Excel worksheet
description: Aspose.Cells Cloud REST API يدعم إعداد التكبير لورقة العمل Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 20
kwords: Excel، Office كلاود، ريست API، جدول بيانات، PDF، CSV، Json، Markdwon، ضبط التكبير لورقة عمل Excel
---
يشير REST API إلى `set the zoom value of Excel worksheet`.
 
## رسيت API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/zoom
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق||
| اسم الورقة| خيط| طريق||
| قيمة| عدد صحيح| استفسار||
| مجلد| خيط| استفسار||
| اسم التخزين| خيط| استفسار| اسم التخزين.|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetZoom) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/zoom?value=40" \
-X POST \
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
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:
 

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}

{{< /tab >}}

{{< /tabs >}}
