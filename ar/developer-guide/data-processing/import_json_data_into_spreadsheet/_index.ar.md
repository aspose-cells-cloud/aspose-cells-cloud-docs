---
title: "استيراد بيانات JSON إلى جدول بيانات"
ArticleTitle: "استيراد بيانات JSON إلى جدول بيانات – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktype: "استيراد بيانات JSON إلى جدول بيانات"
type: docs
url: /ar/cells/import/data/json
aliases: []
keywords: "استيراد JSON, Aspose.Cells, جدول بيانات, واجهة برمجة تطبيقات"
description: "استيراد ملف بيانات JSON إلى جدول البيانات المحلي."
weight: 1
---

## استيراد بيانات JSON إلى جدول بيانات باستخدام خدمات Aspose.Cells Cloud الويبية

استيراد ملف بيانات JSON إلى جدول البيانات المحلي. تُحلّ هذه الطريقة تنسيق JSON، وتُعيّن البيانات على هيكل خلايا جدول البيانات، ثم تحفظ الملف محليًا. وتشمل تنسيقات جداول البيانات المدعومة: `.xlsx` و `.ods`.

### نقطة نهاية واجهة برمجة التطبيقات الويبية

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار/سلسلة الاستعلام/جسم HTTP | الوصف |
|-------------|--------|--------------------------------|--------|
| datafile | ملف | FormData | رفع ملف البيانات. |
| Spreadsheet | ملف | FormData | رفع ملف جدول البيانات. |
| worksheet | نص | استعلام | اسم ورقة العمل التي يجب استيراد بيانات JSON إليها. |
| startcell | نص | استعلام | الموقع الابتدائي لاستيراد البيانات. |
| insert | منطقي | استعلام | يتحكم في سلوك الإدراج. `true`: إدراج البيانات؛ `false`: استبدال البيانات الموجودة. (الافتراضي: true) |
| outPath | نص | استعلام | (اختياري) مسار المجلد الذي يتم فيه تخزين المصنف. الافتراضي هو `null`. |
| outStorageName | نص | استعلام | اسم وحدة التخزين للملف الناتج. |
| fontsLocation | نص | استعلام | استخدام خطوط مخصصة. |
| region | نص | استعلام | إعداد المنطقة/اللغة لجدول البيانات (مثل `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام، وتحليل التواريخ، والسلوك الخاص باللغة. |
| password | نص | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **الاستجابة**

```json
{
  "file": "تيار ثنائي"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | ناجح | تم إنشاء الملف وعودته بنجاح. |
| 400 | طلب غير صالح | عنوان URL غير صالح. |
| 401 | غير مصرح به | فشلت المصادقة أو لم تُقدّم أي بيانات اعتماد. |
| 404 | غير موجود | الملف المصدر غير قابل للوصول. |
| 413 | حجم الحمولة كبير جدًا | [TBD] |
| 500 | خطأ داخلي في الخادم | واجه جدول البيانات خطأً أثناء استلام البيانات. |

## كيفية استخدام استيراد بيانات JSON إلى جدول بيانات باستخدام مكتبات SDK

###仕様 استيراد بيانات JSON إلى جدول بيانات

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet" rel="noopener noreferrer">仕樣 واجهة برمجة تطبيقات استيراد بيانات JSON إلى جدول البيانات</a> واجهة برمجة تطبيقات قابلة للوصول عامّة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب Aspose Cells Cloud. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}
{< tab tabNum="1" >}
```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Sheet1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=en-US&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "تيار ثنائي"
}
```
{< /tab >}
{< /tabs >}

### استخدام مكتبات Aspose Cells Cloud SDK

استخدام مكتبة SDK هو أسرع طريقة لتسريع التطوير. فتقوم مكتبة SDK بإخفاء التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب Aspose Cells Cloud باستخدام مكتبات SDK المختلفة:
`[TBD]`