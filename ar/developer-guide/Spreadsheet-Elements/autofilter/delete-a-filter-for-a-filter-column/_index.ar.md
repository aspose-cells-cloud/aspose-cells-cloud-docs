﻿---
title: حذف مرشح في ورقة عمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: حذف الفلتر
type: docs
url: /ar/delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/,/delete-auto-filter/]
keywords: Deletes a filter on an Excel worksheet
description: يدعم الإصدار Aspose.Cells Cloud API حذف مُرشِّح من ورقة عمل Excel. تدعم حزمة SDK لغات تطوير متنوعة، منها Android وGo وNodeJS وRuby وSwift.
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، حذف مرشح في ورقة عمل Excel
---
يشير هذا REST API إلى حذف `filter` في ورقة العمل Excel.

## RSET API

```bash

DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter

```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق| اسم المصنف.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
|يتراوح|خيط| استفسار||
|فهرس الحقل|عدد صحيح| استفسار||
|نوع المجموعة الزمنية والتاريخية|خيط| استفسار| اليوم/الساعة/الدقيقة/الشهر/الثانية/السنة|
|سنة|عدد صحيح| استفسار||
|شهر|عدد صحيح| استفسار||
|يوم|عدد صحيح| استفسار||
|ساعة|عدد صحيح| استفسار||
|دقيقة|عدد صحيح| استفسار||
|ثانية|عدد صحيح| استفسار||
|مطابقة الفراغات|خيط| استفسار|صواب/خطأ|
|ينعش|خيط| استفسار|صواب/خطأ|
|مجلد|خيط| استفسار|مجلد المصنف الأصلي.|
|اسم التخزين|خيط| استفسار|اسم التخزين.|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&criteria=Year" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

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

## عائلة SDK السحابية

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل البسيطة وتُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
