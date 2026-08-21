---
title: "إضافة علامة مائية إلى ملفات Excel"
second_title: "مستند"
linktype: "إضافة علامة مائية إلى ملفات Excel"
type: docs
url: /add-watermark-into-excel-files/
aliases: [/watermark/]
keywords: "إضافة علامة مائية إلى Excel، Aspose.Cells Cloud، REST API، SDK، C#، Java، PHP، Ruby، Node.js، Python، Perl، Go"
description: "تعرّف على كيفية إضافة علامة مائية نصية إلى كتب عمل Excel باستخدام REST API الخاص بـ Aspose.Cells Cloud (الإصدار 3.0). يشمل مثال cURL، والمعاملات المطلوبة، وتفاصيل الاستجابة."
weight: 39
ArticleTitle: "إضافة علامة مائية إلى ملفات Excel – مستندات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بإضافة **علامة مائية** إلى ملفات Excel.

**المتطلبات المسبقة:** يجب الحصول على رمز وصول JWT صالح، وتأكد من أن ملف Excel بصيغة مدعومة (مثل `.xlsx` أو `.xls`).  
**الخلفية:** العلامة المائية هي طبقة نصية شبه شفافة تُطبّق على كل ورقة عمل للإشارة إلى الملكية أو السرية.

## واجهة PostWatermark API

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### **معاملات الطلب**

| اسم المعامل | النوع | الموقع | الوصف |
|------------|-------|--------|--------|
| `file` | ملف | formData (جسم multipart) | ملف Excel الذي سيتم تطبيق العلامة المائية عليه. |
| `text` | نص | استعلام | النص المراد عرضه كعلامة مائية. |
| `color` | نص | استعلام | لون العلامة المائية بصيغة سداسية ARGB (مثل `004433ff`). |

### **الاستجابة**

تحتوي الاستجابة JSON على مصفوفة **Files**. بالنسبة لكائن كل ملف:

- **Filename** – اسم ملف الكتاب المعالَج.  
- **FileSize** – حجم الملف بالبايت.  
- **FileContent** – المحتوى المُرمّز بـ Base64 لملف Excel الذي يحتوي على العلامة المائية؛ قم بفك التشفير للحصول على الملف الفعلي.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[اسم الملف1]",
            "Filesize" : [حجم الملف],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[اسم الملف2]",
            "Filesize" : [حجم الملف],
            "FileContent" : "[Base64String]"
        },        {
            "Filename" : "[اسم الملف3]",
            "Filesize" : [حجم الملف],
            "FileContent" : "[Base64String]"
        }
    ]
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | OK (تم بنجاح) | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request (طلب غير صالح) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized (غير مصرّح) | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large (حمولة كبيرة جداً) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostWatermark API باستخدام SDKs

### **مواصفات واجهة PostWatermark API**

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) واجهة برمجة تطبيقات متاحة عموماً، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات Aspose.Cells. يُظهر المثال التالي طلباً كاملاً، بما في ذلك رأس المصادقة المطلوب. استبدل `<your-jwt-token>` برمز وصول JWT صالح تم الحصول عليه من نقطة نهاية مصادقة Aspose.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **استخدام SDKs الخاصة بـ Aspose.Cells Cloud**

استخدام SDK هو أسرع طريقة للتطوير. تقوم SDK بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على منطق أعمالك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}