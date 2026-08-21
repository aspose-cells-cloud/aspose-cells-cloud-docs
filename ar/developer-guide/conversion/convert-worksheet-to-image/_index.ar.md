---
title: "تحويل ورقة العمل – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
second title: "مستند"
articleTitle: "كيفية تحويل بيانات جدول بيانات ورقة عمل محلية إلى ملف صورة: دليل خطوة بخطوة"
linkTitle: "تحويل ورقة العمل إلى صورة"
type: docs
url: /ar/convert-worksheet-to-image/
keywords: "Aspose.Cells Cloud، تحويل ورقة عمل إلى صورة، تحويل ورقة عمل إلى صورة، Excel إلى PNG، Excel إلى SVG، Excel إلى TIFF، Excel إلى JPEG، Excel إلى BMP، واجهة برمجة تطبيقات تحويل الصور، واجهة برمجة تطبيقات REST، تصدير صور جداول البيانات، أمثلة SDK"
description: "دليل خطوة بخطوة لتحويل ورقة عمل Excel إلى تنسيقات الصور (PNG، SVG، TIFF، JPEG، BMP، وما إلى ذلك) باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud، بما في ذلك معلمات الطلب، تفاصيل الاستجابة، رموز الأخطاء، سيناريوهات الاستخدام، وأكواد الأمثلة لـ SDK."
weight: 100
---

تصدير البيانات من ورقة عمل في ملف Excel محلي إلى ملف [صورة](https://docs.fileformat.com/image/) باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. تدعم هذه العملية تنسيقات الصور المتعددة، وهي مثالية لإنشاء لقطات بصرية لبيانات جداول البيانات.

**تنسيقات الصور المدعومة**

- [PNG](https://docs.fileformat.com/image/png/)
- [SVG](https://docs.fileformat.com/page-description-language/svg/)
- [TIFF](https://docs.fileformat.com/image/tiff/)
- [JPEG](https://docs.fileformat.com/image/jpeg/)
- [BMP](https://docs.fileformat.com/image/bmp/)

## **واجهة برمجة تطبيقات تحويل ورقة العمل إلى صورة**

### واجهة برمجة التطبيقات عبر الويب

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/image
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الطلب**

| اسم المعلمة | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
| :----------- | :----- | :------------------------- | :----------------------------------------------------------------------------------- |
| Spreadsheet | ملف | FormData | رفع ملف جدول البيانات. |
| worksheet | سلسلة نصية | استعلام | اسم ورقة العمل المراد تحويلها. |
| format | سلسلة نصية | استعلام | تنسيق الصورة المطلوب (`svg`، `png`، `tiff`، `jpeg`، `bmp`، إلخ). |
| outPath | سلسلة نصية | استعلام | _(اختياري)_ مسار المجلد الذي سيتم حفظ صورة الإخراج فيه؛ القيمة الافتراضية هي `null`. |
| outStorageName | سلسلة نصية | استعلام | اسم موقع التخزين لملف الإخراج. |
| fontsLocation | سلسلة نصية | استعلام | مسار مجلد خطوط مخصصة، إن احتجت لاستخدام خطوط غير متوفرة على الخادم. |
| region | سلسلة نصية | استعلام | إعداد منطقة جدول البيانات (مثل `en-US`). |
| password | سلسلة نصية | استعلام | كلمة المرور المطلوبة لفتح ملف جدول البيانات المحمي. |

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
| 200 | ناجح (OK) | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معلمات ناقصة أو غير صحيحة (مثل نوع الملف غير المدعوم). |
| 401 | غير مصرح (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## **أين يجب استخدام واجهة برمجة تطبيقات تحويل ورقة العمل إلى صورة؟**

- **لقطات ثابتة للتقارير** – تحويل الجداول المالية أو الحسابات أو غيرها من البيانات إلى صور لاستخدامها في تقارير PDF أو شرائح PowerPoint أو المستندات المطبوعة حيث لا يُطلب تعديلها.
- **تمثيل بصري للبيانات في العروض التقديمية** – تحويل جداول البيانات المعقدة (بما في ذلك التنسيق الشرطي أو المخططات البسيطة) إلى صور يمكن تضمينها في العروض التقديمية (PPTX، Google Slides).
- **المستندات ومواد التدريب** – التقاط أمثلة جداول البيانات أو القوالب أو نماذج إدخال البيانات كصور لاستخدامها في الكتيبات أو الدلائل أو المقالات في قواعد المعرفة.
- **معاينات مصغرة** – إنشاء معاينات صور صغيرة لأقسام جداول البيانات الأساسية لمستعرضات الملفات أو مكتبات المستندات أو نتائج البحث.

## **لماذا يجب استخدام واجهة برمجة تطبيقات تحويل ورقة العمل إلى صورة؟**

- **سهلة الاستخدام للمطورين** – توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يمكّن من تطوير سريع ويأتي مع وثائق شاملة. مقارنةً بإنشاء حل مخصص لعرض الرسوم البيانية، فإن هذا يقلل بشكل كبير من حجم العمل التطويري.
- **فعالة من حيث التكلفة** – يمكنك تحويل بيانات الجداول دون الحاجة لتخزين ملفات المصنف بشكل دائم، مما يوفر مساحة تخزين ويقلل التكاليف.
- **الحفاظ على دقة البكسل** – إعادة إنتاج مظهر Excel بدقة، بما في ذلك تنسيق الخلايا والصيغ (كقيم معروضة)، والحدود والألوان والتنسيق الشرطي، في صورة الإخراج.
- **توافق عالمي** – تنسيقات الصور (PNG، JPEG، TIFF، BMP، SVG، وما إلى ذلك) قابلة للعرض على أي جهاز أو منصة دون برامج متخصصة، مما يضمن أقصى قدر من إمكانية الوصول.

## **كيفية استخدام واجهة برمجة تطبيقات تحويل ورقة العمل إلى صورة مع مكتبات SDK؟**

### مواصفات واجهة برمجة تطبيقات تحويل ورقة العمل إلى صورة

تعرّف [مواصفات واجهة برمجة تطبيقات تحويل ورقة العمل إلى صورة](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToImage) واجهة برمجة تطبيقات قابلة للوصول بشكل عام وتسمح بالتفاعل مع REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة تطبيقات السحابة باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/image?format=png&worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (مشفرة بـ Base64)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK لـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، حيث يُجرّد التفاصيل من المستوى المنخفض ويجعلك قادرًا على تحويل بيانات ورقة العمل إلى صورة باستخدام كود محدود. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK لـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToSvg.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToSvg.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToSvg.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToSvg.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToSvg.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToSvg.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToSvg.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToSvg.go" >}}
{{</tab>}}
{{< /tabs >}}