---
title: "استيراد بيانات XML إلى جدول بيانات"
ArticleTitle: "استيراد بيانات XML إلى جدول بيانات – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "استيراد بيانات XML إلى جدول بيانات"
type: docs
url: /cells/import/data/xml
aliases: []
keywords: "استيراد XML، Aspose.Cells، واجهة برمجة التطبيقات"
description: "استيراد ملف بيانات XML إلى جدول البيانات المحلي باستخدام Aspose.Cells Cloud."
weight: 1000
---

## استيراد بيانات XML إلى جدول بيانات عبر خدمات Aspose.Cells Cloud Web

استيراد ملف بيانات XML إلى جدول البيانات المحلي. وتقوم هذه الطريقة بتحليل ملف XML، وربط البيانات بهيكل خلايا جدول البيانات، ثم حفظ الملف محليًا. وتشمل تنسيقات جداول البيانات المدعومة: .xlsx و .ods.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل        | النوع    | المسار / سلسلة الاستعلام / جسم HTTP | الوصف                                                                                                                            |
|-------------------|----------|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile          | ملف      | FormData                            | تحميل ملف البيانات.                                                                                                                      |
| Spreadsheet       | ملف      | FormData                            | تحميل ملف جدول البيانات.                                                                                                               |
| worksheet         | سلسلة    | استعلام                             | جدول البيانات الذي يجب استيراد بيانات XML إليه.                                                                                            |
| startcell         | سلسلة    | استعلام                             | الموقع الابتدائي لاستيراد البيانات                                                                                                      |
| insert            | منطقية   | استعلام                             | يتحكم في سلوك الإدراج. true: إدراج البيانات؛ false: الكتابة فوق البيانات الموجودة. الافتراضي: **true**                               |
| outPath           | سلسلة    | استعلام                             | (اختياري) مسار المجلد حيث يتم تخزين ملف العمل. الافتراضي هو null.                                                         |
| outStorageName    | سلسلة    | استعلام                             | اسم تخزين ملف الإخراج.                                                                                                              |
| fontsLocation     | سلسلة    | استعلام                             | استخدام خطوط مخصصة.                                                                                                                      |
| region            | سلسلة    | استعلام                             | إعدادات منطقة/لغة جدول البيانات (مثل `en-US`، `fr-FR`). تؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك الخاص بالمنطقة. |
| password          | سلسلة    | استعلام                             | كلمة المرور لفتح ملف جدول البيانات.                                                                                             |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|-------------|-------|-------|
| *لا شيء*    | -     | -     |

### **الاستجابة**

```json
{
  "file": "<تيار ثنائي لملف جدول البيانات المُحدَّث>"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى                 | الوصف                                                                                           |
|-------|-------------------------|-------------------------------------------------------------------------------------------------------|
| 200   | ناجح (OK)              | تم استيراد بيانات XML بنجاح وعودة ملف جدول البيانات المُحدَّث.                        |
| 400   | طلب غير صالح (Bad Request) | عنوان URL للطلب غير صحيح أو معاملات مطلوبة مفقودة.                                                   |
| 401   | غير مخوَّل (Unauthorized) | فشلت المصادقة أو لم تُقدَّم أي بيانات اعتماد.                                          |
| 404   | غير موجود (Not Found)   | الملف المصدر غير قابل للوصول.                                                                           |
| 413   | حملة كبيرة جدًا (Payload Too Large) | حجم ملف التحميل يتجاوز الحد المسموح به.                                                          |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | حدثت مشكلة في جدول البيانات أثناء استلام البيانات.                                         |

## كيفية استخدام استيراد بيانات XML مع مكتبات SDK

### مواصفات استيراد بيانات XML إلى جدول بيانات

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات استيراد بيانات XML إلى جدول البيانات</a> واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells Cloud بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{DataFileName}" \
  -F "Spreadsheet=@{SpreadsheetFileName}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<تيار ثنائي لملف جدول البيانات المُحدَّث>"
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات Aspose Cells Cloud SDK

يُعد استخدام SDK أسرع طريقة لتسريع عملية التطوير. وتوفر SDK تجريدًا للتفاصيل من المستوى المنخفض، ما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الرمز التالية كيفية إجراء مكالمات لخدمات الويب الخاصة بـ Aspose Cells Cloud باستخدام مكتبات SDK المختلفة:
`[TBD]`
---