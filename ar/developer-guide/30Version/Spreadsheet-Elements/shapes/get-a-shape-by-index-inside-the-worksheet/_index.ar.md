---
title: "الحصول على شكل باستخدام الفهرس في ورقة عمل إكسل"
second_title: "المستند"
linktype: "الحصول"
type: docs
url: /ar/shapes/get/
aliases: [  /ar/get-a-shape-by-index-inside-the-worksheet/ ]
keywords: "Aspose.Cells Cloud، واجهة برمجة تطبيقات شكل إكسل، الحصول على شكل باستخدام الفهرس، شكل ورقة العمل، واجهة برمجة التطبيقات REST، استرجاع الأشكال، Aspose.Cells SDK"
description: "استرجاع شكل باستخدام فهرسه من ورقة عمل إكسل باستخدام واجهة برمجة التطبيقات REST لـ Aspose.Cells Cloud. تتضمن بنية الطلب، المُعطَلات، تفاصيل الاستجابة وأمثلة لـ SDKs."
weight: 20
ArticleTitle: "الحصول على شكل باستخدام الفهرس في ورقة عمل إكسل – وثائق Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية لـ REST باسترجاع شكل (بما في ذلك بيانات الصورة أو البيانات الوصفية الخاصة به) من ورقة عمل إكسل.

## GetWorksheetShape API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**المتطلبات المسبقة**  
- رمز وصول صالح لـ Aspose Cloud (Bearer JWT).  
- يجب أن يكون المصنف مخزنًا في مساحة التخزين الخاصة بـ Aspose Cloud أو في مجلد مُحدّد.  

### **الأمان والمصادقة**

تُعدّ واجهات برمجة التطبيقات (APIs) لـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **مُعطَلات الطلب**

| اسم المُعطَل | النوع | الموقع | الوصف |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name | string | path | اسم مستند إكسل. |
| sheetName | string | path | اسم ورقة العمل التي يحتويها الشكل. |
| shapeindex | integer | path | الفهرس (الصفر-الأساسي) للشكل داخل ورقة العمل. |
| folder | string | query | مسار المجلد الذي يُخزّن فيه المستند. |
| storageName | string | query | اسم خدمة التخزين. |

**ملاحظة:** يكون `shapeindex` بصيغة صفر-الأساسية؛ أي أن أول شكل له الفهرس 0. تأكد من أن المصنف مخزن في `folder` و`storageName` المحدّدين إن لم تستخدم مساحة التخزين الافتراضية.

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) واجهة برمجة قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر `cURL` للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمة لواجهة برمجة التطبيقات السحابية باستخدام `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
# Endpoint ومسار مصحّحان
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**رموز حالة HTTP الممكنة**

| الرمز | الوصف |
|------|-------------|
| **200 OK** | تم استرجاع الشكل بنجاح. |
| **400 Bad Request** | الطلب غير صحيح أو مفقود مُعطَلات مطلوبة. |
| **401 Unauthorized** | فشلت المصادقة أو أن الرمز مفقود/غير صالح. |
| **404 Not Found** | المصنف أو ورقة العمل أو فهرس الشكل المحدّد غير موجود. |
| **500 Internal Server Error** | حدث خطأ غير متوقع في الخادم. |

**المشكلات الشائعة:** استخدام مجال أساسي خاطئ (`api.aspose.com`) أو الجزء القديم `/autoshapes/` سيؤدي إلى خطأ 404. استخدم دائمًا الجزء `/shapes/` مع المجال `api.aspose.cloud`.

## مجموعة أدوات التطوير (SDK Family)

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى ويسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

بالنسبة للعمليات ذات الصلة، راجع الوثائق الخاصة بـ **[إضافة شكل](/shapes/add/)** و **[تحديث شكل](/shapes/update/)**.