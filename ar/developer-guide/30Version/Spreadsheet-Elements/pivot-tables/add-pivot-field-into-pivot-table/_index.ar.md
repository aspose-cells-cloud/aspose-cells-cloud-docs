---
title: "إضافة حقل محوري إلى جدول محوري"
second_title: "Document"
linktitle: "إضافة حقل محوري"
type: docs
url: /ar/pivot-tables/add-pivot-field/
aliases: [  /ar/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, جدول محوري, إضافة حقل محوري, REST API, SDK"
description: "إضافة حقل محوري إلى جدول محوري موجود باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن تفاصيل الطلب، مثالًا باستخدام cURL، وأكواد SDK."
weight: 40
ArticleTitle: "إضافة حقل محوري إلى جدول محوري – وثائق Aspose.Cells Cloud"
---

تقوم هذه الواجهة **إضافة** حقل محوري إلى جدول محوري موجود.

> **الشرط المسبق:** لاستدعاء هذه النقطة النهائية، يجب تضمين رمز مصادقة JWT صالح في رأس `Authorization`، وضمان تخزين الملف في المجلد المحدد أو وحدة التخزين الافتراضية.

## واجهة REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### معلمات الطلب

| اسم المعلمة     | النوع     | الموقع   | الوصف                                                              |
|------------------|-----------|----------|---------------------------------------------------------------------|
| name            | string    | path     | اسم المستند.                                                        |
| sheetName       | string    | path     | اسم ورقة العمل.                                                     |
| pivotTableIndex | integer   | path     | فهرس الجدول المحوري.                                                |
| pivotFieldType  | string    | query    | نوع منطقة الحقول (مثل: Row، Column).                               |
| request         | object    | body     | كائن يحتوي على فهارس الحقول المراد إضافتها.                         |
| needReCalculate | boolean   | query    | اضبطها على **true** لإعادة حساب الجدول المحوري بعد تنفيذ العملية.   |
| folder          | string    | query    | المجلد الذي يُخزّن فيه المستند.                                     |
| storageName     | string    | query    | اسم وحدة التخزين.                                                   |

يعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) واجهة برمجة تطبيقات متاحة عمومًا، ويتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إضافة حقل محوري باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

يُعيد الطلب الناجح كائن JSON يحتوي على الحقلين `Code` و `Status`. مخطط المثال:

```json
{
  "Code": 0,        // عدد صحيح يُشير إلى رمز حالة HTTP
  "Status": "OK"    // رسالة نصية
}
```

تشمل استجابات الخطأ المحتملة **400 Bad Request** عند غياب المعلمات، و**401 Unauthorized** إذا كان الرمز غير صالح، و**500 Internal Server Error** في حال حدوث مشكلات من جانب الخادم.

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لدمج هذه الوظيفة. فتتولى SDKs إدارة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على منطق أعمالك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا:**  
- [إضافة جدول محوري](https://docs.aspose.cloud/cells/ar/pivot-tables/add-pivot-table/)  
- [حذف حقل محوري](https://docs.aspose.cloud/cells/ar/pivot-tables/delete-pivot-field/)