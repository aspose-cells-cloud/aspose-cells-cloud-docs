---
title: "استيراد البيانات باستخدام التخزين"
second_title: "مستند"
linktype: docs
url: /import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "استيراد البيانات باستخدام التخزين: استيراد البيانات إلى ورقة عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud من مصادر تخزين متعددة. يدعم تنسيقات JSON وCSV及其他 تنسيقات عبر HTTPS."
keywords: "Aspose.Cells Cloud، Excel، استيراد البيانات، واجهة برمجة تطبيقات REST، تخزين السحابة، JSON، CSV، PDF، Markdown، HTTPS"
weight: 10
ArticleTitle: "استيراد البيانات باستخدام التخزين - مستندات واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST باستيراد البيانات إلى ملف Excel.

## واجهة PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| --- | --- | --- | --- |
| name | سلسلة نصية | المسار | اسم ملف Excel. |
| folder | سلسلة نصية | استعلام | مسار المجلد في التخزين حيث يوجد الملف. |
| storageName | سلسلة نصية | استعلام | اسم خدمة التخزين. |
| importData | كائن | الجسم | كائن JSON يحتوي على البيانات المراد استيرادها. |

**تُوضّح معاملات خيارات استيراد البيانات** في <a href="/cells/import/#import-data-option-parameter" rel="noopener noreferrer">رابط المرجع</a>.

**المتطلبات الأساسية:** يجب توفير رمز JWT صالح في رأس `Authorization`، وضمان وجود المصنف المستهدف مسبقًا في موقع التخزين المحدد.

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**رموز حالة HTTP**

| الكود | المعنى | الوصف |
| --- | --- | --- |
| 200 | ناجح (OK) | تم تطبيق العامل بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حمل البيانات كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | حدوث خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostImportData API باستخدام SDKs

### مواصفات واجهة PostImportData API

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للوصول، وتسمح بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
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

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDKs يُعد أفضل طريقة لتسريع عملية التطوير، حيث تُجرّد SDKs التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على منطق أعمالك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

يُظهر مثال الكود التالي كيفية استدعاء خدمة ويب Aspose.Cells باستخدام SDK بلغة PHP: