---
title: "تحويل ملف Excel إلى PPTX باستخدام واجهة Aspose.Cells Cloud API الإصدار 3.0"
second_title: "مستند"
linktitle: "Excel إلى PPTX"
type: docs
url: /convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, تحويل, REST API, سحابة"
description: "تعرّف على كيفية تحويل كتب عمل Excel إلى عروض تقديمية بصيغة PPTX باستخدام واجهة Aspose.Cells Cloud REST API الإصدار 3.0. يتضمن طلب cURL، وأمثلة على كود SDK، والمصادقة، ومعالجة الأخطاء."
weight: 90
ArticleTitle: "تحويل ملف Excel إلى PPTX باستخدام واجهة Aspose.Cells Cloud API الإصدار 3.0"
---

تقوم هذه الواجهة البرمجية REST بتحويل ملف جدول بيانات إلى تنسيق PPTX.

## واجهة PostConvertWorkbookToPptx

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الاستعلام

| اسم المعامل              | النوع   | الوصف                                                                                       |
| ----------------------- | ------ | ----------------------------------------------------------------------------------------- |
| `password`              | string | كلمة المرور المطلوبة لفتح كتاب عمل Excel.                                             |
| `storageName`           | string | اسم وحدة التخزين التي يقع فيها الملف المصدر.                                     |
| `checkExcelRestriction` | bool   | يُشير إلى ما إذا كان سيتم تطبيق قيود ملف Excel عند تعديل الكائنات المرتبطة بالخلية. |

### معامل نص الطلب

| اسم المعامل | النوع      | الوصف                                                              |
| -------------- | --------- | ------------------------------------------------------------------------ |
| `datafile`     | ملف بيانات | ملف Excel المُضمَّن في الجزء الأول من نص الطلب متعدد الأجزاء. |

**مثال على نص طلب متعدد الأجزاء (مبسَّط):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<المحتوى الثنائي لملف input.xlsx>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### الاستجابة

ترجع الواجهة البرمجية كائن **FileInfo** يحتوي على ملف pptx المُولَّد.

| الحقل           | النوع   | الوصف                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | اسم ملف pptx (مثل `example.pptx`). |
| **FileSize**    | int    | حجم الملف بالبايت.                    |
| **FileContent** | string | محتوى ملف pptx مشفرًا بترميز Base64.      |

[FileInfo](/cells/file-info/)


**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                          | تم تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصادق عليه (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حمل البيانات كبير جدًا (Payload Too Large)           | حجم الملف المرفَق يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقَّع في الخادم. |

*ملاحظات:* تدعم نقطة النهاية التنسيقات الشائعة لملفات Excel (`.xlsx`، `.xls`، `.xlsm`). يقتصر الحد الأقصى لحجم الملف على 50 ميغابايت. قد تُقيَّد عملية التحويل لكتب العمل التي تحتوي على ماكرو أو أوراق محمية ما لم تُزوَّد المعاملات المناسبة.

## كيفية استخدام واجهة PostConvertWorkbookToPptx باستخدام مكتبات SDK

### مواصفات واجهة PostConvertWorkbookToPptx

تُعرِّف <a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات متاحة علنًا وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة لتطوير التطبيقات. فتُجرِّدك المكتبة من تفاصيل البرمجة منخفضة المستوى لتتمكن من التركيز على مشروعك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud" rel="noopener noreferrer") للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## واجهات برمجة تطبيقات أخرى تنفّذ هذه الوظيفة

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – تحويل ملف Excel إلى PDF.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – تحويل ملف Excel إلى صور PNG.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – تحويل ملف Excel إلى تنسيق SVG.