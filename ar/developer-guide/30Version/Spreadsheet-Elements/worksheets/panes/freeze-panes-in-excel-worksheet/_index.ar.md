---
title: "تجميد الأقسام في ورقة عمل Excel"
second_title: "مستند"
linktitle: "تجميد"
type: docs
url: /ar/worksheets/panes/freeze/
aliases: [  /ar/freeze-panes-in-excel-worksheet/ , /ar/worksheets/freeze-panes/ ]
keywords: "Aspose.Cells Cloud, تجميد الأقسام, Excel, REST API, ورقة العمل"
description: "تعرّف على كيفية تجميد الصفوف والأعمدة في ورقة عمل Excel باستخدام REST API الخاص بـ Aspose.Cells Cloud. يتضمّن بنية نقطة نهاية التوصيل، والمعلمات المطلوبة، ومثال على استخدام cURL، وإرشادات المصادقة، وتفاصيل استجابة الأخطاء، وأكواد أمثلة باستخدام SDKs بلغات برمجة متعددة."
weight: 190
---

تُستخدم هذه الواجهة البرمجية **لتحديد** تجميد الأقسام في ورقة عمل Excel.

## واجهة REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

تتضمن معلمات الطلب ما يلي:

| اسم المعلمة   | النوع    | الموقع  | الوصف                                              |
| -------------- | ------- | ------- | --------------------------------------------------- |
| name           | string  | path    | اسم ملف المصنف.                                     |
| sheetName      | string  | path    | اسم ورقة العمل التي سيتم تجميد أقسامها فيها.         |
| row            | integer | query   | الفهرس الصفرِي للصف الأول **غير المُجمّد**.          |
| column         | integer | query   | الفهرس الصفرِي للعمود الأول **غير المُجمّد**.        |
| frozenRows     | integer | query   | عدد الصفوف المراد تجميدها ابتداءً من الأعلى.         |
| frozenColumns  | integer | query   | عدد الأعمدة المراد تجميدها ابتداءً من اليسار.         |
| folder         | string  | query   | مسار المجلد في التخزين حيث يقع المصنف.               |
| storageName    | string  | query   | اسم خدمة التخزين.                                   |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) واجهة برمجة قابلة للوصول من خارج النظام، ويتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### استجابة الأخطاء

| حالة HTTP                 | الكود | الرسالة                         | المثال                                                  |
| ------------------------- | ---- | ------------------------------- | -------------------------------------------------------- |
| 400 Bad Request           | 400  | معلمات غير صالحة                | `{ "Code": 400, "Message": "قيمة frozenRows غير صالحة" }` |
| 401 Unauthorized          | 401  | رمز JWT مفقود أو غير صالح      | `{ "Code": 401, "Message": "رمز الوصول غير صالح" }`     |
| 404 Not Found             | 404  | المصنف أو ورقة العمل غير موجود | `{ "Code": 404, "Message": "الملف غير موجود" }`           |
| 500 Internal Server Error | 500  | خطأ غير متوقع في الخادم         | `{ "Code": 500, "Message": "خطأ داخلي في الخادم" }`    |

## عائلة SDK للسحابة

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. فتتولى SDK معالجة التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات Aspose.Cells عبر وسائل مختلفة باستخدام SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}