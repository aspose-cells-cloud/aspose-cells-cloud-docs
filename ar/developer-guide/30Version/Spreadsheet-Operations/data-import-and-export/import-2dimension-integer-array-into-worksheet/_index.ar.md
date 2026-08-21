---
title: "استيراد مصفوفة صحيحة ثنائية الأبعاد إلى ورقة عمل Excel"
second_title: "مستند"
linktype: "استيراد مصفوفة صحيحة ثنائية الأبعاد"
type: docs
url: /ar/import-a-2D-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, استيراد مصفوفة صحيحة ثنائية الأبعاد, ورقة عمل Excel, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "يتيح لك واجهة برمجة تطبيقات Aspose.Cells Cloud REST استيراد مصفوفات صحيحة ثنائية الأبعاد إلى ورقات عمل Excel. توفر SDKs دعمًا لـ Android وC# وGo وJava وNode.js وPerl وPHP وPython وRuby وSwift."
weight: 20
---

تقوم هذه الواجهة البرمجية **باستيراد مصفوفة صحيحة ثنائية الأبعاد** إلى ورقة عمل Excel.

الطلب هو طلب HTTP يحتوي على محتوى متعدد الأجزاء (انظر [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). الجزء الأول من المحتوى المتعدد الأجزاء يحتوي على بيانات `Import2DimensionIntegerArrayOption` والجزء الثاني يحتوي على ملف البيانات.

البارامترات الأساسية موضحة في الجدول التالي:

## واجهة برمجة التطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **Import2DimensionIntegerArrayOption**

| اسم البارامتر       | النوع       | الوصف                                                                                                                                                                                  |
| -------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | المؤشر (1-الأساس) للصف الأول الذي سيتم وضع البيانات فيه.                                                                                                                            |
| FirstColumn          | int        | المؤشر (1-الأساس) للعمود الأول الذي سيتم وضع البيانات فيه.                                                                                                                         |
| Data                 | Integer[,] | مصفوفة صحيحة ثنائية الأبعاد تحتوي على القيم المراد استيرادها.                                                                                                                               |
| DestinationWorksheet | string     | اسم ورقة العمل الوجهة.                                                                                                                                                           |
| IsInsert             | string     | `"true"` لإدراج البيانات (بتحريك الخلايا الموجودة)، `"false"` لكتابة البيانات فوق الخلايا الموجودة.                                                                                                |
| ImportDataType       | string     | يُحدد تنسيق البيانات. القيم المدعومة: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| Source               | FileSource | يُشير إلى موقع ملف البيانات عندما تكون قيمة البارامتر `BatchData` `null`.                                                                                                                   |

### **مثال**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
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

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | نجاح (OK)                          | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | بارامترات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصادق عليه (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large)           | حجم ملف المرفقات يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |
## كيفية استخدام واجهة PostImportData API باستخدام SDKs

### مواصفات واجهة PostImportData API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) واجهة برمجة تطبيقات متاحة للعامة تسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud


يعتبر استخدام SDK أفضل طريقة لتسريع عملية التطوير. تتعامل SDKs مع التفاصيل منخفضة المستوى وتركّز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}