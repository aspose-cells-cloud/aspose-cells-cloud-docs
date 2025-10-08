---
title: Aspose.Cells Cloud Web API - تحويل مخطط جدول بيانات إلى صورة
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: تحويل الرسم البياني إلى صورة
type: docs
url: /ar/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: تحويل مخطط من جدول بيانات محلي/ملف Excel إلى ملف صورة باستخدام Aspose.Cells Cloud Web API
weight: 100
kwords: تحويل مخطط Excel إلى صورة، png، svg، tiff، jpg، bmp، جدول بيانات
---
تحويل مخطط من جدول بيانات محلي/ملف Excel إلى ملف صورة. مدعوم**تنسيقات الصور:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **تحويل الرسم البياني إلى صورة API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|:- |:- |:- |:- |
|جدول بيانات|ملف|بيانات النموذج|قم بتحميل ملف جدول البيانات الذي يحتوي على الرسم البياني.|
|ورقة عمل|خيط|استفسار|حدد اسم ورقة العمل إذا كان ذلك ممكنا.|
|مؤشر الرسم البياني|عدد صحيح|استفسار|فهرس الرسم البياني للتحويل.|
|شكل|خيط|استفسار|(مطلوب) نوع الصورة المطلوبة (على سبيل المثال، svg، png، jpg).|
|المسار الخارجي|خيط|استفسار|(اختياري) مسار المجلد الذي يتم تخزين المصنف فيه؛ الافتراضي هو null.|
|اسم التخزين الخارجي|خيط|استفسار|اسم التخزين لملف الإخراج.|
|الخطوطالموقع|خيط|استفسار|حدد الخطوط المخصصة إذا لزم الأمر.|
|منطقة|خيط|استفسار|تعيين منطقة جدول البيانات.|
|كلمة المرور|خيط|استفسار|كلمة المرور لفتح ملف جدول البيانات.|

## **إجابة**

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

### رموز الخطأ

- **400 طلب سيء**:عنوان URI الخاص بـ Apose.Cells Cloud API غير صالح.
- **401 غير مصرح به**رمز وصول غير صالح. أو معرف عميل وسر غير صالحين.
- **404 غير موجود**:ملف جدول البيانات غير قابل للوصول.
- **خطأ الخادم 500**:واجهت جدول البيانات خللاً في الحصول على بيانات الحساب.

## أين يجب عليك استخدام تحويل الرسم البياني إلى صورة API؟

- تصدير المخططات البيانية في جدول البيانات كصور.

## لماذا يجب عليك استخدام تحويل الرسم البياني إلى صورة API؟

- لا حاجة للتخزين السحابي، مما يقلل العبء على موارد السحابة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام تحويل الرسم البياني إلى صورة API مع SDKs؟

### تحويل الرسم البياني إلى صورة API المواصفات

 ال[تحويل الرسم البياني إلى صورة API المواصفات](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويمكّنك من تنفيذ تفاعلات REST مباشرة من متصفح الويب.

### استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بتحويل مخطط إلى صورة باستخدام رمز قصير.
 يرجى التحقق من[مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ Aspose.Cells Cloud SDKs.

توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
