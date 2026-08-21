---
title: "حذف مرشح من ورقة عمل إكسل – واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktitle: "حذف المرشح"
type: docs
url: /delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/, /delete-auto-filter/]
keywords: "Aspose.Cells Cloud حذف المرشح، إكسل، واجهة REST API، حزم التطوير (SDK)"
description: "تعرّف على كيفية حذف مرشح تلقائي من ورقة عمل إكسل باستخدام واجهة Aspose.Cells Cloud REST API وواجهة cURL وحزم التطوير (SDK) (C#، Java، Python، إلخ). تتضمن النقطة النهائية (endpoint)، المعلمات، المصادقة، ونماذج من الأكواد."
weight: 100
---

## واجهة REST API

تحذف هذه الواجهة من نوع REST **المرشح التلقائي (AutoFilter)** من ورقة عمل إكسل.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **الأمان والمصادقة**

واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة              | النوع    | الموقع   | مطلوب؟ | الوصف                                                                                   |
| ------------------------- | -------- | -------- | ------ | ----------------------------------------------------------------------------------------- |
| **name**                  | سلسلة   | المسار   | نعم    | اسم ملف المصنف.                                                                          |
| **sheetName**             | سلسلة   | المسار   | نعم    | اسم ورقة العمل.                                                                          |
| **range**                 | سلسلة   | الاستعلام | لا     | النطاق الخلايا الذي يطبّق عليه المرشح (مثال: `A1:C10`).                                 |
| **fieldIndex**            | عدد صحيح | الاستعلام | نعم    | المؤشر المبدئي (صفر) للعمود الذي يطبّق عليه المرشح.                                     |
| **dateTimeGroupingType**  | سلسلة   | الاستعلام | لا     | طريقة تجميع قيم التاريخ/الوقت: `Day`، `Hour`، `Minute`، `Month`، `Second`، أو `Year`.    |
| **year**                  | عدد صحيح | الاستعلام | لا     | مكوّن السنة للتجميع حسب السنة.                                                           |
| **month**                 | عدد صحيح | الاستعلام | لا     | مكوّن الشهر للتجميع حسب الشهر.                                                           |
| **day**                   | عدد صحيح | الاستعلام | لا     | مكوّن اليوم للتجميع حسب اليوم.                                                           |
| **hour**                  | عدد صحيح | الاستعلام | لا     | مكوّن الساعة للتجميع حسب الساعة.                                                        |
| **minute**                | عدد صحيح | الاستعلام | لا     | مكوّن الدقيقة للتجميع حسب الدقيقة.                                                       |
| **second**                | عدد صحيح | الاستعلام | لا     | مكوّن الثانية للتجميع حسب الثانية.                                                      |
| **matchBlanks**           | منطقي   | الاستعلام | لا     | `true` / `false` – ما إذا كانت الخلايا الفارغة تُضمَّن في المرشح أم لا.                   |
| **refresh**               | منطقي   | الاستعلام | لا     | `true` / `false` – ما إذا كان سيتم تحديث ورقة العمل بعد الحذف أم لا.                      |
| **folder**                | سلسلة   | الاستعلام | لا     | مجلد المصنف الأصلي.                                                                     |
| **storageName**           | سلسلة   | الاستعلام | لا     | اسم وحدة التخزين.                                                                        |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                                                 |
|------|----------------------------|-----------------------------------------------------------------------|
| 200  | OK (تم بنجاح)             | تم تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.          |
| 400  | Bad Request (طلب خاطئ)    | معلمات ناقصة أو غير صالحة (مثل: نوع ملف غير مدعوم).                 |
| 401  | Unauthorized (غير مصرّح)   | رمز JWT غير صالح أو مفقود.                                            |
| 413  | Payload Too Large (الحمولة كبيرة جدًا) | ملف المرفوع يتجاوز الحد الأقصى للحجم.                             |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                          |

## كيفية استخدام واجهة DeleteWorksheetFilter باستخدام حزم التطوير (SDKs)

### مواصفات واجهة DeleteWorksheetFilter

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
  -X DELETE \
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

### استخدام حزم التطوير (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام حزمة التطوير (SDK) هو الطريقة الأكثر كفاءة لتسريع عملية التطوير. وتتولى حزمة التطوير إدارة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بحزم التطوير الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الأكواد التالية كيفية إجراء مكالمات إلى خدمات Aspose.Cells عبر الويب باستخدام حزم تطوير مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}