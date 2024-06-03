---
title:  كائن القائمة يزيل التكرارات
second_title: Aspose.Cells Cloud Documen
linktitle: إزالة التكرارات
type: docs
keywords: list object(table) remove duplicates 
url: /ar/list-objects/remove-duplicates/
description:  إزالة التكرارات في كائن القائمة.
weight: 20
kwords: Excel، Office Cloud، REST API، جدول البيانات، PDF، CSV، Json، Markdwon، كائن القائمة إزالة التكرارات
---
 يشير REST API إلى إزالة التكرارات في كائن القائمة.

## رسيت API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates

```

 معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody| وصف|
|:- |:- |:- |:- |
|اسم|خيط|طريق||
|اسم الورقة|خيط|طريق||
|listObjectIndex|عدد صحيح|طريق||
|مجلد|خيط|استفسار||
|اسم التخزين|خيط|استفسار||



 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectRemoveDuplicates) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## عائلة Cloud SDK

يعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. تهتم حزمة SDK بالتفاصيل ذات المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يرجى مراجعة مستودع GitHub للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج (SDK) المتنوعة:
