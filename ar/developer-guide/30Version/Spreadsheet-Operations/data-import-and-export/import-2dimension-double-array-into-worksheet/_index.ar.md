---
title: "استيراد مصفوفة ثنائية الأبعاد من نوع double إلى ورقة عمل Excel"
second_title: "مستند"
linktype: "استيراد مصفوفة ثنائية الأبعاد من نوع double"
type: docs
url: /ar/import-a-2d-double-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-double-array-into-excel-worksheet/,
    /import-2dimension-double-array-into-worksheet/,
    /import-data/2dimension-double-array/,
    /import/2dimension-double-array/,
  ]
keywords: "استيراد مصفوفة ثنائية الأبعاد من نوع double، Excel، Aspose Cells Cloud، واجهة برمجة تطبيقات REST، جدول بيانات، استيراد البيانات"
description: "تعلم كيفية استيراد مصفوفة ثنائية الأبعاد من نوع double إلى ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يشمل تنسيق الطلب، المعاملات، وأكواد الأمثلة باستخدام SDKs."
weight: 20
---

تقوم هذه الواجهة **REST API باستيراد مصفوفة ثنائية الأبعاد من نوع double** إلى ورقة عمل Excel.

يكون الطلب باستخدام بروتوكول HTTP `POST` مع محتوى متعدد الأجزاء (انظر [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). الجزء الأول من جسم الطلب المتعدد يحتوي على بيانات **Import2DimensionDoubleArrayOption**، والجزء الثاني يحتوي على ملف البيانات المصدر.

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

يتم شرح المعاملات المهمة في الجدول التالي:

### Import2DimensionDoubleArrayOption

| اسم المعامل             | النوع         | الوصف                                                                                                             |
| ------------------------ | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | `int`        | فهرس الصف (مبني على 1) الذي يبدأ فيه الاستيراد.                                                                            |
| **FirstColumn**          | `int`        | فهرس العمود (مبني على 1) الذي يبدأ فيه الاستيراد.                                                                         |
| **Data**                 | `Double[,]`  | مصفوفة ثنائية الأبعاد من القيم العائمة (double) المراد استيرادها.                                                                  |
| **DestinationWorksheet** | `string`     | اسم ورقة العمل التي ستستقبل البيانات.                                                                       |
| **IsInsert**             | `string`     | `"true"` لإدراج صفوف جديدة، `"false"` للكتابة فوق الخلايا الموجودة.                                                         |
| **ImportDataType**       | `string`     | نوع البيانات المراد استيرادها (مثل `IntArray`، `DoubleArray`، `TwoDimensionDoubleArray`، `BatchData`، `csvData`، إلخ). |
| **Source**               | `FileSource` | يحدد موقع ملف البيانات عندما تكون قيمة المعامل `BatchData` فارغة (null).                                                |

**مثال**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
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

| الكود | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | تمت عملية التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request                 | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized                | رمز JWT غير صالح أو مفقود. |
| 413  | Payload Too Large           | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500  | Internal Server Error       | خطأ داخلي غير متوقع في الخادم. |
## كيفية استخدام واجهة PostImportData API باستخدام SDKs

### مواصفات واجهة PostImportData API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) واجهة برمجة تطبيقات عامة قابلة للوصول تتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDKs هو أسرع طريقة لدمج هذه الوظيفة. فالمكتبات (SDKs) تتعامل مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق أعمالك. يمكنك الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}