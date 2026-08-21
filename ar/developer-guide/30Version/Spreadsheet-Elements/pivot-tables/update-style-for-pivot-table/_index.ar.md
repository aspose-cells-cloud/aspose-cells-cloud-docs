---
title: "تحديث نمط جدول محوري"
second_title: "مستند"
linktype: "تنسيق الكل"
type: docs
url: /ar/pivot-tables/format-all/
aliases: [  /ar/update-style-for-pivot-table/ ]
keywords: "جدول محوري، تحديث النمط، Aspose.Cells Cloud، REST API، إكسل، جدول بيانات، واجهة برمجة التطبيقات، نمط الجدول المحوري، تنسيق الكل"
description: "تعرّف على كيفية تحديث نمط جدول محوري بالكامل باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن تفاصيل الطلب، مثالًا باستخدام cURL، وأجزاء كود لعدة لغات برمجة."
weight: 100
ArticleTitle: "تحديث نمط جدول محوري - واجهة Aspose.Cells Cloud API"
---

تُحدِّث هذه الواجهة البرمجية REST نمط جدول محوري.

## واجهة PostPivotTableStyle

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**المتطلبات المسبقة / المصادقة**  
يجب تقديم رمز وصول JWT صالح في رأس `Authorization` (مثل `Bearer <رمز jwt>`). تأكّد من أن الرمز يملك الصلاحيات الكافية للوصول إلى ملف المصنف والورقة المحددين.

### **الأمان والمصادقة**

تُعدّ واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **مُعَيّنات الطلب**

| اسم المعَيّن      | النوع    | الموقع | الوصف                                                                                       |
|------------------|---------|--------|---------------------------------------------------------------------------------------------|
| name             | نص     | المسار | اسم ملف المصنف.                                                                             |
| sheetName        | نص     | المسار | الورقة التي يحتوي عليها الجدول المحوري.                                                     |
| pivotTableIndex  | عدد صحيح | المسار | الفهرس (الصفر-based) للجدول المحوري المراد تنسيقه.                                          |
| style            | كائن   | الجسم | كائن DTO لتحديد التنسيق المراد تطبيقه.                                                      |
| needReCalculate  | منطقي  | الاستعلام | عدّله إلى **true** لإعادة حساب الجدول المحوري بعد التنسيق؛ القيمة الافتراضية هي **false**. |
| folder           | نص     | الاستعلام | المجلد الذي يُخزّن فيه المصنف.                                                              |
| storageName      | نص     | الاستعلام | اسم خدمة التخزين.                                                                           |

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تفاعلية مُتاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء استدعاء إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
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

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                                           |
|-------|----------------------------|------------------------------------------------------------------|
| 200   | OK                         | تطبيق التنسيق بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.        |
| 400   | Bad Request                | مُعَيّنات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).          |
| 401   | Unauthorized               | رمز JWT غير صالح أو مفقود.                                      |
| 413   | Payload Too Large          | حجم الملف المرفوع يتجاوز الحد المسموح.                          |
| 500   | Internal Server Error      | خطأ داخلي في الخادم غير متوقع.                                 |

{{< /tab >}}

{{< /tabs >}}

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة لتطوير التطبيقات باستخدام الواجهة البرمجية. تُجسّد SDK التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على منطق أعمالك. راجع <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

يُظهر مثال الكود التالي كيفية استدعاء الواجهة البرمجية باستخدام SDK للغة Go:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}
---