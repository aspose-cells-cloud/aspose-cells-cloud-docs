---
title: "الحصول على فواصل الصفوف الأفقية"
second_title: "الوثيقة"
linktitle: "الحصول على فواصل الصفوف الأفقية"
type: docs
url: /page-breaks/get-horizontal-page-breaks/
aliases: [/get-horizontal-page-breaks-inside-worksheet/]
keywords: "فواصل الصفوف الأفقية، Aspose.Cells Cloud، واجهة برمجة التطبيقات REST، ورقة عمل إكسل، واجهة برمجة تطبيقات (SDK)"
description: "استرجاع فواصل الصفوف الأفقية من ورقة عمل إكسل عبر واجهة برمجة التطبيقات Aspose.Cells Cloud. يشمل النهاية (Endpoint)، المعاملات، مثال cURL، تنسيق الاستجابة، وأجزاء من كود واجهات برمجة التطبيقات (SDK) بلغات C#، Java، Python، والمزيد."
ArticleTitle: "الحصول على فواصل الصفوف الأفقية - وثائق واجهة برمجة التطبيقات Aspose.Cells Cloud"
weight: 10
---

**فواصل الصفوف الأفقية** – هي فواصل تعتمد على الصفوف وتُجبر ورقة العمل على بدء صفحة مطبوعة جديدة بعد الصف المحدد. تُستخدم هذه الواجهة البرمجية REST لاسترجاع فواصل الصفوف الأفقية هذه.

## الأمان والمصادقة

تُعتبر واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة التطبيقات REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف                                                                 |
|------------|---------|--------|-----------------------------------------------------------------------|
| name       | string  | path   | اسم ملف إكسل.                                                        |
| sheetName  | string  | path   | اسم ورقة العمل.                                                      |
| folder     | string  | query  | مسار المجلد في التخزين حيث يقع الملف. _(اختياري)_                     |
| storageName| string  | query  | اسم التخزين. _(اختياري)_                                             |

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/GetHorizontalPageBreaks" rel="noopener" title="مواصفات OpenAPI لـ GetHorizontalPageBreaks">مواصفة OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "HorizontalPageBreaks": {
    "HorizontalPageBreakList": [
      {
        "Row": 6,
        "EndColumn": 16383,
        "StartColumn": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/HorizontalPageBreaks",
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

## معالجة الأخطاء

| حالة HTTP | الوصف                                                           | مثال JSON                                            |
|-----------|------------------------------------------------------------------|------------------------------------------------------|
| 400       | طلب غير صالح – معاملات مفقودة أو غير صحيحة.                    | `{ "Code": 400, "Message": "Invalid parameter." }`     |
| 401       | غير مُصادَق – رمز JWT مفقود أو غير صالح.                       | `{ "Code": 401, "Message": "Authentication failed." }` |
| 404       | غير موجود – الملف أو ورقة العمل المحددة غير موجودة.            | `{ "Code": 404, "Message": "Resource not found." }`    |
| 500       | خطأ داخلي في الخادم – ظرف غير متوقع على الخادم.                | `{ "Code": 500, "Message": "Server error." }`          |

## عائلة واجهات برمجة التطبيقات السحابية (Cloud SDK Family)

استخدام واجهة برمجة التطبيقات (SDK) هي أفضل طريقة لتسريع عملية التطوير. فواجهات برمجة التطبيقات تُدير التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بواجهات برمجة التطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مختلف واجهات برمجة التطبيقات (SDKs):

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetHorizontalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetHorizontalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetHorizontalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetHorizontalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetHorizontalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetHorizontalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetHorizontalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetHorizontalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}