﻿---
title: إضافة مرشح تاريخ ديناميكي في ورقة عمل Excel
second_title: Aspose.Cells Cloud Documen
linktitle: إضافة مرشح ديناميكي
type: docs
url: /ar/autofilter/add-dynamic-filter/
aliases: [/filter-a-list-using-dynamic-filter/,/autofilter/add-a-dynamic-filter/]
keywords: Adds a dynamic filter on an Excel worksheet
description: يدعم الإصدار Aspose.Cells Cloud API إضافة مرشح ديناميكي إلى ورقة عمل Excel. تدعم مجموعة أدوات تطوير البرامج (SDK) أنواعًا مختلفة من لغات التطوير، بما في ذلك Android وGo وNodeJS وRuby وSwift.
weight: 65
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، إضافة مرشح تاريخ ديناميكي في ورقة عمل Excel
---
يشير هذا REST API إلى إضافة `dynamic filter` إلى ورقة عمل Excel.

## RSET API

```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dynamicFilter
 
```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق||
| اسم الورقة| خيط| طريق||
| يتراوح| خيط| استفسار||
| فهرس الحقل| عدد صحيح| استفسار||
| نوع المرشح الديناميكي| خيط| استفسار||
| مطابقة الفراغات| منطقي| استفسار||
| ينعش| منطقي| استفسار||
| مجلد| خيط| استفسار||
| اسم التخزين| خيط| استفسار| اسم التخزين.|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDynamicFilter) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dynamicFilter?range=A1:B1&fieldIndex=0&dynamicFilterType=BelowAverage&matchBlanks=true"  \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDynamicFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDynamicFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDynamicFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDynamicFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDynamicFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDynamicFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDynamicFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDynamicFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
