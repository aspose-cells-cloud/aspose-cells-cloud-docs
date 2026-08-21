---
title: "استيراد بيانات JSON إلى Excel"
second_title: "وثيقة"
linktype: "استيراد JSON"
type: docs
url: /ar/import-json-data-into-excel/
aliases: [  /ar/import/json/ ]
keywords: "Aspose.Cells Cloud، استيراد JSON، API Excel، استيراد JSON عبر REST، أمثلة SDK"
description: "تعلم كيفية استيراد بيانات JSON إلى ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يشمل تفاصيل نقطة النهاية، وأمثلة على الطلبات والاستجابات، وشيفرة برمجية لـ .NET وJava وPython."
weight: 40
---

تقوم هذه الواجهة **استيراد بيانات JSON** إلى ورقة عمل Excel.

## واجهة برمجة التطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معامِلات الطلب**

| اسم المعامل            | الموقع        | النوع   | الوصف                                                                                             |
| --------------------- | ------------- | ------- | -------------------------------------------------------------------------------------------------- |
| name                  | المسار (Path) | نص (string) | اسم ملف المصنف.                                                                                   |
| importJsonRequest     | جسم HTTP      | كلاس (class) | حمولة الطلب التي تحتوي على تفاصيل استيراد JSON.                                                   |
| password              | سلسلة الاستعلام (Query string) | نص (string) | كلمة المرور لفتح المصنف (إن كان مُحميًا).                                                          |
| folder                | سلسلة الاستعلام (Query string) | نص (string) | المجلد الذي يحتوي على المصنف الأصلي.                                                               |
| storageName           | سلسلة الاستعلام (Query string) | نص (string) | اسم وحدة التخزين التي يوجد فيها المصنف.                                                             |
| outPath               | سلسلة الاستعلام (Query string) | نص (string) | المسار المطلوب لملف الإخراج بعد الاستيراد. إذا تُرك فارغًا، فسيُعاد المصنف المُحدّث في الاستجابة. |
| outStorageName        | سلسلة الاستعلام (Query string) | نص (string) | اسم وحدة التخزين الخاصة بملف الإخراج.                                                               |
| checkExcelRestriction | سلسلة الاستعلام (Query string) | نص (string) | علامة تشير إلى ما إذا كان يجب تطبيق قيود Excel المحددة (true/false).                               |

### **مثال على جسم الطلب**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### الاستجابة

يُعاد رمز الحالة **HTTP 200** مع حمولة JSON مشابهة لما يلي في حال نجاح الطلب:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

رموز الحالة المحتملة:

| الكود | المعنى                               |
| ---- | ------------------------------------ |
| 200  | نجح الاستيراد                        |
| 400  | طلب غير صالح – بيانات ناقصة أو خاطئة |
| 401  | غير مصرّح به – رمز غير صالح أو مفقود |
| 500  | خطأ داخلي في الخادم                  |


## كيفية استخدام واجهة PostWorkbookImportJson API باستخدام حزم تطوير البرمجيات (SDKs)

### مواصفات واجهة PostWorkbookImportJson API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) واجهة برمجة قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام حزم تطوير البرمجيات Aspose.Cells Cloud

استخدام حزم تطوير البرمجيات (SDKs) هو أكثر الطرق كفاءة لتسريع التطوير. وتتولى SDKs تفاصيل المستوى المنخفض، مما يسمح لك بالتركيز على منطق أعمالك. للاطلاع على القائمة الكاملة لحزم تطوير البرمجيات Aspose.Cells Cloud، يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud).

تُظهر الأمثلة التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مختلف حزم تطوير البرمجيات (SDKs):

---