---
title: "حذف خاصية مستند محددة"
second_title: "المستند"
linktitle: "حذف"
type: docs
url: /ar/document-properties/delete/
aliases: [  /ar/remove-a-particular-document-property/ ]
keywords: "Aspose.Cells, حذف خاصية المستند, واجهة برمجة تطبيقات بيانات ميتا للإكسل, REST, وحدة تحكم سحابية, مثال cURL"
description: "حذف خاصية مستند محددة من ملف عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API الإصدار 3.0. يتضمن أمثلة لـ cURL ووحدات التحكم (SDKs) لـ C# وJava وPython وغيرها."
weight: 50
---

تقوم هذه الواجهة البرمجية (REST API) بحذف خاصية مستند من ملف عمل.

## واجهة برمجة تطبيقات REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### معلمات الطلب

| اسم المعلمة | النوع | الموقع | الإلزام | الوصف |
| ------------ | ------ | -------- | -------- | --------------------------------------------- |
| name | string | path | نعم | اسم ملف عمل إكسل. |
| propertyName | string | path | نعم | اسم خاصية المستند المراد حذفها. |
| folder | string | query | لا | مسار المجلد الذي يخزن فيه ملف العمل. |
| storageName | string | query | لا | اسم خدمة التخزين. |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) واجهة برمجة قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
     -X DELETE \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استجابات الأخطاء

| حالة HTTP | الوصف | مثال JSON |
| ----------- | ----------------------------------------------------------------------- | ------------------------------------------------------------- |
| 400 | طلب غير صحيح – معلمات مطلوبة مفقودة أو قيم غير صالحة. | `{"Code":400,"Message":"Missing required parameter 'name'."}` |
| 401 | غير مصرح به – رمز JWT غير صالح أو غير موجود. | `{"Code":401,"Message":"Invalid access token."}` |
| 404 | غير موجود – ملف العمل أو الخاصية المحددة غير موجود. | `{"Code":404,"Message":"Document property not found."}` |
| 500 | خطأ داخلي في الخادم – حدثت حالة غير متوقعة على الخادم. | `{"Code":500,"Message":"An unexpected error has occurred."}` |

## عائلة وحدات التحكم (SDK) السحابية

استخدام وحدة التحكم (SDK) هو أفضل طريقة لتسريع عملية التطوير. فوحدات التحكم تتعامل مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بوحدات تحكم Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام مختلف وحدات التحكم (SDKs):

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}