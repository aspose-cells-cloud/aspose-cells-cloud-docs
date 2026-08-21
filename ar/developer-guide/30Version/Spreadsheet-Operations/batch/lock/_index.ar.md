---
title: "قفل دفعات من ملفات إكسل"
second_title: "مستند"
type: docs
url: /batch/lock
keywords: "قفل دفعات، إكسل، Aspose.Cells، واجهة برمجة التطبيقات السحابية، جدول بيانات، حماية الملف"
description: "تتيح واجهة برمجة التطبيقات السحابية Aspose.Cells إمكانية قفل دفعات من ملفات إكسل متعددة. استخدم نقطة نهاية REST أو أيًا من حزم تطوير البرامج (SDKs) المدعومة (C#، Java، PHP، Ruby، Node.js، Python، Perl، Go، إلخ) لقفل الملفات دفعةً واحدةً."
weight: 100
---

تتيح واجهة برمجة التطبيقات هذه **قفل دفعات** من ملفات إكسل المؤهلة.

## واجهة برمجة التطبيقات REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/lock
```

### **الأمان والمصادقة**

واجهات برمجة التطبيقات السحابية الخاصة بـ Aspose.Cells آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الطلب

| اسم المعامل       | النوع               | الموقع | الوصف                                 |
|------------------|--------------------|----------|---------------------------------------------|
| BatchLockRequest | BatchLockRequest   | body     | جسم JSON يحتوي على معاملات القفل.      |

#### خصائص **BatchLockRequest**

| الاسم          | النوع                     | الوصف                                            | الملاحظات    |
|---------------|--------------------------|--------------------------------------------------------|----------|
| SourceFolder  | string                   | المجلد الذي يحتوي على ملفات إكسل المصدر.           | اختياري |
| MatchCondition| MatchConditionRequest    | الشروط المستخدمة لاختيار الملفات المراد قفلها.         | اختياري |
| Password      | string                   | كلمة المرور المطلوب تطبيقها على الملفات المُقفلة.                | اختياري |
| OutFolder     | string                   | المجلد الوجهة للملفات المُقفلة.              | اختياري |

#### خصائص **MatchConditionRequest**

| الاسم               | النوع      | الوصف                                          | الملاحظات    |
|--------------------|-----------|------------------------------------------------------|----------|
| RegexPattern       | string    | نمط تعبير عادي (regex) لمطابقة أسماء الملفات.      | اختياري |
| FullMatchConditions| string[]  | أسماء ملفات مطابقة تامة لعملية القفل.                 | اختياري |

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

| الرمز | المعنى                     | وقت العودة                           |
|------|-----------------------------|-----------------------------------------|
| 200 OK | تم إنشاء المصنف بنجاح | التدفق الطبيعي                              |
| 201 Created | تم إنشاء المصنف (استجابة بديلة) | عند عودة الواجهة بحالة "تم الإنشاء" |
| 400 Bad Request | معاملات غير صالحة | خطأ من جانب العميل                        |
| 401 Unauthorized | نقص أو وجود رمز غير صالح | خطأ في المصادقة                    |
| 409 Conflict | وجود الملف بالفعل و `isWriteOver=false` | تضارب مع ملف موجود    

## كيفية استخدام واجهة PostBatchLock API باستخدام حزم تطوير البرامج (SDKs)

### مواصفات واجهة PostBatchLock API

تعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchLock) واجهة برمجة تطبيقات قابلة للوصول علنًا وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/lock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}"
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

### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام حزمة تطوير البرامج (SDK) هو أسرع طريقة للتطوير. فتقوم الحزمة بإخفاء التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام القفل الخاصة بك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرامج الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchLock.go" >}}

{{< /tab >}}

{{< /tabs >}}
---