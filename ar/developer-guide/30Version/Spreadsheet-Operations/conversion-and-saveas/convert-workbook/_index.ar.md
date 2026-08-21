---
title: "تحويل ملف إكسل إلى تنسيقات مختلفة"
second_title: "Document"
linktitle: "تحويل ملف جدول البيانات"
type: docs
url: /convert-a-spread-file-to-different-formats/
keywords: "تحويل إكسل، تحويل ملفات جداول البيانات، Aspose.Cells Cloud، واجهة برمجة التطبيقات REST، PDF، CSV، JSON، Markdown، تحويل تنسيقات الملفات"
description: "استخدم واجهة برمجة التطبيقات REST الخاصة بـ Aspose.Cells Cloud لتحويل كتب عمل إكسل إلى تنسيقات مختلفة مثل PDF و CSV و JSON و Markdown. تدعم الواجهة عدة حزم تطوير برمجيات (SDKs) لغات برمجة مثل C# و Java و Python وغيرها."
weight: 10
ArticleTitle: "تحويل ملف إكسل إلى تنسيقات مختلفة – دليل واجهة برمجة التطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بتحويل ملف إكسل إلى تنسيق مختلف. وتُدعم مجموعة واسعة من تنسيقات الإخراج، وتسمح لك بضبط إعدادات الصفحة وخيارات الحفظ قبل عملية التحويل.

## PostConvertWorkBook API

```http
POST https://api.aspose.cloud/v3.0/cells/convert
```

قبل استخدام هذه الواجهة، تأكد من امتلاك رمز JWT صالح، وتنصيب حزمة تطوير البرامج (SDK) المناسبة لـ Aspose.Cells Cloud بلغة البرمجة التي تستخدمها.

### **الأمان والمصادقة**

واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

## كيفية استخدام PostConvertWorkBook API مع حزم تطوير البرامج (SDKs)

### مواصفات PostConvertWorkBook API

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostConvertWorkBook">مواصفات OpenAPI</a> واجهة برمجة قابلة للوصول بشكل عام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "filename",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام حزمة تطوير البرامج (SDK) هو أسرع طريقة للتطوير. فتُجرّد SDK التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مشروعك. راجع <a href="https://github.com/aspose-cells-cloud">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الشيفرة التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام حزم تطوير برمجيات مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---