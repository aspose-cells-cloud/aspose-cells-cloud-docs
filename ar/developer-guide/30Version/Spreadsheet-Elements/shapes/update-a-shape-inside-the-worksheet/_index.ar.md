---
title: "تحديث شكل في ورقة عمل Excel"
second_title: "مستند"
linktitle: "تحديث"
type: docs
url: /ar/shapes/update/
aliases: [  /ar/update-a-shape-inside-the-worksheet/ ]
keywords: "تحديث شكل باستخدام API Excel، Aspose.Cells Cloud، تحديث شكل Excel، REST API، SDK، C#، Java، Python، Node.js، Go، Ruby، PHP، Perl، Swift"
description: "تعرّف على كيفية تحديث شكل في ورقة عمل Excel باستخدام REST API الخاص بـ Aspose.Cells Cloud. يشمل الـ HTTPS endpoint، تفاصيل المصادقة، مخطط نقل البيانات (DTO)، إرشادات الاستخدام خطوة بخطوة، مثال باستخدام cURL، وأكواد أمثلة SDK بلغات برمجة متعددة."
ArticleTitle: "تحديث شكل في ورقة عمل Excel - Aspose.Cells Cloud API"
weight: 31
---

تقوم هذه الواجهة البرمجية لـ REST بتحديث شكل في ورقة عمل Excel.

## الأمان والمصادقة

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة التطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

### معاملات الطلب

| اسم المعامل       | النوع    | الموقع | الوصف                                                                                   |
| ----------------- | -------- | ------ | ---------------------------------------------------------------------------------------- |
| **name**          | سلسلة   | المسار | اسم ملف المصنف.                                                                         |
| **sheetName**     | سلسلة   | المسار | اسم ورقة العمل التي يحتوي عليها الشكل.                                                  |
| **shapeindex**    | عدد صحيح | المسار | الفهرس الصفر-الأساسي للشكل داخل ورقة العمل.                                            |
| **dto**           | كائن    | الجسم | كائن نقل بيانات الشكل الذي يحتوي على الخصائص المُحدَّثة (انظر _مخطط نقل البيانات_ أدناه). |
| **folder**        | سلسلة   | الاستعلام | المجلد الذي يُخزَّن فيه المصنف.                                                        |
| **storageName**   | سلسلة   | الاستعلام | اسم مساحة التخزين الخاصة بـ Aspose Cloud.                                              |

### مخطط نقل البيانات (DTO)

يحتوي الكائن `dto` على الخصائص التي يمكن تحديثها. جميع الحقول اختيارية ما لم يُذكر خلاف ذلك.

| الحقل               | النوع    | الإلزام | الوصف                                                                        |
| ------------------- | -------- | ------- | ----------------------------------------------------------------------------- |
| **Name**            | سلسلة    | لا      | الاسم الجديد للشكل.                                                          |
| **UpperLeftRow**    | عدد صحيح | لا      | فهرس الصف لزاوية الشكل العلوية اليسرى.                                       |
| **UpperLeftColumn** | عدد صحيح | لا      | فهرس العمود لزاوية الشكل العلوية اليسرى.                                     |
| **Width**           | عدد صحيح | لا      | عرض الشكل (بالنقاط).                                                         |
| **Height**          | عدد صحيح | لا      | ارتفاع الشكل (بالنقاط).                                                      |
| **RotationAngle**   | عدد صحيح | لا      | زاوية الدوران بالدرجات.                                                      |
| **IsHidden**        | منطقي   | لا      | `true` لإخفاء الشكل.                                                         |
| **IsLocked**        | منطقي   | لا      | `true` لقفل الشكل.                                                            |
| **Font**            | كائن    | لا      | إعدادات الخط (انظر مواصفة OpenAPI لمعرفة الخصائص الفرعية).                 |
| **...**             | …        | لا      | خصائص إضافية مثل `HtmlText` و`AlternativeText` و`ZOrderPosition` وما إلى ذلك. |

> للحصول على قائمة كاملة، يُرجى الرجوع إلى المواصفات الرسمية لـ OpenAPI: <https://apireference.aspose.cloud/cells/#/Shapes/PostWorksheetShape>.

### رؤوس الطلب

- `Content-Type: application/json`
- `Accept: application/json`
- `Authorization: Bearer <accessToken>` _(رمز JWT المستحصل من خطوة _المصادقة_)_

### جسم الطلب (مثال)

```json
{
  "Name": "MyShape",
  "UpperLeftRow": 2,
  "UpperLeftColumn": 3,
  "Width": 150,
  "Height": 80,
  "RotationAngle": 0,
  "IsHidden": false,
  "IsLocked": false,
  "Font": {
    "Name": "Calibri",
    "Size": 12,
    "IsBold": true,
    "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }
  }
}
```

## مثال باستخدام cURL (أداة سطر الأوامر)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes/0?folder=Temp" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <accessToken>" \
  -d '{
        "Name": "UpdatedShape",
        "UpperLeftRow": 1,
        "UpperLeftColumn": 1,
        "Width": 120,
        "Height": 60,
        "IsHidden": false,
        "IsLocked": false
      }'
```

### الاستجابة

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**معالجة الأخطاء** – قد تُعيد الواجهة البرمجية رموز الحالة التالية:

| الرمز | المعنى                 | السبب الشائع                                        |
| ----- | ----------------------- | --------------------------------------------------- |
| 400   | طلب غير صالح           | هيكل JSON غير صالح أو حقول مطلوبة مفقودة.        |
| 401   | غير مُصادَق عليه       | رمز JWT مفقود أو غير صالح.                        |
| 404   | غير موجود              | المصنف أو ورقة العمل أو فهرس الشكل غير موجود.     |
| 500   | خطأ داخلي في الخادم    | مشكلة غير متوقعة من جانب الخادم.                  |

**أمثلة على استجابات الأخطاء**

*400 – طلب غير صالح*

```json
{
  "Code": 400,
  "Message": "حمولة الطلب غير صالحة. حقل 'Name' يتجاوز الحد الأقصى للطول."
}
```

*401 – غير مُصادَق عليه*

```json
{
  "Code": 401,
  "Message": "فشل المصادقة. رمز JWT غير صالح أو منتهٍ."
}
```

*404 – غير موجود*

```json
{
  "Code": 404,
  "Message": "لم يتم العثور على المصنف أو ورقة العمل أو فهرس الشكل المحدَّد."
}
```

*500 – خطأ داخلي في الخادم*

```json
{
  "Code": 500,
  "Message": "حدث خطأ غير متوقع في الخادم."
}
```

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع التطوير. تتعامل SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر الأمثلة التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}