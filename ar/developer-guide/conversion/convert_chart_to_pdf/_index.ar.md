---
title: "تحويل المخطط إلى PDF"
ArticleTitle: "تحويل المخطط إلى PDF – Aspose.Cells Cloud API"
second_title: "وثيقة"
linktitle: "ConvertChartToPdf"
type: docs
url: /ar/cells/convert/chart/pdf
aliases: []
keywords: "ConvertChartToPdf, Aspose.Cells, PDF, تحويل المخطط"
description: "يحوّل مخططًا موجودًا في ملف جدول بيانات على محرك أقراص محلي إلى تنسيق PDF."
weight: 100
---

## خدمة تحويل المخطط إلى PDF من Aspose.Cells Cloud

تقوم هذه الطريقة بقراءة مخطط من ملف جدول بيانات يُرفع محليًا، وتحويله إلى تنسيق PDF، ثم إرجاع النتيجة المحولة. وتُنفَّذ العملية بالكامل على خادم السحابة، لذا لا يتطلب الأمر تخزينًا مؤقتًا. ويجب أن تكون مسار الملف المصدر والتنسيق الهدف صحيحَين، كما يجب أن تكون لديك الصلاحيات المناسبة لقراءة ملف المصدر. وستؤدي الأخطاء مثل غياب الملفات أو مشكلات الوصول أو فشل التحويل إلى استجابة خطأ HTTP مناسبة.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### مَعلمات الطلب

| اسم المعلمة   | النوع   | المسار/سلسلة الاستعلام/جسم HTTP | الوصف |
|----------------|--------|----------------------------------|--------|
| Spreadsheet      | ملف   | FormData                    | رفع ملف جدول البيانات. |
| worksheet        | نص    | استعلام                       | اسم ورقة العمل في جدول البيانات. |
| chartIndex       | عدد صحيح| استعلام                       | مؤشر المخطط داخل ورقة العمل. |
| outPath          | نص    | استعلام                       | (اختياري) مسار المجلد حيث يُخزَّن ملف العمل. القيمة الافتراضية هي null. |
| outStorageName   | نص    | استعلام                       | اسم وحدة التخزين الخاصة بالملف الناتج. |
| fontsLocation    | نص    | استعلام                       | استخدام خطوط مخصصة. |
| region           | نص    | استعلام                       | إعدادات المنطقة/اللغة لجدول البيانات (مثل `en-US`، `fr-FR`). وتؤثر على تنسيق الأرقام وتحليل التواريخ والسلوك المرتبط بالإعدادات المحلية. |
| password         | نص    | استعلام                       | كلمة المرور لفتح ملف جدول البيانات. |

### معلمة جسم الطلب

| اسم المعلمة | النوع | الوصف |
| ------------ | ---- | ----------- |
| Spreadsheet    | ملف | رفع ملف جدول البيانات. |

### **الاستجابة**

```json
{
  "ResponseFile": "تدفق ملف PDF ثنائي"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|--------|--------|
| 200 | نجاح | تم تحويل المخطط بنجاح إلى PDF؛ تم إرجاع ملف PDF ثنائي. |
| 400 | طلب غير صالح | معلمات الطلب غير صحيحة أو رابط URL معطَّل. |
| 401 | غير مُصادَق | فشلت المصادقة أو لم تُوفَّر أي بيانات اعتماد. |
| 404 | غير موجود | لا يمكن الوصول إلى ملف المصدر. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | حدث خطأ أثناء معالجة التحويل. |

## كيفية استخدام خدمة تحويل المخطط إلى PDF باستخدام حزم تطوير البرمجيات (SDKs)

### مواصفات تحويل المخطط إلى PDF

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf" rel="noopener noreferrer">مواصفات API لتحويل المخطط إلى PDF</a> واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}
{< tab tabNum="1" >}
```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "تدفق ملف PDF ثنائي"
}
```
{< /tab >}
{< /tabs >}

### استخدام حزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud

استخدام حزمة تطوير البرمجيات (SDK) هو أسرع طريقة لتسريع عملية التطوير. فحزمة SDK تُجرِّدك من التفاصيل التقنية منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells Cloud باستخدام حزم تطوير البرمجيات المختلفة:
`[TBD]`
---