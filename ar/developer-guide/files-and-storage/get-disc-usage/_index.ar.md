---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – الحصول على استخدام القرص | مقاييس التخزين في الوقت الفعلي"
second_title: "مستند"
ArticleTitle: "حل إدارة ملفات إكسل مبني على السحابة – واجهة لاسترجاع استخدام القرص في السحابة بسرعة."
linktitle: "الحصول على استخدام القرص"
type: docs
url: /ar/get-disk-usage/
keywords: "Aspose Cells, واجهة برمجة تطبيقات سحابية, استخدام القرص, مقاييس التخزين, إكسل, REST"
description: "استرجاع استخدام القرص في الوقت الفعلي لخدمة Aspose.Cells Cloud. تعرّف على نقطة النهاية GET /v4.0/cells/storage/disk، ومصادقة الطلب المطلوبة، ونموذج الاستجابة."
weight: 100
---

تُعيد عملية **الحصول على استخدام القرص** مقاييس تخزين في الوقت الفعلي لحسابك في خدمة Aspose.Cells Cloud. استخدم نقطة النهاية هذه لمراقبة مساحة القرص المستهلكة والمساحة الكلية.

- استرجاع استخدام القرص الحالي لواجهة برمجة تطبيقات إكسل في بيئة Aspose Cloud.
- تمكين المطورين من مراقبة كمية التخزين التي استهلكتها تطبيقاتهم.
- تمكين إدارة احترازية لحدود التخزين والتحكم في التكاليف.

## واجهة برمجة تطبيقات إكسل: GetDiskUsage

### واجهة برمجة التطبيقات عبر الويب

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف                                              | الإلزامية |
| ----------- | ------- | ------ | --------------------------------------------------- | --------- |
| storageName | String  | Query  | اسم وحدة التخزين التي ترغب في استرجاع استخدامها.   | اختياري   |

### **الاستجابة**

```json
{
  "Name": "DiskUsage",
  "Description": ["فئة تحتوي على معلومات مساحة القرص."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["مقدار مساحة القرص المستخدمة من قِبل التطبيق."],
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
      "Description": ["إجمالي مساحة القرص المتاحة."],
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

**رموز حالة HTTP**

| الرمز | المعنى                 | الوصف                                                             |
| ----- | ----------------------- | ------------------------------------------------------------------ |
| 200   | نجاح (OK)              | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.       |
| 400   | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).            |
| 401   | غير مُصادَق (Unauthorized) | رمز JWT غير صالح أو مفقود.                                        |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح.                            |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                         |

## مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) واجهة برمجة تطبيقات متاحة علنًا، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK (حزمة تطوير البرامج) هي أفضل طريقة لتسريع عملية التطوير. فالمكتبات SDK تُدار بالتفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}