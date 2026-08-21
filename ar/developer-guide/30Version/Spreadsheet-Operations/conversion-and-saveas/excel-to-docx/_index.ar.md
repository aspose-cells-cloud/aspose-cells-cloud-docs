---
title: "تحويل ملف Excel إلى DOCX"
second_title: "وثيقة"
linktype: "convert-excel-file-to-docx-file/"
type: docs
url: /arconvert-excel-file-to-docx-file/
keywords: "تحويل Excel إلى DOCX، Aspose.Cells Cloud، REST API، تحويل جداول البيانات، إنشاء المستندات"
description: "حوّل جداول بيانات Excel إلى مستندات DOCX باستخدام REST API الخاص بـ Aspose.Cells Cloud. يدعم عدة SDKs ولغات برمجة لتكامل سلس."
weight: 90
---

يقوم هذا الـ REST API بتحويل ملف جدول بيانات إلى تنسيق ملف DOCX.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


**مُعاملات الاستعلام**

| اسم المُعامل           | النوع   | الوصف                                                                                             |
| --------------------- | ------ | -------------------------------------------------------------------------------------------------- |
| password              | string | كلمة المرور المطلوبة لفتح ملف Excel.                                                               |
| storageName           | string | اسم وحدة التخزين التي يوجد فيها الملف.                                                               |
| checkExcelRestriction | bool   | يشير إلى ما إذا كان سيتم التحقق من قيود ملف Excel عند قيام المستخدم بتعديل الكائنات المرتبطة بالخلية. |

**مُعامل جسم الطلب**

| اسم المُعامل | النوع      | الوصف                                                       |
| ------------ | --------- | ------------------------------------------------------------- |
| datafile     | data file | ملف البيانات المحفوظ في الجزء الأول من جسم الطلب متعدد الأجزاء. |

**الاستجابة**

تعيد الواجهة كائن **FileInfo** يحتوي على ملف Word المُولّد.

| الحقل           | النوع   | الوصف                                      |
| --------------- | ------ | ------------------------------------------- |
| **Filename**    | string | اسم ملف Word (مثل `example.docx`).         |
| **FileSize**    | int    | حجم الملف بالبايت.                          |
| **FileContent** | string | محتوى ملف Word المشفر بترميز Base64.        |


[FileInfo](/cells/file-info/)

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                  |
|------|-----------------------------|--------------------------------------------------------|
| 200  | ناجح (OK)                   | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | مُعاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).     |
| 401  | غير مُصادَق (Unauthorized)  | رمز JWT غير صالح أو مفقود.                              |
| 413  | حملة البيانات كبيرة جدًا (Payload Too Large) | تجاوز ملف المرفقات الحد الأقصى للحجم.                     |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                |

## كيفية استخدام واجهة PostConvertWorkbookToDocx API باستخدام SDKs

### مواصفات واجهة PostConvertWorkbookToDocx API

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.docx",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فتتولّى SDK إدارة التفاصيل من المستوى المنخفض، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## واجهات برمجة تطبيقات أخرى تُنفّذ هذه الوظيفة

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – تحفظ ملف Excel كملف DOCX مع إعدادات إضافية وتخزن النتيجة في وحدة التخزين المحددة.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – تحول ملف Excel إلى ملف DOCX مع إعدادات اختيارية وترد بالنتيجة في الاستجابة.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – تسترجع مصنف Excel وتحوله إلى ملف DOCX مع مُعاملات اختيارية.

---