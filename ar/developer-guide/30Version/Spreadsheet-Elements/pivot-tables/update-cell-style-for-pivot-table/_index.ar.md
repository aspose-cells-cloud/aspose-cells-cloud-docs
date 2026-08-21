---
title: "تحديث نمط الخلية لجدول محوري"
second_title: "مستند"
linktype: التنسيق
type: docs
url: /ar/pivot-tables/format/
aliases: [  /ar/update-cell-style-for-pivot-table/ ]
keywords: "Aspose.Cells Cloud، نمط جدول محوري، واجهة برمجة تطبيقات تحديث نمط الخلية، واجهة برمجة تطبيقات REST، واجهة برمجة تطبيقات Excel، تنسيق جداول البيانات، SDK السحابي، نمط الخلية، جدول محوري"
description: "تعرف على كيفية تحديث نمط خلية محددة في جدول محوري باستخدام Aspose.Cells Cloud عبر واجهة برمجة تطبيقات REST. يشمل ذلك نقطة النهاية، المعاملات، المصادقة، مثال cURL، وقطعة كود SDK لـ Go، وإرشادات مُحسّنة لمحركات البحث (SEO)."
weight: 90
ArticleTitle: "تحديث نمط الخلية لجدول محوري - وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية لـ REST بتحديث **نمط** خلية في جدول محوري.

**المتطلبات المسبقة / المصادقة**  
لاستدعاء نقطة النهاية هذه، يجب أن يكون لديك رمز وصول JWT صالح من Aspose Cloud. احصل على الرمز المميز عبر تدفق OAuth 2.0 الموصوف في [دليل المصادقة](/ar/authentication/). ضع الرمز المميز في رأس الطلب:

```http
Authorization: Bearer <رمز jwt>
```

يُطلب رمز JWT لجميع استدعاءات واجهة برمجة تطبيقات Aspose.Cells Cloud.

## واجهة برمجة تطبيقات PostPivotTableCellStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/Format
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### **معاملات الطلب**

| اسم المعامل        | النوع     | الموقع   | الوصف                                                                                             |
| ------------------ | --------- | -------- | -------------------------------------------------------------------------------------------------- |
| name               | string    | path     | اسم المستند (مطلوب).                                                                               |
| sheetName          | string    | path     | اسم ورقة العمل (مطلوبة).                                                                           |
| pivotTableIndex    | integer   | path     | فهرس الجدول المحوري (مطلوب).                                                                       |
| column             | integer   | query    | فهرس العمود (مبتدأ من الصفر) للخلية المراد تنسيقها (مطلوب).                                         |
| row                | integer   | query    | فهرس الصف (مبتدأ من الصفر) للخلية المراد تنسيقها (مطلوب).                                           |
| style              | object    | body     | كائن نقل البيانات (DTO) يُعرّف نمط الخلية الجديد.                                                 |
| needReCalculate    | boolean   | query    | يُشير إلى ما إذا كان يجب إعادة حساب الجدول المحوري بعد التنسيق. القيمة الافتراضية هي **false**.    |
| folder             | string    | query    | المجلد المخزن فيه المستند (اختياري).                                                               |
| storageName        | string    | query    | اسم وحدة التخزين (اختياري).                                                                        |
| Method             | string    | N/A      | طريقة HTTP المستخدمة في الطلب (**POST**).                                                          |

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableCellStyle" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول العام، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/Format?column=1&row=1" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <رمز jwt>"
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

**الاستجابة**  
في حالة النجاح، تُعيد الخدمة الرمز HTTP 200 مع جسم فارغ يشير إلى تطبيق النمط بنجاح. وفي حالة حدوث خطأ، تُعاد حمولة JSON تحتوي على رمز الخطأ والرسالة.

| حالة HTTP | الوصف                                                                 |
|----------|------------------------------------------------------------------------|
| 200      | تم تطبيق النمط بنجاح.                                                 |
| 400      | طلب غير صالح – مثلاً: فهرس عمود/صف غير صحيح.                          |
| 401      | غير مصرّح به – رمز JWT مفقود أو غير صالح.                             |
| 404      | غير موجود – المستند أو ورقة العمل أو الجدول المحوري المحدد غير موجود. |
| 500      | خطأ داخلي في الخادم – حالة غير متوقعة.                                |

يكون جسم الاستجابة فارغًا في حالة النجاح.

لمزيد من المعلومات، راجع وثائق واجهة برمجة التطبيقات **Get Pivot Table**.

## عائلة SDK السحابية

يُعد استخدام SDK الطريقة الأسرع للتطوير. فتقوم SDK بإخفاء التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على منطق عملك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

يُظهر مثال الكود التالي كيفية استدعاء خدمات Aspose.Cells باستخدام **Go SDK**:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "3236805d26482f06f4656b14f2d00d79" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "تحديث نمط الخلية لجدول محوري",
  "description": "دليل لتحديث نمط خلية محددة في جدول محوري باستخدام Aspose.Cells Cloud عبر واجهة برمجة تطبيقات REST.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud، جدول محوري، نمط الخلية، واجهة برمجة تطبيقات REST، Go SDK",
  "url": "https://docs.aspose.cloud/ar/cells/pivot-tables/format/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>