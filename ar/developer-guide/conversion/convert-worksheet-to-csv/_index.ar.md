---
title: "تحويل ورقة عمل إلى CSV – وثائق واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
ArticleTitle: "كيفية تحويل ورقة عمل في ملف جدول بيانات إلى CSV باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
linktype: "تحويل ورقة عمل إلى CSV"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells، تحويل CSV، تحويل ورقة عمل إلى CSV، واجهة برمجة تطبيقات REST، جدول بيانات في السحابة، Excel إلى CSV"
description: "تعرّف على كيفية تحويل ورقة عمل معيّنة من ملف Excel إلى CSV باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud (الإصدار 4.0). يتضمن الرابط_endpoint_، المُعاملات، مثال cURL، كود SDK، ومعالجة الأخطاء."
weight: 100
---

يحوّل **endpoint_ConvertWorksheetToCsv** ورقة عمل واحدة من ملف جدول بيانات محلي إلى مستند CSV بالكامل على خوادم Aspose.Cells Cloud. وبفضل رفع الملف المصدر وتحديد ورقة العمل المستهدفة، يحصل المطوّرون على تدفق ثنائي لملف CSV دون الحاجة إلى حفظ الملف في تخزين سحابي. وتُعدّ هذه الواجهة المثالية لأتمتة استخراج البيانات، ودمج بيانات جداول البيانات في الأنظمة اللاحقة، وتقليل التكاليف المرتبطة بالتخزين.

## واجهة برمجة تطبيقات تحويل ورقة عمل إلى CSV

### واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **الأمان والمصادقة**

تتوفّر واجهات برمجة تطبيقات Aspose.Cells Cloud بأمان، وتتطلّب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### مُعاملات الطلب

| اسم المُعامل | النوع | الموقع | إلزامي/اختياري | الوصف |
| :------------- | :----- | :------- | :---------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet | ملف | FormData | **إلزامي** | ملف ثنائي لجدول البيانات المصدر (مثل `.xlsx`، `.xls`). مثال: `myWorkbook.xlsx`. |
| worksheet | سلسلة نصية | Query | **إلزامي** | اسم ورقة العمل المراد تحويلها (حالة حساسة). إذا تُرك فارغًا، تُستخدم الورقة الأولى. مثال: `Sheet1`. |
| outPath | سلسلة نصية | Query | اختياري | مسار المجلد المستهدف في التخزين السحابي حيث يُحفظ ملف CSV الناتج. إذا تُرك فارغًا، يُعاد ملف CSV مباشرة في تدفق الاستجابة. |
| outStorageName | سلسلة نصية | Query | اختياري | اسم خدمة التخزين (مثل Azure، AWS S3) حيث يجب وضع ملف الإخراج. مطلوب فقط عند استخدام `outPath`. |
| fontsLocation | سلسلة نصية | Query | اختياري | مسار مجلد الخطوط المخصصة على الخادم، مما يتيح لمحرك التحويل استخدام خطوط غير قياسية. |
| region | سلسلة نصية | Query | اختياري | معرّف محلي يؤثّر في تنسيق الأرقام/التاريخ في ملف CSV (مثل `en-US`، `fr-FR`). |
| password | سلسلة نصية | Query | اختياري | كلمة المرور لفتح جدول بيانات محمي. يجب أن تتطابق مع كلمة مرور التشفير للملف المصدر. |

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

| الرمز | المعنى | الوصف |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | ناجح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح | مُعطَلات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401  | غير مُصادَق عليه | رمز JWT غير صالح أو مفقود. |
| 413  | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500  | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## متى تستخدم واجهة برمجة تطبيقات تحويل ورقة عمل إلى CSV؟

- **استخراج البيانات لخطوط أنابيب تحليل الأعمال (BI)** – استخراج ورقة عمل محددة من تقرير Excel وإرسال ملف CSV الناتج مباشرة إلى Power BI أو Tableau دون الحاجة إلى معالجة الملفات الوسيطة.
- **معالجة الفواتير بشكل آلي** – تحويل ورقة العمل التي تحتوي على صفوف الفواتير إلى CSV لاستيرادها سريعًا في أنظمة المحاسبة.
- **دمج مع أنظمة قديمة** – تصدير بيانات ورقة العمل إلى CSV للاستهلاك من قبل تطبيقات أقدم لا تقبل سوى ملفات النصوص المفصولة بفاصل.
- **توليد التقارير لحظيًا** – إنشاء لقطات CSV لبيانات جدول البيانات الحية في خدمة ويب، وإعادة الملف فورًا إلى متصفح العميل.

## لماذا تستخدم واجهة برمجة تطبيقات تحويل ورقة عمل إلى CSV؟

- **لا يتطلب تخزينًا سحابيًا دائمًا** – يُمرّر الملف مباشرةً إلى محرك التحويل ويُحذف بعد التحويل، مما يوفّر النطاق الترددي وتكاليف التخزين.
- **تنفيذ عالي الأداء في السحابة** – يعمل التحويل على خوادم Aspose المُحسَّنة، وغالبًا ما يكتمل خلال ثانيتين فقط للملفات التي تصل إلى 100 ميغابايت.
- **تحكم دقيق** – اختيار ورقة عمل واحدة، وتطبيق خطوط مخصصة، وتنسيق إقليمي، وحماية بكلمة مرور في طلب واحد.
- **إخراج متسق عبر منصات مختلفة** – يضمن إخراج CSV متطابق عبر SDKs مختلفة مثل .NET وJava وPython وغيرها باستخدام نفس endpoint_واجهة REST.

## كيف تستخدم واجهة برمجة تطبيقات تحويل ورقة عمل إلى CSV باستخدام حزم تطوير البرمجيات (SDKs)؟

### مواصفات واجهة برمجة تطبيقات تحويل ورقة عمل إلى CSV

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات تحويل ورقة عمل إلى CSV</a> توفر واجهة برمجة برمجية متاحة علنًا لتنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

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

### استخدام حزم تطوير البرمجيات (SDKs) الخاصة بـ Aspose.Cells Cloud

يسهّل استخدام SDK تبسيط التطوير من خلال إخفاء التفاصيل من المستوى المنخفض، مما يتيح لك دمج جدول بيانات في جدول بيانات آخر باستخدام كود موجز. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية التفاعل مع خدمات Aspose.Cells عبر الويب باستخدام مكتبات SDK مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}