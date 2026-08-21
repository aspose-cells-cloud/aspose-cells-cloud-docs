---
title: "تصدير نطاق Excel إلى PDF أو PNG أو CSV – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second title: "وثيقة"
ArticleTitle: "كيفية تصدير نطاق جدول بيانات موجود في السحابة إلى تنسيقات أخرى: دليل خطوة بخطوة"
linktitle: "تصدير النطاق كتنسيق"
type: docs
url: /ar/export-range-as-format/
keywords: "Aspose Cells، تصدير نطاق Excel، PDF، PNG، CSV، واجهة برمجة تطبيقات السحابة، تحويل جداول البيانات"
description: "تعرّف على كيفية تحويل نطاق Excel محدّد موجود في Aspose Cells Cloud إلى تنسيقات مثل PDF أو PNG أو CSV أو تنسيقات أخرى. يشمل التفاصيل الخاصة بنقطة النهاية (endpoint)، والمُعاملات (parameters)، وطلبات مثال، ومعالجة الاستجابات، ومعلومات الأخطاء."
weight: 100
---

تصدير نطاق جدول بيانات (أو Excel) الموجود في السحابة إلى ملف بتنسيق معيّن. يمكن حفظ ملف التنسيق في السحابة أو تصديره إلى التخزين المحلي.

## واجهة برمجة تطبيقات تصدير النطاق كتنسيق

### واجهة برمجة التطبيقات عبر الويب (Web API)

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **الأمن والمصادقة**

واجهات برمجة التطبيقات (APIs) الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### مُعاملات الطلب (Request Parameters)

| اسم المُعامل         | النوع   | الموقع   | الوصف                                                                                                                                             |
| :------------------ | :----- | :------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**            | سلسلة نصية (String) | المسار (Path) | (إجباري) اسم ملف المصنف (workbook) المطلوب استرجاعه.                                                                                             |
| **worksheet**       | سلسلة نصية (String) | المسار (Path) | اسم ورقة العمل في جدول البيانات.                                                                                                                  |
| **range**           | سلسلة نصية (String) | المسار (Path) | النطاق المراد تحويله (مثال: `A1:C12`).                                                                                                            |
| **format**          | سلسلة نصية (String) | استعلام (Query) | (إجباري) تنسيق الإخراج المطلوب (مثال: `pdf`، `png`، `svg`).                                                                                        |
| **folder**          | سلسلة نصية (String) | استعلام (Query) | (اختياري) مسار المجلد الذي يحتوي على المصنف.                                                                                                      |
| **storageName**     | سلسلة نصية (String) | استعلام (Query) | (اختياري) اسم التخزين في حال استخدام تخزين سحابي مخصص.                                                                                            |
| **outPath**         | سلسلة نصية (String) | استعلام (Query) | (اختياري) مسار ملف الإخراج في التخزين السحابي.                                                                                                    |
| **outStorageName**  | سلسلة نصية (String) | استعلام (Query) | (اختياري) اسم التخزين المُستخدم لملف الإخراج.                                                                                                      |
| **fontsLocation**   | سلسلة نصية (String) | استعلام (Query) | (اختياري) موقع خطوط مخصصة.                                                                                                                         |
| **region**          | سلسلة نصية (String) | استعلام (Query) | (اختياري) إعداد المنطقة/اللغة لجدول البيانات (مثال: `en-US`، `fr-FR`). يؤثّر على تنسيق الأرقام، وتحليل التواريخ، والسلوك المرتبط بالمنطقة.        |
| **password**        | سلسلة نصية (String) | استعلام (Query) | (اختياري) كلمة المرور المطلوبة لفتح ملف جدول البيانات.                                                                                            |

### الاستجابة (Response)

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

| الرمز | المعنى                  | الوصف                                                             |
| ----- | ----------------------- | ----------------------------------------------------------------- |
| 200   | OK (تم بنجاح)           | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.      |
| 400   | Bad Request (طلب خاطئ)  | مُعاملات مفقودة أو غير صالحة (مثال: نوع ملف غير مدعوم).           |
| 401   | Unauthorized (غير مُصادَق) | رمز JWT غير صالح أو مفقود.                                       |
| 413   | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به.                         |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                         |

## أين يجب استخدام واجهة برمجة تطبيقات تصدير النطاق إلى تنسيق آخر؟

### سيناريوهات تصدير البيانات والنقل (Data Export & Migration)

- **دمج مع قواعد البيانات (Database Integration)** – تصدير نطاقات Excel محددة مباشرةً إلى أنظمة قواعد البيانات.
- **دمج مع التطبيقات (Application Integration)** – إمداد تطبيقات SaaS ببيانات جدول البيانات المحددة.
- **الترحيل بين الأنظمة (System Migration)** – نقل نطاقات بيانات محددة بين الأنظمة القديمة والحديثة.
- **المشاركة عبر منصات مختلفة (Cross‑Platform Sharing)** – مشاركة مجموعات فرعية من البيانات المحددة عبر منصات متنوعة.

### التقارير والتحليلات (Reporting & Analytics)

- **التقارير المُوجّهة (Targeted Reporting)** – تصدير أقسام تقارير محددة إلى تنسيقات أخرى لتحليل مركّز.
- **تغذية بيانات لوحة التحكم (Dashboard Data Feeds)** – تزويد أدوات لوحات تحكم BI بنطاقات بيانات محددة.
- **مقاييس الأداء (Performance Metrics)** – استخراج نطاقات KPI لأنظمة مراقبة الأداء.
- **التقارير المالية (Financial Reporting)** – تصدير أقسام البيانات المالية لغرض التدقيق الخارجي.

### التطوير والاختبار (Development & Testing)

- **إدارة بيانات الاختبار (Test Data Management)** – تصدير نطاقات بيانات محددة لأغراض الاختبار.
- **بيئات التطوير (Development Environments)** – مشاركة نطاقات بيانات مثال مع فرق التطوير.
- **اختبار واجهة برمجة التطبيقات (API Testing)** – إنشاء بيانات اختبار بصيغة CSV من أقسام محددة من جدول البيانات.
- **تطوير النماذج الأولية (Prototype Development)** – توفير مجموعات بيانات مركّزة لنماذج التطبيقات الأولية.

### العمليات التجارية (Business Operations)

- **مشاركة بيانات انتقائية (Selective Data Sharing)** – مشاركة نطاقات بيانات محددة مع شركاء خارجيين.
- **نسخ احتياطي جزئي للبيانات (Partial Data Backup)** – النسخ الاحتياطي ل نطاقات بيانات حرجة بصيغة محددة.
- **نقل البيانات بين الإدارات (Departmental Data Transfer)** – مشاركة نطاقات بيانات محددة بين الإدارات المختلفة.
- **التقارير الامتثالية (Compliance Reporting)** – تصدير نطاقات بيانات تنظيمية لأغراض تقديم تقارير الامتثال.

### سير العمل الآلي (Automation Workflows)

- **تصدير النطاقات المجدولة (Scheduled Range Exports)** – تصدير نطاقات محددة تلقائيًا وفق جدول زمني.
- **الاستخراج المُحفَّز بالحدث (Trigger‑Based Extraction)** – تصدير النطاقات استنادًا إلى أحداث أو مُحفّزات تجارية.
- **دمج تصدير النطاقات في سير العمل (Workflow Integration)** – دمج عمليات تصدير النطاقات في سير العمل للعمليات التجارية.
- **المعالجة الدُفعية للنطاقات (Batch Range Processing)** – معالجة نطاقات محددة متعددة في عمليات دفعية.

## لماذا يجب استخدام واجهة برمجة تطبيقات تصدير النطاق إلى تنسيق آخر؟

- **سهلة الاستخدام للمطورين (Developer‑Friendly)** – توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يتيح تطويرًا سريعًا مع توفر وثائق شاملة. ومقارنةً ببناء حلول مخصصة لعرض الرسوم البيانية، فإنها تقلّل بشكل كبير من جهد التطوير المطلوب.
- **خفض تكاليف العمالة (Reduced Labor Costs)** – الحاجة الأقل إلى الموظفين المخصصين لدمج الوثائق.
- **دفع مقابل الاستخدام فقط (Pay‑per‑Use)** – لا استثمار مبدئي؛ تدفع فقط مقابل طلبات واجهة برمجة التطبيقات التي تستخدمها فعلًا.
- **لا صيانة للخوادم (No Server Maintenance)** – لا خوادم مطلوب صيانتها، ولا تحديثات برمجيات، ولا مشاكل توافق.
- **الحفاظ على تنسيقات Excel المعقدة (Preserves Complex Excel Formatting)** – تحافظ ملفات الإخراج على التنسيق الأصلي لجدول البيانات.

## كيفية استخدام واجهة برمجة تطبيقات تصدير نطاق جدول البيانات كتنسيق باستخدام مكتبات SDK؟

### مواصفات واجهة برمجة تطبيقات تصدير النطاق كتنسيق

توفر <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات تصدير النطاق كتنسيق</a> واجهة برمجة تطبيقات قابلة للوصول علنًا، مما يتيح التفاعل عبر REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إرسال طلبات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 مشفرة)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، نظرًا لأنها تُجرّدك من التفاصيل من المستوى المنخفض، مما يتيح لك تصدير نطاق جدول البيانات إلى ملف بصيغة محددة عبر كود موجز. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}