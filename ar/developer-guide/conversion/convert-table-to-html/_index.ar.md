---
title: "Aspose.Cells Cloud – تحويل الجدول إلى HTML"
description: "حوّل جداول Excel إلى HTML بسرعة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud – آمنة، تحافظ على التنسيق، وسهلة التكامل."
keywords: "Aspose.Cells، تحويل Excel إلى HTML، تحويل الجدول إلى HTML، واجهة برمجة تطبيقات سحابية، تحويل جداول بيانات"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /ar/convert-table-to-html/
type: docs
---

**ملخص سريع** – تقرأ هذه النقطة الطرفية ملف Excel محليًا، وتستخرج **الجدول** المحدّد، وتحوّله إلى ملف **HTML**، ثم تعيد النتيجة كدفق قابل للتنزيل. ولا يُطلب رفع الملف مبدئيًا إلى مساحة التخزين السحابية لـ Aspose Cloud.

## واجهة برمجة تطبيقات ConvertTableToHTML

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### معاملات الطلب

| الاسم                 | الموقع      | النوع      | مطلوب   | الوصف                                                                              |
| --------------------- | ----------- | ---------- | ------- | ---------------------------------------------------------------------------------- |
| **Spreadsheet**       | Form‑Data   | `File`     | **نعم** | ملف Excel الذي يحتوي على الجدول المراد تحويله.                                      |
| **worksheet**         | Query       | `String`   | **نعم** | اسم ورقة العمل التي يحتوي عليها الجدول.                                            |
| **tableName**         | Query       | `String`   | **نعم** | الاسم الدقيق للجدول المراد تحويله.                                                 |
| **outPath**           | Query       | `String`   | لا       | مسار المجلد في مساحة تخزين Aspose Cloud التي سيتم حفظ ملف HTML فيها (اختياري).     |
| **outStorageName**    | Query       | `String`   | لا       | اسم مساحة التخزين الخاصة بالملف الناتج (اختياري).                                 |
| **fontsLocation**     | Query       | `String`   | لا       | مسار مجلد يحتوي على خطوط مخصصة مطلوبة للتحويل.                                    |
| **region**            | Query       | `String`   | لا       | معرّف المنطقة (مثل `en-US`، `fr-FR`). يؤثّر على تنسيق الأرقام/التاريخ.             |
| **password**          | Query       | `String`   | لا       | كلمة المرور لفتح ملف Excel المحمي.                                                 |
| **AutoRowsFit**       | Query       | `Boolean`  | لا       | ضبط ارتفاع جميع الصفوف تلقائيًا في ورقة العمل (`true`/`false`).                    |
| **AutoColumnsFit**    | Query       | `Boolean`  | لا       | ضبط عرض جميع الأعمدة تلقائيًا في ورقة العمل (`true`/`false`).                      |

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

| الرمز | المعنى                 | الوصف                                                              |
| ----- | ---------------------- | ------------------------------------------------------------------ |
| 200   | OK (نجاح)             | تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.          |
| 400   | Bad Request (طلب خاطئ) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).             |
| 401   | Unauthorized (غير مصرّح) | رمز JWT غير صالح أو مفقود.                                        |
| 413   | Payload Too Large (حِمْل كبير جدًا) | حجم الملف المرفَع يتجاوز الحد المسموح.                         |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقّع في الخادم.                                   |

## متى تستخدم واجهة برمجة تطبيقات تحويل الجدول إلى HTML؟

- **محتوى ويب ديناميكي** – أدمج جداول الأسعار أو الجداول الزمنية أو قوائم المنتجات مباشرةً في صفحات الويب أو أنظمة إدارة المحتوى (CMS).
- **قوالب البريد الإلكتروني** – أنشئ مقاطع HTML لملخّصات الطلبات أو التقارير التي تُعرَض بشكل متسق عبر برامج البريد الإلكتروني المختلفة.
- **لوحات التحكم وأدوات التقارير** – عرض بيانات جداول البيانات الحية دون تحميل ملف Excel بالكامل أو استخدام مكوّنات جداول بيانات ثقيلة.
- **معاينة المستندات** – قدم معاينات سريعة وتحتفظ بالتنسيق لمُقتطفات محددة من جداول البيانات.

## كيف تستخدم واجهة برمجة تطبيقات تحويل الجدول إلى HTML باستخدام مكتبات SDK؟

### مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى HTML

توفر [مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى HTML](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) واجهة برمجة تطبيقات برمجية متاحة علنًا، مما يتيح التفاعل مع REST مباشرةً من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
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

### استخدام مكتبات Aspose.Cells Cloud SDK

يُعد استخدام مكتبة SDK أسرع طريقة للتطوير، حيث تُجرّدك من تفاصيل المستوى المنخفض، مما يتيح لك تحويل بيانات جدول جدول البيانات إلى ملف CSV باستخدام كود محدود. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات Aspose.Cells Cloud SDK.

توضّح أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

---