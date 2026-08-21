---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud عبر الويب – تحويل بيانات جدول إكسل محلي إلى ملف JSON"
second_title: "وثيقة"
ArticleTitle: "كيفية تحويل بيانات جدول جدول البيانات المحلي إلى ملف JSON: دليل خطوة بخطوة"
linktype: "تحويل الجدول إلى JSON"
type: docs
url: /convert-table-to-json/
keywords: "إكسل، واجهة برمجة تطبيقات، JSON، تحويل، سحابة، ملف، جدول بيانات"
description: "استخدم واجهة برمجة تطبيقات Aspose.Cells Cloud لتحويل جدول إكسل محلي إلى ملف JSON في طلب PUT واحد. يشمل مثالًا باستخدام cURL، والمُعطَلات، ومقتطفات SDK للغات C#، Java، Python، والمزيد."
weight: 100
---

قم بتحويل جدول جدول البيانات/إكسل المحلي إلى ملف **JSON** باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud عبر الويب.

## **واجهة برمجة تطبيقات تحويل الجدول إلى JSON**

### واجهة برمجة تطبيقات الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### مُعطَلات الطلب

| اسم المُعطَل         | النوع   | الموقع        | الوصف                                                                                      |
| ------------------ | ------ | ------------- | ------------------------------------------------------------------------------------------ |
| **جدول البيانات**    | ملف   | FormData      | ملف إكسل المراد تحميله.                                                                    |
| **worksheet**      | سلسلة نصية | استعلام       | اسم ورقة العمل التي تحتوي على الجدول.                                                       |
| **tableName**      | سلسلة نصية | استعلام       | اسم الجدول المراد تحويله.                                                                  |
| **outPath**        | سلسلة نصية | استعلام       | (اختياري) مسار المجلد الذي سيتم فيه تخزين ملف JSON الناتج؛ القيمة الافتراضية هي **null**. |
| **outStorageName** | سلسلة نصية | استعلام       | (اختياري) اسم وحدة التخزين التي سيتم وضع ملف الإخراج فيها.                                |
| **fontsLocation**  | سلسلة نصية | استعلام       | (اختياري) مسار الخطوط المخصصة المستخدمة أثناء التحويل.                                    |
| **region**         | سلسلة نصية | استعلام       | (اختياري) الإعدادات الإقليمية لكتاب العمل.                                                |
| **password**       | سلسلة نصية | استعلام       | (اختياري) كلمة المرور لفتح كتاب عمل محمي.                                                 |

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

| الرمز | المعنى                 | الوصف                                                                 |
| ---- | ---------------------- | --------------------------------------------------------------------- |
| 200  | نجاح (OK)              | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.          |
| 400  | طلب غير صالح (Bad Request) | مُعطَلات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).               |
| 401  | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود.                                          |
| 413  | حملة الطلب كبيرة جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.                            |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                             |

## **أين يجب استخدام واجهة برمجة تطبيقات تحويل الجدول إلى JSON؟**

- **لوحات التحكم في الوقت الفعلي** – حوّل بيانات إكسل الحية إلى JSON لاستخدامها في مكتبات الرسم البياني مثل Chart.js أو D3.js.
- **جدول البيانات كخدمة (Spreadsheet-as-a-Service)** – عرّض جداول إكسل كنقاط نهاية JSON لخدمات ميكرو-خدمات أخرى.
- **أحمال Webhook** – حوّل بيانات جدول البيانات إلى JSON لإشعارات Webhook.
- **نماذج البيانات السريعة (Rapid Data Prototyping)** – حوّل بيانات إكسل المنظمة بسرعة إلى JSON لتحليلها باستخدام Python أو R.
- **أنابيب التعلم الآلي (Machine-Learning Pipelines)** – قم بمعالجة مسبق لبيانات التدريب المخزّنة في جداول بيانات الأعمال.
- **عمليات التجارة الإلكترونية (E-commerce Operations)** – زامن قوائم المنتجات أو أوراق الأسعار مع المواقع عبر JSON.
- **أتمتة التقارير (Reporting Automation)** –ولّد تغذّيات JSON من نماذج مالية لتقارير آلية.
- **تكوين التطبيقات (App Configuration)** – أدر أعلام الميزات والإعدادات أو معلمات اختبارات A/B في إكسل → JSON.
- **الدعم متعدد اللغات (Multi-language Support)** – حوّل جداول البيانات الخاصة بالترجمة إلى JSON لمكتبات التدويل (i18n).
- **قوائم/تنقل ديناميكي (Dynamic Menus/Navigation)** – خزّن هياكل التنقل في الموقع في إكسل ونفّذها كملفات JSON.

## لماذا يجب استخدام واجهة برمجة تطبيقات تحويل الجدول إلى JSON؟

- **سهلة المطورين (Developer-Friendly)** – توفر Aspose.Cells Cloud SDKs للعديد من اللغات، مما يقلل من جهود التطوير ويقدم توثيقًا شاملاً.
- **فعالة من حيث التكلفة (Cost-Effective)** – حوّل بيانات الجدول دون الحاجة أولاً لتحميل كتاب العمل، مما يوفر مساحة تخزين ويقلل التكاليف.
- **متوافقة مع الويب والجوّال الحديثة (Modern Web & Mobile Compatibility)** – JSON هي لغة البيانات الأصلية للويب؛ تتيح لك واجهة البرمجة هذه تغذية بيانات جدول البيانات الحية مباشرةً في React أو Vue أو Angular أو تطبيقات الجوال أو تطبيقات الصفحة الواحدة دون تحليل معقد.
- **دعم واسع للغات (Broad Language Support)** – يعمل JSON مع تقريب جميع لغات البرمجة وقواعد البيانات وخدمات الويب.
- **الحفاظ على هيكلية البيانات (Structured Data Preservation)**
  - **كشف تلقائي للهيكل (Intelligent Structure Detection)** – يحول بيانات الجدول تلقائيًا إلى مصفوفات/كائنات JSON صحيحة.
  - **ربط الرؤوس (Header Mapping)** – يستخدم الصف الأول كمفاتيح JSON لهياكل الكائنات النظيفة.
  - **الحفاظ على أنواع البيانات (Data Type Retention)** – يحافظ على الأرقام والتاريخ والقيم المنطقية (وليس فقط النصوص).

_سجل الإصدارات:_ تم إدخال نقطة نهاية تحويل الجدول إلى JSON مع إصدار واجهة برمجة التطبيقات **v4.0** (2024)، ويبقى هو الإصدار المستقر الحالي. نقاط نهاية الإصدارات الأقدم v3.x لم تعد مستخدمة (مُهمَلة).

## كيف تستخدم واجهة برمجة تطبيقات تحويل الجدول إلى JSON مع SDKs؟

### مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى JSON

توفر [مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} واجهة برمجة تطبيقات قابلة للوصول للعامة، مما يمكّن من إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
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

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDK يُجرّد التفاصيل من المستوى المنخفض، مما يسمح لك بتحويل جدول جدول البيانات إلى ملف JSON بحد أدنى من الكود. راجع مستودع GitHub الرسمي للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية التفاعل مع خدمات ويب Aspose.Cells باستخدام مختلف SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}