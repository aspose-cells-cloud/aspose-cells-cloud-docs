---
title: "تصدير صفحة ورقة عمل – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud"
ArticleTitle: "تصدير صفحة ورقة عمل – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "صفحة"
type: docs
url: /ar/worksheets/page-to-different-formats/
aliases: [  /ar/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud، تصدير صفحة ورقة العمل، PDF، PNG، CSV، واجهة برمجة تطبيقات REST، مصادقة JWT، تنسيقات الملفات"
description: "تعرَّف على كيفية تصدير صفحة ورقة عمل محددة إلى تنسيقات مثل PDF وPNG وCSV وما إلى ذلك باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يشمل ذلك طلب cURL، ودليل المعاملات، وأمثلة لواجهات برمجة التطبيقات (SDKs) بلغات برمجة متعددة."
weight: 240
---

يُعد تصدير صفحة ورقة عمل محددة مفيدًا عندما تحتاج إلى لقطة قابلة للطباعة لتقرير أو صورة مخطط أو استخراج بيانات دون تنزيل ملف العمل كاملاً. تتيح لك هذه النقطة النهائية استرجاع صفحة واحدة فقط بالتنسيق الأنسب لسير عملك اللاحق.

تتيح لك واجهة [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) تحويل صفحة محددة من ورقة العمل إلى تنسيقات ملفات متعددة. التنسيقات المدعومة: [XLS](https://docs.fileformat.com/spreadsheet/xls/)، [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)، [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)، [CSV](https://docs.fileformat.com/spreadsheet/csv/)، [TSV](https://docs.fileformat.com/spreadsheet/tsv/)، [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)، [ODS](https://docs.fileformat.com/spreadsheet/ods/)، [TXT](https://docs.fileformat.com/word-processing/txt/)، [PDF](https://docs.fileformat.com/pdf/)، [OTS](https://docs.fileformat.com/spreadsheet/ots/)، [XPS](https://docs.fileformat.com/page-description-language/xps/)، [DIF](https://docs.fileformat.com/spreadsheet/dif/)، [PNG](https://docs.fileformat.com/Image/png/)، [JPEG](https://docs.fileformat.com/image/jpeg/)، [GIF](https://docs.fileformat.com/image/gif/)، [BMP](https://docs.fileformat.com/image/bmp/)، [WMF](https://docs.fileformat.com/image/wmf/)، [TIFF](https://docs.fileformat.com/image/tiff/)، [EMF](https://docs.fileformat.com/image/emf/)، [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)، [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## واجهة برمجة التطبيقات REST

يُعرِّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) واجهة برمجة تطبيقات متاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

> **المتطلبات المسبقة** – يجب أن تمتلك رمز مصادقة JWT ساري المفعول وملف العمل المخزن في مجلد سحابي تحدده باستخدام المعامل `folder`.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء استدعاء لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**الاستجابة** – تُعيد الخدمة الصفحة المطلوبة بالتنسيق المختار. بالنسبة لتنسيقات الصور (png، jpeg، gif، إلخ)، يحتوي الجسم على بيانات الصورة الثنائية؛ أما لتنسيقات المستندات (pdf، xls، csv، …) فيحتوي الجسم على محتوى الملف. ويعود استجابة ناجحة برمز HTTP 200.

*مثال على استجابة PNG (مقتطف مُشفَّر بـ base64 مختصر):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**المعاملات**

| المعامل                | النوع     | الوصف                                                                 | القيمة الافتراضية |
| ---------------------- | -------- | --------------------------------------------------------------------- | ----------------- |
| `format`               | نص (string) | تنسيق ملف الإخراج (مثل `pdf`، `png`، `csv`).                            | `pdf`             |
| `verticalResolution`   | عدد صحيح (integer) | الدقة الرأسية للصورة المُرسَلة (DPI).                                  | `100`             |
| `horizontalResolution` | عدد صحيح (integer) | الدقة الأفقية للصورة المُرسَلة (DPI).                                 | `100`             |
| `pageIndex`            | عدد صحيح (integer) | فهرس الصفحة (يبدأ من الصفر) لورقة العمل المراد تصديرها (`0` = الصفحة الأولى). | `0`               |
| `folder`               | نص (string) | مجلد التخزين السحابي الذي يوجد فيه ملف العمل المصدر.                    | —                 |

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                                      |
|------|-----------------------------|-------------------------------------------------------------|
| 200  | ناجح (OK)                   | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.    |
| 400  | طلب خاطئ (Bad Request)     | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).       |
| 401  | غير مصرّح (Unauthorized)    | رمز JWT غير صالح أو مفقود.                                 |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح.                     |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                  |

**الأخطاء المحتملة**

- **401 غير مصرّح (Unauthorized)** – رمز JWT غير صالح أو مفقود.
- **404 غير موجود (Not Found)** – ملف العمل أو ورقة العمل المحددة غير موجودة.
- **400 طلب خاطئ (Bad Request)** – قيمة معامل غير صحيحة (مثل `format` غير مدعوم).
- **500 خطأ داخلي في الخادم (Internal Server Error)** – مشكلة غير متوقعة من جانب الخادم.

## مجموعة أدوات التطوير (Cloud SDK Family)

استخدام SDK يُعد أفضل طريقة لتسريع عملية التطوير. فتتولى SDK إدارة التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام SDKs متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}