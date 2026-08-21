---
title: "الحصول على عدد الصفحات من ملف إكسل"
second_title: "مستند"
linktype: "الصفحات"
type: docs
url: /ar/get-page-count-from-an-excel-file/
aliases: [  /ar/workbook/page-count/ , /ar/workbook/get/page-count/ ]
keywords: "Aspose.Cells, واجهة برمجة التطبيقات السحابية، عدد صفحات إكسل، تقسيم الصفحات في المصنف"
description: "استرجاع العدد الإجمالي للصفحات القابلة للطباعة في مصنف إكسل باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن تنسيق الطلب، المعلمات المطلوبة، مثال باستخدام cURL، مخطط الاستجابة، معالجة الأخطاء، وأجزاء من أكواد SDK لعدة لغات برمجة."
weight: 10
version: "v3.0"
ArticleTitle: "الحصول على عدد الصفحات من ملف إكسل باستخدام واجهة Aspose.Cells Cloud API"
---

تُعيد هذه الواجهة البرمجية للـ REST **عدد الصفحات** للمصنف.

## الأمان والمصادقة
تُعدّ واجهات Aspose.Cells Cloud API آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### معلمات الطلب

| اسم المعلمة | النوع | الموقع | مطلوب | الوصف |
| ------------ | ------ | -------- | -------- | -------------------------------------- |
| name | string | path | نعم | اسم ملف إكسل. |
| folder | string | query | لا | المجلد الذي يحتوي على المستند. |
| storageName | string | query | لا | اسم وحدة التخزين المراد استخدامها. |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى واجهة Aspose.Cells REST بسهولة. يوضح المثال التالي كيفية استدعاء نقطة النهاية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/YourFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*استبدل `YourFile.xlsx` باسم المصنف الفعلي الذي ترغب في الاستعلام عنه.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### مخطط الاستجابة

| حالة HTTP | نوع البيانات | الوصف |
| ----------- | --------- | ----------------------------------------------------------------- |
| 200 | integer | العدد الإجمالي للصفحات القابلة للطباعة في المصنف (مثل: `13`). |
| 4xx‑5xx | JSON | كائن الخطأ (انظر قسم _معالجة الأخطاء_). |

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## معالجة الأخطاء

| حالة HTTP | الوصف | مثال على جسم JSON |
| ----------- | ------------------------------------------ | -------------------------------------------------------------------------------------------- |
| 401 | رمز JWT غير صالح أو مفقود. | `{ "Code": "InvalidAuthenticationToken", "Message": "رمز الوصول مفقود أو غير صالح." }` |
| 404 | تعذّر العثور على المصنف المحدد. | `{ "Code": "FileNotFound", "Message": "الملف المطلوب غير موجود." }` |
| 400 | طلب غير صالح – معلمات مطلوبة مفقودة. | `{ "Code": "BadRequest", "Message": "المعلمة المطلوبة 'name' مفقودة." }` |
| 500 | خطأ داخلي في الخادم. | `{ "Code": "InternalError", "Message": "حدث خطأ غير متوقع." }` |
---