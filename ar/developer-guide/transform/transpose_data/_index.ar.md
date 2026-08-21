---
title: "TransposeData"
ArticleTitle: "TransposeData – واجهة برمجة تطبيقات Aspose.Cells السحابية"
second_title: "وثيقة"
linktype: "docs"
url: /ar/cells/transpose
aliases: [  /ar/cells/transpose ]
keywords: "TransposeData، Aspose.Cells، واجهة برمجة تطبيقات سحابية، جدول بيانات، نقل بيانات"
description: "تبديل الصفوف والأعمدة في جدول البيانات."
weight: 1000
---

## خدمة TransposeData لـ Aspose.Cells Cloud Web

تبديل الصفوف والأعمدة في جدول البيانات.

### نقطة نهاية واجهة برمجة التطبيقات على الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|-------|------------------------------------|--------|
| Spreadsheet | ملف | FormData | تحميل ملف جدول البيانات. |
| worksheet | نص | استعلام | اسم ورقة العمل. |
| cellArea | نص | استعلام | نطاق بيانات محدّد. |
| outPath | نص | استعلام | (اختياري) مسار المجلد حيث يتم تخزين ملف العمل. القيمة الافتراضية هي null. |
| outStorageName | نص | استعلام | اسم وحدة التخزين للملف الناتج. |
| region | نص | استعلام | إعداد المنطقة/اللغة لجدول البيانات (مثل `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك الخاص بالمنطقة المحلية. |
| password | نص | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **الاستجابة**

```json
{
  "file": "تدفق ثنائي لجدول البيانات المُنقل"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|------|---------|--------|
| 200 | ناجح | يتم إرجاع ملف جدول البيانات المُنقل. |
| 400 | طلب غير صالح | معاملات مدخلات غير صحيحة أو طلب مُشكَّل بشكل غير سليم. |
| 401 | غير مصرّح به | فشلت المصادقة أو كان رمز JWT مفقودًا أو غير صالح. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المحمل الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام TransposeData باستخدام مكتبات SDK

### مواصفات TransposeData

تُعرّف [مواصفات واجهة برمجة تطبيقات TransposeData](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose Cells Cloud بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لإنشاء اتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Sheet1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
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
  "file": "تدفق ثنائي لجدول البيانات المُنقل"
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات SDK الخاصة بـ Aspose Cells Cloud

استخدام SDK هو أسرع طريقة لتسريع التطوير. تُجرّدك المكتبة من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose Cells Cloud باستخدام مكتبات SDK المختلفة:
`[TBD]`
---