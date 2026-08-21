---
title: "Excel إلى PNG"
second_title: "مستند"
linktitle: "Excel إلى PNG"
type: docs
url: convert-excel-file-to-png-file/
keywords: "Excel إلى PNG، Aspose.Cells Cloud، REST API، تحويل جداول البيانات، تنسيق PNG"
description: "حوّل جداول بيانات Excel إلى صور PNG باستخدام واجهة Aspose.Cells Cloud REST API. تدعم واجهة برمجة التطبيقات هذه العديد من حزم تطوير البرمجيات (SDKs)، وتوفّر أمثلة مفصّلة بلغات برمجة مختلفة."
weight: 90
---

تقوم هذه الواجهة البرمجية (REST API) بتحويل ملف جدول بيانات إلى تنسيق PNG.

## مواصفات واجهة برمجة التطبيقات (REST API)

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معامل الاستعلام (Query Parameter)**

| اسم المعامل           | النوع  | الوصف                                                                                     |
| --------------------- | ------ | ----------------------------------------------------------------------------------------- |
| password              | string | كلمة المرور المطلوبة لفتح ملف Excel.                                                     |
| storageName           | string | اسم وحدة التخزين التي يقع فيها الملف.                                                     |
| checkExcelRestriction | bool   | يحدّد ما إذا كان سيتم التحقق من قيود ملف Excel عند تعديل الخلايا أو الكائنات ذات الصلة. |

### **معامل جسم الطلب (Request Body Parameter)**

| اسم المعامل | النوع       | الوصف                                                      |
| ------------ | ----------- | ---------------------------------------------------------- |
| datafile     | data file   | ملف جدول البيانات المُضمَّن في الجزء الأول من الطلب المتعدد الأجزاء (multipart request). |

### **الاستجابة**

تُعيد الواجهة البرمجية كائن **FileInfo** يحتوي على ملف PNG المُولّد.

| الحقل            | النوع  | الوصف                                        |
| ----------------- | ------ | -------------------------------------------- |
| **Filename**      | string | اسم ملف PNG (مثل `example.png`).            |
| **FileSize**      | int    | حجم الملف بالبايت.                           |
| **FileContent**   | string | محتوى ملف PNG المُشفّر بتشفير Base64.        |

[FileInfo](/cells/file-info/)

**رموز حالات HTTP (HTTP Status Codes)**

| الرمز | الدلالة                    | الوصف                                                         |
|------|----------------------------|---------------------------------------------------------------|
| 200  | ناجح (OK)                  | تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.   |
| 400  | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).        |
| 401  | غير مُصرّح (Unauthorized)  | رمز JWT غير صالح أو مفقود.                                   |
| 413  | حجم الحمولة كبير جدًّا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.                 |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقّع في الخادم.                                  |

## كيفية استخدام PostConvertWorkbookToPNG API باستخدام حزم تطوير البرمجيات (SDKs)

### مواصفات PostConvertWorkbookToPNG API

يُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) واجهة برمجة تطبيقات عامة يمكن الوصول إليها، ويتيح لك إجراء تفاعلات REST مباشرةً من متصفّح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إرسال طلبات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام حزم تطوير البرمجيات (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام حزمة تطوير البرمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير. وتتولّى حزمة تطوير البرمجيات إدارة التفاصيل من المستوى المنخفض، بحيث تتمكن من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام حزم تطوير البرمجيات المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## واجهات برمجة تطبيقات أخرى تُ实施 نفس الوظائف

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – تحفظ ملف Excel كملف CSV (أو صيغ أخرى) مع إعدادات إضافية وتخزّن النتيجة.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – تحول ملف Excel إلى CSV (أو صيغ أخرى) باستخدام معاملات اختيارية وترجع النتيجة في الاستجابة.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – تسترجع ملف Excel وتحوله إلى CSV (أو صيغ أخرى) أثناء التنقّل (on the fly).