---
title: "تصدير الأشكال"
second_title: "المستند"
linktitle: "الشكل"
type: docs
url: /ar/export-excel-shape-to-different-formats/
aliases: [  /ar/export/excel-shape-to-different-formats/ ]
keywords: "تصدير الأشكال، Aspose.Cells Cloud، تصدير شكل Excel، تنسيقات الصور، REST API، SDK"
description: "تعرّف على كيفية تصدير أشكال Excel إلى تنسيقات صور متعددة (PNG وGIF وJPEG وBMP وSVG وTIFF وEMF وWMF) باستخدام واجهة Aspose.Cells Cloud REST API وSDKs."
weight: 20
ArticleTitle: "تصدير الأشكال – Aspose.Cells Cloud"
---

يمكّن تصدير الأشكال من ملفات Excel من إعادة استخدام المحتوى التخطيطي عبر منصّات وتطبيقات مختلفة. **المتطلبات المسبقة:** رمز وصول JWT صالح وملف Excel المصدر المراد رفعه.

يمكنك تصدير الأشكال إلى التنسيقات التالية: **PNG**، **GIF**، **JPEG**، **BMP**، **SVG**، **TIFF**، **EMF**، **WMF**.

## واجهة PostExport API

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.


### معاملات الطلب

| اسم المعامل | النوع | المسار/سلسلة الاستعلام/جسم HTTP | مطلوب | الوصف |
|-------------|--------|-----------------------------|----------|-------------|
| file | ملف | formData | True | الملف المراد رفعه |
| objectType | نص | query | True | نوع الكائن المراد تصديره. لتصدير المخطط، استخدم `chart`. القيم الصالحة تشمل `shape` و`worksheet` و`picture` وما إلى ذلك. |
| format | نص | query | True | تنسيق الإخراج المرغوب. القيم المدعومة: `png` و`jpeg` و`gif` و`bmp` و`svg` و`tiff` و`emf` و`wmf` و`pdf`. |

### **مثال على الطلب**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### الاستجابة

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... كائنات ملفات إضافية ...
  ]
}
```

*تتراوح أحجام حمولة الملفات المشفرة بـBase64 عادةً من بضعة مئات من البايتات إلى عدة ميغابايت، حسب أبعاد الصورة وتنسيقها.*

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|--------|-----------------------|-------------|
| 200 | ناجح | تم تصدير الأشكال بنجاح؛ تحتوي الاستجابة على قائمة الملفات. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صالحة. |
| 401 | غير مخوّل | رمز وصول غير صالح أو مفقود. |
| 413 | حملة كبيرة جدًا | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |


## كيفية استخدام واجهة PostExport API باستخدام SDKs

### مواصفات واجهة PostExport API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) واجهة برمجة تطبيقات قابلة للوصول عامّة، وتمكّنك من إجراء تفاعلات REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة لتطوير تطبيقات تتفاعل مع Aspose.Cells Cloud. وتُجرّد SDK التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على المنطق التجاري. يمكنك زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}