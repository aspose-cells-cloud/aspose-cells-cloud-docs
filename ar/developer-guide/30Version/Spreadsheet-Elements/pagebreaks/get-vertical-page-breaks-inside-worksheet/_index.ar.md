---
title: "الحصول على فواصل الصفحات العمودية"
second_title: "مستند"
linktitle: "الحصول على فواصل الصفحات العمودية"
type: docs
url: /page-breaks/get-vertical-page-breaks/
aliases: [/get-vertical-page-breaks-inside-worksheet/]
keywords: "Aspose.Cells، فواصل الصفحات العمودية، واجهة برمجة تطبيقات إكسل، جدول بيانات سحابي، واجهة برمجة تطبيقات REST"
description: "استرجاع فواصل الصفحات العمودية من ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن عنوان HTTPS، المعاملات المطلوبة، مثال cURL، تفاصيل الاستجابة، معالجة الأخطاء، وأمثلة لحزم تطوير البرمجيات (SDK)."
weight: 20
---

تسترجع هذه الواجهة البرمجية (REST API) **فواصل الصفحات العمودية** من ورقة عمل.

## واجهة برمجة التطبيقات REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### معاملات الطلب

| اسم المعاملة | النوع | الموقع | الوصف | مطلوب |
| ------------ | ------ | -------- | ---------------------------------------------------- | -------- |
| `name` | string | path | اسم ملف إكسل. | نعم |
| `sheetName` | string | path | اسم ورقة العمل التي سيتم استرجاع الفواصل منها. | نعم |
| `folder` | string | query | المجلد الموجود به الملف في التخزين. | لا |
| `storageName` | string | query | اسم تخزين Aspose Cloud المراد استخدامه. | لا |

تُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/PageBreaks/GetVerticalPageBreaks) واجهة برمجة مفتوحة قابلة للاستخدام العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاء لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "VerticalPageBreaks": {
    "VerticalPageBreakList": [
      {
        "Column": 3,
        "EndRow": 1048575,
        "StartRow": 0
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/VerticalPageBreaks",
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

| الحقل | النوع | الوصف |
| ----------------------- | ------ | ----------------------------------------------------------------------------------- |
| `VerticalPageBreakList` | array | مجموعة من كائنات فاصل الصفحات العمودي. |
| `Column` | int | فهرس العمود (مبني على الصفر) حيث يحدث الفاصل. |
| `StartRow` | int | الصف الأول في نطاق الفاصل (مبني على الصفر). |
| `EndRow` | int | الصف الأخير في نطاق الفاصل (مبني على الصفر، عادةً `1048575` لآخر صف). |
| `link.Href` | string | رابط ذاتي يشير إلى المورد (بروتوكول HTTPS). |
| `Code` | int | رمز حالة HTTP المردود من الخدمة. |
| `Status` | string | وصف نصي لحالة HTTP. |

### معالجة الأخطاء

| رمز HTTP | المعنى | السبب الشائع |
| --------- | --------------------- | ------------------------------------------- |
| 401 | غير مُصدق (Unauthorized) | رمز JWT مفقود أو غير صالح. |
| 404 | غير موجود (Not Found) | الملف أو ورقة العمل المحددة غير موجودة. |
| 400 | طلب غير صالح (Bad Request) | معاملات استعلام غير صالحة أو مشوّهة. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | حالة غير متوقعة على جانب الخادم. |

تحقق من الحقلين `Code` و `Status` في استجابة JSON للحصول على تفاصيل إضافية.

## عائلة حزم تطوير البرمجيات (SDK) السحابية

استخدام حزمة تطوير البرمجيات (SDK) هو أسرع طريقة لتطوير تطبيقات تتفاعل مع Aspose.Cells Cloud. تُجرّد SDK التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على منطق عملك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام حزم تطوير البرمجيات المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetVerticalPageBreaks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetVerticalPageBreaks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetVerticalPageBreaks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetVerticalPageBreaks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetVerticalPageBreaks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetVerticalPageBreaks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetVerticalPageBreaks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetVerticalPageBreaks.go" >}}

{{< /tab >}}

{{< /tabs >}}