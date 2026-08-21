---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud عبر الويب – تحويل جداول البيانات إلى JSON"
second_title: "مستند"
ArticleTitle: "كيفية تحويل جدول بيانات محلي إلى JSON باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
linktype: "تحويل جدول البيانات إلى JSON"
type: docs
url: /ar/convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud، تحويل جدول البيانات إلى JSON، API تحويل Excel إلى JSON، واجهة برمجة تطبيقات Aspose.Cells Cloud، REST API، تحويل جداول البيانات"
description: "تعرّف على كيفية تحويل ملفات Excel المحلية إلى تنسيق JSON باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. يتضمن الـ Endpoint، والمعاملات، وعينات من الكود، وإدارة الأخطاء لدمج سلس."
weight: 100
---

يحوّل الـ **Endpoint** **ConvertSpreadsheetToJson** جدول بيانات مخزّن على محرك أقراص محلي إلى ملف JSON بالكامل على خوادم خدمة Aspose.Cells Cloud. وبإرسال جدول البيانات كـ `multipart/form-data`، تُرجع الخدمة تدفق JSON جاهزًا للتنزيل أو المعالجة اللاحقة. ويُلغي هذا التحويل القائم على السحابة الحاجة إلى رفع الملف إلى التخزين مسبقًا، ويقلّل من تكاليف التخزين، ويبسّط سير العمل للتطبيقات التي تتطلب بيانات جداول البيانات بصيغة JSON لأغراض التحليل، أو التقارير، أو تبادل البيانات.

**المتطلبات الأساسية**: يجب أن تمتلك حسابًا في Aspose Cloud، ورمز وصول JWT صالحًا، وتم إعداد SDK أو مفتاح API لخدمة Aspose.Cells Cloud.

**الخلفية**: يُعد تحويل جداول البيانات إلى تنسيق JSON خطوة شائعة عند دمج بيانات Excel مع خدمات الويب، أو قواعد بيانات NoSQL، أو تطبيقات JavaScript من جانب العميل. وتوفّر واجهة برمجة تطبيقات تحويل جدول البيانات إلى JSON تحويلًا سريعًا من جانب الخادم دون الحاجة إلى تخزين الملف الأصلي.

## واجهة برمجة تطبيقات تحويل جدول البيانات إلى JSON

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **الأمان والمصادقة**

تُعد واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز JWT</a>.

### معاملات الطلب

| اسم المعامل         | النوع                       | الموقع    | إلزامي/اختياري | الوصف                                                                                                                                                                     |
| :----------------- | :------------------------- | :------- | :-------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet        | ملف (multipart/form-data)  | FormData | إلزامي          | ملف جدول البيانات المصدر (مثل: `.xls`، `.xlsx`، `.xlsm`). مثال: `curl -F "Spreadsheet=@myfile.xlsx"`                                                                           |
| outPath            | سلسلة نصية (String)        | Query    | اختياري         | مسار المجلد الهدف في التخزين السحابي حيث سيتم حفظ ملف JSON المحول. إذا تُرك فارغًا، يُعاد JSON مباشرةً في تدفق الاستجابة. مثال: `outPath=/output/`. |
| outStorageName     | سلسلة نصية (String)        | Query    | اختياري         | اسم خدمة التخزين السحابي (مثل: Amazon S3، Azure Blob) حيث يجب كتابة ملف الإخراج. مطلوب فقط عند استخدام `outPath` مع تخزين غير افتراضي.               |
| fontsLocation      | سلسلة نصية (String)        | Query    | اختياري         | مسار مجلد خطوط مخصص على الخادم. استخدم هذا الخيار عندما يشير جدول البيانات إلى خطوط غير متوفرة في المكتبة الافتراضية.                                      |
| region             | سلسلة نصية (String)        | Query    | اختياري         | إعداد منطقة/لغة جدول البيانات (مثل: `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام والتواريخ والعملات أثناء التحويل.                                               |
| password           | سلسلة نصية (String)        | Query    | اختياري         | كلمة المرور لفتح جدول بيانات محمي بكلمة مرور. تجاهله للملفات غير المحمية.                                                                                                  |

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

**رموز حالة HTTP**

| الرمز | المعنى               | الوصف                                                       |
| ---- | -------------------- | ----------------------------------------------------------- |
| 200  | نجاح (OK)            | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل: نوع ملف غير مدعوم).      |
| 401  | غير مُصادَق (Unauthorized) | رمز JWT غير صالح أو مفقود.                                     |
| 413  | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح.                                 |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                          |

## أين يجب استخدام واجهة برمجة تطبيقات تحويل جدول البيانات إلى JSON؟

- **خطوط أنابيب نقل البيانات (Data migration pipelines)** – تحويل تقارير Excel القديمة إلى تنسيق JSON لاستهلاكها في قواعد بيانات NoSQL الحديثة أو بحيرات البيانات.
- **التطبيقات المحمولة أو الويب** – تحويل جداول البيانات التي يُرفعها المستخدم بسرعة إلى تنسيق JSON لعرضها من جانب العميل دون تخزين الملف الأصلي في السحابة.
- **توليد التقارير تلقائيًا** – إنشاء حمولات JSON لخدمات التحليل اللاحقة (مثل: Power BI، Tableau) مباشرةً من مدخلات جداول البيانات.
- **الوظائف بدون خادم (Serverless functions)** – استخدام الواجهة داخل AWS Lambda أو Azure Functions لأداء عمليات تحويل فورية دون إدارة تخزين مؤقت.

## لماذا يجب استخدام واجهة برمجة تطبيقات تحويل جدول البيانات إلى JSON؟

- التحويل القائم على السحابة يلغي الحاجة إلى رفع ملفات كبيرة إلى التخزين قبل المعالجة، مما يقلل من زمن الاستجابة وتكاليف التخزين.
- سير عمل مكوّن من طلب واحد: رفع جدول البيانات واستلام JSON في نفس استدعاء HTTP، مما يبسّط منطق الدمج.
- يدعم جداول البيانات المحمية بكلمة مرور والجداول المخصصة للمناطق، مما يضمن تمثيلًا دقيقًا للبيانات عبر المناطق المختلفة.
- قابل للتحجيم على بنية Aspose الأساسية – يتعامل مع كتب عمل كبيرة ومعادلات معقدة دون التأثير على موارد خادمك.

## كيفية استخدام واجهة برمجة تطبيقات تحويل جدول البيانات إلى JSON باستخدام SDKs

### مواصفات واجهة برمجة تطبيقات تحويل جدول البيانات إلى JSON

توفر [مواصفات واجهة برمجة تطبيقات تحويل جدول البيانات إلى JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson) واجهة برمجة تطبيقات قابلة للوصول بشكل عام لتنفيذ تفاعلات REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، حيث يُخفي التفاصيل من المستوى المنخفض ويجعلك قادرًا على تحويل جدول بيانات إلى JSON باستخدام بضع سطور من الكود.  
يرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.  
تُظهر أمثلة الكود التالية كيفية التفاعل مع خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}