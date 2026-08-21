---
title: "فتح دفعّة"
second_title: "مستند"
type: docs
url: /ar/batch/unlock
keywords: "فتح دفعّة، Aspose.Cells Cloud، Excel، REST API، جدول بيانات، SDK سحابي"
description: "افتح ملفات Excel متعددة دفعة واحدة باستخدام REST API الخاص بـ Aspose.Cells Cloud. يدعم SDKs لغات C#، Java، Python، وأخرى."
weight: 100
---

تقوم هذه الواجهة البرمجية لواجهة REST بفتح ملفات Excel المؤهلة دفعة واحدة.

## واجهة REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|----------------|------|----------|-------------|
| **BatchLockRequest** |  | body | جسم الطلب الذي يحتوي على إعدادات الفتح. |

### خصائص **BatchLockRequest**

| الاسم          | النوع                     | الوصف                                 | الملاحظات |
|---------------|--------------------------|---------------------------------------------|-------|
| SourceFolder  | string                   | المجلد الذي يحتوي على ملفات Excel المصدر. | [اختياري] |
| MatchCondition| MatchConditionRequest    | المعايير المستخدمة لتحديد الملفات المراد فتحها. | [اختياري] |
| Password      | string                   | كلمة المرور المطبّقة على المصنفات المحمية. | [اختياري] |
| OutFolder     | string                   | المجلد الوجهة للملفات المُفتَحة. | [اختياري] |

### خصائص **MatchConditionRequest**

| الاسم               | النوع      | الوصف                                 | الملاحظات |
|--------------------|-----------|---------------------------------------------|-------|
| RegexPattern       | string    | التعبير النمطي لتطابق أسماء الملفات.    | [اختياري] |
| FullMatchConditions| string[]  | شروط أسماء الملفات الدقيقة المطلوب تطابقها. | [اختياري] |

### معامل جسم الطلب

| اسم المعامل | النوع | الوصف                                    |
| -------------- | ---- | ---------------------------------------------- |
| data           | file | المحتوى الثنائي لملف المصنف المراد إنشاؤه. |
  
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
| 200 OK | تم إنشاء المصنف بنجاح | في السير الاعتيادي |
| 201 Created | تم إنشاء المصنف (استجابة بديلة) | عندما تُعيد الواجهة البرمجية حالة الإنشاء |
| 400 Bad Request | معاملات غير صالحة | خطأ من جانب العميل |
| 401 Unauthorized | رمز مفقود أو غير صالح | خطأ في المصادقة |
| 409 Conflict | الملف موجود و`isWriteOver=false` | تضارب مع ملف موجود |

## كيفية استخدام واجزة PostBatchLock API باستخدام SDKs

### مواصفات واجهة PostBatchLock API


تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) واجهة برمجة تطبيقات متاحة للعامة، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة cURL سطر الأوامر للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء استدعاءات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"SourceFolder":"CellsTests","OutFolder":"Output","MatchCondition":{"RegexPattern":"(^Book)(.+)(xlsx$)"},"Password":"123456"}'
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

### استخدام Aspose.Cells Cloud SDKs

استخدام SDK هو أسرع طريقة لتطوير وظيفة الفتح. فهي تُجرّدك من التفاصيل منخفضة المستوى لتتمكن من التركيز على منطق أعمالك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}