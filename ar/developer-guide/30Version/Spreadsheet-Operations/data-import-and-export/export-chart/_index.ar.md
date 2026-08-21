---
title: "تصدير مخطط Excel"
second_title: "مستند"
linktype: "مخطط"
type: docs
url: /export-excel-chart-to-different-formats/
aliases: [/export/excel-chart-to-different-formats/]
description: "تصدير كائنات المخططات من ملفات Excel إلى تنسيقات شائعة مثل PNG و JPEG و PDF و SVG و TIFF و EMF و WMF والمزيد باستخدام واجهة Aspose.Cells Cloud REST API أو SDKs. يشمل المصادقة ومثال cURL وأمثلة على الأكواد بلغات برمجة متعددة."
keywords: "Aspose.Cells, تصدير مخطط, تصدير مخطط Excel, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, تنسيقات المخططات, Aspose Cells Cloud"
weight: 20
ArticleTitle: "تصدير مخطط Excel – مستند"
---

تصدير كائنات المخططات من ملفات Excel إلى تنسيقات مختلفة للصور والمستندات هو متطلب شائع في إعداد التقارير والنشر. توفر Aspose.Cells Cloud نقطة نهاية REST بسيطة تحول المخططات مباشرةً إلى تنسيقات شائعة مثل PNG و JPEG و PDF و SVG و TIFF و EMF و WMF والمزيد.

يمكنك تصدير المخططات إلى التنسيقات التالية: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/), و [PDF](https://docs.fileformat.com/pdf/).

**متطلبات مسبقة:**  
- حساب Aspose.Cells Cloud ساري المفعول مع اشتراك نشط.  
- رمز مميز OAuth 2.0 Bearer (JWT) تم الحصول عليه عبر عملية المصادقة.  
- ملف المصنف المراد تحميله (أقصى حجم < 50 ميجابايت).  

## **واجهة REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | مطلوب | الوصف |
|-------------|-------|------------------------------------|--------|--------|
| file | ملف | formData | نعم | الملف المراد تحميله |
| objectType | نص | استعلام | نعم | نوع الكائن المراد تصديره. لتصدير المخطط استخدم `chart`. القيم المحتملة الأخرى تشمل `worksheet` و `picture` وما إلى ذلك. |
| format | نص | استعلام | نعم | التنسيق المطلوب للإخراج. القيم المدعومة: `png` و `jpeg` و `gif` و `bmp` و `svg` و `tiff` و `emf` و `wmf` و `pdf`. |

### **الاستجابة**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|---------|--------|
| 200 | نجاح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مخوّل | رمز JWT غير صالح أو مفقود. |
| 413 | حملة البيانات كبيرة جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostExport API باستخدام SDKs

### مواصفات واجهة PostExport API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يجب أن تتضمن جميع الطلبات رمز مميز OAuth 2.0 Bearer صالح في رأس `Authorization`. يُظهر المثال التالي كيفية استدعاء الواجهة باستخدام **cURL** وتحميل مصنف باستخدام multipart/form-data.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDKs هو أفضل طريقة لتسريع عملية التطوير. تقوم SDKs بالتعامل مع التفاصيل منخفضة المستوى وتسمح لك بالتركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب Aspose.Cells باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}