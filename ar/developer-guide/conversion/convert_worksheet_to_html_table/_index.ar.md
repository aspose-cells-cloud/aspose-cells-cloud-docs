---
title: "تحويل ورقة عمل إلى جدول HTML"
ArticleTitle: "تحويل ورقة عمل إلى جدول HTML – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "تحويل_ورقة_عمل_إلى_جدول_HTML"
type: docs
url: /cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells، ConvertWorksheetToHtmlTable، جدول HTML، واجهة برمجة تطبيقات"
description: "يحول ورقة عمل من ملف جدول محسوب محلي إلى ملف جدول HTML باستخدام Aspose.Cells Cloud."
weight: 100
---

## تحويل ورقة العمل إلى جدول HTML ضمن خدمات ويب Aspose.Cells Cloud

تقوم هذه العملية بقراءة ملف جدول محاسبي من نظام الملفات المحلي، وتحويل ورقة العمل المحددة فيه إلى جدول HTML، ثم إعادة النتيجة المحولة ك поток ملف (file stream). ويتم إجراء التحويل بالكامل على خادم السحابة، لذا لا يتطلب تحميلًا مبدئيًّا إلى مساحة التخزين السحابية. كما يدعم إعدادات التوطين (Locale) الاختيارية وملفات العمل المحمية بكلمة مرور.

### نقطة نهاية واجهة برمجة التطبيقات على الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|------------|--------|-------------------------------------|--------|
| Spreadsheet | ملف | FormData | رفع ملف الجدول المحاسبي. |
| worksheet | نص | استعلام | اسم ورقة العمل داخل الجدول المحاسبي. (مطلوبة) |
| region | نص | استعلام | إعدادات المنطقة/اللغة للجدول المحاسبي (مثل `en-US`، `fr-FR`). تؤثر على تنسيق الأرقام، وتفسير التواريخ، وسلوك الإعدادات المحلية. |
| password | نص | استعلام | كلمة المرور المطلوبة لفتح ملف الجدول المحاسبي. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| ------------ | ---- | ----------- |
| *لا يوجد* | *لا يوجد* | *لا يُطلب وجود جسم JSON؛ يُرسل الملف على شكل multipart/form-data.* |

### **الاستجابة**

```json
{
  "File": " поток ثنائي للجدول HTML الناتج"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|---------|--------|
| 200 | نجاح | تم تحويل ورقة العمل إلى جدول HTML بنجاح، وتم إعادته ك поток ملف. |
| 400 | طلب غير صالح | عنوان URL غير صالح أو معاملات مطلوبة مفقودة. |
| 401 | غير مُصادَق عليه | فشلت المصادقة أو لم تُقدَّم أي بيانات اعتماد. |
| 404 | غير موجود | الملف المصدر غير قابل للوصول. |
| 500 | خطأ داخلي في الخادم | واجه الجدول المحاسبي حالة شاذة أثناء جلب بيانات التحويل. |
| 413 | حجم الحمولة كبير جدًّا | تجاوز حجم الملف المرفوع الحد المسموح به. |

## كيفية استخدام خدمة تحويل ورقة العمل إلى جدول HTML باستخدام مكتبات SDK

### مواصفات تحويل ورقة العمل إلى جدول HTML

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات تحويل ورقة العمل إلى جدول HTML</a> واجهة برمجة تطبيقات عامة قابلة للاستعمال، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام بروتوكول HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": " поток ثنائي للجدول HTML الناتج"
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات Aspose.Cells Cloud SDK

يُعد استخدام مكتبات SDK أسرع طريقة لتسريع عملية التطوير. فهي تُجرّدك من التفاصيل التقنية الدقيقة، وتسمح لك بالتركيز على مهام مشروعك. يُرجى زيارة <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells Cloud باستخدام مكتبات SDK مختلفة:
`[TBD]`
---