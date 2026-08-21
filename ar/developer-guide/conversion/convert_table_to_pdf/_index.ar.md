---
title: "تحويل الجدول إلى PDF"
ArticleTitle: "تحويل الجدول إلى PDF – واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktype: "docs"
url: /ar/cells/convert/table/pdf
aliases: []
keywords: "تحويل الجدول إلى PDF، Aspose.Cells، واجهة برمجة التطبيقات"
description: "يحوّل جدولًا من ملف جدول بيانات مخزن محليًا إلى ملف PDF باستخدام Aspose.Cells Cloud."
weight: 1000
---

## خدمة تحويل الجدول إلى PDF في Aspose.Cells Cloud

تقوم هذه العملية بقراءة ملف جدول بيانات من نظام الملفات المحلي، وتحويل الجدول المُحدّد فيه إلى مستند PDF، ثم إرجاع النتيجة المحولة. وتُنفَّذ العملية بالكامل على خوادم السحابة، لذا لا حاجة لرفع الملف مؤقتًا إلى مساحة التخزين السحابية. وتدعم واجهة برمجة التطبيقات مُعاملات اختيارية لتحديد موقع الإخراج، وخطوط مخصّصة، وتلقائي ضبط ارتفاع الصفوف/عرض الأعمدة، والإعدادات الإقليمية، وملفات العمل المحمية بكلمة مرور.

### نقطة نهاية واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المُعامل       | النوع   | المسار/سلسلة الاستعلام/جسم HTTP | الوصف                                                                                                                                                     |
|-------------------|---------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet       | ملف     | FormData                         | رفع ملف جدول البيانات.                                                                                                                                    |
| worksheet         | نص      | استعلام                         | اسم ورقة العمل في جدول البيانات.                                                                                                                          |
| tableName         | نص      | استعلام                         | اسم الجدول.                                                                                                                                               |
| outPath           | نص      | استعلام                         | (اختياري) مسار المجلد حيث يُخزَّن ملف العمل. القيمة الافتراضية هي null.                                                                                   |
| outStorageName    | نص      | استعلام                         | اسم مساحة التخزين للملف الناتج.                                                                                                                           |
| fontsLocation     | نص      | استعلام                         | استخدام خطوط مخصّصة.                                                                                                                                      |
| AutoRowsFit       | منطقي   | استعلام                         | (اختياري) ضبط ارتفاع الصفوف تلقائيًا في جميع أوراق العمل.                                                                                                |
| AutoColumnsFit    | منطقي   | استعلام                         | (اختياري) ضبط عرض الأعمدة تلقائيًا في جميع أوراق العمل.                                                                                                 |
| region            | نص      | استعلام                         | إعداد المنطقة/اللغة لجدول البيانات (مثل `en-US` أو `fr-FR`)؛ ويؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك المرتبط بالإعدادات المحلية.           |
| password          | نص      | استعلام                         | كلمة المرور لفتح ملف جدول البيانات.                                                                                                                      |

### مُعامل جسم الطلب

| اسم المُعامل | النوع | الوصف |
|-------------|-------|-------|
| *لا شيء*    | *لا شيء* | *لا يُطلَب جسم JSON؛ يُرسل الملف عبر multipart/form-data.* |

### **الاستجابة**

```json
{
  "file": "<محتوى PDF ثنائي>"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|--------|-------|
| 200 | ناجح | تمت عملية تحويل الجدول إلى PDF بنجاح؛ ويحتوي جسم الاستجابة على تيار ملف PDF. |
| 400 | طلب غير صالح | مُعطَلات الطلب غير صحيحة أو عنوان URL مُشكَل بشكل خاطئ. |
| 401 | غير مُصرّح | فشلت المصادقة أو لم تُقدَّم بيانات اعتماد. |
| 404 | غير موجود | لم يكن الملف المصدر متاحًا أو لم يُعثر على ورقة العمل/الجدول. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم ملف جدول البيانات المرفوع الحد المسموح. |
| 500 | خطأ داخلي في الخادم | حدث خطأ أثناء تحويل جدول البيانات إلى PDF. |

## كيفية استخدام خدمة تحويل الجدول إلى PDF باستخدام مكتبات SDK

###仕様 تحويل الجدول إلى PDF

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf" rel="noopener noreferrer">仕様 واجهة برمجة تطبيقات تحويل الجدول إلى PDF</a> واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells Cloud بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
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
  "file": "<محتوى PDF ثنائي>"
}
```

{< /tab >}

{< /tabs >}

### استخدام مكتبات Aspose Cells Cloud SDK

يُعد استخدام مكتبة SDK أسرع طريقة لتسريع التطوير. فالمكتبة تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells Cloud باستخدام مكتبات SDK مختلفة:

```csharp
// مثال على الكود باستخدام SDK لغة C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// مثال على الكود باستخدام SDK لغة Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# مثال على الكود باستخدام SDK لغة Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`
---