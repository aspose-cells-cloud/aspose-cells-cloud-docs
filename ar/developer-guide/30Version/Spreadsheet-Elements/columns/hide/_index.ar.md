---
title: "إخفاء أعمدة في ورقة عمل Excel"
second_title: "مستند"
linktitle: "إخفاء"
type: docs
url: /ar/columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, واجهة برمجة تطبيقات لإخفاء الأعمدة, إخفاء عمود في Excel, واجهة REST API لإخفاء الأعمدة, Aspose.Cells SDK, أتمتة جداول البيانات"
description: "تعلم كيفية إخفاء عمود واحد أو أكثر في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). تتضمن النقطة النهائية (endpoint)، المعاملات، مثال باستخدام cURL، أمثلة لرموز SDK، وإجراءات معالجة الأخطاء."
weight: 40
---

تقوم هذه الواجهة البرمجية (REST API) بإخفاء أعمدة في ورقة عمل.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### معاملات الطلب

| اسم المعاملة | النوع     | الموقع    | الوصف                                                                 |
|--------------|-----------|-----------|------------------------------------------------------------------------|
| name         | string    | path      | اسم ملف المصنف (workbook).                                            |
| sheetName    | string    | path      | اسم ورقة العمل التي سيتم إخفاء الأعمدة فيها.                         |
| startColumn  | integer   | query     | المؤشر الصفري (zero-based) للعمود الأول الذي سيتم إخفاؤه.           |
| totalColumns | integer   | query     | عدد الأعمدة المتتالية التي سيتم إخفاؤها، ابتداءً من **startColumn**. |
| folder       | string    | query     | المسار إلى المجلد الذي يحتوي على المصنف.                             |
| storageName  | string    | query     | اسم خدمة التخزين التي يوجد فيها الملف.                                |

يعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) واجهة برمجة تطبيقات متاحة عمومًا، وتتيح لك إجراء تفاعلات REST مباشرةً من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إخفاء عمود باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**رموز الاستجابة المحتملة**

| الرمز HTTP | المعنى                                   | مثال JSON (خطأ)                                      |
|------------|-------------------------------------------|------------------------------------------------------|
| 200        | نجاح                                      | `{ "Code": 200, "Status": "OK" }`                   |
| 400        | طلب غير صالح (مثل: معاملات غير صحيحة)   | `{ "Code": 400, "Message": "نطاق أعمدة غير صالح." }` |
| 401        | غير مصرّح (مفتاح وصول مفقود أو غير صالح) | `{ "Code": 401, "Message": "مفتاح وصول غير صالح." }` |
| 404        | غير موجود (المصنف أو ورقة العمل)         | `{ "Code": 404, "Message": "الملف غير موجود." }`    |
| 500        | خطأ داخلي في الخادم                       | `{ "Code": 500, "Message": "خطأ غير متوقع." }`      |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لتطوير التطبيقات. فالـ SDK يُجرّدك من التفاصيل منخفضة المستوى، مما يمكّنك من التركيز على منطق أعمالك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}