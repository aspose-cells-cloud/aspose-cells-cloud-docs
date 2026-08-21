---
title: "تحويل ملف إكسل إلى تنسيق ماركداون"
second_title: "مستند"
linktype: "conversion"
type: docs
url: /ar/convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, conversion, Aspose.Cells Cloud, REST API, excel to markdown conversion, aspose cells markdown api, excel markdown export"
description: "تحويل أوراق عمل إكسل إلى تنسيق ماركداون باستخدام واجهة Aspose.Cells Cloud REST API – يتضمن مثالًا باستخدام cURL، وأمثلة لأكواد SDK، والمعلمات المطلوبة وتفاصيل المصادقة."
weight: 100
ArticleTitle: "تحويل ملف إكسل إلى ماركداون – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية لواجهة REST بتحويل ملف جدول بيانات إلى ملف بصيغة ماركداون.

## الأمان والمصادقة
تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## واجهة REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معاملات الاستعلام

| اسم المعامل             | النوع   | الموقع   | الوصف                                                                                                      |
| ----------------------- | ------- | -------- | ---------------------------------------------------------------------------------------------------------- |
| password                | string  | query    | كلمة المرور المطلوبة لفتح ملف إكسل.                                                                       |
| storageName             | string  | query    | اسم وحدة التخزين التي يقع عليها الملف.                                                                    |
| checkExcelRestriction   | bool    | query    | يُشير إلى ما إذا كان سيتم تطبيق القيود الخاصة بإكسل عند تعديل الخلايا أو الكائنات المرتبطة بها.         |
| datafile                | file    | body     | ملف إكسل المراد رفعه كجزء أول من المحتوى متعدد الأجزاء (multipart content).                                |

### الاستجابة

ترجع الواجهة البرمجية كائن JSON من النوع **FileInfo**:

- **FileInfo** – كائن يحتوي على اسم الملف وحجمه ومحتواه المشفر بصيغة base64 للملف المُولَّد بصيغة ماركداون.

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### استجابات الأخطاء

| رمز HTTP | الوصف                                                       | مثال محتوى JSON                                 |
| --------- | ------------------------------------------------------------ | ----------------------------------------------- |
| 401       | غير مُعتمد – رمز مفقود أو غير صالح.                         | `{"error":"Invalid access token."}`             |
| 400       | طلب غير صحيح – معلمات مطلوبة مفقودة أو تنسيق ملف غير صالح. | `{"error":"The 'datafile' field is required."}` |
| 500       | خطأ داخلي في الخادم – مشكلة غير متوقعة في الخادم.          | `{"error":"An unexpected error occurred."}`     |



## كيفية استخدام واجهة PostConvertWorkbookToMarkdown باستخدام SDKs

###仕様 واجهة PostConvertWorkbookToMarkdown

يُعرّف [仕اء OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) واجهة برمجة قابلة للوصول العام، ويسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء الواجهة البرمجية السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDKs هو أسرع طريقة للتطوير. فتتولى SDKs معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق أعمالك. يمكنك الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## واجهات برمجية أخرى تنفذ نفس الوظيفة

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – تحفظ ملف إكسل بصيغة HTML مع إعدادات إضافية وتخزن النتيجة.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – تحول ملف إكسل إلى HTML مع خيارات إضافية وترد بالنتيجة في الاستجابة.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – تسترد ملف إكسل ويمكن تحويله إلى HTML مع إعدادات اختيارية.
---