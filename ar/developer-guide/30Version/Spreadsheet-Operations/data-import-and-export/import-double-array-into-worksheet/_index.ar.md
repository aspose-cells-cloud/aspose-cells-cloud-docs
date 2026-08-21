---
title: "استيراد مصفوفة أعداد عشرية (Double Array) إلى ورقة عمل Excel"
second_title: "مستند"
linktitle: "استيراد مصفوفة أعداد عشرية"
type: docs
url: /ar/import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, استيراد مصفوفة أعداد عشرية, API لـ Excel, SDK للحوسبة السحابية"
description: "تعرّف على كيفية استيراد مصفوفة أعداد عشرية (Double Array) إلى ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يشمل ذلك التوثيق الخاص بالمصادقة، وتنسيق الطلب، والمعاملات، وأمثلة XML/JSON، وتفاصيل الاستجابة."
weight: 20
ArticleTitle: "استيراد مصفوفة أعداد عشرية إلى ورقة عمل Excel – دليل Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية للواجهة السحابية **باستيراد بيانات مصفوفة أعداد عشرية (Double Array)** إلى ورقة عمل Excel.

> **المتطلبات المسبقة:** يجب أن تمتلك رمز JWT صالحًا قبل استدعاء هذه الواجهة. راجع دليل المصادقة لمزيد من التفاصيل.

تُرسِل طلب HTTP يحتوي على محتوى **متعدد الأجزاء (multipart)** (انظر [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
يحتوي الجزء الأول من جسم الطلب المتعدد الأجزاء على بيانات **ImportDoubleArrayOption**، بينما يحتوي الجزء الثاني على ملف البيانات.

## واجهة PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **الأمان والمصادقة**

تستخدم واجهات Aspose.Cells Cloud APIs نظام مصادقة قائم على رموز <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT</a>، وهي آمنة.

### معاملات الطلب

#### **ImportDoubleArrayOption**

| اسم المعامل         | النوع       | الوصف                                                                                             |
| ------------------- | ----------- | ------------------------------------------------------------------------------------------------- |
| FirstRow            | int         | فهرس الصف الأول (مبني على الصفر) حيث سيتم وضع البيانات.                                          |
| FirstColumn         | int         | فهرس العمود الأول (مبني على الصفر) حيث سيتم وضع البيانات.                                        |
| IsVertical          | boolean     | `true` / `false` – يحدد ما إذا كانت المصفوفة تُدخل عموديًا (`true`) أم أفقيًا (`false`).          |
| Data                | Double[]    | مصفوفة من القيم العددية العشرية (Double) المراد استيرادها.                                       |
| DestinationWorksheet | string     | اسم ورقة العمل الهدف.                                                                             |
| IsInsert            | boolean     | `true` / `false` – إذا كانت القيمة `true`، تُدرج البيانات؛ وإذا كانت `false`، تُستبدل الخلايا الموجودة. |
| ImportDataType      | string      | نوع البيانات التي يتم استيرادها (مثل `IntArray`، `DoubleArray`، `StringArray`، `TwoDimensionIntArray`). |
| Source              | FileSource  | يحدد موقع ملف البيانات عند تعيين المعامل `BatchData` إلى `null`.                                 |

#### مثال (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### مثال (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### الاستجابة

يُعيد الطلب الناجح رمز الحالة **HTTP 200** مع حمولة JSON مشابهة لما يلي:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

رموز الحالة الممكنة:

| الكود | المعنى                                   |
| ----- | ---------------------------------------- |
| 200   | نجح الاستيراد                            |
| 400   | طلب غير صالح – بيانات مفقودة أو غير صحيحة |
| 401   | غير مخوّل – رمز غير صالح أو مفقود        |
| 500   | خطأ داخلي في الخادم                      |

### معالجة الأخطاء

عند حدوث خطأ، تُعيد الواجهة كائن JSON يحتوي على رمز الخطأ ورسالة وصفية. مثال على طلب غير مخوّل:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

لمزيد من المعلومات حول عمليات الاستيراد ذات الصلة، راجع صفحات التوثيق الخاصة بـ "استيراد مصفوفة أعداد عشرية ثنائية الأبعاد" و"استيراد مصفوفة أعداد صحيحة".

## كيفية استخدام واجهة PostImportData مع مكتبات SDK

### مواصفات واجهة PostImportData

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) واجهة برمجة تطبيقات عامة قابلة للاستعمال، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

### استخدام مكتبات Aspose.Cells Cloud SDK

يعتبر استخدام مكتبة SDK الطريقة الأفضل لتسريع عملية التطوير، إذ تُدار التفاصيل منخفضة المستوى تلقائيًا، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}