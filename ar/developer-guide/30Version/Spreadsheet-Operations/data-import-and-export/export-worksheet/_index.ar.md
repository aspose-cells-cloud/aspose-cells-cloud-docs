---
title: "تصدير ورقة عمل – Aspose.Cells Cloud"
second_title: "المستند"
linktitle: "ورقة العمل"
type: docs
url: /ar/export-excel-worksheet-to-different-formats/
aliases: [  /ar/export/excel-worksheet-to-different-formats/ ]
keywords: "Aspose.Cells, تصدير ورقة عمل, API لملفات إكسل, PDF, CSV, TIFF, ODS, تنسيقات الصور"
description: "تعرّف على كيفية تصدير ورقة عمل إكسل إلى تنسيقات مثل PDF وCSV وTIFF وغيرها باستخدام واجهة Aspose.Cells Cloud REST API. يشمل مثال cURL وتفاصيل المصادقة المطلوبة ومعلمات الاستدعاء ومعالجة الاستجابة."
weight: 20
ArticleTitle: "تصدير ورقة عمل إكسل إلى تنسيقات متنوعة – Aspose.Cells Cloud"
---

يمكنك تصدير ورقة العمل إلى التنسيقات التالية:

- **XLS** – [تفاصيل تنسيق XLS](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [تفاصيل تنسيق XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [تفاصيل تنسيق XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [تفاصيل تنسيق CSV](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [تفاصيل تنسيق TSV](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [تفاصيل تنسيق XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [تفاصيل تنسيق ODS](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [تفاصيل تنسيق TXT](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [تفاصيل تنسيق PDF](https://docs.fileformat.com/pdf/)
- **OTS** – [تفاصيل تنسيق OTS](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [تفاصيل تنسيق XPS](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [تفاصيل تنسيق DIF](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [تفاصيل تنسيق PNG](https://docs.fileformat.com/Image/png/)
- **JPEG** – [تفاصيل تنسيق JPEG](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [تفاصيل تنسيق BMP](https://docs.fileformat.com/image/bmp/)
- **SVG** – [تفاصيل تنسيق SVG](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [تفاصيل تنسيق TIFF](https://docs.fileformat.com/image/tiff/)
- **EMF** – [تفاصيل تنسيق EMF](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [تفاصيل تنسيق Numbers](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [تفاصيل تنسيق FODS](https://docs.fileformat.com/spreadsheet/fods/)

[استكشف عمليات التصدير ذات الصلة مثل تصدير ملف العمل كاملاً أو مخطط بياني.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## واجهة PostExport API

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **الأمان والمصادقة**

تستخدم واجهات برمجة تطبيقات Aspose.Cells Cloud آليات أمنية وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### معلمات الطلب

| اسم المعلمة | النوع | المسار/سلسلة الاستعلام/محتوى جسم HTTP | مطلوب | الوصف |
|-------------|-------|----------------------------------------|--------|---------|
| file | ملف | formData | نعم | الملف المراد تحميله |
| objectType | سلسلة نصية | استعلام | نعم | نوع الكائن المراد تصديره. لتصدير المخططات استخدم `chart`. قيم أخرى محتملة: `worksheet` (ورقة عمل)، `picture` (صورة)، إلخ. |
| format | سلسلة نصية | استعلام | نعم | التنسيق المطلوب للإخراج. القيم المدعومة: `png`، `jpeg`، `gif`، `bmp`، `svg`، `tiff`، `emf`، `wmf`، `pdf`. |

### الاستجابة

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **معالجة الأخطاء**

إذا فشل الطلب، تُعيد واجهة API كائن JSON يحتوي على حقول مثل `Code` و `Message`. تشمل رموز حالة HTTP الشائعة **401 Unauthorized** (رمز مفقود أو غير صالح) و **400 Bad Request** (معلمات غير صالحة).

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | نجاح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصدق | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

**ملاحظات**

- الحد الأقصى لحجم الملف المسموح برفعه هو 50 ميغابايت.  
- تدعم واجهة API تصدير عدة أوراق عمل في طلب واحد؛ تُعاد كل ورقة عمل كملف منفصل داخل المصفوفة `Files`.  
- تتوفر المعالجة غير المتزامنة لملفات العمل الكبيرة؛ استخدم رمز الحالة `202 Accepted` لمراقبة حالة العملية عبر الاستبيان (polling).

## كيفية استخدام واجهة PostExport API مع مكتبات SDK

### المتطلبات الأساسية

قبل استدعاء واجهة API، احصل على رمز وصول JWT صالح باستخدام عملية مصادقة Aspose.Cells Cloud. تأكد من تضمين الرمز في رأس الطلب `Authorization` لكل طلب. تتعامل مكتبات SDK مع الحصول على الرمز تلقائيًا عند تكوينها ببيانات اعتماد العميل الخاصة بك.

### مواصفات واجهة PostExport API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) واجهة برمجة تطبيقات عامة قابلة للاستدعاء مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية استدعاء واجهة API عبر cURL.

```bash
# تصدير ورقة عمل إلى تنسيق TIFF
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة لتطوير التطبيقات مع Aspose.Cells Cloud. فالمكتبة SDK تُجرّدك من التفاصيل التقنية منخفضة المستوى، مما يسمح لك بالتركيز على منطق عملك. للاطلاع على القائمة الكاملة للمكتبات المدعومة، يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud).

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر مكتبات SDK متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---