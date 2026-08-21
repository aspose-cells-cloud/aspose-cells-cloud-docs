---
title: "تحويل ملف إكسل إلى SQL"
second_title: "مستند"
linktitle: "تحويل ملف إكسل إلى SQL"
type: docs
url: /convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, تحويل إكسل إلى SQL, واجهة برمجة التطبيقات السحابية, تحويل جداول البيانات, REST"
description: "استخدم واجهة برمجة التطبيقات السحابية REST الخاصة بـ Aspose.Cells لتحويل جداول بيانات إكسل إلى ملفات SQL. تدعم عدة SDKs ولغات برمجة لدمج سلس في تطبيقاتك."
weight: 100
ArticleTitle: "تحويل إكسل إلى SQL – واجهة برمجة التطبيقات السحابية لـ Aspose.Cells"
---

تقوم هذه الواجهة البرمجية REST بتحويل ملف جدول بيانات إلى تنسيق ملف SQL.

**المتطلبات الأساسية**  
ل استخدام هذه الواجهة، يجب أن يكون لديك رمز JWT صالح تم إنشاؤه كما هو موضح في دليل <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>. تدعم الواجهة ملفات إكسل حتى حدود الحجم المحددة في وثائق الخدمة، ويمكنها معالجة ملفات العمل المحمية بكلمة مرور عند تزويد معامل الاستعلام `password`.

## واجهة PostConvertWorkbookToSQL البرمجية

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة التطبيقات السحابية لـ Aspose.Cells أمانًا ويجب المصادقة عبر <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">رمز JWT</a>.

### **معامل الاستعلام**

| اسم المعامل             | النوع   | الوصف                                                                 |
| ----------------------- | ------- | --------------------------------------------------------------------- |
| password                | string  | كلمة المرور المطلوبة لفتح ملف إكسل.                                  |
| storageName             | string  | اسم وحدة التخزين التي يُخزَّن فيها الملف.                             |
| checkExcelRestriction   | bool    | يشير إلى ما إذا كان سيتم فحص قيود ملف إكسل عند تعديل كائنات مرتبطة بالخلايا. |

### **معامل جسم الطلب**

| اسم المعامل | النوع       | الوصف                                                                |
| ----------- | ----------- | -------------------------------------------------------------------- |
| datafile    | data file   | ملف جدول البيانات المراد تحويله، ويُضمَّن كجزء أول في الطلب.        |

### الاستجابة

ترجع الواجهة كائن **FileInfo** يحتوي على ملف SQL المُولَّد.

| الحقل            | النوع   | الوصف                                      |
| ----------------- | ------- | ------------------------------------------ |
| **Filename**      | string  | اسم ملف SQL (مثل `example.sql`).         |
| **FileSize**      | int     | حجم الملف بالبايت.                         |
| **FileContent**   | string  | محتوى ملف SQL مشفرًا بترميز Base64.        |

[FileInfo](/cells/file-info/)

**كودات حالة HTTP**

| الكود | المعنى                         | الوصف                                                           |
|------|-------------------------------|-----------------------------------------------------------------|
| 200  | نجاح                          | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.     |
| 400  | طلب غير صالح                  | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).           |
| 401  | غير مصرح به                   | رمز JWT غير صالح أو مفقود.                                     |
| 413  | حجم الحمولة كبير جدًا          | حجم الملف المرفوع يتجاوز الحد المسموح.                          |
| 500  | خطأ داخلي في الخادم            | خطأ غير متوقع في الخادم.                                       |

## كيفية استخدام واجهة PostConvertWorkbookToSQL باستخدام SDKs

### مواصفات واجهة PostConvertWorkbookToSQL

تُعرِّف <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تفاعلية عامة وتتيح تنفيذ تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى الواجهة السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فهي تُدار بالتفاصيل من المستوى المنخفض، وتتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## واجهات برمجية أخرى تنفذ هذه الوظيفة

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – تحفظ ملف عمل بتنسيق مختلف وتخزن الناتج في وحدة التخزين المحددة.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – تحول ملف عمل إلى تنسيق آخر مع إعدادات اختيارية وترد بالنتيجة في الاستجابة.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – تسترجع ملف عمل مع إعدادات تحويل اختيارية.

**ملاحظات**  
- عند تحويل ملفات إكسل المحمية بكلمة مرور، تأكد من تزويد معامل الاستعلام `password`؛ وإلا فشلت العملية مع خطأ 400.  
- تُرجع الخدمة محتوى ملف SQL كنص مشفر بـ Base64؛ ويجب فك التشفير قبل حفظه في ملف `.sql`.  

**ملفات عينات**  
حمّل ملف عمل إكسل تجريبي [هنا](https://example.com/sample.xlsx) ونتائج SQL جاهزة [هنا](https://example.com/sample.sql) لاختبار الواجهة بسرعة.