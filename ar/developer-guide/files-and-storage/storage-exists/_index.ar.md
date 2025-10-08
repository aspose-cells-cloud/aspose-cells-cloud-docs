---
title: التخزين موجود
second_title: Documen
linktitle: التخزين موجود
type: docs
url: /ar/storage-exists/
keywords: Excel API, Storage Exists, REST API, Office Cloud, Cloud Storage, Excel Worksheet, Check Storage, Data Management, API Integratio
description: تعرف على كيفية التحقق من وجود مساحة تخزين باستخدام Aspose.Cells REST API. يوفر هذا الدليل معلومات مفصلة عن نقطة النهاية API ومعلمات الطلب وأوصاف الاستجابة
weight: 100
kwords: Excel، Office Cloud، REST API، جدول بيانات، PDF، CSV، JSON، Markdown، مطابقة جميع الخلايا الفارغة في ورقة عمل Excel
---
## **Excel API : التخزين موجود**

```
GET http://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **وصف الوظيفة**

 ال**التخزين موجود**يتحقق API من وجود وحدة تخزين محددة في خدمة السحابة Aspose.Cells. هذه الوظيفة ضرورية لضمان سير جميع العمليات التي تعتمد على وحدة التخزين دون أخطاء.

###  معلمات الطلب**التخزين موجود** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|اسم التخزين|خيط|طريق|اسم التخزين الذي يجب التحقق من وجوده.|

### **وصف الاستجابة**

```json
{
  "Name": "StorageExist",
  "Description": [
    "Indicates whether the specified storage exists."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/StorageExists) يعرف واجهة برمجة يمكن الوصول إليها بشكل عام، مما يسمح للمطورين بالتفاعل بسلاسة مع REST API مباشرة من متصفح الويب.

## Excel API مجموعة تطوير البرامج

 يُعد استخدام حزمة تطوير برمجيات (SDK) الطريقة الأكثر فعالية لتسريع عملية التطوير. تُلخص حزمة تطوير البرمجيات تفاصيل التنفيذ البسيطة، مما يُمكّن المطورين من التركيز على مهام مشاريعهم. للاطلاع على قائمة شاملة بحزم تطوير البرمجيات السحابية Aspose.Cells المتاحة، يُرجى زيارة[مستودع GitHub](https://github.com/aspose-cells-cloud).

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات API إلى خدمات الويب Aspose.Cells باستخدام مجموعات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
