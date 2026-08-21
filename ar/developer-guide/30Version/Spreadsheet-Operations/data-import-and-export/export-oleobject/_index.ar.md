---
title: "تصدير كائن OLE – واجهة برمجة تطبيقات Aspose.Cells السحابية"
second_title: "الوثيقة"
linktitle: "كائن OLE"
type: docs
url: /ar/export-excel-ole-object/
aliases: [  /ar/export/excel-ole-object/ ]
keywords: "Aspose.Cells, كائن OLE, تصدير, Excel, واجهة برمجة تطبيقات سحابية, PDF, PNG, DOCX, PPTX"
description: "تصدير كائنات OLE من ملف Excel باستخدام واجهة برمجة تطبيقات Aspose.Cells السحابية. تعلّم تنسيق الطلب والمعلمات وعينة cURL ومعالجة الأخطاء."
weight: 20
ArticleTitle: "تصدير كائن OLE – واجهة برمجة تطبيقات Aspose.Cells السحابية"
---

## **واجهة برمجة تطبيقات REST**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells السحابية آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معلمات الطلب

| المعلمة          | الموقع        | النوع  | مطلوبة | الوصف                                                                      |
| ---------------- | ------------- | ------ | ------ | --------------------------------------------------------------------------- |
| `file`           | بيانات النموذج (Form‑data) | ملف   | نعم    | ملف Excel (`.xlsx`, `.xls`, إلخ) الذي يحتوي على كائنات OLE.                |
| `outputFormat`   | استعلام (Query) | نص (string) | نعم    | التنسيق المستهدف للكائنات المصدرَة (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`     | استعلام (Query) | نص (string) | نعم    | القيمة الثابتة `oleobject`.                                                 |


### الاستجابة

يُعيد الطلب الناجح كائن JSON يسرد الملفات المصدرَة:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**رموز حالة HTTP**

| الرمز | المعنى                        | الوصف                                                                 |
|------|-------------------------------|------------------------------------------------------------------------|
| 200  | ناجح (OK)                     | تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.             |
| 400  | طلب غير صالح (Bad Request)   | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).                  |
| 401  | غير مُصادَق (Unauthorized)    | رمز JWT غير صالح أو مفقود.                                            |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.                             |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                              |
## كيفية استخدام واجهة PostExport API مع حزم تطوير البرامج (SDKs)

### مواصفات واجهة PostExport API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) واجهة برمجة تطبيقات قابلة للوصول العام، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### ما هو كائن OLE؟

كائن **OLE (Object Linking and Embedding)** يُضمّن محتوى خارجيًا — مثل مستندات Word أو شرائح PowerPoint أو الصور أو ملفات أخرى — داخل ملف Excel. عند التصدير، يتم استخراج المحتوى المُضمّن وحفظه بالتنسيق المطلوب.

### نظرة عامة على نقطة النهاية (Endpoint)

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – يجب أن تُعيَّن على `oleobject`.
- `format` – التنسيق المستهدف للإخراج (مثل `pdf`, `png`, `jpeg`, `docx`, `pptx`).

### استخدام حزم تطوير البرامج (SDKs) الخاصة بـ Aspose.Cells Cloud

استخدام حزمة تطوير البرامج (SDK) هو أفضل طريقة لتسريع التطوير، حيث تتعامل SDK مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرامج الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مختلف حزم تطوير البرامج:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---