---
title: "تحويل دفعات من ملفات إكسل"
second_title: "مستند"
type: docs
url: /batch/convert
keywords: "التحويل الدفعي، إكسل، Aspose.Cells Cloud، واجهة REST API، PDF، CSV، JSON، Markdown، جدول بيانات"
description: "تعرّف على كيفية استخدام واجهة Aspose.Cells Cloud API لتحويل دفعات متعددة من ملفات إكسل إلى تنسيقات مثل PDF وCSV وJSON أو Markdown. يتضمّن هذا الدليل تفاصيل نقطة نهاية REST ومعلمات الطلب ومثال باستخدام cURL وأكواد مقتطفات SDK بلغات برمجة مختلفة."
weight: 100
---

تتيح هذه الواجهة البرمجية لواجهة REST **التحويل الدفعي** للملفات المؤهلة.

## واجهة REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/convert
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة         | النوع   | الموقع | الوصف                                                |
|----------------------|--------|--------|--------------------------------------------------------|
| **batchConvertRequest** | كائن   | الجسم  | جسم الطلب الذي يحتوي على إعدادات التحويل.             |

#### خصائص BatchConvertRequest

| الاسم               | النوع                 | الوصف                                              | الملاحظات |
|--------------------|----------------------|-----------------------------------------------------|-----------|
| **SourceFolder**    | سلسلة نصية            | مسار المجلد الذي يحتوي على ملفات إكسل المصدر.      | [اختياري]  |
| **MatchCondition**  | MatchConditionRequest | الشروط المستخدمة لاختيار الملفات للتحويل.          | [اختياري]  |
| **Format**          | سلسلة نصية            | التنسيق الهدف للتحويل (مثل `pdf`، `csv`).           | [اختياري]  |
| **OutFolder**       | سلسلة نصية            | المجلد الوجهة التي سيتم حفظ الملفات المحولة فيها.   | [اختياري]  |
| **SaveOptions**     | SaveOptions           | خيارات إضافية تتحكم في كيفية حفظ الملفات.           | [اختياري]  |

#### خصائص MatchConditionRequest

| الاسم                  | النوع       | الوصف                                              | الملاحظات |
|------------------------|-------------|-----------------------------------------------------|-----------|
| **RegexPattern**       | سلسلة نصية   | التعبير النمطي المستخدم لتصفية أسماء الملفات.      | [اختياري]  |
| **FullMatchConditions** | سلسلة نصية[] | قائمة بشروط أسماء الملفات الدقيقة للمطابقة.        | [اختياري]  |

### معلمة جسم الطلب

| اسم المعلمة | النوع | الوصف                                      |
|-------------|-------|---------------------------------------------|
| data        | ملف   | المحتوى الثنائي لملف كشف العمل المطلوب إنشاؤه. |

### **الاستجابة**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                         | متى يتم الإرجاع                             |
|-------|--------------------------------|---------------------------------------------|
| 200 OK | تم إنشاء ملف كشف العمل بنجاح  | التدفق الطبيعي                              |
| 201 Created | تم إنشاء ملف كشف العمل (استجابة بديلة) | عندما تُرجع الواجهة البرمجية حالة "تم الإنشاء" |
| 400 Bad Request | معلمات غير صالحة | خطأ من جانب العميل                          |
| 401 Unauthorized | رمز مفقود أو غير صالح | خطأ في المصادقة                             |
| 409 Conflict | الملف موجود وقيمة `isWriteOver=false` | تضارب مع ملف موجود                         |

## كيفية استخدام واجهة PostBatchConvert مع وحدات SDK

### مواصفات واجهة PostBatchConvert

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PostBatchConvert) واجهة برمجة تطبيقات متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/convert" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\",\"SaveOptions\":{\"SaveFormat\":\"pdf\",\"CalculateFormula\":true,\"EnableHTTPCompression\":true,\"OnePagePerSheet\":true,\"CreateDirectory\":false,\"Compliance\":\"None\"}}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام وحدات SDK الخاصة بـ Aspose.Cells Cloud

استخدام وحدة SDK هو أفضل طريقة لتسريع عملية التطوير. تتعامل وحدة SDK مع التفاصيل منخفضة المستوى وتسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بوحدات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء المكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام وحدات SDK متنوعة:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Batch-Convet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Batch-Convet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-Batch-Convet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Batch-Convet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Batch-Convet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Batch-Convet.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Batch-Convet.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d763dc80b0aff6275403dc1d82ad59a5" "Examples-Batch-Convet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---