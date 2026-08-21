---
title: "تحويل ملف Excel إلى PDF – واجهة برمجة تطبيقات Aspose.Cells Cloud"
ArticleTitle: "تحويل ملف Excel إلى PDF – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "المستند"
linktitle: "تحويل ملف Excel إلى PDF"
type: docs
url: /convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, تحويل, واجهة برمجة تطبيقات السحابة"
description: "تعرّف على كيفية تحويل كتب عمل Excel إلى تنسيق PDF باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يشمل أمثلة cURL وحزم تطوير برمجيات (SDK) (C#, Java, Python) ودليل المصادقة."
weight: 80
---

تقوم هذه واجهة برمجة تطبيقات REST بتحويل ملف جدول بيانات إلى ملف بصيغة PDF. **المتطلبات المسبقة:** احصل على رمز وصول JWT صالح، وتأكد من أن ملف Excel المصدر مخزن في مساحة تخزين مدعومة، وامتلك الصلاحيات المناسبة لاستدعاء نقطة نهاية التحويل.

## واجهة برمجة تطبيقات PostConvertWorkbookToPDF

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معامل الاستعلام**

| اسم المعامل          | النوع  | الوصف                                                                           |
| :-------------------- | :----- | :------------------------------------------------------------------------------ |
| password              | string | كلمة المرور لفتح ملف Excel.                                                     |
| storageName           | string | اسم مساحة التخزين التي يُخزّن فيها الملف.                                        |
| checkExcelRestriction | bool   | ما إذا كان سيتم تطبيق قيود ملف Excel عند تعديل الكائنات المرتبطة بالخلايا.      |

يُفترض أن تكون قيمة `checkExcelRestriction` تساوي `false` في حال حُذف هذا المعامل.

### **معامل جسم الطلب**

| اسم المعامل | النوع | الوصف                                                        |
| :---------- | :---- | :----------------------------------------------------------- |
| datafile    | file  | ملف البيانات المُحفوظ كالجزء الأول لمحتوى متعدد الأجزاء.     |

### **الاستجابة**

[FileInfo](/cells/file-info/)

ترجع الاستجابة كائن JSON يحتوي على بيانات تعريف الملف. يمكن تنزيل ملف PDF نفسه باستخدام `FileContent` (المُشفّر بترميز base64) أو عبر الرابط الموجود في `FileInfo`. تُرجع واجهة برمجة التطبيقات كائن JSON من النوع **FileInfo**:

- **FileInfo** – كائن يحتوي على اسم وحجم ومحتوى مشفّر بترميز base64 لملف **PDF** المُولّد.

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                              |
|------|-----------------------------|----------------------------------------------------|
| 200  | ناجح (OK)                   | تمت عملية التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مخوّل (Unauthorized)    | رمز JWT غير صالح أو مفقود.                         |
| 413  | حملة الطلب كبيرة جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.           |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                            |

## كيفية استخدام واجهة برمجة تطبيقات PostConvertWorkbookToPDF باستخدام حزم تطوير البرمجيات (SDKs)

### مواصفات واجهة برمجة تطبيقات PostConvertWorkbookToPDF

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

**رؤوس الطلب**

| الرأس          | النوع  | الوصف                                                    |
| :------------- | :----- | :-------------------------------------------------------- |
| Authorization  | string | رمزBearer تم الحصول عليه عبر المصادقة باستخدام JWT.      |
| Content-Type   | string | يجب أن تكون قيمته `multipart/form-data` لرفع الملفات.    |
| Accept         | string | `application/json` لتلقي بيانات تعريف الاستجابة.         |

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. ضع رمز الوصول في رأس `Authorization`، ثم نفّذ الطلب التالي:

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}


### استخدام حزم تطوير البرمجيات (SDKs) الخاصة بـ Aspose.Cells Cloud


قد يبسّط استخدام SDK تطوير البرمجيات من خلال التعامل مع التفاصيل منخفضة المستوى. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات (SDKs) الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات Aspose.Cells عبر SDKs متنوعة:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## واجهات برمجة تطبيقات أخرى تنفّذ هذه الوظيفة

| **واجهة برمجة التطبيقات** | **النوع** | **الوصف**                                                     | **رابط Swagger**                                                                          |
| :----------------------- | :-------- | :------------------------------------------------------------- | :---------------------------------------------------------------------------------------- |
| /cells/convert            | PUT       | تحويل كتاب عمل من محتوى الطلب إلى تنسيق محدّد.                | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

واجهة برمجة تطبيقات [POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) تتيح لك حفظ ملف Microsoft Excel بصيغة PDF مع إمكانية ضبط إعدادات إضافية وتخزين النتيجة في مساحة التخزين.

تقوم هذه واجهة برمجة تطبيقات REST بتحويل ملف Excel إلى PDF.

واجهة برمجة تطبيقات [PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) تتيح لك تحويل ملف Microsoft Excel إلى PDF مع إمكانية ضبط إعدادات إضافية وإعادة النتيجة في الاستجابة.

واجهة برمجة تطبيقات [GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) تتيح لك تحويل ملف Microsoft Excel إلى PDF مع إمكانية ضبط إعدادات إضافية وإعادة النتيجة في الاستجابة.

تُعرّف واجهات برمجة التطبيقات [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)، و[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)، و[PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

للحصول على خيارات تحويل إضافية، راجع صفحة [خيارات الحفظ](/cells/save-options/).