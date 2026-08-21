---
title: "قبول جميع المراجعات"
ArticleTitle: "قبول جميع المراجعات – Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "قبول جميع المراجعات"
type: docs
url: /cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, جدول بيانات, مراجعات"
description: "قبول جميع المراجعات في ملف جدول بيانات باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud."
weight: 100
---

## خدمة AcceptAllRevisions في Aspose.Cells Cloud

قبول جميع المراجعات في ملف جدول البيانات المرفوع وإعادة مصنف العمل المعالج.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة ويتطلب الأمر <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|--------|--------------------------------------|--------|
| Spreadsheet | ملف | FormData (جسم HTTP) | رفع ملف جدول البيانات. |
| outPath | سلسلة نصية | استعلام | (اختياري) مسار المجلد الذي يتم فيه تخزين مصنف العمل. القيمة الافتراضية هي null. |
| outStorageName | سلسلة نصية | استعلام | اسم وحدة التخزين الخاصة بالملف الناتج. |
| fontsLocation | سلسلة نصية | استعلام | استخدام خطوط مخصصة. |
| region | سلسلة نصية | استعلام | إعدادات المنطقة/اللغة لجدول البيانات (مثال: `en-US`, `fr-FR`). تؤثر على تنسيق الأرقام وتحليل التواريخ والسلوك الخاص بالمنطقة المحلية. |
| password | سلسلة نصية | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| ----------- | ----- | ----- |
| Spreadsheet | ملف | رفع ملف جدول البيانات. |

### **الاستجابة**

```json
{
  "File": "تيار ثنائي لملف جدول البيانات المعالج"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|--------|-------|
| 200 | ناجح | تمت قبول المراجعات بنجاح وعودة الملف المعالج. |
| 400 | طلب غير صالح | الطلب غير صالح (مثال: ملف مطلوب مفقود أو معاملات غير صالحة). |
| 401 | غير مصرّح به | فشلت المصادقة أو رمز JWT مفقود/غير صالح. |
| 413 | حجم البيانات كبير جدًا | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | حدث خطأ غير متوقع في الخادم. |

## كيفية استخدام AcceptAllRevisions باستخدام مكتبات التطوير (SDKs)

### مواصفات AcceptAllRevisions

تعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات AcceptAllRevisions</a> واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=en-US&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "تيار ثنائي لملف جدول البيانات المعالج"
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات Aspose Cells Cloud SDKs

استخدام مكتبات التطوير (SDKs) هو أسرع طريقة لتسريع عملية التطوير. تقوم مكتبات التطوير بإخفاء التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="[TBD]" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDKs.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose Cells Cloud باستخدام مكتبات تطوير مختلفة:
 `[TBD]`
---