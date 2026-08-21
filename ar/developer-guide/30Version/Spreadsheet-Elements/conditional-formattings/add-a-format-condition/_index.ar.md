---
title: "إضافة شرط التنسيق"
type: docs
url: /conditional-formattings/add-format-condition/
aliases: [/add-a-format-condition/]
keywords: "Aspose.Cells Cloud, واجهة برمجة تطبيقات التنسيق الشرطي, إضافة شرط التنسيق, Excel REST API, Cells API"
description: "تعلم كيفية إضافة شرط تنسيق إلى ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API (الإصدار 3.0). يتضمن بنية الطلب، المعاملات، مثال cURL الآمن، وأجزاء كود SDK."
ArticleTitle: "إضافة شرط التنسيق – مستندات واجهة برمجة تطبيقات Aspose.Cells Cloud"
weight: 50
---

تقوم هذه الواجهة البرمجية REST بإضافة شرط تنسيق إلى ورقة عمل.

## الأمان والمصادقة
تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [مصادقة تعتمد على رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة برمجة تطبيقات REST

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### معاملات الطلب

| اسم المعامل | النوع   | الموقع | الوصف                                                                 |
|-------------|---------|--------|------------------------------------------------------------------------|
| name        | string  | path   | اسم ملف جدول العمل Excel.                                             |
| sheetName   | string  | path   | اسم ورقة العمل التي تحتوي على النطاق المراد تنسيقه.                   |
| index       | integer | path   | الفهرس الصفر-based لشرط التنسيق المراد إضافته أو استبداله.           |
| cellArea    | string  | query  | نطاق الخلايا (مثل `A1:C3`) الذي يطبّق عليه الشرط.                    |
| type        | string  | query  | نوع الشرط (مثل `Expression`, `CellValue`).                            |
| operatorType| string  | query  | العامل المستخدم في الشرط (مثل `Between`, `Equal`).                    |
| formula1    | string  | query  | الصيغة أو القيمة الأولى المستخدمة في الشرط.                           |
| formula2    | string  | query  | الصيغة أو القيمة الثانية (مطلوبة لبعض العوامل مثل `Between`).         |
| folder      | string  | query  | المجلد في التخزين حيث يوجد ملف جدول العمل.                            |
| storageName | string  | query  | اسم خدمة التخزين (مثل `Default`).                                     |

### استجابات الأخطاء

| رمز HTTP | السبب                                                | محتوى الاستجابة المثال                              |
|----------|------------------------------------------------------|-----------------------------------------------------|
| **400**  | طلب غير صالح – معاملات مفقودة أو غير صالحة.        | `{ "Code":"400", "Message":"Invalid parameter value." }`            |
| **401**  | غير مصرّح – رمز JWT مفقود أو غير صالح.              | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | غير موجود – ملف جدول العمل أو ورقة العمل غير موجود. | `{ "Code":"404", "Message":"File not found." }`                     |
| **500**  | خطأ داخلي في الخادم – فشل غير متوقع في الخادم.      | `{ "Code":"500", "Message":"An unexpected error occurred." }`       |

### استجابة ناجحة

| رمز HTTP | السبب                                           | محتوى الاستجابة المثال                    |
|----------|------------------------------------------------|-------------------------------------------|
| **200**  | ناجح – تم إضافة الشرط أو تحديثه بنجاح.         | `{ "Code": "200", "Status": "OK" }`       |

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) واجهة برمجة تطبيقات متاحة للعامة وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام **cURL** لاستدعاء واجهة برمجة تطبيقات Aspose.Cells. يوضح المثال التالي طلبًا كاملًا، بما في ذلك جسم JSON فارغ.

### مثال باستخدام cURL

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}