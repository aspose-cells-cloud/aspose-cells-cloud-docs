---
title: "الحصول على رابط تشعبي في ورقة العمل"
type: docs
url: /ar/hyperlinks/get/
keywords: "Aspose.Cells Cloud, الحصول على رابط تشعبي في ورقة العمل, API للروابط التشعبية في Excel, REST, المصادقة بـ JWT, ورقة عمل Excel, نقطة نهاية API"
description: "استرجاع رابط تشعبي محدد من ورقة عمل Excel باستخدام Aspose.Cells Cloud API (الإصدار 3.0). يتضمن نقطة النهاية، المعلمات، مثال باستخدام cURL، تفاصيل المصادقة، التعامل مع الأخطاء، وأكواد مقتطفات من SDKs."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – الحصول على رابط تشعبي في ورقة العمل"
---

تسترجع هذه الواجهة البرمجية (REST API) **الرابط التشعبي** في ورقة العمل باستخدام **واجهة Aspose.Cells Get Hyperlink API**.

## الأمان والمصادقة

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).  
قبل استدعاء نقطة النهاية، احصل على رمز وصول JWT باستخدام مُعرِّف العميل (Client ID) وسر العميل (Client Secret)، ثم ضعه في رأس الطلب `Authorization: Bearer <jwt token>`.

## واجهة برمجة التطبيقات (REST API)

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

### معلمات الطلب

| اسم المعلمة | النوع | الموقع | الوصف |
| ------------ | ------- | -------- | ---------------------------------------------- |
| name | string | path | اسم ملف Excel. |
| sheetName | string | path | اسم ورقة العمل التي تحتوي على الرابط. |
| hyperlinkIndex | integer | path | الفهرس بصفر كبداية للرابط التشعبي المراد استرجاعه. |
| folder | string | query | المجلد الذي يتم فيه تخزين المستند. |
| storageName | string | query | اسم خدمة التخزين. |

### استجابات الأخطاء

| رمز HTTP | السبب | مثال على جسم الاستجابة |
| --------- | -------------------------------------------------- | ------------------------------------------------------------------- |
| **400** | طلب غير صالح – معلمات مفقودة أو غير صحيحة. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | غير مصرّح به – رمز JWT مفقود أو غير صالح. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | غير موجود – ملف العمل أو ورقة العمل غير موجودة. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | خطأ داخلي في الخادم – فشل غير متوقع في الخادم. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

تُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlink) واجهة برمجة قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء استدعاء لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlink": {
    "Address": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "Area": {
      "EndColumn": 0,
      "EndRow": 1,
      "StartColumn": 0,
      "StartRow": 1
    },
    "ScreenTip": null,
    "TextToDisplay": "https://docs.aspose.cloud/display/cellscloud/Get+Hyperlink+from+Excel+Worksheet",
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/hyperlinks/1",
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

## عائلة SDKs السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}