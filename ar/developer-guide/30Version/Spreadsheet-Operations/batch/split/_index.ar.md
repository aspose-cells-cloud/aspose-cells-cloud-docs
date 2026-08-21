---
title: "التفريق بالدفعة"
second_title: "مستند"
type: docs
url: /ar/batch/split
keywords: "التفريق بالدفعة، Aspose.Cells Cloud، REST API، Excel، PDF، CSV، JSON، Spreadsheet، Cloud SDK"
description: "توثيق لواجهة برمجة تطبيقات التفريق بالدفعة في Aspose.Cells Cloud، والتي تقوم بتفريق ملفات الجداول الإلكترونية إلى تنسيقات متعددة مثل PDF وCSV أو JSON. ويشمل تفاصيل الطلب وأوامر cURL المثالية واستخدام SDK عبر لغات برمجة متنوعة."
weight: 100
---

تقوم هذه واجهة برمجة تطبيقات REST بتنفيذ **تفريق بالدفعة** للملفات المؤهلة.

## واجهة برمجة تطبيقات REST

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/split
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة      | النوع               | المسار/الاستعلام/النص/جسم HTTP | الوصف                                        |
|------------------|--------------------|----------------------------|-----------------------------------------------|
| BatchSplitRequest| BatchSplitRequest  | body                       | حمل الطلب الذي يحتوي على خيارات التفريق.     |

### **خصائص BatchSplitRequest**

| الاسم           | النوع                | الوصف                                      | الملاحظات      |
|----------------|---------------------|---------------------------------------------|------------|
| SourceFolder   | string              | المجلد الذي يحتوي على الملف المصدر.         | [اختياري]   |
| SourceStorage  | string              | اسم التخزين الذي يوجد فيه الملف المصدر.      | [اختياري]   |
| MatchCondition | MatchConditionRequest| الشروط المستخدمة لاختيار الملفات للتفريق.   | [اختياري]   |
| Format         | string              | التنسيق المطلوب للإخراج (مثل: pdf، csv).    | [اختياري]   |
| FromIndex      | integer             | الفهرس الابتدائي للصفحات المراد تفريزها.     | [اختياري]   |
| ToIndex        | integer             | الفهرس النهائي للصفحات المراد تفريزها.       | [اختياري]   |
| OutFolder      | string              | المجلد الوجهة لملفات التفريق.               | [اختياري]   |
| SaveOptions    | SaveOptions         | خيارات إضافية لحفظ الإخراج.                 | [اختياري]   |

### **خصائص MatchConditionRequest**

| الاسم                 | النوع       | الوصف                                      | الملاحظات      |
|----------------------|-------------|---------------------------------------------|------------|
| RegexPattern         | string      | التعبير المنتظم لمطابقة أسماء الملفات.      | [اختياري]   |
| FullMatchConditions  | string[]    | قائمة بشروط المطابقة الدقيقة.              | [اختياري]   |

### معلمة جسم الطلب

| اسم المعلمة | النوع | الوصف                                      |
| ------------ | ---- | ------------------------------------------- |
| data         | file | المحتوى الثنائي لملف كشف الحساب المراد إنشاؤه. |

  
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

**كودات حالة HTTP**

| الكود | المعنى                      | وقت العودة                              |
|------|-----------------------------|-----------------------------------------|
| 200 OK | تم إنشاء ملف كشف الحساب بنجاح         | في التدفق الطبيعي                             |
| 201 Created | تم إنشاء ملف كشف الحساب (استجابة بديلة) | عند عودة الواجهة بحالة تم الإنشاء |
| 400 Bad Request | معلمات غير صالحة | خطأ من جانب العميل                        |
| 401 Unauthorized | نقص أو عدم صلاحية الرمز | خطأ في المصادقة                    |
| 409 Conflict | يوجد الملف وقيمة `isWriteOver=false` | تعارض مع الملف الموجود            |


## كيفية استخدام واجهة PostBatchSplit API باستخدام SDKs

### مواصفات واجهة PostBatchSplit API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}"
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

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير. وتتولى SDK معالجة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام التفريق الخاصة بك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}