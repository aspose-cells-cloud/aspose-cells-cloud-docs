---
title: "دمج ملفات إكسل متعددة في جدول بيانات واحد – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
ArticleTitle: "دمج ملفات إكسل متعددة في ملف واحد – دمج دفعة لجداول البيانات إلى أكثر من 30 صيغة"
linktype: "دمج جداول البيانات"
type: docs
url: /ar/merge-spreadsheets/
keywords: "Aspose.Cells، دمج جداول البيانات، واجهة برمجة تطبيقات إكسل، جدول بيانات سحابي، دمج دفعة، تحويل إلى PDF، دمج CSV، دمج ODS، مرجع واجهة برمجة التطبيقات، حزمة تطوير برمجيات (SDK)"
description: "دمج ملفات إكسل أو CSV أو ODS المحلية المتعددة في ملف عمل واحد وتحويل الناتج إلى أكثر من 30 صيغة (PDF، HTML، إلخ) باستخدام Aspose.Cells Cloud. يشمل نقطة النهاية (endpoint)، المعاملات، دليل المصادقة، وأمثلة SDK."
weight: 100
---

قم بدمج ملفات إكسل أو CSV أو ODS المحلية المتعددة في ملف عمل واحد وتحويله إلى أكثر من 30 صيغة إخراج باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud.

### واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معاملات الطلب**

| اسم المعامل      | النوع   | الموقع             | الوصف                                                                                           |
| ---------------- | ------- | ------------------ | ----------------------------------------------------------------------------------------------- |
| Spreadsheet      | ملف    | FormData           | ملف جدول البيانات المحلي المراد تحميله. يدعم XLSX وXLS وCSV وODS وغيرها.                         |
| outFormat        | نص     | استعلام (Query)    | صيغة الإخراج المرغوبة (مثل: `XLSX`، `PDF`، `CSV`، `HTML`). يدعم أكثر من 30 صيغة.                |
| mergeInOneSheet  | منطقي  | استعلام (Query)    | `true` → تُدمج كل البيانات في ورقة عمل واحدة؛ `false` → تحافظ على كل ورقة أصلية على حدة.         |
| outPath          | نص     | استعلام (اختياري)  | مسار المجلد السحابي الذي سيتم حفظ الملف المدمج فيه. إذا تُرك فارغًا، يُستخدم الموقع الافتراضي.    |
| outStorageName   | نص     | استعلام (Query)    | اسم التخزين السحابي المراد استخدامه (افتراضي أو مخصص).                                         |
| fontsLocation    | نص     | استعلام (اختياري)  | مسار المجلد السحابي الذي يحتوي على الخطوط المخصصة لتصيير PDF أو الصور بشكل صحيح.               |
| region           | نص     | استعلام (اختياري)  | الإعدادات المحلية لتنسيق الأرقام والتاريخ والعملات (مثل: `en-US`، `zh-CN`).                    |
| password         | نص     | استعلام (اختياري)  | كلمة المرور لفتح جدول بيانات محمي.                                                              |

### **الاستجابة**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

يمكن تنزيل الملف مباشرة أو حفظه في الموقع المحدد عبر `outPath`.

**تفاصيل استجابة ناجحة**

| رمز الحالة | نوع المحتوى (Content‑Type) | الوصف                                         |
| ----------- | -------------------------- | ---------------------------------------------- |
| 200 OK      | `application/octet-stream` | تدفق ثنائي لملف العمل المدمج.                 |

**أكواد حالة HTTP**

| الرمز | المعنى                     | الوصف                                                           |
| ----- | -------------------------- | --------------------------------------------------------------- |
| 200   | OK (نجاح)                 | تمت تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.    |
| 400   | Bad Request (طلب خاطئ)    | معاملات ناقصة أو غير صالحة (مثل: نوع ملف غير مدعوم).          |
| 401   | Unauthorized (غير مُصادَق) | رمز JWT غير صالح أو مفقود.                                     |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح.                     |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                |

## أين يجب استخدام واجهة برمجة تطبيقات دمج جداول البيانات؟

### **التعليم والتطبيقات الأكاديمية**

- **تصحيح وتصنيف مهام الطلاب** – دمج ملفات مهام الطلاب المتعددة لتقديم تعليقات موحدة وتصنيفها.
- **جمع بيانات البحوث** – دمج جداول البيانات من مجموعات تجريبية مختلفة في ملف واحد.
- **إنشاء مواد تعليمية** – دمج تمارين من فصول متعددة في ملف عمل واحد لقاعدة أسئلة موحدة.

### **معالجة البيانات وتحليلها**

- **دمج مجموعات بيانات صغيرة** – دمج ملفات CSV أو إكسل المصدر من مصادر متنوعة.
- **المعالجة المسبقة لتحليل البيانات** – دمج ملفات البيانات ذات الصلة قبل إجراء التحليل.
- **ملء قوالب البيانات النموذجية** – تعبئة قوالب التقارير الجاهزة بالبيانات المدمجة.

### **التطوير ودعم التقنية**

- **تجهيز بيانات الاختبار** – دمج ملفات حالات اختبار متعددة للاختبار الآلي.
- **تحليل سجلات النظام** – دمج تقارير سجلات النظام (Excel) من فترات زمنية مختلفة.
- **إدارة الإعدادات** – دمج ملفات إعدادات متعددة في ملف إعداد موحد.

## لماذا يجب استخدام واجهة برمجة تطبيقات دمج جداول البيانات؟

- **سهلة الاستخدام للمطورين** – تتوفر مكتبات SDK للعديد من لغات البرمجة، ما يقلل جهد التطوير مقارنةً ببناء حل مخصص.
- **خفض تكاليف العمالة** – يلغي الحاجة إلى موظفين مخصصين لأداء مهام دمج المستندات يدويًا.
- **الدفع حسب الاستخدام** – ادفع فقط مقابل استدعاءات واجهة برمجة التطبيقات التي تستخدمها فعليًا؛ لا حاجة لاستثمار مسبق.
- **أصفار تكاليف الصيانة** – لا خوادم للصيانة، ولا تحديثات برمجية، ولا مخاوف تتعلق بالتوافق.

## كيفية استخدام واجهة برمجة تطبيقات دمج جداول البيانات مع SDKs

### مواصفات OpenAPI

توفر <a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">مواصفات OpenAPI</a> وصفًا قابلًا للقراءة من قبل الآلة لواجهة برمجة التطبيقات، ما يتيح التفاعل المباشر عبر REST.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء استدعاءات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (مشفرة بـ Base64)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، حيث يُجرّدك من تفاصيل المستوى المنخفض، ويسمح لك باستيراد البيانات في ورقة عمل جدول بيانات باستخدام كود موجز. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}