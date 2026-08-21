---
title: "Aspose.Cells Cloud – تحويل نطاق Excel إلى HTML"
description: "تحويل نطاق محدد من ملف Excel (مثل A1:C10) إلى ملف HTML باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يتضمن المصادقة، أمثلة على الطلبات، معالجة الاستجابات، مقاطع كود SDK، وأكواد الأخطاء."
keywords: "Aspose.Cells, Excel إلى HTML, تحويل النطاق, واجهة برمجة تطبيقات سحابية, جدول بيانات"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

تحويل نطاق محدد من ملف Excel محلي إلى ملف HTML مباشرةً عبر Aspose.Cells Cloud. تتم عملية التحويل بالكامل على خوادم السحابة، لذا لا تحتاج أبدًا إلى تحميل الملف الكامل أو تثبيت Excel محليًا.

## واجهة برمجة تطبيقات تحويل النطاق إلى HTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

يحتوي جسم الطلب على `multipart/form-data` يحتوي ملف جدول البيانات. وتُزوَّد جميع الخيارات الأخرى كمعلّمات استعلام.

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| الاسم               | النوع    | الموقع       | الإجباري | الوصف                                                                       |
| ------------------ | ------- | ------------ | -------- | ----------------------------------------------------------------------------- |
| **Spreadsheet**    | ملف    | FormData     | نعم      | ملف Excel المراد تحويله.                                                      |
| **worksheet**      | نص    | استعلام      | نعم      | اسم ورقة العمل التي تحتوي على النطاق.                                          |
| **range**          | نص    | استعلام      | نعم      | منطقة الخلايا المراد تحويلها، مثل `A1:C10`.                                  |
| **outPath**        | نص    | استعلام      | لا       | مسار المجلد الذي يجب حفظ ملف HTML الناتج فيه (افتراضيًا `null`).             |
| **outStorageName** | نص    | استعلام      | لا       | اسم خدمة التخزين المستخدمة لحفظ ملف الإخراج.                                 |
| **fontsLocation**  | نص    | استعلام      | لا       | مسار مجلد الخطوط المخصصة.                                                    |
| **AutoRowsFit**    | منطقي | استعلام      | لا       | ضبط ارتفاع جميع الصفوف تلقائيًا في ورقة العمل.                               |
| **AutoColumnsFit** | منطقي | استعلام      | لا       | ضبط عرض جميع الأعمدة تلقائيًا في ورقة العمل.                                 |
| **region**         | نص    | استعلام      | لا       | معرّف التوطين (مثل `en-US`, `fr-FR`). يؤثر على تنسيق الأرقام والتاريخ.        |
| **password**       | نص    | استعلام      | لا       | كلمة المرور لفتح ملف Excel المحمي.                                            |
| **fontsLocation**  | نص    | استعلام      | لا       | موقع الخطوط المخصصة.                                                          |
| **region**         | نص    | استعلام      | لا       | إعداد منطقة/لغة جدول البيانات.                                                |
| **password**       | نص    | استعلام      | لا       | كلمة المرور لفتح ملف جدول البيانات.                                          |

## الاستجابة

ترجع واجهة برمجة التطبيقات ملف HTML المحول كـ **دفق ثنائي** (`application/octet-stream`).

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### مثال على استجابة ناجحة (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

احفظ محتوى جسم الاستجابة في ملف (مثل `report.html`) لعرض الجدول المُرسَل في المتصفح.

---

**أكواد حالة HTTP**

| الكود | المعنى                | الوصف                                                           |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK (نجاح)            | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.     |
| 400  | Bad Request (طلب غير صالح) | معلمات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم).             |
| 401  | Unauthorized (غير مصرّح) | رمز JWT غير صالح أو مفقود.                                      |
| 413  | Payload Too Large (حجم البيانات كبير جدًا) | ملف التحميل يتجاوز الحد الأقصى للحجم.                           |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                        |

## كيف تستخدم واجهة برمجة تطبيقات تحويل النطاق إلى HTML باستخدام مكتبات SDK؟

### مواصفات OpenAPI

تُحدّد [مواصفات OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML) واجهة برمجة تطبيقات متاحة عمومًا، مما يتيح التفاعل عبر REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.html"
Content-Length: 8423

<table>
  <tr><th>Product</th><th>Price</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة للتطوير، حيث تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بتحويل نطاق من البيانات إلى ملف HTML باستخدام كود موجز.  
استكشف القائمة الكاملة لمكتبات SDK الخاصة بـ Aspose.Cells Cloud في [مستودع GitHub](https://github.com/aspose-cells-cloud).

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة. إذا تم حظر تحميل الأمثلة من Gist، يمكنك تنزيلها مباشرةً من المستودع.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}