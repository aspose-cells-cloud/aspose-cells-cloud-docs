---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud لحماية إلغاء Excel – إزالة كلمات المرور لفتح وتعديل الملفات برمجيًا"
second_title: "وثيقة"
ArticleTitle: "إزالة حماية كلمة المرور من ملفات Excel – فتح كلمات المرور للفتح والتعديل فورًا"
linktitle: "إلغاء حماية جدول البيانات"
type: docs
url: /ar/unprotect-spreadsheet/
keywords: "إلغاء الحماية، جدول البيانات، Aspose.Cells، واجهة برمجة التطبيقات، Excel، إزالة كلمة المرور"
description: "قم بإزالة كلمات المرور للفتح والتعديل من ملفات Excel برمجيًا باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud لإلغاء حماية جداول البيانات. تدعم التنسيقات .xlsx/.xls ومصادقة OAuth2 ومعالجة الدُّفعات."
weight: 100
---

تقوم واجهة برمجة تطبيقات إلغاء حماية جدول البيانات بإزالة حماية كلمات المرور للفتح والتعديل من ملفات Excel في استدعاء واحد فقط. وهي مثالية لسُلُكَات البيانات، وأنظمة إدارة المستندات، وسير عمل النقل.

## **واجهة برمجة تطبيقات إلغاء حماية جدول البيانات**

### **واجهة برمجة التطبيقات على الويب**

```http
PUT https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **معلمات الطلب**

| اسم المعلمة | النوع   | الموقع | الوصف                                                                          |
| ------------ | ------ | -------- | ------------------------------------------------------------------------------------ |
| Spreadsheet | ملف   | FormData | ملف Excel الذي سيتم إلغاء حمايته.                                                    |
| password | نص | استعلام | كلمة المرور التي تحمي الملف ضد الفتح.                                     |
| modifyPassword | نص | استعلام | كلمة المرور المطلوبة لتعديل الملف (اختيارية إذا كانت مُعيّنة كلمة مرور فتح فقط). |
| outPath | نص | استعلام | (اختياري) مسار المجلد الذي سيتم حفظ الملف غير المحمي فيه.                 |
| outStorageName | نص | استعلام | (اختياري) اسم وحدة التخزين التي سيتم كتابة الملف الناتج فيها.                |
| region | نص | استعلام | (اختياري) إعدادات منطقة جدول البيانات.                                              |

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

تُعيد الاستجابة الناجحة ملف غير محمي كتيار بيانات (stream). ويمكن حفظ الملف في الموقع المحدّد بواسطة `outPath` و`outStorageName`، أو استرجاعه مباشرةً من حمولة الاستجابة.

**رموز حالة HTTP**

| الرمز | المعنى               | الوصف                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | نجاح (OK)                    | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)           | معلمات ناقصة أو غير صحيحة (مثل: نوع ملف غير مدعوم).      |
| 401  | غير مُصادَق (Unauthorized)          | رمز JWT غير صالح أو مفقود.                                     |
| 413  | حمولة كبيرة جدًا (Payload Too Large)     | تجاوز حجم الملف المرفوع الحد المسموح.                                 |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                          |

## متى يجب استخدام واجهة برمجة تطبيقات إلغاء حماية جدول البيانات؟

- **استعادة الوصول إلى الملفات المُقفلة** – أزِل كلمات المرور المنسية للفتح أو التعديل بسرعة دون تدخل يدوي.
- **أتمتة فتح الدُّفعات** – عالِج كميات كبيرة من الملفات في مشاريع نقل البيانات أو الأرشفة.
- **التكامل مع سير العمل الحالي** – اجمعها مع واجهات برمجة تطبيقات التخزين أو التحويل لإنشاء سير عمل متكامل (مثل: رفع → إلغاء الحماية → تحويل إلى PDF).
- **الحفاظ على أمن البيانات** – تتم العملية من جانب الخادم، مما يضمن أمان الملفات الأصلية بينما يُخزّن النسخة غير المحمية في مساحة التخزين السحابية الخاصة بك.

## كيفية استخدام واجهة برمجة تطبيقات إلغاء حماية جدول البيانات باستخدام مكتبات SDK

### **مواصفات OpenAPI**

توفّر <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Protection/ProtectSpreadsheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات إلغاء حماية جدول البيانات</a> واجهة برمجة برمجية متاحة عمومًا لتسهيل التفاعل المباشر مع REST من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. ويُظهر المثال التالي كيفية إرسال استدعاءات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet?password=OldPass&modifyPassword=ModPass" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myfile.xlsx"
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

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK يبسّط الاستدعاء من خلال معالجة المصادقة، وبناء الطلب، وتحليل الاستجابة. وتُوفَّر مكتبات SDK لعدة لغات برمجة، وتشمل طُرقًا جاهزة لإلغاء حماية جداول البيانات.

تُظهر الأمثلة التالية كيفية استدعاء واجهة برمجة تطبيقات إلغاء حماية جدول البيانات باستخدام مكتبات SDK مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}