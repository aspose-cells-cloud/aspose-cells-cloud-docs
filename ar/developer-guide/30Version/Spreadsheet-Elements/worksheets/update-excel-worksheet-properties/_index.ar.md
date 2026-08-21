---
title: "تحديث خصائص ورقة العمل – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
second_title: "مستند"
linktitle: "تحديث"
type: docs
url: /ar/worksheets/update-properties/
aliases: [  /ar/update-excel-worksheet-properties/ ]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "worksheet",
    "update properties",
    "REST API",
    "cloud",
    "v3.0",
  ]
description: "تعرّف على كيفية تحديث الخصائص الأساسية لورقة عمل Excel (مثل عرض الأصفار، ورؤية المسطرة) باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API الإصدار 3.0. يتضمن طلب cURL، وأمثلة لواجهات برمجة التطبيقات (SDK)، والمعلمات، ومعالجة الأخطاء."
ArticleTitle: "تحديث خصائص ورقة العمل – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 3.0)"
---

تقوم هذه الواجهة البرمجية لواجهة الويب (REST API) بتحديث الخصائص الأساسية لورقة العمل.

## واجهة برمجة تطبيقات REST

**المتطلبات المسبقة:** يجب أن يكون لديك حساب Aspose Cloud ساري المفعول، والحصول على رمز وصول JWT، وضمان تخزين ملف المصنف المستهدف في موقع تخزين مدعوم. ويجب أن تُرسل جميع الطلبات عبر بروتوكول **HTTPS**.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **معلمات الطلب**

| اسم المعلمة | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
| ------------ | ------ | -------------------------- | --------------------------------------------------------------------------------------------------- |
| name | string | path | اسم ملف المصنف (مع امتداده). |
| sheetName | string | path | اسم ورقة العمل التي سيتم تحديثها. |
| sheet | object | body | كائن JSON يحتوي على أزواج (مفتاح/قيمة) لخصائص ورقة العمل (مثل `DisplayZeros`، `IsRulerVisible`). |
| folder | string | query | مسار المجلد داخل مساحة التخزين حيث يوجد المصنف. |
| storageName | string | query | اسم مساحة التخزين المراد استخدامها. |

يُرسل كائن **sheet** في جسم الطلب بصيغة JSON. وتتضمن الخصائص التي يمكن تعديلها على سبيل المثال: `DisplayZeros`، `IsRulerVisible`، `IsGridlinesVisible`، وغير ذلك من الخصائص المُعرّفة في مواصفات الواجهة البرمجية.

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء استدعاءات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

رموز الاستجابة الشائعة:

- **200** – نجاح. تم تحديث خصائص ورقة العمل بنجاح.
- **400** – طلب غير صالح (مثل JSON معطّل أو معلمة مطلوبة مفقودة).
- **401** – غير مصرّح به – رمز JWT مفقود أو غير صالح.
- **404** – المصنف أو ورقة العمل غير موجودين.
- **500** – خطأ داخلي في الخادم.

| الرمز | المعنى |
|------|---------|
| 200 | نجاح – تم تحديث خصائص ورقة العمل. |
| 400 | طلب غير صالح – JSON معطّل أو معلمة مطلوبة مفقودة. |
| 401 | غير مصرّح به – رمز JWT مفقود أو غير صالح. |
| 404 | غير موجود – المصنف أو ورقة العمل غير موجودين. |
| 500 | خطأ داخلي في الخادم. |

## مجموعة أدوات تطوير البرمجيات (SDK) السحابية

استخدام إطار عمل SDK هو أسرع طريقة لتسريع عملية التطوير، حيث يتعامل إطار العمل مع التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر الأمثلة التالية كيفية إجراء استدعاءات لخدمات الويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}