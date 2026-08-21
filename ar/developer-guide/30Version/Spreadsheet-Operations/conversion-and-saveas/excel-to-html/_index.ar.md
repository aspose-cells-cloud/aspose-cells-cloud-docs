---
title: تحويل ملف إكسل إلى HTML  
description: تحويل ملف عمل إكسل إلى ملف HTML باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud الإصدار 3.0.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# تحويل ملف إكسل إلى HTML  

تقدم Aspose.Cells Cloud نقطة نهاية REST قوية لتحويل ملف عمل إكسل (XLS أو XLSX أو CSV، إلخ) إلى مستند HTML. وتعيد العملية كائن **FileInfo** يحتوي على ملف HTML الناتج (الاسم والحجم والمحتوى مشفر بـ Base64).

---

## المتطلبات الأساسية

| المتطلبات | كيفية الاستيفاء |
|-------------|----------------|
| **حساب Aspose Cloud** | التسجيل عبر [aspose.cloud](https://www.aspose.cloud). |
| **رمز وصول JWT** | الحصول على رمز مميز نوع Bearer عبر نقطة النهاية OAuth 2.0 `POST /connect/token`. |
| **التخزين (اختياري)** | إذا أردت أن تقرأ وتخزن الواجهة البرمجية الملفات من تخزين معيّن، فقم بإنشائه أولًا (مثل Amazon S3 أو Azure Blob أو تخزين Aspose Cloud). |
| **cURL أو SDK** | أي عميل HTTP يمكنه إرسال multipart/form-data (مثل cURL أو Postman أو أحد SDKs الخاصة بـ Aspose.Cells). |

---

## المصادقة

تتطلب جميع طلبات Aspose.Cells Cloud **مصادقة تعتمد على رمز JWT**.

```http
Authorization: Bearer <access-token>
```

ويجب تضمين الرمز في رأس `Authorization` في كل طلب.

---

## نقطة النهاية

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **ملاحظة** – يجب إرسال الطلب كـ `multipart/form-data`. ويكون ملف إكسل هو الجزء الأول من جسم الطلب المتعدد الأجزاء.

---

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

## معاملات الطلب  

### معاملات الاستعلام  

| الاسم                     | النوع    | الإلزام | القيمة الافتراضية | الوصف |
|--------------------------|---------|----------|---------|-------------|
| `password`               | نص      | لا       | –       | كلمة المرور لفتح ملف عمل محمي. |
| `storageName`            | نص      | لا       | –       | اسم التخزين الذي يوجد فيه الملف المصدر. |
| `checkExcelRestriction` | منطقي   | لا       | `true`  | عندما تكون القيمة `true`، تتحقق الخدمة من القيود الخاصة بإكسل (مثل الأوراق المحمية). |
| `region`                 | نص      | لا       | –       | الإعدادات الإقليمية لملف العمل (مثل `en-US`). |
| `FontsLocation`          | نص      | لا       | –       | عنوان URL أو مسار لمجلد يحتوي على الخطوط المخصصة المطلوبة للعرض. |

### بيانات النموذج (multipart)  

| الاسم | النوع | الإلزام | الوصف |
|------|------|----------|-------------|
| **File** | ملف | **نعم** | ملف عمل إكسل المراد تحويله. يجب تزويده كأول جزء في طلب multipart. |

---

## مثال على الطلب (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/your_workbook.xlsx"
```

---

## الاستجابة الناجحة  

**رمز الحالة:** `200 OK`

| الحقل        | النوع   | الوصف |
|--------------|--------|-------------|
| `Filename`   | نص     | اسم ملف HTML الناتج (مثل `example.html`). |
| `FileSize`   | عدد صحيح | حجم ملف HTML بالبايتات. |
| `FileContent`| نص     | محتوى HTML مشفر بـ Base64. |

```json
{
  "Filename": "example.html",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

ويُعرّف مخطط الاستجابة باستخدام نموذج **FileInfo**: [/cells/file-info](/cells/file-info/).

---

## استجابات الأخطاء  

| الرمز | المعنى | مثال على حمل البيانات |
|------|------------------------|-----------------|
| `400` | طلب غير صالح – معلمات مفقودة أو غير صحيحة | ```json { "Code": "BadRequest", "Message": "الجزء 'File' إلزامي." } ``` |
| `401` | غير مُصادق عليه – رمز JWT غير صالح أو مفقود | ```json { "Code": "InvalidToken", "Message": "رمز الوصول مفقود أو منتهٍ." } ``` |
| `404` | غير موجود – الملف المصدر غير موجود في التخزين المحدد | ```json { "Code": "FileNotFound", "Message": "الملف 'my.xlsx' غير موجود في التخزين 'MyStorage'." } ``` |
| `413` | حمل البيانات كبير جدًا – تجاوز حجم الملف المرفوع الحد المسموح به | ```json { "Code": "RequestEntityTooLarge", "Message": "تجاوز الملف المرفوع الحد المسموح به وهو 100 ميغابايت." } ``` |
| `429` | طلبات كثيرة جدًا – تم تجاوز حد المعدل | ```json { "Code": "TooManyRequests", "Message": "تم تجاوز حد المعدل المكوّن من 60 طلب في الدقيقة." } ``` |
| `500` | خطأ داخلي في الخادم – ظرف غير متوقع في الخادم | ```json { "Code": "InternalError", "Message": "حدث خطأ غير متوقع. يُرجى المحاولة مرة أخرى لاحقًا." } ``` |

---

## حدود المعدل  

| الحد | الوصف |
|-------|-------------|
| **60 طلب في الدقيقة** لكل حساب (الافتراضي) | يؤدي تجاوز هذا الحد إلى إرجاع `429 Too Many Requests`. عدّل منطق عميلك أو اطلب حصة أعلى عبر بوابة Aspose Cloud. |

---

## دعم SDKs

تقدم Aspose SDKs مُخصصة تغلف نقطة النهاية هذه لعدة لغات برمجة. توضح الأمثلة التالية نفس عملية التحويل باستخدام SDKs الرسمية.

| اللغة | المثال |
|----------|--------|
| C#       | <details><summary>عرض المثال</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java     | <details><summary>عرض المثال</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python   | <details><summary>عرض المثال</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js  | <details><summary>عرض المثال</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go       | <details><summary>عرض المثال</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP      | <details><summary>عرض المثال</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby     | <details><summary>عرض المثال</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl     | <details><summary>عرض المثال</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

للاطلاع على القائمة الكاملة لـ SDKs المدعومة ولتعليمات التثبيت، راجع مستودع **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud>.

---

## نقاط نهاية ذات صلة  

| نقطة النهاية | الوصف |
|----------|-------------|
| `POST /cells/{name}/saveAs` | حفظ ملف إكسل موجود مسبقًا كملف HTML (أو تنسيقات أخرى) مباشرة في التخزين. |
| `PUT /cells/convert` | تحويل ملف عمل إلى HTML مع خيارات تحويل إضافية؛ وتُرجع النتيجة في جسم الاستجابة. |
| `GET /cells/{name}` | استرجاع ملف عمل مخزن مسبقًا كـ HTML (أو تنسيقات أخرى) مع معاملات استعلام اختيارية. |

---

## الأسئلة الشائعة  

**س:** *كيف أُجري المصادقة عند استدعاء API تحويل ملف إكسل إلى HTML؟*  
**ج:** يتطلب تضمين رأس `Authorization: Bearer <access-token>` تم الحصول عليه من نقطة النهاية OAuth 2.0 `/connect/token`.

**س:** *ماذا يحتوي رمز الاستجابة fileInfo؟*  
**ج:** يحتوي على ثلاثة حقول – `Filename` (نص)، `FileSize` (عدد صحيح بالبايتات)، و`FileContent` (محتوى HTML مشفر بـ Base64).

**س:** *ما هي رموز الأخطاء التي قد أصادفها؟*  
**ج:** `400` (طلب غير صالح)، `401` (غير مُصادق عليه)، `404` (الملف غير موجود)، `413` (حمل البيانات كبير جدًا)، `429` (طلبات كثيرة جدًا)، `500` (خطأ داخلي في الخادم). وتعيد كل منها حمل بيانات JSON يحتوي على `Code` و`Message`.

**س:** *هل يمكنني تحديد موقع مخصص للخطوط؟*  
**ج:** نعم. استخدم معامل الاستعلام `FontsLocation` لتحديد مجلد أو عنوان URL يحتوي على الخطوط المطلوبة.

**س:** *هل يوجد حد لمعدل هذه العملية؟*  
**ج:** الحد الافتراضي هو **60 مكالمة في الدقيقة** لكل حساب. يؤدي تجاوزه إلى إرجاع `429 Too Many Requests`.

---

## Breadcrumb JSON‑LD (بيانات هيكلية)

إضافة هذا المقطع يحسّن تحسين محركات البحث (SEO) من خلال تمكين شريط التنقل الغني (rich-snippet breadcrumbs) في نتائج البحث.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "الصفحة الرئيسية", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "مركز المطورين", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "التحويل", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "تحويل إكسل إلى HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## سجل التغييرات  

| الإصدار | التاريخ | التغييرات |
|---------|--------|---------|
| **v3.0** | 2024-10-01 | الإصدار العام الأول لـ `PostConvertWorkbookToHtml`. |
| **v3.1** | 2025-04-15 | أُضيف معاملات الاستعلام `region` و`FontsLocation`؛ وحدّث تنسيق حمل بيانات الأخطاء. |
| **v3.2** | 2026-03-20 | أُدخل وثائق حدود المعدل ونماذج استجابات الأخطاء. |

--- 

*لأي مساعدة إضافية، يُرجى التواصل مع دعم Aspose أو زيارة المرجع الرسمي لواجهة برمجة التطبيقات:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---