---
title: "تصدير مخطط Excel – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "مستند"
description: "تحويل مخطط من ملف Excel مخزن في السحابة إلى تنسيق PDF أو PNG أو SVG أو تنسيقات أخرى باستخدام استدعاء REST واحد فقط."
ArticleTitle: "كيفية تحويل ورقة عمل جدول بيانات محلي إلى ملف PDF: دليل خطوة بخطوة"
linktitle: "تحويل ورقة العمل إلى PDF"
type: docs
url: /ar/export-chart-as-format/
keywords: "Aspose.Cells Cloud, تصدير المخطط, واجهة برمجة التطبيقات, PDF, PNG, SVG, Excel, REST, التحويل السحابي"
weight: 100
---

قم بتحويل مخطط موجود في ملف عمل مخزن في مساحة التخزين الخاصة بـ Aspose Cloud إلى تنسيق ملف مختلف (PDF أو PNG أو SVG أو غيرها) دون تنزيل الملف المصدر.

## واجهة برمجة تطبيقات ExportChartAsFormat

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **الأمان والمصادقة**

تُعد واجهات برمجة التطبيقات الخاصة بـ Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### 📦 معاملات الطلب

| الاسم               | النوع    | الموقع | إجباري | الوصف                                                     |
| ------------------ | ------- | ------ | ------ | --------------------------------------------------------- |
| **name**           | نص     | المسار | نعم    | اسم ملف العمل.                                            |
| **worksheet**      | نص     | المسار | نعم    | اسم ورقة العمل التي يحتويها المخطط.                        |
| **chartIndex**     | عدد صحيح | المسار | نعم    | الفهرس بصفر كبداية للمخطط المراد تصديره.                  |
| **format**         | نص     | الاستعلام | نعم    | تنسيق الإخراج المرغوب (مثل: `png`، `pdf`، `svg`).          |
| **folder**         | نص     | الاستعلام | لا      | مسار المجلد الذي يخزن فيه ملف العمل (الافتراضي: الجذر).   |
| **storageName**    | نص     | الاستعلام | لا      | اسم التخزين المخصص؛ تجاهل هذا الخيار لاستخدام التخزين الافتراضي. |
| **outPath**        | نص     | الاستعلام | لا      | مسار المجلد الذي سيتم حفظ الملف المحول فيه.                |
| **outStorageName** | نص     | الاستعلام | لا      | اسم التخزين لملف الإخراج.                                  |
| **fontsLocation**  | نص     | الاستعلام | لا      | مسار مجلد يحتوي على الخطوط المخصصة.                        |
| **region**         | نص     | الاستعلام | لا      | إعدادات الإقليم (مثل: `en-US`، `fr-FR`).                   |
| **password**       | نص     | الاستعلام | لا      | كلمة المرور لفتح ملف عمل محمي.                             |

### **الاستجابة**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**رموز حالة HTTP**

| الرمز | المعنى                   | الوصف                                                        |
| ---- | ------------------------ | ------------------------------------------------------------ |
| 200  | نجاح                     | تمت عملية التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح             | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).        |
| 401  | غير مصادق عليه           | رمز JWT غير صالح أو مفقود.                                   |
| 413  | حجم الحمولة كبير جداً     | حجم الملف المرفوع يتجاوز الحد المسموح به.                    |
| 500  | خطأ داخلي في الخادم       | خطأ غير متوقع في الخادم.                                     |

## كيف تستخدم واجهة برمجة تطبيقات Export Chart as Format باستخدام مكتبات SDK؟

### مواصفات واجهة برمجة تطبيقات Export Chart as Format

توفر <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات Export Chart as Format</a> واجهة برمجة تطبيقات متاحة للعامة وتتيح التفاعل عبر REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
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

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

يعتبر استخدام مكتبة SDK الطريقة الأسرع للتطوير، لأنها تُجريد التفاصيل من المستوى المنخفض، مما يسمح لك بتحويل بيانات جدول البيانات إلى ملف PDF باستخدام كود محدود جداً. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK مختلفة: