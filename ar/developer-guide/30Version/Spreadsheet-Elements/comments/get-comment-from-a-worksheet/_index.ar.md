---
title: "الحصول على تعليق ورقة العمل – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
type: docs
url: /comments/get/
aliases: [/get-comment-from-a-worksheet/]
keywords: "Aspose.Cells، تعليق ورقة العمل، واجهة برمجة التطبيقات، GET، Excel"
description: "تعرّف على كيفية استرجاع تعليق ورقة عمل باستخدام اسم الخلية عبر واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0). يتضمن عنوان URL للطلب، المعلمات، مثال باستخدام cURL، تفاصيل الاستجابة، وأكواد مقتطفة من SDK."
weight: 10
ArticleTitle: "الحصول على تعليق ورقة العمل – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تسترجع واجهة برمجة تطبيقات **Aspose.Cells Cloud** تعليق ورقة العمل باستخدام اسم الخلية.

**المتطلبات المسبقة:** لاستدعاء هذه العملية، يجب تضمين رمز وصول JWT صالح في رأس `Authorization` (بالصيغة `Bearer <jwt token>`). ويمكنك الحصول على الرموز من خلال عملية المصادقة الموضحة في [دليل المصادقة](/cells/authentication/).

## واجهة برمجة التطبيقات GetWorksheetComment

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة | النوع   | الموقع (مسار URL / سلسلة الاستعلام) | الوصف                                                             |
| ------------ | ------ | ---------------------------------- | ----------------------------------------------------------------- |
| name         | string | مسار URL                           | اسم ملف Excel.                                                    |
| sheetName    | string | مسار URL                           | اسم ورقة العمل التي يحتوي التعليق عليها.                         |
| cellName     | string | مسار URL                           | عنوان الخلية (مثل **A1**) التي يتم استرجاع تعليقها.              |
| folder       | string | سلسلة الاستعلام                    | مسار المجلد الذي يخزن فيه المستند.                                |
| storageName  | string | سلسلة الاستعلام                    | اسم خدمة التخزين.                                                 |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات متاحة للعامة وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Comment": {
    "CellName": "A1",
    "Author": "roy.wang",
    "HtmlNote": "",
    "Note": "Aspose.Cells Cloud.",
    "AutoSize": "True",
    "IsVisible": "True",
    "Width": 30,
    "Height": 10,
    "TextHorizontalAlignment": "Bottom",
    "TextOrientationType": "TopToBottom",
    "TextVerticalAlignment": "Bottom"
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**الاستجابة:** تُعيد واجهة برمجة التطبيقات كائن JSON يحتوي على كائن `Comment` به الحقول التالية:

| الحقل                      | النوع    | الوصف                                               |
| -------------------------- | ------- | ---------------------------------------------------- |
| `CellName`                 | string  | عنوان الخلية (مثل **A1**).                          |
| `Author`                   | string  | اسم مؤلف التعليق.                                   |
| `HtmlNote`                 | string  | محتوى التعليق بصيغة HTML (إن وُجد).                 |
| `Note`                     | string  | النسخة النصية العادية من التعليق.                   |
| `AutoSize`                 | boolean | يُشير إلى ما إذا كانت صندوق التعليق تحجم تلقائيًا.  |
| `IsVisible`                | boolean | يُحدد ما إذا كان التعليق مرئيًا.                    |
| `Width`                    | integer | عرض صندوق التعليق (بالأحرف).                       |
| `Height`                   | integer | ارتفاع صندوق التعليق (بالأحرف).                     |
| `TextHorizontalAlignment` | string  | المحاذاة الأفقية للنص (مثل **Bottom**).             |
| `TextOrientationType`      | string  | اتجاه النص (مثل **TopToBottom**).                   |
| `TextVerticalAlignment`    | string  | المحاذاة العمودية للنص (مثل **Bottom**).            |

## الأخطاء الشائعة

- **401 Unauthorized (غير مُصرّح)** – تأكّد من أن رمز JWT صالح وغير منتهٍ ومُدرج بشكل صحيح في رأس `Authorization`.
- **404 Not Found (غير موجود)** – تأكّد من أن اسم الملف واسم ورقة العمل وعنوان الخلية صحيحان، وأن الملف موجود في المجلد أو التخزين المحدّد.
- **500 Internal Server Error (خطأ داخلي في الخادم)** – تحقق من وجود بيانات مُشكّلة في حمولة الطلب، وتأكد من أن الخدمة تعمل بشكل سليم.

**رموز حالات HTTP**

| الرمز | المعنى                      | الوصف                                             |
|------|-----------------------------|---------------------------------------------------|
| 200  | OK (تم بنجاح)              | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request (طلب غير صالح) | معلمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم).   |
| 401  | Unauthorized (غير مُصرّح)  | رمز JWT غير صالح أو مفقود.                         |
| 413  | Payload Too Large (حمولة كبيرة جدًا) | ملف مرسل يتجاوز الحد الأقصى للحجم.             |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                     |

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع التطوير، حيث تتعامل SDK مع التفاصيل منخفضة المستوى وتسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية إجراء استدعاءات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetComments.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetComments.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetComments.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetComments.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetComments.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetComments.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetComments.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetComments.go" >}}

{{< /tab >}}

{{< /tabs >}}