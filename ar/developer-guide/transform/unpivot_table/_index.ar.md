---
title: "إلغاء تدوير الجدول"
ArticleTitle: "إلغاء تدوير الجدول – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "إلغاء تدوير الجدول"
type: docs
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells، إلغاء تدوير، تحويل"
description: "تبديل الصفوف والأعمدة في المصنف."
weight: 1
---

## جدول إلغاء تدوير Aspose.Cells Cloud Web Services

تبديل الصفوف والأعمدة في المصنف.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل       | النوع     | المسار / سلسلة الاستعلام / جسم HTTP | الوصف                                                                                                           |
|------------------|-----------|-------------------------------------|------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | ملف       | FormData                            | رفع ملف المصنف.                                                                                                 |
| worksheet        | نص        | استعلام                             | اسم ورقة العمل.                                                                                                 |
| index            | عدد صحيح   | استعلام                             | نطاق بيانات مُحدَّد.                                                                                             |
| skipEmptyValue   | منطقي     | استعلام                             | تخطي القيم الفارغة (الافتراضي: true).                                                                             |
| outPath          | نص        | استعلام                             | (اختياري) مسار المجلد حيث يُخزَّن المصنف. القيمة الافتراضية هي null.                                              |
| outStorageName   | نص        | استعلام                             | اسم وحدة التخزين للملف الناتج.                                                                                  |
| region           | نص        | استعلام                             | إعداد منطقة/لغة المصنف (مثل `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام، وتحليل التواريخ، والسلوك الخاص بالمنطقة.   |
| password         | نص        | استعلام                             | كلمة المرور لفتح ملف المصنف.                                                                                    |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|------------|-------|-------|
| N/A        | N/A   | لا توجد معاملات في جسم الطلب. |

### **الاستجابة**

```json
{
  "File": "تدفق ثنائي لمصنف تم إلغاء تدويره"
}
```

**رموز حالة الاستجابة**

| الكود | المعنى | الوصف |
|------|--------|-------|
| 200 | ناجح | يتم إرجاع ملف المصنف الذي تم إلغاء تدويره. |
| 400 | طلب غير صالح | معاملات طلب غير صحيحة. |
| 401 | غير مصادق عليه | فشلت المصادقة أو نقص رمز JWT أو كان غير صالح. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام إلغاء تدوير الجدول مع مكتبات SDK

### مواصفات إلغاء تدوير الجدول

تُعرِّف [مواصفات API إلغاء تدوير الجدول](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) واجهة برمجة تطبيقات متاحة علنًا، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "تدفق ثنائي لمصنف تم إلغاء تدويره"
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات SDK الخاصة بـ Aspose Cells Cloud

استخدام SDK هو أسرع طريقة لتسريع عملية التطوير. وتُجرِّدك المكتبة من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose Cells Cloud باستخدام مكتبات SDK المختلفة:
 `[TBD]`
---