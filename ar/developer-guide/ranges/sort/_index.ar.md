﻿---
title:  فرز النطاق
second_title: Aspose.Cells Cloud Documen
linktitle: سور
type: docs
keywords: Range Sort
url: /ar/ranges/sort/
description:  يعين حدودًا تفصيلية حول نطاق من الخلايا.
weight: 20
kwords: Excel، Office كلاود، ريست API، جدول بيانات، PDF، CSV، Json، Markdwon، فرز النطاق
---
 يشير REST API إلى نوع النطاق.

## رسيت API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

 معلمات الطلب هي:

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/HTTPBody| وصف|
|:- |:- |:- |:- |
|اسم|خيط|طريق|اسم المصنف.|
|اسم الورقة|خيط|طريق|اسم ورقة العمل.|
|rangeOperate|فصل|جسم| طلب فرز النطاق|
|مجلد|خيط|استفسار|مجلد المصنف الأصلي.|
|اسم التخزين|خيط|استفسار|اسم التخزين.|



 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى Cloud API مع cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
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

