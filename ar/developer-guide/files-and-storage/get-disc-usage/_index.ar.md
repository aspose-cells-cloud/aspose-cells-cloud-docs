---
title: الحصول على استخدام القرص
second_title: Documen
linktitle: الحصول على استخدام القرص
type: docs
url: /ar/get-disk-usage/
keywords: API, Disk Usage, Aspose, Cloud, Excel, REST, Storage, Disc Space, SDK, Programming Interfac
description: استرداد استخدام القرص الحالي لـ Excel API في Aspose Cloud
weight: 100
kwords: استخدام القرص، Excel API، Aspose السحابة، REST API، معلومات التخزين، أمثلة SDK، واجهة البرمجة
---
## **Excel API : GetDiskUsage**

```
GET http://api.aspose.cloud/v4.0/cells/storage/disk
```

### **وصف الوظيفة**

تسترد نقطة النهاية API هذه استخدام القرص الحالي لـ Excel API في بيئة السحابة Aspose، مما يسمح للمطورين بمراقبة مساحة التخزين التي تستخدمها تطبيقاتهم.

###  معلمات الطلب**الحصول على استخدام القرص** API هم

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|اسم التخزين|خيط|استفسار|اسم وحدة التخزين التي سيتم استرداد استخدام القرص لها.|

### **وصف الاستجابة**

```json
{
  "Name": "DiskUsage",
  "Description": [
    "Class for disk space information."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": [
        "Amount of disk space used by the application."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": [
        "Total available disk space."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

## مواصفات OpenAPI

 ال[مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

## Excel API مجموعة تطوير البرامج

 يُعد استخدام حزمة تطوير برمجيات (SDK) أفضل طريقة لتسريع عملية التطوير. تُعالج حزمة تطوير البرمجيات (SDK) التفاصيل البسيطة، مما يُتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{< /tab >}}
{{< /tabs >}}
