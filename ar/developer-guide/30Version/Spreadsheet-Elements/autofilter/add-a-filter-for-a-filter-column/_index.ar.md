---
title: "إضافة مرشّح في ورقة عمل Excel"
second_title: "مستند"
linktitle: "إضافة مرشّح"
type: docs
url: /ar/autofilter/add-filter/
aliases: [  /ar/add-a-filter-for-a-filter-column/ ]
keywords: "Aspose.Cells, سحابة, Excel, المرشّح التلقائي، إضافة مرشّح، واجهة برمجة تطبيقات REST، مكتبة تطوير برمجيات"
description: "تعرّف على كيفية إضافة مرشّح تلقائي إلى عمود في ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمّن أمثلة cURL ومكتبات تطوير برمجيات (SDK) ودليل المعاملات."
weight: 60
ArticleTitle: "إضافة مرشّح في ورقة عمل Excel باستخدام Aspose.Cells Cloud"
---

**المتطلبات المسبقة:** قبل استدعاء هذه الواجهة، يجب عليك الحصول على رمز JWT صالح، والتأكّد من أن مصنف العمل المستهدف مُحمّل في التخزين المحدّد، وامتلاك الصلاحيات اللازمة للوصول إلى الملف. يُوصى باستخدام إصدار حديث من cURL (7.68 أو أحدث) لتشغيل الأمثلة المبنية على سطر الأوامر.

تضيف هذه الواجهة البرمجية للخدمات REST مرشّحًا لعمود معيّن في ورقة عمل Excel.

## واجهة PutWorksheetFilter البرمجية

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف |
|-------------|---------|--------|--------|
| name        | string  | Path   | اسم مصنف العمل. |
| sheetName   | string  | Path   | اسم ورقة العمل. |
| range       | string  | Query  | النطاق الخلوي الذي يحتوي على المرشّح (مثل `A1:B1`). |
| fieldIndex  | integer | Query  | الفهرس الصفري (zero-based) للعمود الذي يُطبّق عليه المرشّح. |
| criteria    | string  | Query  | معايير المرشّح (مثل قيمة أو تعبير). |
| matchBlanks | boolean | Query  | اضبطها على `true` لتضمين الخلايا الفارغة في المرشّح، وإلا فاضبطها على `false`. |
| refresh     | boolean | Query  | اضبطها على `true` لتحديث المرشّح بعد تطبيقه، وإلا فاضبطها على `false`. |
| folder      | string  | Query  | المجلد الذي يخزّن فيه مصنف العمل الأصلي. |
| storageName | string  | Query  | اسم خدمة التخزين. |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                        | الوصف |
|-------|-------------------------------|--------|
| 200   | OK (نجاح)                     | تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب خاطئ)        | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | Unauthorized (غير مُعتمد)      | رمز JWT غير صالح أو مفقود. |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقّع في الخادم. |

## كيفية استخدام واجهة PutWorksheetFilter مع مكتبات تطوير البرمجيات (SDKs)

### مواصفات واجهة PutWorksheetFilter

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">مواصفة OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells Web. يوضح المثال التالي كيفية استدعاء الواجهة باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
-X PUT \
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

### استخدام مكتبات Aspose.Cells Cloud SDKs

استخدام مكتبة تطوير برمجيات (SDK) هو أسرع طريقة لتطوير التطبيقات. فهي تتعامل مع التفاصيل الدقيقة من المستوى المنخفض، مما يتيح لك التركيز على مشروعك. يُرجى مراجعة <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDKs.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells Web باستخدام مكتبات تطوير برمجيات متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
---