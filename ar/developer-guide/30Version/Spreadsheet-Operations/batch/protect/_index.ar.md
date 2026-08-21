---
title: "حماية دفعات من ملفات Excel"
second_title: "مستند"
type: docs
url: /batch/protect
keywords: "حماية دفعات من ملفات Excel، Aspose Cells Cloud، واجهة REST API، حماية ملفات Excel، الحماية الدفعية"
description: "تعرّف على كيفية استخدام واجهة Aspose.Cells Cloud REST API لحماية دفعات من ملفات Excel متعددة. يشمل التفاصيل الخاصة بالطلب، مثالًا باستخدام cURL، وأكواد نموذجية لواجهات برمجة التطبيقات (SDKs) بلغات برمجة مختلفة."
weight: 100
---

تتيح واجهة REST هذه **الحماية الدفعية** لملفات Excel المؤهلة.

## واجهة REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل            | النوع                | الموقع | الوصف                                                                                              |
|-----------------------|---------------------|----------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body     | حمولة JSON تحدّد مجلد المصدر، شروط المطابقة، نوع الحماية، كلمة المرور ومجلد الإخراج. |

### خصائص BatchProtectRequest

| الاسم            | النوع                     | الوصف                                                                                 | الملاحظات |
|-----------------|--------------------------|---------------------------------------------------------------------------------------------|-------|
| SourceFolder    | string                   | المجلد الذي يحتوي على ملفات Excel المصدر.                                                   | اختياري |
| MatchCondition  | MatchConditionRequest   | المعايير المستخدمة لتحديد الملفات المراد حمايتها.                                               | اختياري |
| ProtectionType  | string                   | نوع الحماية المراد تطبيقها (مثل `All` أو `ReadOnly`).                                      | اختياري |
| Password        | string                   | كلمة المرور التي سيتم تعيينها للملفات المحمية.                                                    | اختياري |
| OutFolder       | string                   | المجلد الوجهة للملفات المحمية.                                                 | اختياري |

### خصائص MatchConditionRequest

| الاسم                | النوع       | الوصف                                   | الملاحظات |
|---------------------|------------|-----------------------------------------------|-------|
| RegexPattern        | string     | التعبير النمطي المستخدم لمطابقة أسماء الملفات. | اختياري |
| FullMatchConditions | string[]   | قائمة بشروط أسماء الملفات الدقيقة.          | اختياري |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | المحتوى الثنائي لملف المصنّف المراد إنشاؤه. |

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

| الرمز | المعنى                     | وقت الإرجاع                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | تم إنشاء المصنّف بنجاح | التدفق الطبيعي                              |
| 201 Created | تم إنشاء المصنّف (استجابة بديلة) | عندما تُعيد واجهة API حالة الإنشاء |
| 400 Bad Request | معاملات غير صالحة | خطأ من جانب العميل                        |
| 401 Unauthorized | نقص أو عدم صلاحية الرمز | خطأ في المصادقة                    |
| 409 Conflict | الملف موجود و`isWriteOver=false` | تضارب مع ملف موجود    

## كيفية استخدام واجهة PostProtectConvert باستخدام واجهات برمجة التطبيقات (SDKs)

### مواصفات واجهة PostProtectConvert

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/PostProtectConvert) واجهة برمجة تطبيقات مفتوحة ومتاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة API السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
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

### استخدام واجهات برمجة التطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام واجهات برمجة التطبيقات (SDKs) هو أفضل طريقة لتسريع التطوير. فتتولى واجهة SDK إدارة التفاصيل من المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بواجهات برمجة التطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء استدعاءات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام واجهات برمجة التطبيقات (SDKs) المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}