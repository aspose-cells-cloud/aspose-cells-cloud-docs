---
title: "ConvertRangeToPdf"
ArticleTitle: "تحويل النطاق إلى PDF – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktype: "ConvertRangeToPdf"
type: docs
url: /ar/cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells، تحويل النطاق إلى PDF، واجهة برمجة تطبيقات"
description: "يُحوّل نطاقًا مُحدّدًا من جدول بيانات إلى PDF باستخدام Aspose.Cells Cloud."
weight: 1
---

## خدمة تحويل النطاق إلى PDF في Aspose.Cells Cloud Web Services

يُحوّل نطاقًا من جدول بيانات على محرك محلي إلى ملف PDF.

### نقطة نهاية واجهة برمجة تطبيقات الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|-------|-------------------------------------|--------|
| Spreadsheet | ملف | FormData | رفع ملف جدول البيانات. |
| worksheet | نص | استعلام | اسم ورقة العمل في جدول البيانات. |
| range | نص | استعلام | منطقة الخلايا. مثال: A1:C10 |
| outPath | نص | استعلام | (اختياري) مسار المجلد الذي يُخزَّن فيه كتاب العمل. القيمة الافتراضية هي null. |
| outStorageName | نص | استعلام | اسم وحدة التخزين الخاصة بالملف الناتج. |
| fontsLocation | نص | استعلام | استخدام خطوط مخصصة. |
| AutoRowsFit | منطقي (Boolean) | استعلام | (اختياري) ضبط ارتفاع جميع الصفوف في أوراق العمل تلقائيًا. |
| AutoColumnsFit | منطقي (Boolean) | استعلام | (اختياري) ضبط عرض جميع الأعمدة في أوراق العمل تلقائيًا. |
| region | نص | استعلام | إعدادات منطقة/لغة جدول البيانات (مثل `en-US` أو `fr-FR`). تؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك الخاص باللغة المحلية. |
| password | نص | استعلام | كلمة المرور لفتح ملف جدول البيانات. |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف |
|-------------|-------|--------|
| Spreadsheet | ملف | رفع ملف جدول البيانات. |

### **الاستجابة**

```json
{
  "file": "<محتوى PDF ثنائي>"
}
```

**رموز حالة الاستجابة**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح | تم التحويل بنجاح؛ يُعيد تدفق ملف PDF المُولّد. |
| 400 | طلب غير صالح | عنوان URL غير صحيح. |
| 401 | غير مُعتمد | فشلت المصادقة، أو لم تُقدَّم أي بيانات اعتماد. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | واجه جدول البيانات مشكلة أثناء استرجاع بيانات التحويل. |

## كيفية استخدام ConvertRangeToPdf مع مكتبات تطوير البرمجيات (SDKs)

### مواصفات ConvertRangeToPdf

تُعرّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات ConvertRangeToPdf</a> واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose Cells Cloud بسهولة. يُظهر المثال التالي كيفية إجراء استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}

{< tab tabNum="1" >}

```bash
# استخدام HTTPS لاتصال آمن
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
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

### استخدام مكتبات تطوير Aspose.Cells Cloud (SDKs)

استخدام مكتبات تطوير البرمجيات (SDKs) هو أسرع طريقة لتسريع التطوير. وتُجرّد مكتبات التطوير SDKs من التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات تطوير Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose Cells Cloud باستخدام مكتبات تطوير مختلفة:

```csharp
// كود مثال للمكتبة في C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Sheet1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// كود مثال للمكتبة في Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Sheet1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# كود مثال للمكتبة في Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Sheet1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// كود مثال للمكتبة في JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Sheet1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`
---