---
title: "واجهة برمجة تطبيقات استيراد البيانات في Aspose.Cells Cloud – حل سحابي لاستيراد بيانات CSV وJSON وXML تلقائيًا إلى أوراق عمل Excel."
second_title: "مستند"
ArticleTitle: "منصة دمج البيانات من مصادر متعددة – واجهة برمجة تطبيقات Aspose.Cells Cloud للاستيراد والتحويل التلقائي للبيانات."
linktitle: "استيراد البيانات إلى ورقة العمل"
type: docs
url: /ar/import-data-into-spreadsheet/
keywords: "Aspose Cells، واجهة برمجة تطبيقات استيراد البيانات، CSV إلى Excel، JSON إلى Excel، XML إلى Excel، ورقة عمل سحابية، واجهة برمجة تطبيقات REST"
description: "استورد بيانات CSV أو JSON أو XML إلى أوراق عمل Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. اكتشف تنسيق الطلب، والمتغيرات، وأكواد عينات SDK، وإدارة الأخطاء."
weight: 100
---

## الميزات الأساسية

### دعم تنسيقات البيانات المتعددة

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a> استيراد البيانات**: يدعم فواصل متعددة ويكتشف الترميز تلقائيًا.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a> معالجة البيانات**: يُسطّح الهياكل المعقدة لملفات JSON في جداول Excel.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a> تحويل الملفات**: يُعيّن بيانات العقد إلى هيكل الصفوف والأعمدة في Excel.

## **وصف واجهة برمجة تطبيقات استيراد البيانات إلى ورقة العمل**

### واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### متغيرات الطلب

| اسم المتغير      | النوع   | الموقع         | الوصف                                                                 |
| ---------------- | ------- | -------------- | --------------------------------------------------------------------- |
| datafile         | ملف     | FormData       | ملف البيانات (CSV أو JSON أو XML) المراد استيراده.                    |
| spreadsheet      | ملف     | FormData       | المصنف المستهدف الذي سيتلقّى البيانات المستوردة.                     |
| worksheet        | نص      | Query          | اسم ورقة العمل التي ستُوضع فيها البيانات.                             |
| startCell        | نص      | Query          | الخلية العلوية اليسرى (مثل `A1`) التي تُحدّد نقطة البداية للاستيراد. |
| insert           | منطقي   | Query          | `true` لإدراج صفوف؛ `false` لكتابة البيانات فوق البيانات الموجودة.   |
| convertNumericData | منطقي | Query          | `true` لتحويل النصوص الرقمية إلى أرقام أثناء الاستيراد.              |
| splitter         | نص      | Query          | فاصل CSV مكوّن من حرف واحد (الافتراضي هو `,`).                        |
| outPath          | نص      | Query (اختياري) | مسار المجلد الذي سيتم فيه حفظ المصنف المحدّث.                         |
| outStorageName   | نص      | Query (اختياري) | اسم موقع التخزين لملف الإخراج.                                        |
| fontsLocation    | نص      | Query (اختياري) | مسار مجلد خطوط مخصّص، إن لزم الأمر.                                   |
| region           | نص      | Query (اختياري) | إعدادات إقليم ورقة العمل (مثل `en-US`).                               |
| password         | نص      | Query (اختياري) | كلمة المرور لفتح مصنف محمي.                                           |

### الاستجابة

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

**رموز حالة HTTP**

| الرمز | المعنى                   | الوصف                                                               |
| ----- | ------------------------ | ------------------------------------------------------------------- |
| 200   | ناجح                     | تمت تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.      |
| 400   | طلب غير صالح             | مفقود أو غير صالح المتغيرات (مثل نوع ملف غير مدعوم).              |
| 401   | غير مُصادَق عليه         | رمز JWT غير صالح أو مفقود.                                         |
| 413   | حجم الحمولة كبير جدًا     | حجم الملف المرفوع يتجاوز الحد المسموح.                             |
| 500   | خطأ داخلي في الخادم       | خطأ غير متوقّع في الخادم.                                           |

## أسباب استخدام هذه الواجهة

- **تحميل بيانات فعّال** – يتيح الاستيراد الجُملي لمجموعات بيانات كبيرة مباشرةً إلى مصنف دون إنشاء ملفات وسيطة.
- **دعم واسع لـ SDKs** – يوفّر مكتبات عميل لـ .NET وJava وPHP وRuby وNode.js وPython وGo وPerl، ما يبسّط التكامل.
- **معالجة في الذاكرة** – يُجري التحويلات في الذاكرة، ما يقلّل متطلبات التخزين المؤقت.

## كيفية استخدام واجهة برمجة تطبيقات استيراد البيانات إلى ورقة العمل باستخدام SDKs

**ملاحظات / قيود:** تدعم الواجهة ما يصل إلى 1,000,000 صف في كل استيراد. الفاصل الافتراضي لملفات CSV هو الفاصلة فقط؛ ويمكن تحديد فواصل حرفية أخرى عبر المتغير `splitter`. قد تزيد ملفات XML الكبيرة من وقت المعالجة.

لعمليات مرتبطة مثل تصدير البيانات أو تحويل تنسيقات المصنفات، راجع مستندات **تصدير البيانات** و**تحويل المصنف**.

### مواصفات واجهة برمجة تطبيقات استيراد البيانات إلى ورقة العمل

توفّر <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات استيراد البيانات إلى ورقة العمل</a> واجهة برمجة برمجية متاحة علنًا، ما يسمح بالتفاعل مع REST مباشرةً من متصفح الويب الخاص بك.
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (مشفر بـ Base64)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDKs الطريقة الأسرع لتطوير التطبيقات، إذ يُجرّدك من التفاصيل منخفضة المستوى، مما يتيح لك استيراد البيانات إلى ورقة عمل باستخدام كود قصير. يُرجى مراجعة <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

---