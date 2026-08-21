---
title: "الحصول على خاصية مستند محددة"
second_title: "المستند"
linktitle: "الحصول على"
type: docs
url: /ar/document-properties/get/
aliases: [  /ar/get-a-particular-document-property/ ]
keywords: "Aspose.Cells, واجهة برمجة التطبيقات السحابية، الحصول على خاصية المستند، بيانات التعريف الخاصة بملف إكسل، REST GET، أمثلة ل_sdk"
description: "استرجاع خاصية مستند مسمّاة (مثل المؤلف أو العنوان) من ملف إكسل باستخدام واجهة Aspose.Cells Cloud REST API. يشمل مثالًا باستخدام أداة cURL، وأجزاء من كود SDK، ومخطط الاستجابة."
weight: 20
---

تقوم هذه الواجهة البرمجية للتطبيقات (REST API) بقراءة خاصية المستند حسب اسمها.

## واجهة برمجة التطبيقات (REST API)

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### مُعلَمات الطلب

| اسم المُعلَمة | النوع | الموقع | الوصف |
| -------------- | ------ | -------- | ---------------------------------------------- |
| name | string | path | اسم ملف إكسل. |
| propertyName | string | path | اسم خاصية المستند المراد استرجاعها. |
| folder | string | query | المجلد الذي يحتوي على الملف (اختياري). |
| storageName | string | query | اسم وحدة التخزين (اختياري). |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperty) واجهة برمجة تطبيقات متاحة عمومًا، وتتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة **cURL** لسهولة الوصول إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperty": {
    "Name": "Author",
    "Value": "",
    "BuiltIn": "True",
    "link": {
      "Href": "/test.xlsx/documentproperties/Author",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### تفاصيل الاستجابة

يحتوي كائن JSON المُعاد من الواجهة البرمجية على الحقول التالية:

| الحقل | النوع | الوصف |
| ------------------------------- | ------- | ------------------------------------------------------------ |
| **DocumentProperty.Name** | string | اسم الخاصية (مثل `Author`). |
| **DocumentProperty.Value** | string | قيمة الخاصية. قد تكون فارغة إذا لم تُحدّد. |
| **DocumentProperty.BuiltIn** | boolean | يُشير إلى ما إذا كانت الخاصية جزءًا من مجموعة خصائص إكسل المدمجة. |
| **DocumentProperty.link.Href** | string | عنوان URL النسبي لمورد الخاصية. |
| **DocumentProperty.link.Rel** | string | نوع العلاقة، وغالبًا ما يكون `self`. |
| **DocumentProperty.link.Title** | string | عنوان قابل للقراءة (قد يكون `null`). |
| **DocumentProperty.link.Type** | string | نوع MIME لمورد الارتباط (قد يكون `null`). |
| **Code** | integer | رمز حالة HTTP الذي تعيده الخدمة. |
| **Status** | string | وصف نصّي لحالة الطلب (مثل `OK`). |

### استجابات الأخطاء

| حالة HTTP | الرمز | الوصف |
| ----------- | ---------------------- | ----------------------------------------------- |
| 400 | `InvalidParameter` | أحد مُعلَمات الطلب أو أكثر غير صالحة. |
| 401 | `AuthenticationFailed` | رمز JWT مفقود أو غير صالح. |
| 404 | `PropertyNotFound` | خاصية المستند المحددة غير موجودة. |
| 500 | `InternalError` | حدث خطأ غير متوقع على الخادم. |

يبدو محتوى الخطأ النموذجي كالتالي:

```json
{
  "Code": 404,
  "Status": "Property not found"
}
```

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فالـ SDK يتعامل مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}

### المصطلحات

| المصطلح | التعريف |
| --------------------- | -------------------------------------------------------------------------------------------------- |
| **خصائص المستند** | جزء من بيانات التعريف المرتبطة بمصنف إكسل (مثل المؤلف أو العنوان أو تاريخ الإنشاء). |
| **بيانات التعريف** | مصطلح عام يشير إلى البيانات التي تصف بيانات أخرى؛ وفي هذا السياق يشير إلى خصائص المستند. |
| **خصائص مخصّصة** | خصائص يحددها المستخدم ولا تندرج ضمن الخصائص المدمجة. |

### الأسئلة الشائعة

**س:** _كيف يمكنني استرجاع خاصية المؤلف لملف إكسل مخزن في Aspose Cloud؟_  
**ج:** أرسل طلب GET إلى `https://api.aspose.cloud/v3.0/cells/{fileName}/documentproperties/author` مع رمز Bearer صالح. ستتضمن استجابة JSON الحقل `DocumentProperty.Name = "Author"` وقيمته `Value`.

**س:** _ما هو الخطأ الذي يتم إعادته إذا لم تكن الخاصية المطلوبة موجودة؟_  
**ج:** تُعيد الواجهة البرمجية حالة HTTP 404 مع جسم JSON يحتوي على `Code: 404` و `Status: "Property not found"`.

**س:** _هل يلزم تحديد `storageName` عند وجود الملف في وحدة التخزين الافتراضية؟_  
**ج:** لا. مُعلَمة الاستعلام `storageName` اختيارية؛ يمكنك حذفها لاستخدام وحدة التخزين الافتراضية المُعدّة لحسابك.