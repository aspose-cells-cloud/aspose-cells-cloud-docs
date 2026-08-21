---
title: "واجهة Aspose.Cells Cloud Web API – تحويل ورقة عمل Excel محلية إلى ملف PDF – أداة مجانية عبر الإنترنت"
second_title: "مستند"
ArticleTitle: "كيفية تحويل ورقة عمل جدول بيانات محلي إلى ملف PDF: دليل خطوة بخطوة"
linktype: "تحويل ورقة عمل إلى PDF"
type: docs
url: /ar/convert-worksheet-to-pdf/
keywords: "Aspose.Cells، Excel إلى PDF، تحويل ورقة العمل، واجهة REST API، التحويل السحابي، PDF جدول البيانات، نقطة نهاية API، إنشاء ملف PDF"
description: "استخدم واجهة Aspose.Cells Cloud API لتحويل ورقة عمل من ملف Excel محلي إلى مستند PDF بسرعة وأمان."
weight: 100
---

تصدير ورقة عمل من ملف Excel محلي إلى ملف [PDF](https://docs.fileformat.com/pdf/) باستخدام واجهة Cloud API.

## **واجهة تحويل ورقة العمل إلى PDF**

### واجهة Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **الأمان والمصادقة**

تعمل واجهات Aspose.Cells Cloud API بشكل آمن وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **مُعلمات الطلب:**

| اسم المُعلمة | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|------|-----------------------------------|--------|
| Spreadsheet | ملف | FormData | تحميل ملف جدول البيانات. |
| worksheet | سلسلة نصية | استعلام | اسم ورقة العمل داخل جدول البيانات. |
| outPath | سلسلة نصية | استعلام | (اختياري) مسار المجلد لتخزين ملف جدول العمل؛ القيمة الافتراضية هي null. |
| outStorageName | سلسلة نصية | استعلام | اسم تخزين ملف الإخراج. |
| fontsLocation | سلسلة نصية | استعلام | استخدام خطوط مخصصة لإنشاء ملف PDF. |
| region | سلسلة نصية | استعلام | تحديد إعداد منطقة جدول البيانات. |
| password | سلسلة نصية | استعلام | كلمة المرور المطلوبة لفتح ملف جدول البيانات. |

### **الاستجابة**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**رموز حالة HTTP**

| الكود | المعنى | الوصف |
|-------|--------|--------|
| 200 | نجاح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مخوَّل | رمز JWT غير صالح أو مفقود. |
| 413 | حجم البيانات كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500 | خطأ داخلي في الخادم | حدث خطأ غير متوقع في الخادم. |

## **أين يجب عليك استخدام واجهة تحويل ورقة العمل إلى PDF؟**

- **البيانات المالية**: تحويل ميزانيات التشغيل، قوائم الدخل (جداول محددة) إلى PDF لتوثيق جاهز للمراجعة.
- **تقارير المبيعات**: تحويل لوحات عرض المبيعات أو حسابات العمولات إلى ملفات PDF قابلة للتوزيع.
- **مقاييس العمليات**: تصدير جداول المؤشرات الرئيسية للأداء (KPI) ومقاييس الأداء كتقرير PDF رسمي.
- **البيانات التعاقدية**: تصدير جداول الأسعار واتفاقيات مستوى الخدمة من جداول البيانات إلى ملفات PDF مُرفقة.
- **سجلات التدقيق**: الاحتفاظ بورقات العمل المالية كأدلة PDF غير قابلة للتعديل.
- **ملخصات المحافظ الاستثمارية**: تصدير جداول أداء الاستثمارات كبيانات PDF جاهزة للعميل.
- **تقارير ضبط الجودة**: تصدير ورقات عمل الفحص إلى PDF لسجلات الامتثال.
- **ملخصات المخزون**: تحويل ورقات عمل المخزون إلى PDF لمراجعة الإدارة.

## **لماذا يجب عليك استخدام واجهة تحويل ورقة العمل إلى PDF؟**

- **سهلة للمطورين**: توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، ما يُسهّل التطوير السريع، وتأتي مع وثائق شاملة. وبالمقارنة مع بناء حلول مخصصة لعرض الرسوم البيانية، فإن هذه الميزة تقلل بشكل كبير من جهد التطوير.
- **فعالة من حيث التكلفة**: يمكنك تحويل بيانات الجداول دون تحميل جدول العمل أولاً، مما يوفر مساحة التخزين ويقلل التكاليف.
- **الحفاظ على التنسيق**: تحافظ على تنسيق Excel المعقد في تنسيق PDF عالمي القابلية للوصول.

## **كيفية استخدام واجهة تحويل ورقة العمل إلى PDF باستخدام مكتبات SDK؟**

### مواصفات واجهة تحويل ورقة العمل إلى PDF

تقدم [مواصفات واجهة تحويل ورقة العمل إلى PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) واجهة برمجة تطبيقات عامة قابلة للوصول، وتمكّنك من إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، إذ تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بتحويل بيانات جداول البيانات إلى ملف PDF باستخدام كود محدود. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على القائمة الكاملة لمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}