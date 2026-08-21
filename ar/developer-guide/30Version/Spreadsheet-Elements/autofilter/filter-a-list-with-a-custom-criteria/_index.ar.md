---
title: "إضافة معيار مخصص في ورقة عمل إكسل"
second_title: "وثيقة"
linktitle: "إضافة تصفية مخصصة"
type: docs
url: /autofilter/add-custom-filter/
aliases: [/filter-a-list-with-a-custom-criteria/,/autofilter/add-a-custom-filter/]
keywords: "إكسل، تصفية مخصصة، Aspose.Cells Cloud، واجهة برمجة تطبيقات REST، تصفية تلقائية، ورقة عمل، معيار مخصص"
description: "تعرّف على كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST لإضافة تصفية مخصصة إلى ورقة عمل إكسل. يتضمّن تفاصيل الطلب، مثالًا باستخدام cURL، وأجزاء من كود SDK بلغات برمجة متعددة."
weight: 65
ArticleTitle: "إضافة معيار مخصص في ورقة عمل إكسل – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تُطبّق هذه واجهة برمجة تطبيقات REST تصفيةً لقائمة باستخدام **معيار مخصص**.

## PutWorksheetCustomFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب:

| اسم المعامل | النوع | الموقع | الوصف |
|-------------|-------|--------|--------|
| name | سلسلة نصية | المسار | اسم ملف إكسل. |
| sheetName | سلسلة نصية | المسار | اسم ورقة العمل التي تحتوي على البيانات المراد تصفيتها. |
| range | سلسلة نصية | الاستعلام | النطاق الخلوي الذي سيتم تطبيق التصفية عليه (مثال: `A1:B1`). |
| fieldIndex | عدد صحيح | الاستعلام | المؤشر الصفر-based للعمود الذي تُطبّق عليه التصفية. |
| operatorType1 | سلسلة نصية | الاستعلام | عامل المقارنة الأول (مثال: `LessOrEqual`، `Equal`). |
| criteria1 | سلسلة نصية | الاستعلام | القيمة أو التعبير الأول للتصفية. |
| isAnd | منطقي | الاستعلام | إذا كانت القيمة `true`، تُدمج المعياران باستخدام **AND**؛ وإلا باستخدام **OR**. |
| operatorType2 | سلسلة نصية | الاستعلام | عامل المقارنة الثاني (اختياري). |
| criteria2 | سلسلة نصية | الاستعلام | القيمة أو التعبير الثاني للتصفية (اختياري). |
| matchBlanks | منطقي | الاستعلام | عند القيمة `true`، تُضمّن الخلايا الفارغة في نتائج التصفية. |
| refresh | منطقي | الاستعلام | إذا كانت القيمة `true`، تُجبر ورقة العمل على التحديث بعد تطبيق التصفية. |
| folder | سلسلة نصية | الاستعلام | مسار المجلد في التخزين حيث يقع الملف. |
| storageName | سلسلة نصية | الاستعلام | اسم خدمة التخزين. |

### **الاستجابة**

```json
{
    "Status":"OK",
    "Code":200
}
```

**كود حالات HTTP**

| الكود | المعنى | الوصف |
|-------|--------|--------|
| 200 | OK (نجاح) | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request (طلب غير صالح) | معاملات مفقودة أو غير صحيحة (مثال: نوع ملف غير مدعوم). |
| 401 | Unauthorized (غير مصادق) | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large (حمولة كبيرة جدًا) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PutWorksheetCustomFilter API باستخدام SDKs

### مواصفات واجهة PutWorksheetCustomFilter API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) واجهة برمجة تطبيقات عامة قابلة للاستدعاء، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
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


### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDKs هو أسرع طريقة للتطوير. تُعالج SDKs التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

لعمليات التصفية التلقائية الأخرى، مثل إضافة تصفية قياسية أو تصفية تاريخ، راجع صفحات الوثائق ذات الصلة ضمن قسم التصفية التلقائية.