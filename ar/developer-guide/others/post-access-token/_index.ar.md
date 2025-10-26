---
title: Aspose.Cells Cloud Web API - Post Access Toke
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: مفتاح الوصول بعد النشر
type: docs
url: /ar/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: استرداد رمز الوصول باستخدام الرمز Cells Cloud Get Token API، الذي يعمل كخدمة وكيل لإعادة توجيه طلبات المستخدم إلى خادم المصادقة السحابي Aspose، ويعيد رمز الوصول الناتج إلى العميل بشكل آمن
weight: 100
kwords: Excel، Office السحابة، REST API، المصادقة، إدارة الرمز، تكامل البرامج الوسيطة، السحابة الآمنة API، Aspose
---
استرداد رمز الوصول باستخدام الرمز Cells Cloud Get Token API مع معرف العميل والسر.

## **رمز وصول البريد API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
| معرف العميل| خيط| استفسار| معرف العميل|
| سر العميل| خيط| استفسار| سر العميل|

### **إجابة**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## كيفية استخدام الحصول على المفتاح العام API مع مجموعات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يسمح لك بتطبيق رمز الوصول للخلايا بسهولة وبأقل قدر من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بمجموعات SDK السحابية Aspose.Cells. تهتم مجموعة SDK بالتفاصيل البسيطة وتتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:
