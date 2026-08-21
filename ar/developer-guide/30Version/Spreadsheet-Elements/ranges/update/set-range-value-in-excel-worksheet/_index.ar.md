---
title: "تحديد قيمة النطاق في ورقة عمل Excel"
second_title: "وثيقة"
linktype: "تحديد القيم"
type: docs
url: /ar/ranges/update/values/
aliases: [  /ar/set-range-value-in-excel-worksheet/ ]
keywords: "Aspose.Cells، واجهة برمجة تطبيقات Excel، تحديد قيمة النطاق، واجهة برمجة التطبيقات عبر الويب، حزمة تطوير البرامج السحابية، تحديث ورقة العمل"
description: "تعرّف على كيفية تحديد قيمة خلية أو نطاق في ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API (النسخة 3.0). يشمل ذلك عنوان الواجهة، المُعلمات، مثال باستخدام cURL، أمثلة لرموز حزم التطوير، وإدارة الأخطاء."
weight: 72
ArticleTitle: "تحديد قيمة النطاق في ورقة عمل Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

استخدم هذه الواجهة البرمجية لتحديد قيمة في النطاق المحدّد. وعند الاقتضاء، يتم تحويل القيمة إلى نوع بيانات آخر وإعادة تعيين تنسيق رقم الخلية.

**المتطلبات المسبقة**  
- حساب Aspose Cloud ساري المفعول.  
- رمز JWT يشمل النطاق `Cells.ReadWrite`.  
- يجب أن يكون ملف جدول العمل مرفوعًا مسبقًا إلى موقع التخزين المستهدف.

## PostWorksheetCellsRangeValue API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

مُعلّمات الطلب هي:

| اسم المُعلّمة | النوع    | الموقع | الوصف                                                |
|---------------|----------|--------|--------------------------------------------------------|
| name          | string   | path   | اسم ملف جدول العمل                                   |
| sheetName     | string   | path   | اسم ورقة العمل                                        |
| value         | string   | query  | القيمة المُدخلة                                       |
| range         | object   | body   | كائن النطاق داخل ورقة العمل                            |
| isConverted   | boolean  | query  | يشير إلى ما إذا كان يجب تحويل القيمة المُدخلة         |
| setStyle      | boolean  | query  | يشير إلى ما إذا كان يجب تطبيق التنسيق على الخلايا المستهدفة |
| folder        | string   | query  | مجلد ملف جدول العمل                                   |
| storageName   | string   | query  | اسم وحدة التخزين                                      |

**مثال لكائن `range`** الذي يمكن إرساله في جسم الطلب:

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

يعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue) واجهة برمجة تطبيقات متاحة علنًا، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL. **قم بتضمين رمز JWT ساري المفعول في رأس `Authorization`.**

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
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

**مخطط الاستجابة**

| الحقل   | النوع    | الوصف                                              |
|---------|----------|------------------------------------------------------|
| Code    | integer  | رمز حالة HTTP للاستدعاء.                            |
| Status  | string   | وصف موجز للنتيجة (مثل "OK").                        |
| Message | string   | رسالة خطأ تفصيلية عند فشل الطلب (اختياري).          |
| Result  | object   | بيانات إضافية تُعاد في حالة النجاح (اختياري).       |

**رموز حالة HTTP المحتملة**

- **200 OK** – تم تحديد قيمة النطاق بنجاح.  
- **400 Bad Request** – مُعلمات غير صالحة أو جسم طلب غير مهيّأ بشكل صحيح.  
- **401 Unauthorized** – رمز JWT مفقود أو غير صالح.  
- **403 Forbidden** – صلاحيات غير كافية للعمليّة المطلوبة.  
- **404 Not Found** – ملف جدول العمل أو ورقة العمل أو النطاق المحدّد غير موجود.  
- **500 Internal Server Error** – خطأ غير متوقع في الخادم.

*مثال على استجابة خطأ لحالة 400 Bad Request:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "كائن 'range' يفتقر إلى الحقول المطلوبة."
}
```

## عائلة حزم تطوير البرامج السحابية

استخدام حزمة تطوير البرامج (SDK) هو أفضل طريقة لتسريع عملية التطوير. وتتولّى SDK تفاصيل المستوى المنخفض تلقائيًا، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرامج السحابية لـ Aspose.Cells.

تُظهر أمثلة الرمز التالية كيفية إجراء استدعاءات لخدمات ويب Aspose.Cells باستخدام مختلف SDKs:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}