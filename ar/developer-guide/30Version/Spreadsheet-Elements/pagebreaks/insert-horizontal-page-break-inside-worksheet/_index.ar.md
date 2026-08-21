---
title: "إضافة فاصل صفحات أفقي"
second_title: "مستند"
linktype: "إضافة فاصل صفحات أفقي"
type: docs
url: /ar/page-breaks/add-horizontal-page-break/
aliases: [  /ar/insert-horizontal-page-break-inside-worksheet/ ]
keywords: "فاصل صفحات أفقي، Aspose.Cells Cloud، Excel API، REST، SDK، ورقة عمل، cURL"
description: "تعلم كيفية إضافة فاصل صفحات أفقي إلى ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن تفاصيل الطلب، مثالًا بـ cURL، وأجزاء من أكواد SDK لعدة لغات برمجة."
weight: 30
ArticleTitle: "إضافة فاصل صفحات أفقي – Aspose.Cells Cloud API"
---

تقوم واجهة **Add Horizontal Page Break** بإدخال فاصل صفحات أفقي داخل ورقة عمل Excel.

**المتطلبات المسبقة والمصادقة**  
يلزم وجود رمز مميز (JWT token) صالح لجميع الاستدعاءات إلى واجهة Aspose.Cells Cloud API. احصل على الرمز المميز عبر سير عمل OAuth 2.0 الموصوف في دليل المصادقة، وشُمُله في رأس الطلب كالتالي: `Authorization: Bearer <jwt token>`. يجب أن يكون الملف المُ workbooks الهدف مخزنًا في موقع متاح لواجهة API (التخزين الافتراضي أو `storageName` مخصص تحدده).

## PutHorizontalPageBreak API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks
```

### **الأمان والمصادقة**

تتطلب واجهات Aspose.Cells Cloud API <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز مميز JWT</a> لتكون آمنة.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
| ------------ | ------- | -------- | ------------------------------------------------------------------------- |
| name | string | path | اسم ملف Excel. |
| sheetName | string | path | اسم ورقة العمل التي سيتم إضافة الفاصل فيها. |
| cellname | string | query | مرجع الخلية (مثل **A1**) الذي يُشير إلى بداية الفاصل. |
| row | integer | query | فهرس الصف (بدءًا من الصفر) للفاصل. |
| column | integer | query | فهرس العمود (بدءًا من الصفر) للفاصل. |
| startColumn | integer | query | العمود الابتدائي لنطاق عند إدخال فاصل. |
| endColumn | integer | query | العمود النهائي لنطاق عند إدخال فاصل. |
| folder | string | query | مسار المجلد الذي يحتوي على ملف Excel. |
| storageName | string | query | اسم مساحة التخزين في Aspose Cloud. |

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/PageBreaks/PutHorizontalPageBreak" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة عامة قابلة للوصول تسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية استدعاء الواجهة باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
# استخدم HTTPS لضمان اتصال مشفر
curl -v "https://api.aspose.cloud/v3.0/cells/sampleExcelPageBreaks.xlsx/worksheets/Sheet1/horizontalpagebreaks?row=18" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

مثال على استجابة خطأ عند غياب أو فساد رمز JWT:

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "رمز JWT غير صالح أو مفقود."
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|------|-----------------------------|--------------------------------------------------|
| 200 | OK (نجاح) | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request (طلب غير صالح) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized (غير مصرّح) | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

لمزيد من التفاصيل حول العمليات ذات الصلة، راجع صفحات الواجهة الخاصة بـ **[Get Horizontal Page Breaks](../get-horizontal-page-breaks/)** و **[Delete Horizontal Page Break](../delete-horizontal-page-break/)**.

## عائلة SDK للسحابة

استخدام SDK هو أسرع طريقة للتطوير. تُجرّد SDK التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutHorizontalPageBreak.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutHorizontalPageBreak.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutHorizontalPageBreak.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutHorizontalPageBreak.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutHorizontalPageBreak.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutHorizontalPageBreak.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutHorizontalPageBreak.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutHorizontalPageBreak.go" >}}
{{< /tab >}}

{{< /tabs >}}