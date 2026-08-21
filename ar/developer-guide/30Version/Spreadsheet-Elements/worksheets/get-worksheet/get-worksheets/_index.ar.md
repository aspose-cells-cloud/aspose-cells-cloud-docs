---
title: "الحصول على جميع أوراق العمل"
second_title: "Document"
linktitle: "الكل"
type: docs
url: /ar/worksheets/get-all/
aliases: [  /ar/get-worksheet-count/ ]
keywords: "Aspose.Cells، واجهة Cloud API، الحصول على أوراق العمل، Excel، REST، SDK"
description: "استرجاع قائمة أوراق العمل الموجودة في ملف Excel عبر واجهة Aspose.Cells Cloud REST API (النسخة 3.0). يشمل مثالًا باستخدام cURL، وأجزاء من الشيفرة البرمجية باستخدام SDKs، وتنسيق الاستجابة."
weight: 10
---

تقدم هذه الواجهة (REST API) معلومات حول أوراق العمل الموجودة داخل ملف جدول بيانات.

## واجهة REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **معطيات الطلب**

| اسم المعطى | النوع | الموقع | الوصف |
|-----------|-------|--------|--------|
| name | string | path | اسم ملف Excel. |
| folder | string | query | المجلد الذي يحتوي على الملف. |
| storageName | string | query | اسم وحدة التخزين المراد استخدامها. |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheets) واجهة برمجية قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells Cloud. يُظهر المثال التالي طلب GET لاسترجاع أوراق العمل.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": {
    "WorksheetList": [
      {
        "link": {
          "Href": "/Sheet1",
          "Rel": "self"
        }
      },
      {
        "link": {
          "Href": "/Sheet2",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## معالجة الأخطاء

الأكواد الشائعة لحالات الحالة HTTP التي تُرجعها هذه الواجهة:

| الكود | المعنى | الوصف |
|------|--------|-------|
| 400 | Bad Request (طلب غير صالح) | معطى مطلوب مفقود (مثل `name`). |
| 401 | Unauthorized (غير مصرّح) | رمز JWT غير صالح أو مفقود. |
| 404 | Not Found (غير موجود) | ملف العمل المحدد غير موجود. |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | حالة غير متوقعة في الخادم. |

تُعاد استجابات الأخطاء بصيغة JSON، مثال:

```json
{
  "Code": "401",
  "Message": "Invalid access token."
}
```

## مجموعة أدوات SDK للسحابة

استخدام SDK يُعدّ أفضل طريقة لتسريع عملية التطوير، حيث تُعالج SDKs التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الشيفرة البرمجية التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}