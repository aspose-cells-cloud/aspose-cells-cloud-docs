---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "Document"
linktype: "FlipData"
type: docs
url: /ar/cells/flip
aliases: []
keywords: "FlipData, تحويل، Aspose.Cells"
description: "يُقلب اتجاه نطاق بيانات مُحدّد في ملف جدول بيانات."
weight: 100
---

## FlipData في خدمات ويب Aspose.Cells Cloud

تُعيد هذه الواجهة البرمجية تغيير اتجاه مصفوفة البيانات المعطاة. فعلى سبيل المثال، سيتحول النطاق 3×2 (3 صفوف وعمودان) إلى نطاق 2×3 (صفان و3 أعمدة) في المخرجات. وتُستخدم هذه الميزة عادةً لإعادة هيكلة البيانات لتلبية متطلبات الإدخال الخاصة بمختلف المخططات أو التقارير أو نماذج البيانات.

### نقطة نهاية الواجهة البرمجية للويب

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **الأمان والمصادقة**

تعمل واجهات برمجة تطبيقات Aspose.Cells Cloud بشكل آمن وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|-------|-------------------------------------|--------|
| Spreadsheet | ملف | FormData | رفع ملف جدول البيانات. |
| worksheet | نص | استعلام | اسم ورقة العمل. |
| cellArea | نص | استعلام | نطاق بيانات مُحدّد. |
| Horizontal | منطقي | استعلام | قلب أفقي/رأسي. القيمة الافتراضية: true |
| outPath | نص | استعلام | (اختياري) مسار المجلد حيث يتم حفظ ملف العمل. القيمة الافتراضية: null. |
| outStorageName | نص | استعلام | اسم وحدة التخزين الخاصة بالملف الناتج. |
| region | نص | استعلام | إعدادات منطقة/لغة جدول البيانات (مثل `en-US`, `fr-FR`). تؤثر على تنسيق الأرقام، وتحليل التواريخ، والسلوك الخاص بالمنطقة المحلية. |
| password | نص | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|-------------|-------|-------|
| *لا يوجد* | *غير مُعرّف* | *لا يُطلب أي جسم JSON إضافي؛ يتم إرسال الملف كـ multipart/form-data.* |

### **الاستجابة**

```json
{
  "File": "<تدفق ثنائي لملف العمل المحوّل>"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح | اكتملت العملية بنجاح وعُاد ملف جدول البيانات المحوّل. |
| 400 | طلب غير صالح | معامل مطلوب مفقود أو غير صالح أو أكثر. |
| 401 | غير مصرّح به | فشلت المصادقة – رمز JWT مفقود أو غير صالح. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوق الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | حدث خطأ غير متوقع في الخادم. |

## كيفية استخدام FlipData مع مكتبات SDK

### مواصفات FlipData

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData" rel="noopener noreferrer">مواصفات FlipData API</a> واجهة برمجة تطبيقات متاحة للعامة وتسمح لك بإجراء عمليات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells Cloud. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
# استخدم HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<تدفق ثنائي لملف العمل المحوّل>"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة لتسريع عملية التطوير. وتُجسّد مكتبة SDK التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose Cells Cloud باستخدام مكتبات SDK مختلفة:
 `[TBD]`
---