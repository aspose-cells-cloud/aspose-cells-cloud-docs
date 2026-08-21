---
title: "نسخ الأعمدة في ورقة عمل Excel"
second_title: "مستند"
linktitle: "نسخ"
type: docs
url: /columns/copy/
aliases:
  [/copy-columns-in-excel-worksheet/, /copy-columns-in-an-excel-worksheet/]
keywords: "Aspose.Cells, نسخ الأعمدة, واجهة برمجة تطبيقات Excel, REST, واجهات برمجة التطبيقات السحابية, cURL, C#, Java, Python, Ruby, Node.js, Go, Perl"
description: "تعرّف على كيفية نسخ عمود واحد أو أكثر في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن بناء جملة الطلب، المعلمات المطلوبة، تفاصيل المصادقة، معالجة الأخطاء، وأمثلة لواجهات برمجة التطبيقات (SDKs) بلغات C# وJava وPython وRuby وNode.js وGo وPerl وغيرها."
articleTitle: "نسخ الأعمدة في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
weight: 30
---

تقوم هذه الواجهة البرمجية (REST API) بنسخ **الأعمدة** في ورقة عمل Excel. وتتيح عملية **نسخ الأعمدة** تكرار عمود واحد أو نطاق من الأعمدة وإدراج النسخة في موقع محدّد ضمن نفس ورقة العمل. استخدم هذه الواجهة لنسخ الأعمدة بكفاءة عند التعامل مع جداول بيانات كبيرة، وراجع العمليات ذات الصلة مثل [إضافة عمود](/columns/add/) و[إخفاء عمود](/columns/hide/) لإكمال مهام إدارة الأعمدة الأخرى.

## الأمان والمصادقة
واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة مبنية على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة التطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/copy
```

### معلمات الطلب

| اسم المعلمة               | النوع    | الموقع  | الوصف                                                                                      |
| -------------------------- | ------- | -------- | ------------------------------------------------------------------------------------- |
| **name**                   | نص (string)  | مسار (path)     | اسم ملف المصنف.                                                                    |
| **sheetName**              | نص (string)  | مسار (path)     | اسم ورقة العمل.                                                                   |
| **sourceColumnIndex**      | عدد صحيح (integer) | استعلام (query)    | فهرس العمود المراد نسخه (يبدأ من الصفر).                                                  |
| **destinationColumnIndex** | عدد صحيح (integer) | استعلام (query)    | فهرس الموضع المراد إدراج الأعمدة المنسوخة فيه (يبدأ من الصفر).                            |
| **columnNumber**           | عدد صحيح (integer) | استعلام (query)    | عدد الأعمدة المتتالية المراد نسخها.                                                |
| **worksheet**              | نص (string)  | استعلام (query)    | _(اختياري)_ مُعرّف ورقة العمل يُستخدم عندما يختلف اسم ورقة العمل عن ما ورد في المسار. |
| **folder**                 | نص (string)  | استعلام (query)    | مسار المجلد الذي يحتوي على المصنف في مساحة التخزين السحابية لـ Aspose.                   |

يمكنك الاطّلاع على [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostCopyWorksheetColumns) للحصول على العقد الكاملة لهذه العملية.

### مثال باستخدام cURL

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/copy?sourceColumnIndex=1&destinationColumnIndex=12&columnNumber=10" \
     -H "Authorization: Bearer $ASPOSE_TOKEN" \
     -H "accept: application/json"
```

### الاستجابة

```json
{
  "Code": 200,
  "Status": "OK"
}
```

## معالجة الأخطاء

تعيد الواجهة رموز الحالة القياسية (HTTP Status Codes) مع جسم استجابة بصيغة JSON يصف الخطأ.

| رمز الحالة | المعنى                                          | مثال على جسم JSON                                                   |
| ----------- | ------------------------------------------------ | ------------------------------------------------------------------- |
| **400**     | طلب غير صالح – معلمات غير صحيحة                 | `{ "Code": 400, "Message": "فهرس عمود غير صالح." }`               |
| **401**     | غير مصرّح – رمز وصول مفقود أو غير صالح          | `{ "Code": 401, "Message": "رمز الوصول غير صالح أو منتهٍ." }` |
| **404**     | غير موجود – المصنف أو ورقة العمل غير موجودين | `{ "Code": 404, "Message": "لم يتم العثور على المصنف." }`                 |
| **500**     | خطأ داخلي في الخادم – ظرف غير متوقّع             | `{ "Code": 500, "Message": "حدث خطأ غير متوقّع." }`       |

> **كيفية استكشاف الأخطاء وحلّها:** تحقّق من أن رمز الوصول ساري المفعول، وأن اسم المصنف وورقة العمل صحيحان، وأن قيم `sourceColumnIndex` و`destinationColumnIndex` و`columnNumber` تقع ضمن نطاق أعمدة ورقة العمل.

## عائلة واجهات برمجة التطبيقات السحابية (Cloud SDK Family)

يُعدّ استخدام مكتبات SDK أفضل طريقة لتسريع عملية التطوير، إذ تُدار التفاصيل منخفضة المستوى تلقائيًا، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بواجهات برمجة تطبيقات Aspose.Cells Cloud SDK.

تُظهر الأمثلة التالية كيفية إجراء مكالمات لخدمات الويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCopyWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCopyWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCopyWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCopyWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCopyWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCopyWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCopyWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCopyWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "كيف أُجري المصادقة عند استدعاء واجهة برمجة تطبيقات نسخ الأعمدة؟",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "احصل على رمز وصول OAuth2 من Aspose Cloud باستخدام مُعرّف العميل والسر الخاصّين بك، ثم أدرج الرمز في رأس الطلب كـ `Authorization: Bearer <access_token>`."
      }
    },
    {
      "@type": "Question",
      "name": "ما الفرق بين `sourceColumnIndex` و`destinationColumnIndex`؟",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "يُمثل `sourceColumnIndex` فهرس العمود (الذي يبدأ من الصفر) الذي ترغب في نسخه، بينما يُمثل `destinationColumnIndex` فهرس الموضع (الذي يبدأ من الصفر) الذي سيتم إدراج الأعمدة المنسوخة فيه."
      }
    },
    {
      "@type": "Question",
      "name": "ما الاستجابة التي أتلقّاها في حال فشل عملية النسخ؟",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "تعيد الواجهة رمز حالة غير مساوٍ لـ 200 (مثل 400 لطلب غير صالح أو 401 لحالة عدم مصرّح). ويحتوي جسم الاستجابة على كائن JSON يحتوي على حقلَي `Code` و`Message` اللذين يصفان طبيعة الخطأ."
      }
    }
  ]
}
</script>
---