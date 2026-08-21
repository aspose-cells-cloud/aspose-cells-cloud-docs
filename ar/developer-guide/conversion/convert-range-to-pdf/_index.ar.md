---
title: "تحويل نطاق إكسل إلى PDF باستخدام واجهة Aspose.Cells Cloud API"
second_title: "مستند"
ArticleTitle: "كيفية تحويل بيانات نطاق جدول محلي إلى ملف PDF: دليل خطوة بخطوة"
linktype: "تحويل النطاق إلى PDF"
type: docs
url: /ar/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, تحويل نطاق إكسل إلى PDF, تحويل إكسل إلى PDF, التحويل السحابي"
description: "تحويل نطاق معيّن من جدول إكسل محلي إلى PDF باستخدام واجهة Aspose.Cells Cloud REST API."
weight: 100
---

تصدير نطاق من البيانات من ملف إكسل محلي إلى ملف [PDF](https://docs.fileformat.com/pdf/) باستخدام واجهة Cloud API.

**المتطلبات المسبقة**: قبل استخدام هذه الواجهة، تحتاج إلى حساب Aspose.Cells Cloud صالح، ورمز وصول JWT، وربما واجهة برمجة تطبيقات (SDK) خاصة بـ Aspose.Cells Cloud للغة البرمجة التي تستخدمها. تأكد من تهيئة مخزن الوجهة (الافتراضي أو المخصص) إذا كنت تخطط لاستخدام معامل `outStorageName`.

## **واجهة تحويل النطاق إلى PDF**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معاملات الطلب:**

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
|-------------|-------|--------------------------------------|--------|
| Spreadsheet | ملف | FormData | رفع ملف الجدول. |
| worksheet | نص | استعلام | اسم ورقة العمل داخل الجدول. |
| range | نص | استعلام | منطقة الخلايا المراد تحويلها، مثل A1:C10. |
| outPath | نص | استعلام | (اختياري) مسار المجلد الذي يُخزَّن فيه الملف. القيمة الافتراضية هي null. |
| outStorageName | نص | استعلام | اسم مخزن ملف الإخراج. |
| fontsLocation | نص | استعلام | موقع تخزين الخطوط المخصصة للاستخدام الشخصي. |
| region | نص | استعلام | إعداد منطقة الجدول. |
| password | نص | استعلام | كلمة المرور لفتح ملف الجدول. |

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

_الاستجابة النموذجية هي دفق ثنائي PDF يُعاد كتنزيل ملف._

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
|-------|--------|--------|
| 200 | ناجح | تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرّح | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## **أين يجب عليك استخدام واجهة تحويل النطاق إلى PDF؟**

- **البيانات المالية**: تحويل ميزانيات العمليات، والقوائم المالية (نطاقات محددة) إلى PDF لتوثيق جاهز للمراجعة.
- **تقارير المبيعات**: تحويل لوحات معلومات المبيعات أو حسابات العمولات إلى ملفات PDF قابلة للتوزيع.
- **مقاييس العمليات**: تصدير جداول المؤشرات الرئيسية للأداء ومقاييس الأداء كتقارير PDF رسمية.
- **البيانات التعاقدية**: تصدير جداول الأسعار واتفاقيات مستوى الخدمة من الجداول إلى مرفقات PDF.
- **سجلات التدقيق**: الحفاظ على نطاقات البيانات المالية كأدلة PDF غير قابلة للتعديل.
- **ملخصات المحافظ**: تصدير نطاقات أداء الاستثمارات كبيانات PDF جاهزة للعميل.
- **تقارير ضبط الجودة**: تصدير نطاقات بيانات التفتيش إلى PDF للسجلات الامتثالية.
- **ملخصات المخزون**: تحويل جداول مستويات المخزون إلى PDF لمراجعة الإدارة.

## **لماذا يجب عليك استخدام واجهة تحويل النطاق إلى PDF؟**

- **سهلة للمطورين**: توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يمكّن من تطوير سريع مع وثائق شاملة. ومقارنةً ببناء حلول مخصصة لعرض الرسوم البيانية، فإن هذا يقلل بشكل كبير من جهد التطوير.
- **فعّالة من حيث التكلفة**: يمكنك تحويل بيانات النطاق دون الحاجة لرفع الملف كاملاً مسبقًا، مما يوفر مساحة التخزين ويقلل التكاليف.
- **يحافظ على تنسيقات إكسل المعقدة** في تنسيق PDF قابل للوصول عالميًا.

## **كيفية استخدام واجهة تحويل النطاق إلى PDF باستخدام SDK؟**

### **مواصفات واجهة تحويل النطاق إلى PDF**

[مواصفات واجهة تحويل النطاق إلى PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) تعرّف واجهة برمجة تطبيقات عامة قابلة للوصول وتسمح لك بإجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء استدعاءات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### **استخدام SDKs الخاصة بـ Aspose.Cells Cloud**

استخدام SDK هو أسرع طريقة للتطوير، حيث يُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بتحويل نطاق من البيانات إلى ملف PDF باستخدام كود موجز. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء استدعاءات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}