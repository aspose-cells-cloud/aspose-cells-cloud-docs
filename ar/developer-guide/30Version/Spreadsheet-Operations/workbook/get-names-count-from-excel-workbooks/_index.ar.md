---
title: "استرجاع الأسماء من ملف Excel"
second_title: "مستند"
linktitle: "الأسماء"
type: docs
url: /get-names-from-an-excel-file/
aliases:
  [
    "/get-names-count-from-excel-workbooks/",
    "/workbook/names/",
    "/workbook/get/names/",
  ]
keywords: "Aspose.Cells, Cloud, Excel, Workbook, Names, REST API, SDK"
description: "استرجاع جميع الأسماء المُعرَّفة من ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن إرشادات المصادقة، مثال cURL، مخطط الاستجابة، معالجة الأخطاء، وأمثلة SDK."
weight: 120
ArticleTitle: "استرجاع الأسماء من ملف Excel – واجهة Aspose.Cells Cloud API"
---

تُعيد هذه الواجهة REST API استرجاع الأسماء المُعرَّفة من ملف Excel.

### **الأمان والمصادقة**

تتطلب واجهات Aspose.Cells Cloud مصادقة تعتمد على رمز <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a>، وهي آمنة.

## واجهة GetWorkbookNames

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/names
```

مُعطَلات الطلب هي:

| اسم المُعطَل | النوع   | الموقع | الوصف                                      |
|-------------|---------|--------|--------------------------------------------|
| name        | string  | path   | اسم ملف Workbook.                          |
| folder      | string  | query  | المجلد الذي يحتوي على ملف Workbook.        |
| storageName | string  | query  | اسم وحدة التخزين التي سيتم استخدامها.      |

يجب أن يتضمّن الطلب الرؤوس (HTTP headers) التالية:

| الرأس           | النوع   | الوصف                                          |
|----------------|---------|------------------------------------------------|
| Authorization  | string  | رمز Bearer JWT (إجباري)                        |
| Accept         | string  | `application/json`                             |
| Content-Type   | string  | `application/json` (للطلبات التي تحتوي على جسم) |

**المصادقة** – تتطلب الواجهة رمز مُفوَّض OAuth2/JWT bearer. احصل على الرمز من `https://api.aspose.cloud/connect/token` باستخدام مُعرِّف العميل (client-id) وسر العميل (client‑secret)، ثم أضف الرأس `Authorization: Bearer <jwt token>` في كل طلب.

يُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkbookNames) واجهة برمجة تطبيقات متاحة عمومًا، ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب. يوضّح المثال التالي كيفية استدعاء واجهة Aspose.Cells Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/names" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Names": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Count": 0,
    "NameList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        }
      }
    ]
  }
}
```

**حقول الاستجابة**

- **Status** _(string)_ – رسالة حالة العملية.
- **Names.link** _(object)_ – معلومات الارتباط التشعبي (Hyperlink) للمجموعة.
- **Names.Count** _(integer)_ – العدد الإجمالي للأسماء المُعرَّفة التي تم إعادتها.
- **Names.NameList** _(array)_ – قائمة كائنات الأسماء؛ يحتوي كل كائن على كائن **link** يحتوي على تفاصيل التنقّل.

**معالجة الأخطاء** – قد تُعيد الخدمة رموز الحالة (HTTP status codes) التالية:

| الرمز | المعنى                  | الإجراء الموصى به                                            |
|-------|--------------------------|-------------------------------------------------------------|
| 401   | غير مُصادَق (Unauthorized) | تأكّد من صحة رمز JWT المُزوَّد.                             |
| 404   | غير موجود (Not Found)     | تحقّق من صحة اسم ملف Workbook والمجلد ووحدة التخزين.       |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | أعد المحاولة لاحقًا، أو اتصل بدعم Aspose إن استمرت المشكلة. |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة للتطوير. يتعامل SDK مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbookNames.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbookNames.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbookNames.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbookNames.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbookNames.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbookNames.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbookNames.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbookNames.go" >}}

{{< /tab >}}

{{< /tabs >}}