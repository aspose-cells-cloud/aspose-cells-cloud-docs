---
title: "واجهة Aspose.Cells Cloud Web API – تحويل ورقة العمل إلى HTML"
second_title: "مستند"
ArticleTitle: "كيفية تحويل ورقة عمل إلى HTML باستخدام واجهة Aspose.Cells Cloud API"
linktitle: "تحويل ورقة العمل إلى HTML"
type: docs
url: /ar/convert-worksheet-to-html/
description: "تعرّف على كيفية تحويل ورقة عمل Excel إلى HTML باستخدام واجهة Aspose.Cells Cloud API – بدون رفع ملفات، مع دعم الخطوط المخصّصة، والمناطق، ومعالجة الأخطاء."
keywords: "Aspose.Cells، تحويل Excel إلى HTML، تحويل ورقة العمل، واجهة سحابية"
weight: 100
---

يقوم endpoint **ConvertWorksheetToHtml** بقراءة ملف مصنف Excel من نظام الملفات المحلي، واستخراج ورقة العمل المحدّدة، وإرجاع المحتوى كملف HTML. ويتم تنفيذ التحويل بالكامل على خوادم Aspose السحابية، لذا لا يتطلّب رفعًا مبدئيًا أو تخزينًا مؤقتًا. وهو مثالي لإنشاء عروض جاهزة للويب لبيانات جداول البيانات، ويدعم مسارات الإخراج الاختيارية، والخطوط المخصّصة، وإعدادات المناطق، والمصنفات المحمية بكلمة مرور.

## واجهة تحويل ورقة العمل إلى HTML

### واجهة الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **الأمان والمصادقة**

تتطلّب واجهات برمجة تطبيقات Aspose.Cells Cloud أمانًا عاليًا وتتطلّب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب

| اسم المعامل | النوع | الموقع | إجباري/اختياري | الوصف |
| :---------- | :---- | :----- | :-------------- | :----- |
| Spreadsheet | ملف | مطلوب | FormData | ملف Excel ثنائي لمعالجته. يجب أن يكون ملفًا صالحًا بامتدادات مثل .xlsx أو .xls أو .xlsb وما إلى ذلك. مثال: `myWorkbook.xlsx`. ويُقرأ ملف Excel مباشرة من جسم الطلب، ولا حاجة لرفعه مسبقًا إلى التخزين السحابي. |
| worksheet | نص | مطلوب | استعلام | اسم ورقة العمل المراد تحويلها (حساس لحالة الأحرف). يجب أن تكون موجودة في المصنف المزوّد. مثال: `Sheet1`. |
| outPath | نص | اختياري | استعلام | مسار المجلد الهدف (في التخزين السحابي) الذي سيتم حفظ ملف HTML الناتج فيه. وإذا تُرك فارغًا، يُعاد الملف مباشرةً في الاستجابة. مثال: `/output/html/`. |
| outStorageName | نص | اختياري | استعلام | اسم خدمة التخزين السحابي المراد استخدامها لمسار الإخراج (`outPath`). يتطلّب فقط عند توجيه `outPath` إلى تخزين غير افتراضي. |
| fontsLocation | نص | اختياري | استعلام | المسار المطلق لمجلد يحتوي على خطوط TrueType/OpenType مخصّصة تُستخدم أثناء التحويل، مما يضمن عرض الأحرف غير القياسية بشكل صحيح. |
| region | نص | اختياري | استعلام | معرّف محلي يؤثّر على تنسيق الأرقام/التواريخ (مثل `en-US` أو `fr-FR`)، ويُستخدم الافتراضي المُعرّف داخليًا في المصنف في حال إهماله. |
| password | نص | اختياري | استعلام | كلمة المرور المطلوبة لفتح مصنف محمي. يُترك فارغًا للملفات غير المحمية. |

### الاستجابة

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

**رموز حالات HTTP**

| الرمز | المعنى | الوصف |
| ---- | ------ | ----- |
| 200 | ناجح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصادق عليه | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقّع في الخادم. |

## أين يجب استخدام واجهة تحويل ورقة العمل إلى HTML؟

- **دمج بيانات جداول البيانات الحية في بوابة ويب** – تحويل ورقة عمل تقرير مالي إلى HTML لعرضها مباشرة في المتصفحات دون الحاجة لإضافات Excel.
- **توليد فواتير HTML قابلة للطباعة من قالب Excel** – أتمتة إنشاء صفحات فواتير جاهزة للويب من ورقة عمل مُعدّة مسبقًا.
- **إنشاء مقاطع وثائقية** – تحويل ورقات مواصفات التصميم إلى مقاطع HTML يمكن إدماجها في الدلائل الفنية أو الويكي.
- **تطوير لوحات تحكم BI منخفضة الكود** – استخراج بيانات ورقة العمل، وتحويلها إلى HTML، وعرضها داخل عناصر واجهة لوحة التحكم المخصّصة.

## لماذا يجب استخدام واجهة تحويل ورقة العمل إلى HTML؟

- **سير عمل بدون رفع** – تحويل الملفات المحلية مباشرةً في السحابة، ما يلغي الحاجة لنقل المصنفات الكبيرة إلى التخزين مسبقًا.
- **عرض عالي الأداء** – يستفيد التحويل من محرك Aspose المُحسّن على الخوادم، ما يضمن إخراج HTML سريعًا ودقيقًا.
- **تحكم كامل في الإخراج** – تسمح المعاملات الاختيارية (الخطوط المخصّصة، المنطقة، كلمة المرور) بتخصيص HTML بما يتوافق مع متطلبات التوطين والهوية البصرية.
- **تكامل سلس** – طلب PUT بسيط مع multipart/form‑data يناسب بيئات سير العمل التلقائي (CI/CD)، أو الميكروسيرفيس (microservices)، أو وظائف serverless.

## كيفية استخدام واجهة تحويل ورقة العمل إلى HTML باستخدام SDKs

### مواصفات واجهة تحويل ورقة العمل إلى HTML

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">مواصفات واجهة تحويل ورقة العمل إلى HTML</a> توفر واجهة برمجة تطبيقات مفتوحة للوصول مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. ويُعرض المثال التالي كيفية إجراء المكالمات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
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

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDKs هو أسرع طريقة للتطوير، إذ يُخفّي التفاصيل منخفضة المستوى، ويسمح لك بدمج ورقات العمل بكود موجز.  
يرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">مستودع GitHub لـ Aspose.Cells Cloud SDK</a> للاطّلاع على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.  
تُظهر أمثلة الكود التالية كيفية التفاعل مع خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}