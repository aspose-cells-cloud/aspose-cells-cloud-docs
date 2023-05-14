---
title: احذف فاصل الصفحة الأفقي
second_title: Aspose.Cells Cloud Documen
linktitle: احذف فاصل الصفحة الأفقي
type: docs
url: /ar/page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: Delete a page break in an Excel worksheet
description: Aspose.Cells Cloud REST API يدعم حذف فاصل صفحة في ورقة عمل Excel. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 50
---
 يشير هذا REST API إلى حذف فاصل صفحة `horizontal`.
 
## RSET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
 
```
 معلمات الطلب هي:
 
| اسم المعلمة| يكتب| المسار / سلسلة الاستعلام / HTTPBody|وصف|
|:- |:- |:- |:- |
| اسم| خيط| طريق||
| اسم الورقة| خيط| طريق||
| فِهرِس| عدد صحيح| طريق||
| مجلد| خيط| استفسار||
| اسم التخزين| خيط| استفسار| اسم التخزين.|
 
 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.
 
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
-X DELETE \
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
 
 يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يرجى التحقق من[مستودع جيثب](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة من Aspose.Cells Cloud SDKs.
 
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام حزم SDK متنوعة:


{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="Go" tabName3="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "16a442c2c2fb97afac8bd89fbbdca563" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "8ec70b4733866d10eae5e5e8c687d3ca" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "0a767f9030525d7f9be51bf9c6342b7d" >}}

{{< /tab >}}

{{< /tabs >}}
