---
title: "تصدير منطقة ورقة عمل إلى PNG و PDF و CSV – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
linktitle: "المنطقة"
type: docs
url: /worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: "Aspose.Cells, تصدير منطقة ورقة العمل, PNG, PDF, CSV, تحويل Excel, واجهة برمجة تطبيقات REST, مكتبات SDK"
description: "تعرّف على كيفية تصدير نطاق خلايا محدّد من ورقة عمل Excel إلى تنسيقات PNG و PDF و CSV وأكثر من 20 تنسيقًا آخر باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST أو مكتبات SDK (C# و Java و Python…)."
weight: 230
ArticleTitle: "تصدير منطقة ورقة العمل إلى PNG و PDF و CSV باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud – دليل شامل"
---

يتيح لك [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API تحويل منطقة محددة من ورقة العمل إلى تنسيقات ملفات متعددة. التنسيقات المدعومة: [XLS](https://docs.fileformat.com/spreadsheet/xls/)، [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)، [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)، [CSV](https://docs.fileformat.com/spreadsheet/csv/)، [TSV](https://docs.fileformat.com/spreadsheet/tsv/)، [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)، [ODS](https://docs.fileformat.com/spreadsheet/ods/)، [TXT](https://docs.fileformat.com/word-processing/txt/)، [PDF](https://docs.fileformat.com/pdf/)، [OTS](https://docs.fileformat.com/spreadsheet/ots/)، [XPS](https://docs.fileformat.com/page-description-language/xps/)، [DIF](https://docs.fileformat.com/spreadsheet/dif/)، [PNG](https://docs.fileformat.com/Image/png/)، [JPEG](https://docs.fileformat.com/image/jpeg/)، [GIF](https://docs.fileformat.com/image/gif/)، [BMP](https://docs.fileformat.com/image/bmp/)، [WMF](https://docs.fileformat.com/image/wmf/)، [TIFF](https://docs.fileformat.com/image/tiff/)، [EMF](https://docs.fileformat.com/image/emf/)، [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/)، [FODS](https://docs.fileformat.com/spreadsheet/fods/).

يُظهر هذا الدليل كيفية تصدير **نطاق خلايا محدّد** من ورقة عمل Excel إلى تنسيقات PNG و PDF و CSV وأكثر من 20 تنسيق إضافي باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. وللمهام ذات الصلة مثل تصدير ورقة العمل بالكامل أو تحويل ملف книга، راجع صفحات **[تصدير ورقة العمل بالكامل](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** و **[تحويل ملف книга إلى PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)**.

## واجهة برمجة تطبيقات REST

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفّح ويب.

### معاملات الطلب

| المعامل             | النوع   | الإلزام | الوصف                                           |
|---------------------|---------|---------|--------------------------------------------------|
| `name`              | نص      | نعم     | اسم ملف книга.                                 |
| `sheetName`         | نص      | نعم     | اسم ورقة العمل المستهدفة.                       |
| `format`            | نص      | نعم     | تنسيق الإخراج المطلوب (png أو pdf أو csv…).     |
| `area`              | نص      | لا      | نطاق الخلايا المراد تصديره (مثال: `B3:K8`).    |
| `verticalResolution`| عدد صحيح| لا      | الدقة الرأسية للتنسيقات النقطية.               |
| `horizontalResolution`| عدد صحيح| لا    | الدقة الأفقية للتنسيقات النقطية.               |
| `folder`            | نص      | لا      | مجلد تخزين السحابة الذي يحتوي على الملف.       |
| `storage`           | نص      | لا      | اسم خدمة التخزين.                               |

### الاستجابة الناجحة

* **200 OK** – يُعيد الملف المطلوب بصيغته الثنائية (PNG أو PDF أو CSV… إلخ).

### استجابات الأخطاء

| رمز الحالة | الوصف                                              |
|------------|-----------------------------------------------------|
| 400        | طلب خاطئ – معاملات مفقودة أو غير صالحة.          |
| 401        | غير مُصادَق – رمز المصادقة مفقود أو غير صالح.     |
| 404        | غير موجود – لم يُعثر على книга أو ورقة العمل المحدّدة. |
| 500        | خطأ داخلي في الخادم – حالة غير متوقعة في الخادم.  |

**مثال على حمولة خطأ**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "المعامل 'area' بصيغة غير صحيحة. الصيغة المتوقعة: B3:K8."
  }
}
```

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء استدعاء لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

صورة محوّلة (PNG ثنائي)

{{< /tab >}}

{{< /tabs >}}

## عائلة مكتبات SDK السحابية

يُعد استخدام مكتبات SDK الطريقة الأسرع للتطوير. فتُجرّد مكتبات SDK التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على منطق مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية استدعاء خدمات Aspose.Cells عبر مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}