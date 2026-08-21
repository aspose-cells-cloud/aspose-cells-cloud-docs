---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud عبر الويب - تحويل بيانات جدول في جدول بيانات إلى ملف CSV - أداة مجانية عبر الإنترنت"
second_title: "وثيقة"
ArticleTitle: "كيفية تحويل بيانات جدول الجداول إلى ملف CSV: دليل خطوة بخطوة"
linktype: "تحويل الجدول إلى CSV"
type: docs
url: /ar/convert-table-to-csv/
keywords: "Aspose.Cells Cloud, تحويل جدول إلى CSV, تحويل جداول بيانات, Excel إلى CSV, واجهة برمجة تطبيقات, REST, تصدير البيانات"
description: "قم بتحويل جدول من ملف جدول بيانات Excel إلى ملف CSV بسرعة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud."
weight: 100
---

تصدير بيانات الجدول من ملف Excel محلي إلى ملف CSV باستخدام واجهة برمجة التطبيقات السحابية.

## **واجهة برمجة تطبيقات تحويل الجدول إلى CSV**

### واجهة برمجة التطبيقات عبر الويب

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **الأمان والمصادقة**

تُعتبر واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **مُعاملات الطلب:**

| اسم المُعامل | النوع | المسار / سلسلة الاستعلام / جسم الطلب HTTP | الوصف |
| --- | --- | --- | --- |
| Spreadsheet | ملف | FormData | رفع ملف جدول البيانات. |
| worksheet | سلسلة نصية | سلسلة الاستعلام | اسم ورقة العمل داخل جدول البيانات. |
| tableName | سلسلة نصية | سلسلة الاستعلام | اسم الجدول المراد تحويله. |
| outPath | سلسلة نصية | سلسلة الاستعلام | (اختياري) مسار المجلد الذي يُخزَّن فيه المصنف؛ القيمة الافتراضية هي null. |
| outStorageName | سلسلة نصية | سلسلة الاستعلام | اسم وحدة التخزين التي سيتم حفظ ملف الإخراج فيها. |
| fontsLocation | سلسلة نصية | سلسلة الاستعلام | مسار استخدام الخطوط المخصصة. |
| region | سلسلة نصية | سلسلة الاستعلام | إعداد منطقة/لغة جدول البيانات (مثل `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام، وتحليل التواريخ، والسلوك الخاص باللغة والمنطقة. |
| password | سلسلة نصية | سلسلة الاستعلام | كلمة المرور لفتح ملف جدول البيانات. |

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
| --- | --- | --- |
| 200 | ناجح | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | مُعاملات ناقصة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُصادَق عليه | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | ملف التحميل يتجاوز الحد الأقصى للحجم. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## **أين يجب عليك استخدام واجهة برمجة تطبيقات تحويل الجدول إلى CSV؟**

- **الترحيل إلى قواعد البيانات**: تحويل جداول Excel إلى CSV لاستيرادها دفعة واحدة إلى قواعد بيانات SQL (MySQL، PostgreSQL، SQL Server).
- **تحميل مخازن البيانات**: تحويل جداول التقارير المستندة إلى Excel إلى CSV لتحميلها في Snowflake أو Redshift أو BigQuery.
- **حمولة دفعات واجهات برمجة التطبيقات**: تحويل بيانات جدول Excel إلى CSV لرفعها دفعة واحدة إلى خدمات REST.
- **الاتصال بين الخدمات**: استخدام CSV كصيغة خفيفة لتبادل البيانات بين الخدمات الدقيقة.
- **تحضير البيانات لتعلم الآلة**: تحويل جداول الميزات من Excel إلى CSV لاستخدامها مع مكتبات تعلم الآلة بلغتي Python أو R.
- **التحليل الإحصائي**: تحويل جداول بيانات البحث إلى CSV لاستيرادها في SPSS أو SAS أو Stata.
- **ترحيل المحتوى**: نقل المحتوى المنظم من Excel إلى أنظمة إدارة المحتوى (CMS) عبر CSV.

## لماذا يجب عليك استخدام واجهة برمجة تطبيقات تحويل الجدول إلى CSV؟

- **سهلة للمطورين**: توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، ما يُسرّع التطوير، وت伴随ها وثائق شاملة. ومقارنةً ببناء حلول مخصصة، فإنها تقلّل بشكل كبير من جهد التطوير.
- **فعالة من حيث التكلفة**: يمكنك تحويل بيانات الجدول دون الحاجة أولاً لتحميل المصنف، ما يوفر مساحة تخزين ويقلل التكاليف.
- **استخراج البيانات النقي فقط دون التنسيق**.
- **CSV مدعوم من قبل تقريبًا جميع الأنظمة**:
  - قواعد البيانات (كل أنظمة قواعد البيانات العلائقية الرئيسية)
  - لغات البرمجة (مُحللات أصلية مدمجة في كل لغة)
  - أدوات ذكاء الأعمال (Tableau، Power BI، Looker)
  - برامج جداول البيانات (Excel، Google Sheets، LibreOffice)
  - أدوات سطر الأوامر (awk، sed، grep)

## كيف تستخدم واجهة برمجة تطبيقات تحويل الجدول إلى CSV باستخدام مكتبات SDK؟

### مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى CSV

توفر [مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV) واجهة برمجة تطبيقات متاحة للعامة، ما يسمح بإجراء تفاعلات REST مباشرة من متصفح ويب.
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
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

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، حيث يُجرّدك من التفاصيل منخفضة المستوى، ويسمح لك بتحويل بيانات جدول الجداول إلى ملف CSV باستخدام كود بسيط جدًا. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مكتبات SDK مختلفة:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}