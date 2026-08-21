---
title: "الحصول على وصف الصف من ورقة عمل Excel"
second_title: "مستند"
linktitle: "صف"
type: docs
url: /rows/get/row/
aliases: [/get-row-from-a-worksheet/]
keywords: "Aspose.Cells Cloud, API صف Excel, الحصول على صف ورقة العمل, REST API, .NET SDK, Java SDK, Python SDK"
description: "استرجاع معلومات مفصّلة (مثل الارتفاع، النمط، الحالة المخفية، إلخ) لصف معيّن في ورقة عمل Excel باستخدام Aspose.Cells Cloud REST API. يشمل مثالًا لـ curl، وأجزاء من أكواد SDK، ومعالجة الأخطاء."
weight: 10
ArticleTitle: "الحصول على وصف الصف من ورقة عمل Excel – Aspose.Cells Cloud API"
---

**المتطلبات المسبقة:**  
- احصل على رمز وصول JWT صالح وشّمله في الرأس `Authorization: Bearer <jwt token>`.  
- تأكّد من أن ملفّ المصنف مخزّن في مستودع Aspose Cloud، أو حدد مسار المجلّد الذي يوجد فيه.  
- استخدم إصدار API **v3.0** كما هو مبيّن في عنوان URL للنهاية.

تُعيد هذه الواجهة البرمجية لـ REST استرجاع بيانات الصف باستخدام فهرسه في ورقة عمل Excel.

## واجهة GetWorksheetRow البرمجية

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **الأمان والمصادقة**

تُعدّ واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلّمات الطلب**

| اسم المعلّمة | النوع | الموقع | الوصف |
| -------------- | ------- | -------- | --------------------------------------------------- |
| name | string | path | اسم ملف المصنف. |
| sheetName | string | path | اسم ورقة العمل داخل المصنف. |
| rowIndex | integer | path | الفهرس بصيغة الصفر-مبني للصف المراد استرجاعه. |
| folder | string | query | المجلّد الذي يحتوي على المصنف. |
| storageName | string | query | اسم المستودع الذي يوجد فيه المصنف. |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفّح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL. شمّل الرأس `Authorization: Bearer <jwt token>` لمصادقة الطلب.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**مخطط الاستجابة**

| الخاصية | النوع | الوصف |
|-------------------|---------|----------------------------------------------------------------------|
| `GroupLevel` | integer | المستوى التفصيلي (المحوري) للصف (يُستخدم للتجميع). |
| `Height` | number | ارتفاع الصف بوحدات النقاط. |
| `Index` | integer | الفهرس بصيغة الصفر-مبني للصف المُعاد. |
| `IsBlank` | boolean | يشير إلى ما إذا كان الصف يحتوي على أي بيانات. |
| `IsHeightMatched`| boolean | `true` إذا كان ارتفاع الصف مطابقًا لارتفاع الصف الافتراضي. |
| `IsHidden` | boolean | `true` إذا كان الصف مخفيًّا. |
| `Style` | object | كائن يحتوي على معلومات النمط للصف. |
| `link` | object | مرجع رابط تشعبي إلى مورد الصف. |
| `Code` | integer | رمز حالة HTTP للاستجابة. |
| `Status` | string | وصف نصّي للحالة (مثل "OK"). |

{{< /tab >}}

{{< /tabs >}}

**ملاحظات / معالجة الأخطاء:** قد تُعيد الواجهة البرمجية رموز الحالة التالية لـ HTTP:

- **200** – نجاح; تُعاد بيانات الصف.  
- **401** – غير مصادق; رمز JWT مفقود أو غير صالح.  
- **404** – غير موجود; المصنف أو ورقة العمل أو الصف المحدّد غير موجود.  
- **500** – خطأ داخلي في الخادم; حدثت حالة غير متوقّعة.

| الكود | الوصف | التصحيح |
|------|-----------------------------------------------|------------------------------------------|
| 200 | نجاح – تُعاد بيانات الصف. | – |
| 401 | غير مصادق – رمز JWT مفقود أو غير صالح. | قدم رمز JWT صالحًا. |
| 404 | غير موجود – المصنف أو ورقة العمل أو الصف مفقود. | تأكّد من أسماء الملفات وفهرس الصف. |
| 500 | خطأ داخلي في الخادم – حالة غير متوقّعة. | اتّصل بدعم Aspose. |

للحصول على قائمة كاملة برموز الأخطاء، راجع [مستند رموز الأخطاء](https://docs.aspose.cloud/cells/) في Aspose.Cells Cloud.

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لتطوير التطبيقات. SDK يُجرّد التفاصيل منخفضة المستوى لتمكينك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}