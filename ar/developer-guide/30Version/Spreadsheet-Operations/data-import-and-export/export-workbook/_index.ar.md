---
title: "تصدير كُتيّب عمل"
second_title: "مستند"
linktitle: "كُتيّب عمل"
type: docs
url: /ar/export-excel-to-different-formats/
aliases: [  /ar/export/excel-to-different-formats/ ]
keywords: "Aspose.Cells Cloud, تصدير Excel, تحويل كُتيّب العمل, PDF, CSV, JSON, تنسيقات الصور, واجهة برمجة تطبيقات جداول الحسابات, XLSX, ODS, PNG"
description: "دليل خطوة بخطوة لتصدير كُتيّبات عمل Excel إلى صيغ متعددة، بما في ذلك PDF وCSV وJSON وأنواع الصور المختلفة، باستخدام واجهة Aspose.Cells Cloud REST API ومكتبات SDK."
weight: 20
---

يمكنك تصدير كُتيّبات العمل إلى أيٍّ من الصيغ التالية: [XLS](https://docs.fileformat.com/spreadsheet/xls/)، [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)، [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)، [CSV](https://docs.fileformat.com/spreadsheet/csv/)، [TSV](https://docs.fileformat.com/spreadsheet/tsv/)، [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)، [ODS](https://docs.fileformat.com/spreadsheet/ods/)، [TXT](https://docs.fileformat.com/word-processing/txt/)، [PDF](https://docs.fileformat.com/pdf/)، [OTS](https://docs.fileformat.com/spreadsheet/ots/)، [XPS](https://docs.fileformat.com/page-description-language/xps/)، [DIF](https://docs.fileformat.com/spreadsheet/dif/)، [PNG](https://docs.fileformat.com/Image/png/)، [JPEG](https://docs.fileformat.com/image/jpeg/)، [BMP](https://docs.fileformat.com/image/bmp/)، [SVG](https://docs.fileformat.com/page-description-language/svg/)، [TIFF](https://docs.fileformat.com/image/tiff/)، [EMF](https://docs.fileformat.com/image/emf/)، [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)، [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## واجهة برمجة التطبيقات REST


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **الأمان والمصادقة**

تتطلب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الطلب

| اسم المعامل | النوع | المسار/سلسلة الاستعلام/جسم HTTP | مطلوب | الوصف |
|-------------|-------|----------------------------------|--------|--------|
| file | ملف | formData | نعم | الملف المراد رفعه |
| objectType | نص | استعلام | نعم | نوع الكائن المراد تصديره. لتصدير المخططات، استخدم `chart`. القيم الممكنة الأخرى هي `worksheet` و`picture` وما إلى ذلك. |
| format | نص | استعلام | نعم | الصيغة المطلوبة للإخراج. القيم المدعومة: `png`، `jpeg`، `gif`، `bmp`، `svg`، `tiff`، `emf`، `wmf`، `pdf`. |


### **الاستجابة**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | نجاح | تم تصدير الأشكال بنجاح؛ تحتوي الاستجابة على قائمة الملفات. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صالحة. |
| 401 | غير مُصرّح | رمز وصول غير صالح أو مفقود. |
| 413 | حمل البيانات كبير جدًا | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |


## كيفية استخدام واجهة PostExport مع مكتبات SDK

### مواصفات واجهة PostExport


تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) واجهة برمجة تطبيقات عامة قابلة للوصول تتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

يساعد استخدام مكتبة SDK في تسريع عملية التطوير من خلال التعامل مع التفاصيل منخفضة المستوى، بحيث يمكنك التركيز على منطق الأعمال. تتوفر قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud في [مستودع GitHub](https://github.com/aspose-cells-cloud).

تُظهر أمثلة الكود التالية كيفية استدعاء خدمة الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}