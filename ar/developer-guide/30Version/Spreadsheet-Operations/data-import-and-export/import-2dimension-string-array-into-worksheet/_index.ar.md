---
title: "استيراد مصفوفة سلاسل ثنائية الأبعاد إلى ورقة عمل Excel"
second_title: "مستند"
linktitle: "استيراد مصفوفة سلاسل ثنائية الأبعاد"
type: docs
url: /ar/import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-string-array-into-excel-worksheet/,
    /import-2dimension-string-array-into-worksheet/,
    /import-data/-2dimension-string-array/,
    /import-data/2dimension-string-array/,
    /import/2dimension-string-array/,
  ]
keywords: "Aspose.Cells Cloud، استيراد مصفوفة سلاسل ثنائية الأبعاد، Excel، REST API، SDK"
description: "تعرّف على كيفية استخدام واجهة Aspose.Cells Cloud REST API لاستيراد مصفوفة سلاسل ثنائية الأبعاد إلى ورقة عمل Excel. يشمل تنسيق الطلب، تفاصيل المعاملات، وأمثلة للكود باستخدام SDKs بلغات C# و PHP و Ruby."
weight: 20
---

تقوم هذه الواجهة **REST API باستيراد مصفوفة سلاسل ثنائية الأبعاد** إلى ورقة عمل Excel.

يُشكّل الطلب طلب HTTP يحتوي على محتوى متعدد الأجزاء (انظر [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). يحتوي الجزء الأول من المحتوى متعدد الأجزاء على بيانات `Import2DimensionStringArrayOption`، ويحتوي الجزء الثاني على ملف البيانات.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

يُوضّح الجدول التالي المعاملات المهمة:

### **Import2DimensionStringArrayOption**

| اسم المعاملة          | النوع               | الوصف                                                                          |
| --------------------- | ------------------- | ------------------------------------------------------------------------------ |
| FirstRow             | int                 | الفهرس الصفري للصف الذي يبدأ منه الاستيراد.                                   |
| FirstColumn          | int                 | الفهرس الصفري للعمود الذي يبدأ منه الاستيراد.                                 |
| Data                 | String[,]           | مصفوفة ثنائية الأبعاد تحتوي على قيم السلاسل المراد استيرادها.                 |
| DestinationWorksheet | string              | اسم ورقة العمل التي ستتلقّى البيانات المستوردة.                               |
| IsInsert             | string (true/false) | إذا كانت القيمة **true**، تُدرج البيانات وتُزاحَم الخلايا الموجودة وفقًا لذلك. |
| ImportDataType       | string              | يحدّد نوع البيانات؛ لاستخدام هذه العملية، اضبط القيمة على `TwoDimensionStringArray`. |
| Source               | FileSource          | يشير إلى موقع ملف البيانات عند كون المعاملة `BatchData` تساوي null.           |

### مثال على جسم الطلب

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
}
```

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                         |
|-------|-----------------------------|---------------------------------------------------------------|
| 200   | OK (تمت العملية بنجاح)     | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.   |
| 400   | Bad Request (طلب غير صالح) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).         |
| 401   | Unauthorized (غير مصادَق)   | رمز JWT غير صالح أو مفقود.                                   |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح.            |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقّع في الخادم.                              |

## كيفية استخدام PostImportData API باستخدام SDKs

### مواصفات PostImportData API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) واجهة برمجة تطبيقات عامة قابلة للاستدعاء مباشرةً من متصفح الويب.

### استخدام SDKs لـ Aspose.Cells Cloud

يُعدّ استخدام SDK أسرع طريقة لدمج هذه الوظيفة. فتُجَسّد SDKs التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على منطق أعمالك. يمكنك الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهِر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}