---
title: "مسح محتويات وتنسيقات الخلايا في ورقة عمل Excel"
type: docs
url: /ar/clear-contents-and-styles-of-cells-in-excel-worksheet/
weight: 50
keywords:
  - Aspose.Cells
  - Excel API
  - clear cell contents
  - clear cell styles
  - cloud spreadsheet
  - REST API
description: "تعلم كيفية استخدام واجهة Aspose.Cells Cloud REST API لمسح محتويات وتنسيقات الخلايا في ورقة عمل Excel، مع أمثلة باستخدام cURL وأجزاء من أكواد SDK."
ArticleTitle: "مسح محتويات وتنسيقات الخلايا في ورقة عمل Excel – واجهة Aspose.Cells Cloud API"
---

قبل استخدام نقطة النهاية **Clear Contents and Styles**، تأكد من توفر ما يلي:

* رمز <b>JWT</b> صالح تم الحصول عليه من عملية مصادقة Aspose.Cells Cloud.  
* تحميل ملف جدول العمل إلى موقع التخزين الذي اخترته (أو الوصول إليه عبر المعلمة `folder`).  
* تثبيت إصدار SDK المطلوب إذا كنت تفضل استخدام أحد مكتبات العميل المخصصة للغات البرمجة.

تقدم هذه الواجهة البرمجية للخدمات (REST API) إمكانية مسح محتويات الخلايا في ملف Excel.

## واجهة PostClearContents

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/clearcontents
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالات HTTP**

| الرمز | المعنى                      | الوصف                                            |
|------|----------------------------|--------------------------------------------------|
| 200  | OK (نجاح)                  | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request (طلب غير صالح) | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized (غير مصرّح)    | رمز JWT غير صالح أو مفقود. |
| 413  | Payload Too Large (حمولة كبيرة جدًا) | حجم ملف التحميل يتجاوز الحد المسموح. |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostClearContents مع SDKs

### **مواصفات واجهة PostClearContents**

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostClearContents) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/clearcontents?range=A2:C11" \
  -X POST \
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

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام أحد SDKs هو أفضل طريقة لتسريع عملية التطوير. تتعامل SDKs مع التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات Aspose.Cells باستخدام SDKs المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostClearContents.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostClearContents.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostClearContents.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostClearContents.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostClearContents.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostClearContents.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostClearContents.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostClearContents.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Clear Contents and Styles of Cells in an Excel Worksheet",
  "description": "كيفية استخدام واجهة Aspose.Cells Cloud REST API لمسح محتويات وتنسيقات الخلايا في ورقة عمل Excel.",
  "url": "https://docs.aspose.cloud/cells/clear-contents-and-styles-of-cells-in-excel-worksheet/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2023-07-08",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://docs.aspose.cloud/cells/images/Aspose-image-for-open-graph.jpg",
      "caption": "Aspose.Cells Cloud – Clear Contents and Styles of Cells"
    }
  },
  "keywords": "Aspose.Cells, Excel API, clear cell contents, clear cell styles, REST API, cloud spreadsheet"
}
</script>