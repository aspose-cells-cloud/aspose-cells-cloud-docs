---
title: "تحويل جدول إلى جدول محوري"
second_title: "Document"
linktitle: تحويل
type: docs
url: /pivot-tables/convert-table-to-pivottable/
aliases:
  [
    /create-a-pivottable-with-table/,
    /create-new-pivot-table-with-list-object-as-source-data/,
  ]
keywords: "جدول محوري، كائن قائمة، Aspose.Cells Cloud، REST API، تحويل جدول إلى جدول محوري"
description: "تعرّف على كيفية إنشاء جدول محوري من كائن قائمة باستخدام Aspose.Cells Cloud REST API. يتضمن تفاصيل الطلب، مثال cURL، وإشارات إلى حزم التطوير (SDK)."
weight: 60
ArticleTitle: "تحويل الجدول إلى جدول محوري – وثائق Aspose.Cells Cloud"
---

تُنشئ هذه الواجهة البرمجية (REST API) **جدولاً محورياً** من كائن قائمة.

يُلخّص الجدول المحوري البيانات الواردة من كائن قائمة، مما يتيح لك تحليل البيانات وإعداد تقارير عنها في مجموعات بيانات كبيرة مباشرةً داخل المصنف.

**المتطلبات المسبقة:**
- رمز مُعتمد (bearer token) صالح من نوع JWT للتحقق من الهوية.
- يجب أن يكون المصنف موجوداً في موقع التخزين المحدّد.
- يجب أن تحتوي الورقة المستهدفة على كائن القائمة الذي ترغب في تلخيصه.

## واجهة PostWorksheetListObjectSummarizeWithPivotTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **الأمان والمصادقة**

تتطلب واجهات Aspose.Cells Cloud API المصادقة باستخدام رمز <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token</a>، وهي آمنة.

### **مُعاملات الطلب**

| اسم المُعامل          | النوع    | الموقع  | الوصف                                                |
|----------------------|----------|---------|--------------------------------------------------------|
| name                 | string   | path    | اسم ملف المصنف.                                        |
| sheetName            | string   | path    | اسم الورقة التي تحتوي على كائن القائمة.               |
| listObjectIndex      | integer  | path    | فهرس كائن القائمة داخل الورقة.                        |
| destsheetName        | string   | query   | اسم الورقة الوجهة.                                     |
| request              | object   | body    | حمولة JSON التي تُعرّف الجدول المحوري.                 |
| folder               | string   | query   | مسار المجلد الذي يوجد فيه المصنف.                      |
| storageName          | string   | query   | اسم مساحة التخزين.                                     |

يجب أن يتّبع محتوى جسم الطلب المخطط (schema) المُعرّف في JSON أدناه:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "اسم الجدول المحوري الجديد." },
    "DestCellName": { "type": "string", "description": "الخلية العلوية اليسرى للجدول المحوري (مثال: \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "فهارس الحقول (تبدأ من الصفر) التي سيتم وضعها في الصفوف."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "فهارس الحقول (تبدأ من الصفر) التي سيتم وضعها في الأعمدة."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "فهارس الحقول (تبدأ من الصفر) التي ستُستخدم كحقول بيانات."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

يُعرّف <a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات قابلة للوصول العام، ويتيح لك إجراء تفاعلات REST مباشرة من متصفّح ويب.

يمكنك استخدام أداة <strong>cURL</strong> للاستفادة من خدمات Aspose.Cells عبر واجهة سطر الأوامر بسهولة. يوضّح المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*ملاحظة: استخدم نقطة النهاية الإنتاجية (`api.aspose.cloud`) في البيئات الحية. وتُستخدم نقطة النهاية التجريبية (`api-qa.aspose.cloud`) للتجربة والاختبار فقط. ويجب استخدام بروتوكول HTTPS لجميع المكالمات في البيئات الإنتاجية.*

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

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                                  |
|-------|----------------------------|---------------------------------------------------------|
| 200   | OK (تم بنجاح)             | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب غير صالح) | معطيات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).     |
| 401   | Unauthorized (غير مصرّح)   | رمز JWT غير صالح أو مفقود.                             |
| 413   | Payload Too Large (حمولة كبيرة جداً) | تجاوز حجم الملف المرفوع الحد المسموح به.                |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | حدث خطأ غير متوقع في الخادم.                             |

## عائلة SDK للسحابة

استخدام حزمة التطوير (SDK) هو أفضل طريقة لتسريع عملية التطوير. فتتولى حزم التطوير معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بحزم Aspose.Cells Cloud SDK.

توضّح أمثلة الكود أدناه كيفية إجراء مكالمات إلى خدمات Aspose.Cells عبر واجهات مختلفة لحزم التطوير (SDK):
---