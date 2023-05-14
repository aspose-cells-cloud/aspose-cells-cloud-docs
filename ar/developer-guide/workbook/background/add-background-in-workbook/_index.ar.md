---
title: أضف الخلفية في Workboo
second_title: Aspose.Cells Cloud Documen
linktitle: إعلان
type: docs
url: /ar/workbook/background/add/
aliases: [/add-background-in-workbook/,/workbook/add-background/]
keywords: Add background on an Excel workbook
description: Aspose.Cells Cloud REST API دعم إضافة خلفية على مصنف Excel في ملف Excel. SDK يدعم أنواع لغات التطوير. وهي تشمل Android و C# و Go و Java و NodeJS و Perl و PHP و Python و Ruby و swift
weight: 160
---
يشير هذا REST API إلى إضافة `background` على مصنف Excel.


**معامِل الاستعلام**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|picPath|خيط|موقف الصورة.|
|مجلد|خيط|مجلد المصنف الأصلي.|
|اسم التخزين|خيط|اسم التخزين.|

**طلب معلمة الجسم**

|اسم المعلمة|يكتب|وصف|
|:- |:- |:- |
|ملف البيانات| ملف البيانات|يتم حفظ ملف البيانات في نص الطلب.|

## REST API

|**API**|**يكتب**|**وصف**|**رابط الموارد**|
|:- |:- |:- |:- |
|/ الخلايا / {name} / الخلفية|يضع|إضافة خلفية في ملف اكسل|[PutWorkbookBackground](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground)|

 ال[مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك إجراء تفاعلات REST مباشرة من مستعرض ويب.

 يمكنك استخدام**cURL** أداة سطر الأوامر للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

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

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Android" tabName5="Perl" tabName6="Ruby" tabName7="PHP" tabName8="Node.js" tabName9="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "4f5e06ec874b8b698dfa0e5359c85f96" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "b47350fc841e7c7e8889b1f57723ad94" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "bef09b36e0e7b769022bd810898dbd73" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "a984b922e2a7373755fb877e8754452b" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "7b9fa1a76c49c164d034342a2a59d4e0" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "a56d3fa3fff9c61191ee3e869ec51cdd" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "4a63cab36bb9f03e4e58bc30267b60b8" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "4009896954c23f8a1394b3757a30ee9d" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d3b449b5e5e2cdbb25da9e8de37bdccc" >}}

{{< /tab >}}

{{< /tabs >}}
