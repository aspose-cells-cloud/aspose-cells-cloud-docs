---
title: "استيراد مصفوفة أعداد صحيحة إلى ورقة عمل إكسل"
linktype: "استيراد مصفوفة أعداد صحيحة"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, إكسل, استيراد مصفوفة أعداد صحيحة, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "تعلم كيفية استيراد مصفوفة أعداد صحيحة إلى ورقة عمل إكسل باستخدام Aspose.Cells Cloud REST API. يشمل بنية الطلب، المعلمات، أمثلة للكود بعدة لغات برمجة، وتفاصيل الاستجابة."
weight: 30
ArticleTitle: "استيراد مصفوفة أعداد صحيحة إلى ورقة عمل إكسل – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST باستيراد مصفوفة أعداد صحيحة إلى ورقة عمل إكسل.

يجب أن يكون الطلب طلب <b>POST</b> عبر HTTP مع محتوى متعدد الأجزاء (انظر [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). الجزء الأول من جسم الطلب المتعدد يحتوي على حمولة JSON لـ **ImportIntegerArrayOption**، والجزء الثاني يحتوي على ملف البيانات المصدر (مثل ملف CSV أو ملف إكسل ثنائي).

## واجهة PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

يقبل كلا_endpoint_ين نفس الحمولة المتعددة الأجزاء. يقوم الـ endpoint الأول بتنفيذ عملية استيراد عامة، بينما يستهدف الـ endpoint الثاني مصنفًا محددًا عبر اسمه `{name}`.

### **الأمان والمصادقة**

تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة باستخدام رمز JWT</a>.

### **معلمات الطلب**

### ImportIntegerArrayOption

| اسم المعلمة              | النوع      | الوصف                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | المؤشر المُبدَأ من الصفر لصف أول خلية سيتم وضع البيانات فيها.                                                                                                                               |
| **FirstColumn**          | int        | المؤشر المُبدَأ من الصفر لعمود أول خلية سيتم وضع البيانات فيها.                                                                                                                            |
| **IsVertical**           | boolean    | `true` لإدخال المصفوفة عموديًّا (لأسفل عمود واحد)؛ `false` لإدخالها أفقيًّا (عبر صف واحد).                                                                                       |
| **Data**                 | Integer[]  | المصفوفة الصحيحة المراد استيرادها.                                                                                                                                                              |
| **DestinationWorksheet** | string     | اسم ورقة العمل التي ستستقبل البيانات.                                                                                                                                              |
| **IsInsert**             | boolean    | `true` لإدراج صفوف/أعمدة قبل كتابة البيانات؛ `false` لكتابة البيانات فوق الخلايا الموجودة.                                                                                                    |
| **ImportDataType**       | string     | نوع البيانات المراد استيرادها. القيم المقبولة: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | يُحدد موقع ملف البيانات عندما تكون قيمة المعامل **BatchData** `null`.                                                                                                            |

#### مثال على جسم الطلب

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### الاستجابة

يُعيد الطلب الناجح رمز الحالة **HTTP 200** مع جسم JSON على الشكل التالي:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

رموز الحالة الممكنة:

| الرمز | المعنى                                 |
| ---- | --------------------------------------- |
| 200  | نجح الاستيراد                        |
| 400  | طلب غير صالح – بيانات ناقصة أو خاطئة   |
| 401  | عدم مصادقة – رمز غير صالح أو مفقود |
| 500  | خطأ داخلي في الخادم                   |

## كيفية استخدام واجهة PostImportData API باستخدام مكتبات SDK

### مواصفات واجهة PostImportData API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) واجهة برمجة قابلة للوصول بشكل عام وتتيح إجراء تفاعلات REST مباشرة من متصفح ويب.

### استخدام مكتبات Aspose.Cells Cloud SDK

استخدام مكتبة SDK هو أسرع طريقة لدمج هذه الوظيفة. فالمكتبات تُجرّد التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق تطبيقك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر مكتبات مختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---