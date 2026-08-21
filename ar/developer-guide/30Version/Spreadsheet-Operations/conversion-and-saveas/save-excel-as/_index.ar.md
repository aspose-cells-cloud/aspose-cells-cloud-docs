---
title: "حفظ ملف مصنف Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "حفظ كـ"
type: docs
url: /ar/save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, حفظ كـ, PDF, CSV, JSON, Markdown, واجهة برمجة تطبيقات REST"
description: "احفظ ملفات مصنفات Excel بصيغ PDF وCSV وJSON وMarkdown وصيغ أخرى باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST."
weight: 30
---

تتيح لك هذه واجهة برمجة التطبيقات **حفظ** ملف Excel بصيغ مختلفة.  
قبل استدعاء هذه النقطة النهائية (endpoint)، تأكد من امتلاك رمز وصول OAuth 2.0 صالح، وأن ملف المصنف المصدر محفوظ في مساحة التخزين الخاصة بك في Aspose Cloud.

**المتطلبات الأساسية**  
1. احصل على رمز وصول JWT وضمنه في رأس الطلب `Authorization: Bearer <token>` لكل طلب.  
2. ارفع ملف المصنف المصدر إلى مساحة التخزين في Aspose Cloud (أو تأكد من وجوده مسبقًا).  
3. اعرف اسم مساحة التخزين ومسار المجلد الذي يحتوي على ملف المصنف.

## واجهة PostWorkbookSaveAs API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud مصادقة قائمة على <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">رمز JWT</a>، وهي آمنة.

### **معامل المسار (Path Parameter)**

| اسم المعامل | النوع   | الوصف                                 |
| -------------- | ------ | --------------------------------------- |
| name           | string | اسم ملف Excel.                         |

### **معامل الاستعلام (Query Parameter)**

| اسم المعامل           | النوع   | الوصف                                                                                      |
| --------------------- | ------ | ------------------------------------------------------------------------------------------ |
| newfilename           | string | اسم الملف الجديد للمستند المحفوظ.                                                          |
| isAutoFitRows         | string | إذا كان `true`، تُضبط ارتفاعات الصفوف تلقائيًا في المصنف. القيمة الافتراضية هي `false`.     |
| isAutoFitColumns      | string | إذا كان `true`، تُضبط عرض الأعمدة تلقائيًا في المصنف. القيمة الافتراضية هي `false`.        |
| folder                | string | المجلد الذي يحتوي على المصنف الأصلي.                                                      |
| storageName           | string | اسم مساحة التخزين التي يوجد فيها ملف المصدر.                                               |
| outStorageName        | string | اسم مساحة التخزين التي سيتم حفظ ملف الإخراج فيها.                                          |
| checkExcelRestriction | bool   | يحدد ما إذا كان يجب تطبيق قيود Excel عند تعديل الخلايا أو الكائنات ذات الصلة.             |
| region                | string | الإعدادات الإقليمية المطبقة على المصنف.                                                    |
| pageWideFitOnPerSheet | bool   | ضبط عرض الصفحة لتناسب كل ورقة عمل عند التحويل.                                             |
| pageTallFitOnPerSheet | bool   | ضبط ارتفاع الصفحة ليناسب كل ورقة عمل عند التحويل.                                           |
| sheetName             | string | اسم ورقة العمل المراد تحويلها.                                                             |
| pageIndex             | string | فهرس الصفحة المراد تحويلها ضمن ورقة العمل المحددة (يتطلب `sheetName`).                    |
| onePagePerSheet       | bool   | عند التحويل إلى PDF، أنشئ صفحة واحدة لكل ورقة عمل.                                         |

### **معامل جسم الطلب (Request Body Parameter)**

| اسم المعامل | النوع   | الوصف                                                         |
| -------------- | ------ | --------------------------------------------------------------- |
| SaveOptions    | Object | خيارات الحفظ المقدمة في الجزء الثاني من الطلب متعدد الأجزاء. |

**مثال على جسم الطلب (الجزء JSON من الطلب متعدد الأجزاء)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### الاستجابة

تعيد واجهة برمجة التطبيقات كائن `SaveResponse`.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**رموز حالة HTTP**

| الرمز | المعنى                        | الوصف                                                             |
|------|-------------------------------|-------------------------------------------------------------------|
| 200  | OK (نجاح)                     | تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.           |
| 400  | Bad Request (طلب غير صالح)   | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).             |
| 401  | Unauthorized (غير مصدق)       | رمز JWT غير صالح أو مفقود.                                        |
| 413  | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به.                         |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                        |

## كيفية استخدام واجهة PostWorkbookSaveAs API مع مكتبات SDK

### مواصفات واجهة PostWorkbookSaveAs API

تُعرّف <a href="https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للوصول، وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات Aspose.Cells Cloud SDK

استخدام مكتبة SDK هو أفضل طريقة لتسريع عملية التطوير، حيث تتعامل المكتبة مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

للحصول على سيناريوهات تحويل أخرى، راجع الدليلين: [تحويل ملف Excel إلى PDF](/convert-excel-to-pdf/) و [تصدير ملف Excel إلى CSV](/export-excel-to-csv/).