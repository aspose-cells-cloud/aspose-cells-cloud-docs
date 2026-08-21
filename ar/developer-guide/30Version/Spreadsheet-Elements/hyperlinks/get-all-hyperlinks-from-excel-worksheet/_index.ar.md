---
title: "الحصول على جميع الروابط التشعبية – واجهة Aspose.Cells Cloud REST API"
type: docs
url: /ar/hyperlinks/get-all/
aliases:
  [/get-hyperlink-from-excel-worksheet/, /get-hyperlinks-from-excel-worksheet/]
keywords: "Aspose.Cells، الحصول على جميع الروابط التشعبية، API للجداول المحسوبة، واجهة REST API، حزمة SDK للحوسبة السحابية، مثال باستخدام cURL، روابط تشعبية في الجداول المحسوبة"
description: "استرجاع جميع الروابط التشعبية من ورقة عمل في ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن عنوان HTTPS، المعلمات المطلوبة، مثال باستخدام cURL، مخطط الاستجابة، وأمثلة للكود باستخدام SDKs."
weight: 10
ArticleTitle: "الحصول على جميع الروابط التشعبية – وثائق Aspose.Cells Cloud REST API"
---

تسترجع هذه الواجهة **جميع الروابط التشعبية** من ورقة عمل محددة في ملف Excel.

## الأمان والمصادقة

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة قائمة على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### معلمات الطلب

| اسم المعلمة | النوع | الموقع | مطلوبة | القيمة الافتراضية | الوصف |
|------------|-------|--------|--------|------------------|-------|
| name | string | path | نعم | – | اسم ملف Excel. |
| sheetName | string | path | نعم | – | اسم ورقة العمل. |
| folder | string | query | لا | – | المجلد الذي يحتوي على الملف. |
| storageName | string | query | لا | – | اسم خدمة التخزين المراد استخدامها. |

يعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Hyperlinks/GetWorksheetHyperlinks) واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتسمح لك بإجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء الواجهة باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Hyperlinks": {
    "Count": 4,
    "HyperlinkList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/1",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/2",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "link": {
          "Href": "/3",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": null
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

تحتوي استجابة JSON على كائن `Hyperlinks`.

- **Count** – العدد الإجمالي للروابط التشعبية في ورقة العمل.
- **HyperlinkList** – مصفوفة تحتوي كل عنصر فيها على كائن `link`. تحتوي الخاصية `Href` على عنوان الرابط التشعبي، بينما توفر الخاصيتان `Rel` و `Title` و `Type` معلومات وصفية إضافية (غالبًا تكون قيمتها `null` للروابط البسيطة).

### استجابات الخطأ

| كود HTTP | السبب | مثال على جسم الاستجابة |
|---------|-------|----------------------|
| **400** | طلب غير صالح – معلمات مفقودة أو غير صالحة. | `{ "Code":"400", "Message":"Invalid parameter value." }` |
| **401** | غير مصادق – رمز JWT مفقود أو غير صالح. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404** | غير موجود – ملف Excel أو ورقة العمل غير موجودة. | `{ "Code":"404", "Message":"File not found." }` |
| **500** | خطأ داخلي في الخادم – فشل غير متوقع في الخادم. | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

## عائلة حزم SDK للحوسبة السحابية

استخدام حزمة SDK هو أسرع طريقة لدمج هذه الوظيفة. تقوم حزم SDK بإدارة التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على منطق تطبيقك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على القائمة الكاملة لحزم SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام حزم SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}