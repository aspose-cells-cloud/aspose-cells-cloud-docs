---
title: "تصدير الصورة"
second_title: "مستند"
linktitle: "صورة"
type: docs
url: /export-excel-picture-to-different-formats/
aliases: [/export/excel-picture-to-different-formats/]
keywords: "تصدير الصورة، Aspose.Cells Cloud، REST API، Excel، تنسيقات الصور، PNG، GIF، JPEG، BMP، SVG، TIFF، EMF، WMF"
description: "تصدير صور Excel إلى تنسيقات صور مختلفة باستخدام Aspose.Cells Cloud REST API. تدعم الخدمة مكتبات SDK بلغات برمجة متعددة، بما في ذلك C#، Java، PHP، Ruby، Node.js، Python، Perl، Go، و Swift."
weight: 20
---

يمكنك تصدير الصور إلى التنسيقات التالية: [PNG](https://docs.fileformat.com/Image/png/)، [GIF](https://docs.fileformat.com/image/gif/)، [JPEG](https://docs.fileformat.com/image/jpeg/)، [BMP](https://docs.fileformat.com/image/bmp/)، [SVG](https://docs.fileformat.com/page-description-language/svg/)، [TIFF](https://docs.fileformat.com/image/tiff/)، [EMF](https://docs.fileformat.com/image/emf/)، و [WMF](https://docs.fileformat.com/image/Wmf/).

## واجهة برمجة التطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الطلب

| المعامل        | الموقع      | النوع  | الإلزام | الوصف                                                                          |
| --------------- | --------- | ------ | -------- | ------------------------------------------------------------------------------ |
| `file`          | بيانات نموذج (Form‑data) | ملف   | نعم      | ملف جدول العمل Excel (`.xlsx`, `.xls`، إلخ) الذي يحتوي على كائنات OLE.       |
| `outputFormat`  | استعلام (Query) | نص (string) | نعم      | التنسيق المستهدف للكائنات المصدرَة (`pdf`, `png`, `jpeg`, `docx`, `pptx`).   |
| `objectType`    | استعلام (Query) | نص (string) | نعم      | القيمة الثابتة `oleobject`.                                                     |


### الاستجابة

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
      "FileSize": 21680,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
      "FileSize": 21286,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**رموز حالة HTTP**

| الرمز | الدلالة                     | الوصف                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | نجاح (OK)                          | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)                 | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصادَق (Unauthorized)                | رمز JWT غير صالح أو مفقود. |
| 413  | حمل البيانات كبير جدًا (Payload Too Large)           | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500  | خطأ داخلي في الخادم (Internal Server Error)       | خطأ غير متوقع في الخادم. |
## كيفية استخدام واجهة PostExport API مع مكتبات SDK

### مواصفات واجهة PostExport API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء استدعاء إلى واجهة Cloud API باستخدام cURL.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أكثر الطرق كفاءةً لتسريع عملية التطوير. فتتولى مكتبة SDK معالجة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells عبر الإنترنت باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}
{{< /tab >}}

{{< /tabs >}}

---