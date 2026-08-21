---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud للحصول على إصدارات الملف – استرجاع سريع لتاريخ إصدارات الملف"
second title: "مستند"
ArticleTitle: "إدارة إكسل عبر السحابة – استرجاع سريع لتاريخ إصدارات الملف في Aspose.Cells Cloud"
linktitle: "الحصول على إصدارات الملف"
type: docs
url: /ar/get-file-versions/
keywords: "واجهة برمجة تطبيقات Aspose Cells، إصدارات الملفات، إصدار جداول البيانات، واجهة برمجة تطبيقات التخزين السحابي، REST، تاريخ ملف إكسل"
description: "احصل على قائمة كاملة بتاريخ الإصدارات لأي ملف إكسل مخزن في Aspose.Cells Cloud. تدعم تحديد مساحة التخزين، المصادقة، وأكواد الأخطاء التفصيلية."
weight: 100
---

احصل على قائمة كاملة بسجلات الإصدارات لجدول بيانات محدد مخزن في Aspose.Cells Cloud. تتيح هذه النقطة النهائية للمطورين تتبع التغييرات، ومراجعة التعديلات، وتطبيق سير عمل التحكم في الإصدارات مباشرةً من مساحة التخزين السحابية.

تُعيد واجهة برمجة التطبيقات **GetFileVersions** جميع سجلات الإصدارات لجدول البيانات المحدد المخزن في Aspose.Cells Cloud. تساعدك هذه الميزة على الاحتفاظ بتاريخ تغييرات كامل لكل ملف.

## **واجهة برمجة تطبيقات إكسل: الحصول على إصدارات الملف**

### واجهة برمجة التطبيقات عبر الويب

```
GET https://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### معاملات الطلب لواجهة برمجة التطبيقات **GetFileVersions** هي:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| `path` | نص | المسار | **إجباري.** المسار الكامل للملف الذي يتم استرجاع إصداراته. |
| `storageName` | نص | الاستعلام | اختياري. اسم مساحة التخزين التي يحتوي عليها الملف. وفي حال تجاهله، تُستخدم مساحة التخزين الافتراضية. |

### **الاستجابة**

```json
{
  "Name": "FileVersions",
  "Description": [
    "تحتوي على قائمة بإصدارات الملفات للمستند المحدد."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": ["مجموعة من تفاصيل إصدار الملف."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

عند النجاح، تُعيد واجهة برمجة التطبيقات **HTTP 200 OK** مع حمولة JSON تحتوي على المصفوفة `Value` لكائنات إصدارات الملفات، كما هو موضح أعلاه.

**أكواد حالة HTTP**

| الكود | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح | تمت تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرّح به | رمز JWT غير صالح أو مفقود. |
| 413 | حملة كبيرة جدًا | يتجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## مواصفات OpenAPI

تُوفر [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions) واجهة برمجة تطبيقات برمجية شاملة لتنفيذ تفاعلات REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/version/MyFolder/MyFile.xlsx" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Value": [
    {
      "VersionId": "1",
      "IsLatest": false,
      "ModifiedDate": "2024-01-15T12:34:56Z",
      "Size": 10240
    },
    {
      "VersionId": "2",
      "IsLatest": true,
      "ModifiedDate": "2024-03-01T08:22:10Z",
      "Size": 10300
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK يُبسّط عملية التطوير من خلال تجريد التعقيدات من المستوى المنخفض، مما يسمح للمطورين بالتركيز على الوظائف الأساسية. استكشف [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية التفاعل مع خدمات الويب الخاصة بـ Aspose.Cells عبر لغات برمجة متعددة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{</tab>}}
{{< /tabs >}}