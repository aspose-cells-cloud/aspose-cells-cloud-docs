---
title: "ConvertWorksheetToPdf"
ArticleTitle: "تحويل ورقة عمل إلى PDF – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "ConvertWorksheetToPdf"
type: docs
url: /cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells، تحويل ورقة عمل إلى PDF، واجهة برمجة تطبيقات"
description: "يحول ورقة عمل من ملف جدول بيانات إلى ملف PDF باستخدام Aspose.Cells Cloud."
weight: 10
---

## دالة ConvertWorksheetToPdf في خدمات الويب Aspose.Cells Cloud

تقوم هذه الطريقة بقراءة ملف جدول بيانات من نظام الملفات المحلي، وتحويل ورقة العمل الخاصة به إلى ملف PDF، ثم إرجاع النتيجة المحولة. يجب تحديد مسار الملف المصدر والتنسيق الهدف بشكل صحيح. تأكد من وجود الأذونات الضرورية لقراءة ملف المصدر وكتابة الملف المحول عند الضرورة. تتم عملية التحويل بالكامل على خادم السحابة، ما يلغي الحاجة إلى أي مساحة تخزين سحابية أو تنزيلات خارجية.

تشمل الميزات الرئيسية التحويل المُبنَى على السحابة، وتقليل العبء على موارد السحابة، وتبسيط سير العمل.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل      | النوع    | المسار / سلسلة الاستعلام / جسم HTTP | الوصف                                                                                                                                              |
|------------------|----------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ملف      | FormData                            | رفع ملف جدول البيانات.                                                                                                                              |
| worksheet        | نص (String) | استعلام                            | اسم ورقة العمل في جدول البيانات.                                                                                                                    |
| outPath          | نص (String) | استعلام                            | (اختياري) مسار المجلد الذي يُخزَّن فيه ملف المصنف. القيمة الافتراضية هي null.                                                                      |
| outStorageName   | نص (String) | استعلام                            | اسم مساحة التخزين للملف الناتج.                                                                                                                     |
| fontsLocation    | نص (String) | استعلام                            | استخدام خطوط مخصصة.                                                                                                                                 |
| AutoRowsFit      | منطقي (Boolean) | استعلام                            | (اختياري) ضبط ارتفاع جميع الصفوف في أوراق العمل تلقائيًا.                                                                                           |
| AutoColumnsFit   | منطقي (Boolean) | استعلام                            | (اختياري) ضبط عرض جميع الأعمدة في أوراق العمل تلقائيًا.                                                                                            |
| region           | نص (String) | استعلام                            | إعدادات إقليم/لغة جدول البيانات (مثل `en-US`، `fr-FR`). تؤثر على تنسيق الأرقام وتحليل التواريخ والسلوك الخاص بالمنطقة الجغرافية.                   |
| password         | نص (String) | استعلام                            | كلمة المرور لفتح ملف جدول البيانات.                                                                                                                 |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| [TBD]          |      |             |

### **الاستجابة**

```json
{
  "file": "<تدفق ثنائي لملف PDF المُولَّد>"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|---------|-------------|
| 200 | نجاح (OK) | تم تحويل ورقة العمل إلى PDF بنجاح وإرجاعها كتدفق ملف. |
| 400 | طلب غير صالح (Bad Request) | معاملات طلب غير صحيحة أو عنوان URL غير مُنسَّق. |
| 401 | غير مُصادَق (Unauthorized) | فشلت المصادقة أو لم تُوفَّر أي بيانات اعتماد. |
| 404 | غير موجود (Not Found) | الملف المصدر غير قابل للوصول. |
| 413 | حمل مُرسل كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | واجه جدول البيانات اختلالًا أثناء عملية التحويل. |

## كيفية استخدام ConvertWorksheetToPdf مع مكتبات SDK

### مواصفات ConvertWorksheetToPdf

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات ConvertWorksheetToPdf</a> واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدم بروتوكول HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sheet1&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&AutoRowsFit=true&AutoColumnsFit=true&region=en-US&password=SecretPwd" \
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
  "file": "<تدفق ثنائي لملف PDF المُولَّد>"
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات Aspose.Cells Cloud SDK

استخدام مكتبة SDK هو أسرع طريقة لتسريع عملية التطوير. فتُجرِّد مكتبة SDK التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب Aspose.Cells Cloud باستخدام مكتبات SDK المختلفة:
`[TBD]`
---