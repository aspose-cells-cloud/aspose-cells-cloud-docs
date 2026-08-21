---
title: "الحصول على جميع الأشكال الموجودة في ورقة عمل Excel"
second_title: "مستند"
linktitle: "get-all"
type: docs
url: /shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: "Aspose.Cells، واجهة برمجة التطبيقات السحابية، أشكال Excel، الحصول على الأشكال، REST، SDK"
description: "استرجاع جميع الأشكال (المخططات والصور ومربعات النص) من ورقة عمل باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن مثالًا باستخدام cURL، وأجزاء كود من SDK، وخطوات المصادقة، ومعالجة الأخطاء."
ArticleTitle: "الحصول على جميع الأشكال الموجودة في ورقة عمل Excel"
weight: 10
---

تتيح هذه واجهة برمجة التطبيقات (REST API) استرجاع جميع الأشكال الموجودة في ورقة عمل Excel.

## الأمان والمصادقة
تُعد واجهات برمجة التطبيقات السحابية لـ Aspose.Cells آمنة وتتطلب [المصادقة باستخدام رمز مميز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة التطبيقات (REST API)

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| --- | --- | --- | --- |
| **name** | نص (string) | مسار (path) | اسم ملف Excel. |
| **sheetName** | نص (string) | مسار (path) | اسم ورقة العمل. |
| **folder** | نص (string) | استعلام (query) | المجلد الذي يحتوي على المستند. |
| **storageName** | نص (string) | استعلام (query) | اسم خدمة التخزين المراد استخدامها. |
| **include** | نص (string) | استعلام (query) | ضع القيمة `details` لاسترجاع خصائص الشكل الكاملة؛ وإلا سيتم استرجاع كائنات `link` فقط. |

> **اختياري**: يمكن تجاهل `folder` و`storageName` و`include` عندما يكون الملف موجودًا في المجلد الجذر للتخزين.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells. يوضح المثال التالي طلبًا يتضمن معاملات الاستعلام الاختيارية.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?folder=Samples&storageName=MyStorage" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Shapes": {
    "ShapeList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Type": null,
          "Title": null
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes",
      "Rel": "self",
      "Type": null,
      "Title": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### حقول الاستجابة

يحتوي كائن `Shapes` على قائمة من عناصر `Shape`. يشمل كل شكل الخصائص التالية (عند استخدام علامة `include=details`؛ وإلا سيتم استرجاع كائن `link` فقط).

| الخاصية | النوع | الوصف |
| --- | --- | --- |
| **Name** | نص (string) | الاسم المُسنَد إلى الشكل (مثل "Chart 1"). |
| **Type** | نص (string) | نوع الشكل (مثل `Chart` أو `Picture` أو `TextBox`). |
| **Top** | رقم (number) | المسافة (بالنقاط) من الحافة العلوية لورقة العمل إلى الشكل. |
| **Left** | رقم (number) | المسافة (بالنقاط) من الحافة اليسرى لورقة العمل إلى الشكل. |
| **Width** | رقم (number) | عرض الشكل بالنقاط. |
| **Height** | رقم (number) | ارتفاع الشكل بالنقاط. |
| **Link** | كائن (object) | معلومات الارتباط التشعبي (`Href` و`Rel` و`Type` و`Title`). |

## معالجة الأخطاء

| حالة HTTP | الوصف | جسم الخطأ النموذجي |
| --- | --- | --- |
| **400** | طلب غير صالح – معاملات غير صحيحة. | `{ "Code": 400, "Message": "Invalid parameter value." }` |
| **401** | غير مُصادَق – رمز مميز مفقود أو غير صالح. | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404** | غير موجود – المصنف أو ورقة العمل غير موجودين. | `{ "Code": 404, "Message": "File or worksheet not found." }` |
| **500** | خطأ داخلي في الخادم – حالة غير متوقعة. | `{ "Code": 500, "Message": "An unexpected error occurred." }` |

يعيد الطلب الناجح **HTTP 200** مع كائن `Shapes` يحتوي على قائمة الأشكال، كما هو موضح في مثال الاستجابة أعلاه.

تفرض واجهة برمجة التطبيقات حدًا قدره **150 طلبًا في الدقيقة لكل رمز مميز JWT**. وعند تجاوز هذا الحد، تُعاد استجابة **HTTP 429** مع رأس `Retry-After` يُحدِّد متى يجب إعادة المحاولة.

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولى SDK معالجة التفاصيل منخفضة المستوى وتركز أنت على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShapes.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShapes.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShapes.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShapes.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShapes.go" >}}

{{< /tab >}}

{{< /tabs >}}