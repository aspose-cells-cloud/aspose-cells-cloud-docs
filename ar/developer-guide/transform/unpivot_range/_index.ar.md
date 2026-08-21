---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "مستند"
linktype: "docs"
url: /ar/cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "تبديل الصفوف والأعمدة في جدول البيانات."
weight: 10
---

## دالة UnpivotRange في خدمات الويب Aspose.Cells Cloud

تبديل الصفوف والأعمدة في جدول البيانات.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار/سلسلة الاستعلام/جسم HTTP | الوصف |
|-------------|-------|----------------------------------|--------|
| Spreadsheet | ملف | FormData | رفع ملف جدول البيانات. |
| worksheet | سلسلة نصية | استعلام | اسم ورقة العمل. |
| cellArea | سلسلة نصية | استعلام | نطاق بيانات محدّد. |
| skipEmptyValue | منطقي (boolean) | استعلام | إذا كانت القيمة true، فتجاهل القيم الفارغة. القيمة الافتراضية: true. |
| outPath | سلسلة نصية | استعلام | (اختياري) مسار المجلد الذي يُخزَّن فيه ملف جدول العمل. القيمة الافتراضية: null. |
| outStorageName | سلسلة نصية | استعلام | اسم وحدة التخزين للملف الناتج. |
| region | سلسلة نصية | استعلام | إعدادات منطقة/لغة جدول البيانات (مثل `en-US`، `fr-FR`). تؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك المرتبط باللغة المحلية. |
| password | سلسلة نصية | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|-------------|-------|-------|
| — | — | — |

### **الاستجابة**

```json
{
  "File": "تدفق ثنائي"
}
```

**كود حالات الاستجابة**

| الكود | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح (OK) | إرجاع ملف جدول البيانات بعد إلغاء التحويل الدائري (Unpivot). |
| 400 | طلب غير صالح (Bad Request) | معاملات طلب غير صالحة. |
| 401 | غير مصرّح (Unauthorized) | فشلت المصادقة. |
| 413 | حجم البيانات كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | واجه الخادم حالة غير متوقعة. |

## كيفية استخدام UnpivotRange باستخدام حزم تطوير البرمجيات (SDKs)

### مواصفات UnpivotRange

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}" rel="noopener noreferrer">مواصفات واجهة برمجة التطبيقات UnpivotRange</a> واجهة برمجة تفاعلية عامة مُتاحة، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose.Cells Cloud. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS للاتصال الآمن
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Sheet1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=yourPassword" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt token>" -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/unpivoted.xlsx"
}
```

{< /tab >}

{< /tabs >}

### استخدام حزم تطوير البرمجيات Aspose Cells Cloud

استخدام SDK هو أسرع طريقة لتسريع عملية التطوير. فتقوم SDK بإخفاء التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرمجيات Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب Aspose Cells Cloud باستخدام SDKs متنوعة:
 `[TBD]`
---