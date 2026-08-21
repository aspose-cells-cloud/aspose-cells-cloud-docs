---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud - تحويل بيانات جدول Excel المحلية إلى ملف صورة - أداة مجانية عبر الإنترنت"
secondtitle: "وثيقة"
articletitle: "كيفية تحويل بيانات جدول جداول البيانات المحلية إلى ملف صورة: دليل خطوة بخطوة"
linktitle: "تحويل الجدول إلى صورة"
type: docs
url: /convert-table-to-image/
keywords: "Aspose.Cells, واجهة برمجة تطبيقات سحابية, تحويل الجدول إلى صورة, Excel, PNG, JPEG, TIFF, BMP, SVG"
description: "حوّل بسرعة جدول جدول بيانات Excel المحلي إلى ملف صورة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. يدعم تنسيقات PNG وJPEG وTIFF وBMP وSVG وغيرها."
weight: 100
---

تصدير بيانات الجدول من ملف Excel المحلي إلى ملف [صورة](https://docs.fileformat.com/image/) باستخدام واجهة برمجة تطبيقات السحابة.

**تنسيقات الصور المدعومة:**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **واجهة برمجة تطبيقات تحويل الجدول إلى صورة**

قبل استخدام هذه النقطة النهائية، تأكد من توفر المتطلبات الأساسية التالية:

- رمز وصول JWT صالح تم الحصول عليه من خلال مصادقة Aspose.Cells Cloud.
- حساب تخزين قابل للوصول إذا كنت تنوي استخدام معاملات `outPath` أو `outStorageName`.
- يجب أن يكون ملف المصنف المصدر (ملف Excel المحلي) قابلًا للقراءة، وإذا كان مشفرًا، يجب توفير كلمة المرور الصحيحة.

### واجهة برمجة تطبيقات الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معاملات الطلب:**

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم الـ HTTP | الوصف |
| :---------- | :----- | :-------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet | ملف | FormData | تحميل ملف جدول البيانات. |
| worksheet | نص | استعلام | اسم ورقة العمل الخاصة بجدول البيانات أو Excel. |
| tableName | نص | استعلام | اسم الجدول المراد تحويله. |
| format | نص | استعلام | تنسيق ملف الصورة المرغوب (مثل: png, svg). |
| outPath | نص | استعلام | (اختياري) مسار المجلد حيث سيتم حفظ الصورة المحولة. القيمة الافتراضية هي null. |
| outStorageName | نص | استعلام | تحديد اسم تخزين ملف الإخراج. |
| fontsLocation | نص | استعلام | استخدام خطوط مخصصة عند الحاجة. |
| region | نص | استعلام | إعداد منطقة/لغة جدول البيانات (مثل: `en-US`, `fr-FR`). يؤثر على تنسيق الأرقام، وتفسير التواريخ، والسلوك الخاص باللغة المحلية. |
| password | نص | استعلام | كلمة المرور المطلوبة للوصول إلى ملف جدول البيانات. |

### **الاستجابة**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | نجاح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح | معاملات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401  | غير مصرح به | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمل كبير جدًا | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500  | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## **أين يجب عليك استخدام واجهة برمجة تطبيقات تحويل الجدول إلى صورة؟**

- **لقطات ثابتة للتقارير**: حوّل جداول مالية أو نتائج الحسابات أو أي بيانات منسقة إلى صور لتضمينها في تقارير PDF أو شرائح PowerPoint أو المستندات المطبوعة حيث لا يُطلب تعديلها.
- **تصور البيانات في العروض التقديمية**: حوّل جداول جداول البيانات المعقدة – بما في ذلك التنسيق الشرطي أو التصورات البسيطة – إلى صور يمكن تضمينها في العروض التقديمية (PPTX، Google Slides).
- **المستندات ومواد التدريب**: خذ لقطات لדוגمات جداول البيانات أو القوالب أو نماذج إدخال البيانات كصور لأدلة المستخدم أو البرامج التعليمية أو مقالات قاعدة المعرفة.
- **معاينات مصغرة**: أنشئ معاينات صغيرة لصور أقسام جدول البيانات الرئيسية لمستعرضات الملفات أو مكتبات المستندات أو نتائج البحث.

## لماذا يجب عليك استخدام واجهة برمجة تطبيقات تحويل الجدول إلى صورة؟

- **سهلة للمطورين**: توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يمكّن من تطوير سريع، وتُرفق معها وثائق شاملة. بالمقارنة مع بناء حلول عرض مخصصة، فإن هذا يقلل بشكل كبير من جهد التطوير.
- **موفرة من حيث التكلفة**: يمكنك تحويل بيانات الجدول دون الحاجة أولاً لرفع المصنف بالكامل، مما يوفر مساحة تخزين ويقلل التكاليف.
- **الحفاظ على دقة البكسل**: إعادة إنتاج مظهر Excel بدقة – بما في ذلك تنسيق الخلايا، والصيغ (كقيم معروضة)، والحدود، والألوان، والتنسيق الشرطي – في صورة الإخراج.
- **توافق عالمي**: تنسيقات الصور (PNG وJPEG وTIFF وBMP وSVG وما إلى ذلك) قابلة للعرض على أي جهاز أو منصة دون برامج متخصصة، مما يضمن أقصى قدر من إمكانية الوصول.

## كيف تستخدم واجهة برمجة تطبيقات تحويل الجدول إلى صورة باستخدام مكتبات SDK؟

### مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى صورة

توفر [مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى صورة](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToImage) واجهة برمجة تطبيقات برمجية متاحة علنًا لإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة تطبيقات السحابة باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة للتطوير، حيث يُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بتحويل بيانات جدول جداول البيانات إلى صورة باستخدام كود معدود. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}