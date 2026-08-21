---
title: "واجهة برمجة تطبيقات (API) ويب ضغط ملفات إكسل في Aspose.Cells Cloud – تقليل حجم ملفات جداول البيانات برمجيًا"
second_title: "وثيقة"
ArticleTitle: "كيفية ضغط ملفات إكسل – تقليل حجم جدول البيانات وتحسين الأداء"
linktitle: "ضغط جدول البيانات"
type: docs
url: /ar/compress-spreadsheet/
keywords: "ضغط إكسل، Aspose.Cells Cloud، تقليل حجم جدول البيانات، واجهة برمجة تطبيقات (API)، تحسين المصنف"
description: "تعرّف على كيفية ضغط مصنفات إكسل باستخدام واجهة برمجة تطبيقات (API) Aspose.Cells Cloud. احصل على أمثلة تفصيلية خطوة بخطوة، ومعاملات، ومصادقة، وأفضل الممارسات."
weight: 100
---

اضغط برمجيًا على جداول بيانات إكسل وقلّل حجم الملف باستخدام واجهة برمجة تطبيقات (API) Aspose.Cells Cloud.حسّن أداء المصنف من خلال إزالة البيانات غير المستخدمة، وضغط الكائنات المُضمَّنة، وتنظيف التنسيقات. تتيح هذه الواجهة القائمة على REST تنفيذ سير عمل ضغط وتحسين ملفات إكسل تلقائيًا.

## **واجهة برمجة تطبيقات (API) لضغط جدول البيانات**

### واجهة برمجة تطبيقات (API) الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات (APIs) Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### معاملات الطلب

| اسم المعامل | النوع | المسار/الاستعلام/النص/جسم الطلب HTTP | الوصف |
|-------------|--------|----------------------------------------|--------|
| Spreadsheet | ملف | FormData | **إجباري.** ملف المصنف إكسل المصدر (`.xlsx`، `.xls`، إلخ) المراد ضغطه. |
| level | عدد صحيح | استعلام | **اختياري.** شدة الضغط (0 = أسرع/أدنى، 9 = أبطأ/أعلى). إذا تُرك فارغًا، يُطبَّق إعداد افتراضي متوازن (5). |
| outPath | سلسلة نصية | استعلام | **اختياري.** مسار مجلد الوجهة في مساحة التخزين السحابية الخاصة بك. إذا تُرك فارغًا، يُحفظ الملف في نفس المجلد الذي يحتوي على المصنف المصدر. |
| outStorageName | سلسلة نصية | استعلام | **إجباري.** مُعرّف خدمة تخزين سحابية مُعدّة مسبقًا (مثل `CorporateDrive`). |
| region | سلسلة نصية | استعلام | **اختياري.** إعداد الإقليم (مثل `de-DE`) الذي قد يؤثر على معالجة البيانات الخاصة بالمنطقة. |
| password | سلسلة نصية | استعلام | **اختياري.** كلمة المرور لفك تشفير جدول بيانات محمي. اتركه فارغًا إذا لم يكن الملف مشفرًا. |

### الاستجابة

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح (OK) | تم تطبيق الضغط بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرّح (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حمل بيانات كبير جدًا (Payload Too Large) | حجم الملف المرفّق يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## أين يجب استخدام واجهة برمجة تطبيقات (API) لضغط جدول البيانات؟

- **توصيل التقارير تلقائيًا** – اضغط على البيانات المالية الشهرية قبل إرسالها بالبريد الإلكتروني لضمان التسليم الناجح وتحسين تجربة المستلم.
- **تحسين تحميل الملفات من قِبل المستخدمين** – اضغط على ملفات إكسل المرفوعة في الخلفية لتوفير مساحة تخزين سحابية وتقليل تكاليف التخزين.
- **معالجة وتحويل البيانات (Data-pipeline) والترحيل** – اضغط على ملفات إكسل الوسيطة الناتجة خلال عمليات ETL لتسريع نقل البيانات عبر الشبكة وتقليل الضغط على مساحات التخزين المؤقتة.

## لماذا يجب استخدام واجهة برمجة تطبيقات (API) لضغط جدول البيانات؟

- **سهل الاستخدام للمطورين** – توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يُمكّن من التطوير السريع مع توفر توثيق شامل.
- **تقليل تكاليف العمالة** – يلغي الحاجة إلى موظفين مخصصين لدمج المستندات يدويًا.
- **نظام تسعير حسب الاستخدام** – لا استثمار مبدئي؛ تدفع فقط مقابل مكالمات API التي تُنفِّذها فعليًا.
- **لا حاجة للصيانة الخوادم** – لا خوادم لصيانتها، ولا تحديثات برامج، ولا مشكلات توافق.

## كيفية استخدام واجهة برمجة تطبيقات (API) لضغط جدول البيانات باستخدام مكتبات SDK

### مواصفات واجهة برمجة تطبيقات (API) لضغط جدول البيانات

توفر [مواصفات واجهة برمجة تطبيقات (API) لضغط جدول البيانات](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) واجهة قابلة للوصول علنًا للتفاعل مع REST، مما يسمح بإجراء مكالمات مباشرة إلى API من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات إلى API السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (مشفر بـ Base64)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK لـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، حيث تُجرّد التفاصيل من المستوى المنخفض وتسمح لك بضغط جدول البيانات باستخدام بضعة أسطر من التعليمات البرمجية فقط. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK لـ Aspose.Cells Cloud.

 تعرض الأمثلة البرمجية التالية كيفية التفاعل مع خدمات ويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}