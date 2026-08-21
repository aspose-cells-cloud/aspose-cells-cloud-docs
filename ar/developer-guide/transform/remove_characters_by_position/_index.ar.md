---
title: "إزالة الأحرف حسب الموقع"
ArticleTitle: "إزالة الأحرف حسب الموقع – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "remove/characters-by-position"
type: docs
url: /cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells، إزالة الأحرف، واجهة برمجة التطبيقات"
description: "حذف الأحرف من الخلايا حسب الموقع في جدول بيانات."
weight: 100
---

## إزالة الأحرف حسب الموقع في خدمات الويب Aspose.Cells Cloud

يحذف الأحرف من كل خلية في النطاق المستهدف حسب الموقع (أول/آخر N أحرف، قبل/بعد سلسلة فرعية، أو بين محددين اثنين)، مع الحفاظ على الصيغ والتنسيق وتحقق البيانات.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة             | النوع   | المسار/سلسلة الاستعلام/جسم HTTP | الوصف                                                                                                        |
|-------------------------|---------|-------------------------------|--------------------------------------------------------------------------------------------------------------|
| Spreadsheet             | ملف     | FormData                      | رفع ملف جدول البيانات.                                                                                        |
| theFirstNCharacters     | عدد صحيح | استعلام                       | تحديد إزالة أول N أحرف من الخلايا المحددة. اختياري.                                                         |
| theLastNCharacters      | عدد صحيح | استعلام                       | تحديد إزالة آخر N أحرف من الخلايا المحددة. اختياري.                                                         |
| allCharactersBeforeText | سلسلة   | استعلام                       | حذف النص الموجود قبل سلسلة فرعية محددة. اختياري.                                                            |
| allCharactersAfterText  | سلسلة   | استعلام                       | حذف النص الموجود بعد سلسلة فرعية محددة. اختياري.                                                            |
| caseSensitive           | منطقي   | استعلام                       | يؤثر على وضع `Substring` و`CustomChars` عند تفعيله. اختياري.                                                |
| worksheet               | سلسلة   | استعلام                       | تحديد ورقة العمل في جدول البيانات. اختياري.                                                                 |
| range                   | سلسلة   | استعلام                       | تحديد نطاق ورقة العمل في جدول البيانات (مثل `A1:B10`). اختياري.                                           |
| outPath                 | سلسلة   | استعلام                       | (اختياري) مسار المجلد الذي يُخزن فيه ملف المصنف. الافتراضي هو null. اختياري.                               |
| outStorageName          | سلسلة   | استعلام                       | اسم وحدة التخزين للملف الناتج. اختياري.                                                                     |
| region                  | سلسلة   | استعلام                       | إعدادات منطقة/لغة جدول البيانات (مثل `en-US`، `fr-FR`). اختياري.                                            |
| password                | سلسلة   | استعلام                       | كلمة المرور لفتح ملف جدول البيانات. اختياري.                                                               |

### معلمة جسم الطلب

| اسم المعلمة | النوع | الوصف |
|-------------|-------|-------|
| Spreadsheet | ملف   | رفع ملف جدول البيانات. |

### **الاستجابة**

```json
{
  "status": "OK",
  "message": "تمت إزالة الأحرف بنجاح.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|--------|-------|
| 200 | ناجح | أكتملت العملية بنجاح وتم إرجاع الملف المعالج. |
| 400 | طلب غير صالح | الطلب غير مهيأ بشكل صحيح أو يحتوي على معلمات غير صالحة. |
| 401 | غير مصرّح | فشلت المصادقة أو أن رمز JWT مفقود/غير صالح. |
| 413 | حجم البيانات كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | حدث خطأ غير متوقع من جانب الخادم. |

## كيفية استخدام ميزة إزالة الأحرف حسب الموقع مع حزم تطوير البرمجيات (SDKs)

### مواصفات إزالة الأحرف حسب الموقع

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات إزالة الأحرف حسب الموقع</a> واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells Cloud بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "تمت إزالة الأحرف بنجاح.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### استخدام حزم تطوير البرمجيات Aspose Cells Cloud

استخدام حزمة تطوير البرمجيات (SDK) هو أسرع طريقة لتسريع التطوير. تُجرّدك حزم التطوير من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرمجيات لـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية استدعاء خدمات الويب Aspose Cells Cloud باستخدام مكتبات (SDKs) مختلفة:
`[TBD]`
---