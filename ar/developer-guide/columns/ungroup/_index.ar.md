﻿---
title: قم بفك تجميع الأعمدة في ورقة عمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Ungro
type: docs
url: /ar/columns/ungroup/
aliases: [/ungroup-columns-in-an-excel-worksheet/, /ungroup-columns-in-excel-worksheet/]
keywords: Ungroup column on an Excel workshee
description: Aspose.Cells Cloud REST API يدعم عمود فك التجميع في ورقة عمل Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android وC# وGo وJava وNodeJS وPerl وPHP وPython وRuby وswift.
weight: 70
kwords: Excel، Office Cloud، REST API، جدول البيانات، PDF، CSV، Json، Markdwon، فك تجميع الأعمدة في ورقة عمل Excel
---
يشير REST API إلى فك تجميع أعمدة ورقة العمل.
 
## رسيت API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/ungroup
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم المصنف.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
| firstIndex| عدد صحيح| استفسار| فهرس العمود الأول المراد تشغيله.|
| lastIndex| عدد صحيح| استفسار| فهرس العمود الأخير المراد تشغيله.|
| مجلد| خيط| استفسار| مجلد المستندات.|
| اسم التخزين| خيط| استفسار| اسم التخزين.|


 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetColumns) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

 يمكنك استخدام**cURL**أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/Columns/ungroup?firstIndex=1&lastIndex=5" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

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

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Columns-UngroupColumnsInWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-Columns-UngroupColumnsInWorksheet-ungroup-Columns-in-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Columns-PostUngroupWorksheetColumns-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Columns-ungroup_worksheet_Columns-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "UngroupColumnsInExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Columns-UngroupColumnsInWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-Columns-UngroupColumnsInWorksheet-ungroup-Columns-in-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Columns-UngroupColumnsInWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b9c6984d8f4f6b863a64da0fd68dbd96" >}}

{{< /tab >}}

{{< /tabs >}}
