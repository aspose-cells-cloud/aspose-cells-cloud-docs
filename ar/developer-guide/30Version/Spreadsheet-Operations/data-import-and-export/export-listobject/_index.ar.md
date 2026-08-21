---
title: "تصدير كائن القائمة"
second_title: "مستند"
linktitle: "كائن القائمة"
type: docs
url: /export-excel-listobject-to-different-formats/
aliases: [/export/excel-listobject-to-different-formats/]
keywords: "تصدير ListObject، كائن القائمة في Excel، Aspose.Cells Cloud، واجهة برمجة تطبيقات REST، PDF، CSV، JSON، XLSX، ODS، PNG، TIFF، مكتبات SDK"
description: "تتيح واجهة Aspose.Cells Cloud REST تصدير كائنات القائمة (ListObjects) في ملفات Excel إلى مجموعة واسعة من تنسيقات الملفات. تتوفر مكتبات SDK للعديد من لغات البرمجة، بما في ذلك C# وJava وPython وNode.js وGo وPHP وRuby وPerl وSwift."
weight: 20
---

يمكنك تصدير التنسيقات التالية: [XLS](https://docs.fileformat.com/spreadsheet/xls/)، [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)، [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)، [CSV](https://docs.fileformat.com/spreadsheet/csv/)، [TSV](https://docs.fileformat.com/spreadsheet/tsv/)، [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)، [ODS](https://docs.fileformat.com/spreadsheet/ods/)، [TXT](https://docs.fileformat.com/word-processing/txt/)، [PDF](https://docs.fileformat.com/pdf/)، [OTS](https://docs.fileformat.com/spreadsheet/ots/)، [XPS](https://docs.fileformat.com/page-description-language/xps/)، [DIF](https://docs.fileformat.com/spreadsheet/dif/)، [PNG](https://docs.fileformat.com/Image/png/)، [JPEG](https://docs.fileformat.com/image/jpeg/)، [BMP](https://docs.fileformat.com/image/bmp/)، [SVG](https://docs.fileformat.com/page-description-language/svg/)، [TIFF](https://docs.fileformat.com/image/tiff/)، [EMF](https://docs.fileformat.com/image/emf/)، [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)، [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## واجهة برمجة تطبيقات REST

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الطلب

| اسم المعامل | النوع | المسار/سلسلة الاستعلام/جسم HTTP | مطلوب | الوصف |
|-------------|-------|----------------------------------|--------|--------|
| file | ملف | formData | نعم | الملف المراد رفعه |
| objectType | نص (string) | استعلام (query) | نعم | نوع الكائن المراد تصديره. لتصدير الرسم البياني استخدم `chart`. قيم محتملة أخرى: `worksheet`، `picture`، إلخ. |
| format | نص (string) | استعلام (query) | نعم | تنسيق الإخراج المرغوب. القيم المدعومة: `png`، `jpeg`، `gif`، `bmp`، `svg`، `tiff`، `emf`، `wmf`، `pdf`. |

### الاستجابة

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2_ListObjects_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**رموز حالات HTTP**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | ناجح (OK) | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل: نوع ملف غير مدعوم). |
| 401 | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حمل مفرط (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostExport API باستخدام مكتبات SDK

### مواصفات واجهة PostExport API

تُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=listobject&format=tiff" \
-H "accept: multipart/form-data" \
-H "Content-Type: multipart/form-data" \
-H "x-aspose-client: Containerize.Swagger" \
-d '{"File":{}}'
```

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أفضل طريقة لتسريع عملية التطوير. تتعامل مكتبة SDK مع التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportListObject.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportListObject.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportListObject.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportListObject.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportListObject.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportListObject.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportListObject.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportListObject.go" >}}
{{< /tab >}}

{{< /tabs >}}