---
title: "حذف الخلفية من ملف Excel"
second_title: "مستند"
linktitle: "حذف"
type: docs
url: /delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "حذف الخلفية باستخدام Aspose Cells، واجهة برمجة تطبيقات Excel لحذف الخلفية، Aspose.Cells Cloud، DELETE /cells background"
description: "إزالة صورة الخلفية من ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. تعلّم نقطة النهاية DELETE والمعطيات المطلوبة ومثال على استخدام cURL ورمز SDK بلغات C# وJava وPython وغيرها."
weight: 170
ArticleTitle: "حذف صورة الخلفية من ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية لـ REST بحذف صورة الخلفية من ملف Excel.

## واجهة برمجة تطبيقات DeleteWorkbookBackground

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معطيات الاستعلام**

| اسم المعطى | النوع   | الوصف                                               | مطلوب |
|-----------|---------|-----------------------------------------------------|--------|
| folder    | string  | المجلد الذي يحتوي على الملف الأصلي (workbook).     | لا     |
| storageName | string | اسم خدمة التخزين التي سيتم استخدامها.              | لا     |

### **الاستجابة**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                     |
|-------|-----------------------------|------------------------------------------------------------|
| 200   | OK (تم بنجاح)              | تم تطبيق العملية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | Bad Request (طلب غير صحيح) | معطيات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).        |
| 401   | Unauthorized (غير مصرّح)   | رمز JWT غير صالح أو مفقود.                                |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح.                   |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                             |

## كيفية استخدام واجهة برمجة تطبيقات DeleteWorkbookBackground باستخدام مكتبات SDK

### **مواصفات واجهة برمجة تطبيقات DeleteWorkbookBackground**

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">مواصفة OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للوصول تتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي طلب DELETE كامل مع رأس المصادقة المطلوب؛ ولا يتطلب هذا الطلب أي جسم (body) في الاستدعاء.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
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

### **استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud**

يُعدّ استخدام مكتبة SDK أفضل طريقة لتسريع عملية التطوير؛ إذ تتعامل المكتبة مع التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}