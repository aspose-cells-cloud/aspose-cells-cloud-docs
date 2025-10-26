---
title: Aspose.Cells Cloud Web API - تحويل مخطط جدول بيانات إلى ملف PDF
second_title: Documen
ArticleTitle: Converting a Spreadsheet Chart to a Pdf file
linktitle: تحويل الرسم البياني إلى PD
type: docs
url: /ar/convert-chart-to-pdf/
keywords: convert an Excel chart to pdf, convert spreadsheet to pdf, Aspose Cloud Web  API, cloud conversion, Excel to PD
description: يقوم هذا البرنامج API بتحويل المخططات من جداول البيانات الموجودة على محرك أقراص محلي إلى ملف PDF بسلاسة
weight: 100
kwords: Excel، Office السحابة، REST API، تحويل جدول البيانات، PDF، CSV، JSON، Markdown، تحويل الرسم البياني إلى PDF، التحويل السحابي
---
 تحويل مخطط من جدول بيانات محلي/ملف Excel إلى[PDF](https://docs.fileformat.com/pdf/) ملف.

## **تحويل المخطط إلى PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **معلمات الطلب:**

| اسم المعلمة| يكتب| المسار/سلسلة الاستعلام/نص HTTP| وصف|
|-------------- ||--------------------- |--------------------------------------------------- |
| جدول بيانات|ملف| بيانات النموذج| تحميل ملف جدول البيانات.|
| ورقة عمل| خيط| استفسار| اسم ورقة العمل التي تحتوي على المخطط.|
| مؤشر الرسم البياني|عدد صحيح| استفسار| مؤشر الرسم البياني الذي سيتم تحويله.|
| المسار الخارجي| خيط| استفسار| (اختياري) مسار المجلد الذي يُخزَّن فيه الملف المُحوَّل. القيمة الافتراضية هي null.|
| اسم التخزين الخارجي| خيط| استفسار| اسم تخزين ملف الإخراج.|
| الخطوطالموقع| خيط| استفسار| استخدم الخطوط المخصصة إذا لزم الأمر.|
| منطقة| خيط| استفسار| إعداد منطقة جدول البيانات.|
| كلمة المرور| خيط| استفسار| كلمة المرور لفتح ملف جدول البيانات.|

### **إجابة**

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

## أين يجب عليك استخدام تحويل الرسم البياني إلى Pdf API؟

- تصدير المخططات البيانية في جدول البيانات بصيغة PDF.

## لماذا يجب عليك استخدام تحويل الرسم البياني إلى Pdf API؟

- لا حاجة للتخزين السحابي، مما يقلل العبء على موارد السحابة.
- يمكن إكمال التطوير بسرعة من خلال مجموعة أدوات التطوير البرمجية الموجودة.

## كيفية استخدام تحويل الرسم البياني إلى PDF API مع SDKs؟

### تحويل المخطط إلى PDF API المواصفات

 ال[تحويل المخطط إلى PDF API المواصفات](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) يحدد واجهة برمجة يمكن الوصول إليها بشكل عام ويسمح لك بتنفيذ تفاعلات REST مباشرة من متصفح الويب.

## استخدم Aspose.Cells Cloud SDKs

يعد استخدام SDK أسرع طريقة للتطوير، حيث يقوم بتجريد التفاصيل منخفضة المستوى، مما يسمح لك بتحويل مخطط إلى ملف pdf باستخدام رمز قصير.
توضح أمثلة التعليمات البرمجية التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مجموعات أدوات تطوير البرامج المختلفة:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
