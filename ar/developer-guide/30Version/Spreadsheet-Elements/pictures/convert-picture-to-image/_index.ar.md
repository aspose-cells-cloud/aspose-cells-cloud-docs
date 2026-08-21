---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud – استرجاع صورة من ورقة عمل"
second_title: "الوثيقة"
linktitle: "استرجاع"
type: docs
url: /pictures/get/
aliases: [/convert-picture-to-image/]
keywords: "Aspose.Cells, استرجاع صورة, واجهة برمجة تطبيقات, Excel, سحابي, REST"
description: "استرجاع صورة محددة من ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يشمل النقطة النهائية (endpoint)، المعاملات، خطوات المصادقة، رموز الاستجابة، وأمثلة على الأكواد."
weight: 10
ArticleTitle: "واجهة برمجة تطبيقات Aspose.Cells Cloud – استرجاع صورة من ورقة عمل"
---

تقوم هذه الواجهة البرمجية (REST API) باسترجاع صورة باستخدام فهرسها المُعدّ من الصفر من ورقة عمل Excel.

## واجهة برمجة التطبيقات REST

لاستدعاء هذه النقطة النهائية، يجب أن تتضمّن رأس **Authorization** رمز وصول JWT صالح. ويُحصل على الرموز عبر عملية مصادقة Aspose.Cells Cloud، وتحتاج إلى النطاقات (scopes) المناسبة للوصول إلى الملفات. وللمزيد من التفاصيل حول كيفية الحصول على رمز وصول، راجع الدليل العام المعنون **Authentication** (المصادقة).

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### المعاملات المطلوبة في الطلب

| اسم المعاملة | النوع     | الموقع | الوصف                                                                                                               |
|-------------|-----------|--------|---------------------------------------------------------------------------------------------------------------------|
| name        | string    | path   | اسم ملف Excel.                                                                                                      |
| sheetName   | string    | path   | اسم ورقة العمل.                                                                                                     |
| pictureIndex| integer   | path   | فهرس الصورة (يبدأ من الصفر).                                                                                        |
| format      | string    | query  | تنسيق التصدير المطلوب (مثل: png، jpg، bmp، gif، tiff). وإذا تُركت بدون تحديد، تُعاد الصورة بتنسيقها الأصلي.         |
| folder      | string    | query  | المجلد الذي يحتوي على المستند.                                                                                     |
| storageName | string    | query  | اسم موقع التخزين.                                                                                                   |

### استجابات الأخطاء

| الرمز HTTP | الوصف                                                                              |
|------------|------------------------------------------------------------------------------------|
| 401        | غير مُصادَق – رمز وصول مفقود أو غير صالح.                                         |
| 404        | غير موجود – الملف أو ورقة العمل أو فهرس فاصل الصفحات المحدّد غير موجود.           |
| 400        | طلب خاطئ – صيغة الطلب غير سليمة أو المعاملات غير صالحة.                          |
| 500        | خطأ داخلي في الخادم – وُجدت حالة غير متوقعة.                                      |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) واجهة برمجة تطبيقات عامة قابلة للاستخدام، ويسمح لك بإجراء تفاعلات REST مباشرة من متصفّح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# بيانات الصورة الثنائية (PNG) المُعادَة في جسم الاستجابة.
# مثال: جزء مشفر بـ base64
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لتطوير البرمجيات. فSDK تتعامل مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الإنترنت باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}