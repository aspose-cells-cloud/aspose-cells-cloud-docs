---
title: "إنشاء API جدول بيانات – Aspose.Cells Cloud (الإصدار 5.0) | إنشاء ملفات Excel"
second_title: "مستند"
ArticleTitle: "كيفية إنشاء جداول بيانات Excel جديدة – توليد ملفات فارغة أو مبنية على قوالب"
linktype: "create-spreadsheet/"
type: docs
url: /ar/create-spreadsheet/
keywords: "Aspose.Cells، API جدول البيانات، إنشاء Excel، السحابة، XLSX، ODS، CSV، قالب، SDK، أتمتة"
description: "تعرّف على كيفية إنشاء كتب عمل Excel فارغة أو مبنية على قوالب باستخدام API Aspose.Cells Cloud (الإصدار 5.0). يتضمن الرابط_endpoint_، المُعاملات، رموز الأخطاء، خطوات المصادقة، وأمثلة SDK."
weight: 100
---

قم بإنشاء جداول بيانات Excel جديدة برمجيًا باستخدام API Aspose.Cells Cloud. قم بتوليد كتب عمل فارغة أو أنشئ ملفات من قوالب مخصصة. تتيح واجهة RESTful إنشاء ملفات Excel تلقائيًا، وهي مثالية لعملية إنشاء التقارير، وأتمتة المستندات، وسير عمل معالجة البيانات.

## **API إنشاء جدول بيانات**

### واجهة الويب API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### مُعاملات الطلب

| اسم المُعامل         | النوع   | الموقع   | الوصف                                                                                                                                                |
| ------------------- | ------- | -------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**          | نص (String) | استعلام (Query)    | **إلزامي**. تنسيق الملف للجدول الجديد (مثل: `XLSX`، `XLS`، `ODS`، `CSV`).                                                                            |
| **template**        | نص (String) | استعلام (Query)    | **اختياري**. اسم ملف قالب مخزن في مساحة التخزين السحابية الخاصة بك (مثل: `invoice_template.xlsx`). إذا تُرك فارغًا، فسيتم إنشاء كتاب عمل فارغ.              |
| **outPath**         | نص (String) | استعلام (Query)    | **اختياري**. مسار المجلد المستهدف في مساحة التخزين السحابية لحفظ الملف المُولّد. إذا كان `null` أو مُهمَلًا، فسيُحفظ الجدول في الموقع الافتراضي.            |
| **outStorageName**  | نص (String) | استعلام (Query)    | **إلزامي**. مُعرّف مساحة التخزين السحابية المُعدّة مسبقًا (مثل: `MyDrive`).                                                                           |
| **region**          | نص (String) | استعلام (Query)    | **اختياري**. إعداد الإقليم (مثل: `fr-FR`) الذي يُحدّد تنسيقات التواريخ والأرقام والعملات الافتراضية.                                                  |
| **password**        | نص (String) | استعلام (Query)    | **اختياري**. كلمة المرور لملف القالب المشفر. اتركه فارغًا إذا لم يكن القالب محميًا.                                                                    |

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

| الرمز | المعنى                | الوصف                                                             |
| ----- | --------------------- | ----------------------------------------------------------------- |
| 200   | ناجح (OK)             | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.       |
| 400   | طلب غير صالح (Bad Request) | مُعطَلات ناقصة أو غير صالحة (مثل: نوع ملف غير مدعوم).             |
| 401   | غير مصادَق (Unauthorized)   | رمز JWT غير صالح أو مفقود.                                        |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح.                              |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                          |

## أين يجب استخدام API إنشاء جدول البيانات؟

- **تهيئة نظام إنشاء التقارير الآلي** – قم بإنشاء كتاب عمل فارغ جديد أو أنشئ ملف تقرير من قالب قياسي عند بداية كل دورة أتمتة يومية/أسبوعية.
- **بوابة الخدمة الذاتية للمستخدمين** – اسمح للعملاء باختيار قالب (عرض أسعار، جدول زمني للمشروع، إلخ) وتنزيل ملف Excel مُخصّص فورًا.
- **تصدير وتوزيع البيانات دفعة واحدة** – أنشئ كتب عمل منفصلة بتنسيق موحّد لكل مجموعة بيانات مُصدَّرة، مما يبسّط التوزيع والمعالجة اللاحقة.

لعمليات لاحقة مثل إضافة أوراق عمل أو ملء الخلايا، راجع **API إضافة ورقة عمل**، **API تحديث الخلية**، و**API تصدير كتاب العمل**.

## لماذا يجب استخدام API إنشاء جدول البيانات؟

- **سهل الاستخدام للمطورين** – يوفّر مكتبات SDK لعدة لغات ووثائق موسّعة، مما يبسّط التكامل مقارنةً ببناء حلول مخصصة.
- **كفاءة العمالة** – يتيح أتمتة دمج المستندات، مما يقلل الجهد اليدوي.
- **نظام الدفع حسب الاستخدام** – تستند الرسوم إلى استخدام API دون رسوم ترخيص مقدمة.
- **خدمة مُدارة** – يتم استضافة API بالكامل، ما يلغي الحاجة لصيانة الخوادم المحلية أو تحديثات البرامج.

## كيفية استخدام API إنشاء جدول البيانات باستخدام SDKs

### مواصفات API إنشاء جدول البيانات

تُعرّف [مواصفات API إنشاء جدول البيانات](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) واجهة برمجة تطبيقات قابلة للوصول العام، وتتيح التفاعل عبر REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات ويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (مشفر بـ Base64)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKs لـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، حيث يُجرّد التفاصيل من المستوى المنخفض ويسمح لك بإنشاء جدول البيانات باستخدام كود مختصر. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}