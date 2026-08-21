---
title: "تحويل ملف Excel إلى CSV"
second_title: "مستند"
linktitle: "Excel إلى CSV"
type: docs
url: /ar/arconvert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel إلى CSV، Aspose.Cells Cloud، REST API، تحويل جداول البيانات، ملف CSV، تحويل الملفات"
description: "قم بتحويل جداول بيانات Excel إلى تنسيق CSV باستخدام واجهة Aspose.Cells Cloud REST API. تدعم مكتبات SDK متعددة ولغات برمجة مختلفة لتسهيل التكامل."
weight: 90
---

تقوم هذه الواجهة البرمجية لـ REST بتحويل ملف جدول البيانات إلى ملف بصيغة CSV.

## واجهة REST

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الاستعلام

| اسم المعامل              | النوع   | الوصف                                                                           |
| ----------------------- | ------ | ------------------------------------------------------------------------------------- |
| `password`              | نص (string) | كلمة المرور المطلوبة لفتح ملف Excel.                                         |
| `storageName`           | نص (string) | اسم وحدة التخزين التي يوجد فيها الملف.                                    |
| `checkExcelRestriction` | منطقي (bool) | ما إذا كان سيتم التحقق من قيود ملف Excel عند قيام المستخدم بتعديل الكائنات المرتبطة بالخلية. |

### معامل جسم الطلب

| اسم المعامل | النوع      | الوصف                                                             |
| -------------- | --------- | ----------------------------------------------------------------------- |
| `datafile`     | ملف بيانات | ملف البيانات المُضمَّن في الجزء الأول من جسم الطلب متعدد الأجزاء. |

### الاستجابة

تعيد الواجهة كائن **FileInfo** يحتوي على ملف CSV المُولَّد.

| الحقل           | النوع   | الوصف                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | نص (string) | اسم ملف CSV (مثل `example.csv`). |
| **FileSize**    | عدد صحيح (int) | حجم الملف بالبايت.                    |
| **FileContent** | نص (string) | محتوى ملف CSV المشفر بصيغة Base64.      |

[FileInfo](/cells/file-info/)


**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | ناجح (OK)                          | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مصرح به (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حجم حمل البيانات كبير جدًا (Payload Too Large) | يتجاوز حجم الملف المرفوع الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |
## كيفية استخدام واجزة PostConvertWorkbookToCSV مع مكتبات SDK

### مواصفات واجزة PostConvertWorkbookToCSV

تعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبات SDK هو أسرع طريقة لتطوير التطبيقات. فتتولى مكتبات SDK التعامل مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مشروعك. راجع [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر واجهة REST باستخدام مكتبات SDK متنوعة:

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