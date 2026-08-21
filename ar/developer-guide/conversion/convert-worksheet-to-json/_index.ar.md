---
title: "واجهة Aspose.Cells Cloud Web API – تحويل ورقة العمل إلى JSON"
second_title: "وثيقة"
ArticleTitle: "كيفية تحويل ورقة عمل جدول بيانات إلى JSON باستخدام واجهة Aspose.Cells Cloud API"
linktype: "تحويل ورقة عمل إلى JSON"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, تحويل ورقة عمل إلى JSON, تحويل Excel, واجهة سحابية, API v4, تصدير البيانات"
description: "دليل خطوة بخطوة لتحويل ورقة عمل Excel إلى JSON باستخدام واجهة Aspose.Cells Cloud API، بما في ذلك معلمات الطلب، ومعالجة الاستجابة، وأكواد الأخطاء، وأمثلة SDK."
weight: 100
---

يقوم_endpoint_ **ConvertWorksheetToJson** بقراءة ملف جدول البيانات من نظام الملفات المحلي، واستخراج ورقة العمل المحددة، وإرجاع محتواها كملف JSON. ويتم التحويل بالكامل على خوادم Aspose.Cells Cloud، لذا لا يتطلب رفعًا مبدئيًا أو تخزينًا وسيطًا. وتدعم هذه الميزة أوراق العمل المحمية بكلمة مرور، ومواقع الخطوط المخصصة، والإعدادات الإقليمية، مما يقدّم حلاً سريعًا ومُصممًا للسحابة لتصدير بيانات ورقة العمل إلى JSON لمعالجتها في خطوط أنابيب لاحقة.

## **واجهة API لتحويل ورقة العمل إلى JSON**

### واجهة API على الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الطلب:**

| اسم المعلمة | النوع | الموقع | إلزامي/اختياري | الوصف                                                                                                                                                                                            |
| :------------- | :----- | :------- | :---------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | ملف   | FormData | إلزامي          | ملف مصنف Excel المراد معالجته. يجب أن يكون بصيغة مدعومة (مثل xls، xlsx، csv، إلخ). يُرسَل كـ multipart/form-data. مثال: `Spreadsheet=@C:\Docs\Sample.xlsx`.                                       |
| worksheet      | نص    | Query    | إلزامي          | الاسم الدقيق لورقة العمل المراد تحويلها (مع مراعاة حالة الأحرف). إذا حُذفت أو لم يُعثر عليها، تُعيد الواجهة خطأً. مثال: `worksheet=Sheet1`.                                                               |
| outPath        | نص    | Query    | اختياري          | المجلد الوجهة على مساحة التخزين السحابية المُعدة لحفظ ملف JSON الناتج. إن لم يُحدَّد، يُعاد محتوى JSON مباشرةً في تدفق الاستجابة. مثال: `outPath=/converted/`. |
| outStorageName | نص    | Query    | اختياري          | اسم مساحة التخزين المستهدفة (مثل "MyStorage") التي تحتوي على `outPath`. ويُستخدم مساحة التخزين الافتراضية عند حذف هذه المعلمة.                                                                                     |
| fontsLocation  | نص    | Query    | اختياري          | مجلد على الخادم يحتوي على خطوط مخصصة مطلوبة لعرض النصوص في ورقة العمل بدقة. مثال: `fontsLocation=/fonts/custom/`.                                                          |
| region         | نص    | Query    | اختياري          | معرّف ثقافة/منطقة يؤثّر على تنسيق الأرقام والتاريخ والعملات في ملف JSON الناتج (مثل `en-US`، `fr-FR`).                                                                        |
| password       | نص    | Query    | اختياري          | كلمة المرور لفتح مصنف مشفر. إن لم يكن المصنف محميًا بكلمة مرور، يمكن حذف هذه المعلمة.                                                                                                |

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

**أكواد حالة HTTP**

| الكود | المعنى               | الوصف                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | نجاح                 | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح           | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).      |
| 401  | غير مصرّح به          | رمز JWT غير صحيح أو مفقود.                                     |
| 413  | حجم البيانات كبير جدًا     | تجاوز حجم الملف المرفوع الحد المسموح.                                 |
| 500  | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم.                                          |

## أين نستخدم واجهة API لتحويل ورقة العمل إلى JSON؟

- **الوحة القيادية على الويب (Web dashboards)** – تصدير بيانات ورقة العمل إلى JSON لاستخدامها مع مكتبات الرسم البياني من جانب العميل (مثل Chart.js، D3.js).
- **الهجرة البياناتية** – نقل بيانات Excel القديمة إلى قواعد بيانات NoSQL أو خدمات REST التي تستهلك بيانات JSON.
- **تطبيقات الجوال أو غير المتصلة بالإنترنت** – تحويل محتوى ورقة العمل إلى JSON على الخادم، ثم مزامنة البيانات الخفيفة مع أجهزة الجوال.
- **خطوط أنابيب التقرير** – تغذية بيانات ورقة العمل مباشرةً إلى محركات التحليلات التي تقبل إدخال JSON دون الحاجة لخطوات وسيطة بملفات CSV.

## لماذا يجب استخدام واجهة API لتحويل ورقة العمل إلى JSON؟

- **سير عمل بدون رفع مبدئي** – معالجة الملفات المحلية في السحابة دون رفعها أولًا إلى مساحة تخزين، مما يوفر النطاق الترددي وتكاليف التخزين.
- **تحويل شامل الميزات** – يدعم أوراق العمل المحمية بكلمة مرور، والخطوط المخصصة، والتنسيق الإقليمي لتمثيل دقيق للبيانات.
- **تنفيذ سريع وقابل للتوسع** – يستفيد من محرك Aspose.Cells عالي الأداء على البنية التحتية السحابية، ليتعامل بكفاءة مع أوراق العمل الكبيرة.
- **تكامل مبسّط** – استدعاء PUT واحد يُعيد ملف JSON جاهز للاستخدام، أو يحفظه مباشرةً، مما يقلل تعقيد الكود في تطبيقات العميل.

## كيفية استخدام واجهة API لتحويل ورقة العمل إلى JSON باستخدام SDKs

### مواصفات واجهة API لتحويل ورقة العمل إلى JSON

توفّر <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">مواصفات واجهة API لتحويل ورقة العمل إلى JSON</a> واجهة برمجة تطبيقات عامة قابلة للوصول تنفيذ تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة API السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

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
  "fileContents": "byte[] (Base64 encoded)",
  "contentType": "MIME type",
  "fileDownloadName": "optional file name"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDKs هو أسرع طريقة للتطوير، لأنها تُجرّدك من التفاصيل منخفضة المستوى وتمكّنك من العمل مع جداول البيانات عبر كود موجز. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.  
تُظهر أمثلة الكود التالية كيفية التفاعل مع خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}