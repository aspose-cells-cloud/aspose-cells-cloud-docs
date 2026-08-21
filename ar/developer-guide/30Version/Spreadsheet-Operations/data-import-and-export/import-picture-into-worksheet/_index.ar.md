---
title: "استيراد صورة إلى ورقة عمل Excel"
ArticleTitle: "استيراد صورة إلى ورقة عمل Excel – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "استيراد صورة"
type: docs
url: /ar/import-picture-into-excel-worksheet/
aliases:
  - /ar/import-picture-into-worksheet/
  - /ar/import-data/picture/
  - /ar/import/picture/
keywords: "استيراد صورة، Excel، Aspose.Cells Cloud، واجهة برمجة تطبيقات REST، الإصدار 3.0"
description: "تعرّف على كيفية استيراد الصور إلى أوراق عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API الإصدار 3.0. يشمل أمثلة طلبات متعددة الأجزاء، وأكواد عينات SDK، وإرشادات معالجة الأخطاء. ابدأ بسرعة وبخطوات واضحة."
weight: 19
---

يمكنك تحسين محتوى جداول البيانات البصرية من خلال استيراد الصور إليها، مثل الشعارات أو المخططات أو الرسوم البيانية. يوضح هذا الدليل كيفية استخدام عملية **ImportPicture** في Aspose.Cells Cloud، والتنسيق المطلوب للطلب، وكيفية التعامل مع الاستجابات.

**المتطلبات الأساسية:** يجب أن تمتلك رمز مصادقة JWT ساري المفعول وملف مصنف موجود مخزنًا في تخزين Aspose Cloud قبل تنفيذ عملية الاستيراد.

## واجهة PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **متغيرات الطلب**

يكون الطلب عبارة عن **POST** عبر HTTP مع محتوى من نوع **multipart/related** (انظر [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) أو [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- يحتوي **الجزء الأول** على كائن JSON يُسمى **ImportPictureOption** يصف مكان وضع الصورة وكيفية ذلك.
- يحتوي **الجزء الثاني** على ملف الصورة (أو بيانات Base64 المُشفّرة الخاصة بها).

### ImportPictureOption – التعريف

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` قيمة **منطقية (boolean)** – القيمة `true` تُدرج صورة جديدة، و`false` تستبدل صورة موجودة._

### المتغيرات المهمة

**ImportPictureOption**

| اسم المتغير         | النوع         | الوصف                                                                                                                                                                 |
|---------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UpperLeftRow        | عدد صحيح (int) | فهرس الصف للزاوية العلوية اليسرى حيث سيتم وضع الصورة.                                                                                                                  |
| UpperLeftColumn     | عدد صحيح (int) | فهرس العمود للزاوية العلوية اليسرى حيث سيتم وضع الصورة.                                                                                                                |
| LowerRightRow       | عدد صحيح (int) | فهرس الصف للزاوية السفلية اليمنى التي تحدّد حدود الصورة.                                                                                                              |
| LowerRightColumn    | عدد صحيح (int) | فهرس العمود للزاوية السفلية اليمنى التي تحدّد حدود الصورة.                                                                                                            |
| Filename            | سلسلة نصية (string) | اسم ملف الصورة.                                                                                                                                                    |
| Data                | سلسلة نصية (string) | بيانات الصورة الثنائية المُشفّرة بصيغة Base64 (اختيارية إذا تم إرسال الملف كجزء ثانٍ).                                                                               |
| DestinationWorksheet | سلسلة نصية (string) | اسم ورقة العمل التي سيتم إدراج الصورة فيها.                                                                                                                        |
| **IsInsert**         | **قيمة منطقية (boolean)** | `true` لإدراج صورة جديدة؛ `false` لاستبدال صورة موجودة.                                                                                                            |
| ImportDataType      | سلسلة نصية (string) | نوع البيانات التي يتم استيرادها (مثل `Picture` أو `IntArray` أو `DoubleArray` أو `StringArray` أو `TwoDimensionIntArray` أو `TwoDimensionDoubleArray` أو `TwoDimensionStringArray` أو `BatchData` أو `csvData`). |
| Source              | FileSource    | يُحدد موقع ملف البيانات عندما تكون قيمة المعامل `BatchData` فارغة.                                                                                                     |

### الاستجابة

يُعيد الطلب الناجح رمز الحالة **HTTP 200** مع حمولة JSON تشبه ما يلي:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

رموز الحالة الممكنة:

| الرمز | المعنى                                                  |
|-------|----------------------------------------------------------|
| 200   | نجح الاستيراد                                            |
| 400   | طلب غير صالح – بيانات مفقودة أو غير صحيحة              |
| 401   | غير مصرح به – رمز غير صالح أو مفقود                     |
| 500   | خطأ داخلي في الخادم                                      |


## كيفية استخدام واجهة PostImportData API مع مكتبات SDK

### مواصفات واجهة PostImportData API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام مكتبات Aspose.Cells Cloud SDK

يُعد استخدام مكتبات SDK أفضل طريقة لتسريع عملية التطوير. فتتولى مكتبات SDK معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

توضح الأمثلة التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---