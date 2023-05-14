---
title: إضافة عامل تصفية رمز في Excel عمل
second_title: Aspose.Cells Cloud Documen
linktitle: إضافة رمز فيلتي
type: docs
url: /ar/autofilter/add-icon-filter/
aliases: [/add-an-icon-filter/,/autofilter/add-an-icon-filter/]
keywords: Adds an icon filter on an Excel worksheet
description: يدعم Aspose.Cells Cloud API إضافة عامل تصفية رمز في ورقة عمل Excel. يدعم SDK أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 65
---
يشير هذا REST API إلى إضافة `icon filter` على ورقة عمل Excel.

## RSET API

```bash

PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter

```

معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق|اسم المصنف.|
| اسم الورقة| خيط| طريق| اسم ورقة العمل.|
|يتراوح|خيط| استفسار||
|الفهرس الميداني|عدد صحيح| استفسار||
|iconSetType|خيط| استفسار| أسهم 3 / سهام رمادي 3 / أعلام 3 / إشارات 3 / رموز 3 / رموز 32 / إشارات مرور 31 / إشارات مرور 32 / سهام 4 / سهام رمادي 4 / تصنيف 4 / RedToBlack4 / TrafficLights4 / أسهم 5 / سهام رمادي 5 / أرباع 5 / Rating5 / Stars3 / Boxes5 / Triangles3 / None / 3 ColorSet|
|iconId|عدد صحيح| استفسار||
|ماتش بلانكس|خيط| استفسار|خطأ صحيح|
|ينعش|خيط| استفسار|خطأ صحيح|
|مجلد|خيط| استفسار|مجلد المصنف الأصلي.|
|اسم التخزين| استفسار|خيط|اسم التخزين.|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldIndex=0&iconSetType=ArrowsGray3&iconId=1" \
-X PUT \
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


## عائلة Cloud SDK

 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-AddIconFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-AddIconFilterExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-PutWorksheetIconFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-put_worksheet_icon_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-AddIconFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}



{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-AddIconFilterExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-AddIconFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "a05cbd25e102b8369a2ad33d46252a07" >}}

{{< /tab >}}

{{< /tabs >}}
