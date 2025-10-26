---
title: Aspose.Cells Cloud WEb API - احصل على المفتاح العام
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: احصل على Ke العامة
type: docs
url: /ar/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: استرداد مفتاح عام غير متماثل لتشفير البيانات بشكل آمن
weight: 100
kwords: التشفير غير المتماثل، المفتاح العام، REST API، Excel API، الأمان، تشفير البيانات، تكامل API، JSON، توثيق API
---
يسترجع المفتاح العام من خوارزمية التشفير غير المتماثلة.

## **احصل على المفتاح العام API**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|||||

### **إجابة**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

## كيفية استخدام الحصول على المفتاح العام API مع مجموعات تطوير البرامج (SDKs)

### مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب الخاص بك.

### استخدم Aspose.Cells Cloud SDKs

يُعد استخدام حزمة تطوير البرامج (SDK) أفضل طريقة لتسريع عملية التطوير. فهي تُعنى بالتفاصيل الأساسية، مما يسمح لك بتطبيق الحصول على المفتاح العام للخلايا بسهولة وبأقل قدر من التعليمات البرمجية.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية التفاعل مع خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:
