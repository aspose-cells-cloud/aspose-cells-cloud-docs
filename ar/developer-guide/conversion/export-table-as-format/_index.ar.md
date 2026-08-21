---
title: "تصدير الجدول – واجهة برمجة تطبيقات Aspose.Cells Cloud | تحويل Excel إلى PDF و PNG و CSV"
second_title: "مستند"
ArticleTitle: "كيفية تصدير جدول جدول بيانات عن بُعد إلى تنسيق آخر: دليل خطوة بخطوة"
linktype: "تصدير الجدول إلى تنسيق محدد"
type: docs
url: /ar/export-table-as-format/
keywords: "Aspose.Cells, تصدير الجدول, Excel إلى PDF, واجهة برمجة تطبيقات السحابة, REST"
description: "تصدير جدول Excel المخزن عن بُعد إلى تنسيقات PDF و PNG و CSV و JSON أو تنسيقات أخرى باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. نقطة نهاية آمنة باستخدام HTTPS ومصادقة JWT مع أمثلة ل_sdk_."
weight: 100
---

تصدير جدول جدول بيانات (Excel) المخزن في السحابة إلى ملف بتنسيق آخر.

## **واجهة برمجة تطبيقات تصدير الجدول إلى تنسيق**

### **واجهة برمجة التطبيقات عبر الويب**

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **معلمات الطلب:**

| اسم المعلمة | النوع | المسار / سلسلة الاستعلام / جسم الطلب | الوصف |
| :----------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| name | String | Path | **مطلوبة.** اسم ملف المصنف المراد استرجاعه. |
| worksheet | String | Path | اسم ورقة العمل. |
| tableName | String | Path | اسم الجدول. |
| format | String | Query | **مطلوبة.** التنسيق المطلوب للإخراج (مثل "png"، "pdf"، "svg"). |
| folder | String | Query | اختياري. مسار المجلد الذي يُخزَّن فيه المصنف. القيمة الافتراضية هي `null`. |
| storageName | String | Query | اختياري. اسم وحدة التخزين عند استخدام خدمة تخزين سحابية مخصصة. يُستخدم التخزين الافتراضي في حال حذفها. |
| outPath | String | Query | اختياري. مسار المجلد لتخزين الملفات الخارجة. القيمة الافتراضية هي `null`. |
| outStorageName | String | Query | اختياري. اسم وحدة تخزين الملف الخارجي. |
| fontsLocation | String | Query | اختياري. موقع الخطوط المخصصة. |
| region | String | Query | اختياري. إعداد منطقة/لغة جدول البيانات (مثل `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام وتحليل التواريخ والسلوك الخاص باللغة والموقع. |
| password | String | Query | اختياري. كلمة المرور لفتح ملف جدول البيانات. |

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

**كُودات حالة HTTP**

| الكود | المعنى | الوصف |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200 | ناجح (OK) | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معلمات ناقصة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرح (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حجم حمل الطلب كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## **متى يجب استخدام واجهة برمجة تطبيقات تصدير الجدول إلى تنسيق آخر؟**

- **ترحيل الأنظمة القديمة**: تحويل آلاف ملفات XLS القديمة إلى تنسيق XLSX لدعم الأنظمة الحديثة.
- **توحيد تنسيقات الأرشفة**: جعل تنسيقات جداول البيانات المتنوعة (XLS و XLSM و ODS و CSV) متجانسة إلى تنسيق واحد للأرشفة.
- **التوافق مع حزم المكتب**: تحويل ملفات Excel إلى تنسيقات متوافقة مع LibreOffice و Google Sheets أو Apple Numbers.
- **توحيد مصادر البيانات**: تحويل تنسيقات جداول البيانات المختلفة إلى CSV أو JSON لاستيرادها إلى قواعد البيانات.
- **النشر على الويب**: تحويل نماذج البيانات المالية إلى HTML لعرضها على الويب.

## **لماذا يجب استخدام واجهة برمجة تطبيقات تصدير الجدول إلى تنسيق آخر؟**

- **سهلة للمطورين**: تُقدِّم Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، مما يُسهّل التطوير السريع ويوفر وثائق شاملة. ومقارنةً ببناء حلول مخصصة لعرض الرسوم البيانية، تقلل هذه الطريقة بشكل كبير من جهد التطوير.
- **تقليل تكاليف العمالة**: تُقلل الحاجة إلى تخصيص وظائف لدمج المستندات.
- **الدفع حسب الاستخدام**: لا توجد استثمارات مبدئية؛ تدفع فقط مقابل_calls_ التي تُستخدم فعليًا.
- **لا توجد تكاليف صيانة**: لا حاجة لصيانة الخوادم أو تحديث البرمجيات أو التعامل مع مشكلات التوافق.
- **تُعيد الواجهة بيانات الجدول الخام فقط دون أي تنسيق للمصنف الأصلي.**

## **كيفية استخدام واجهة برمجة تطبيقات تصدير جدول جدول البيانات إلى تنسيق باستخدام SDK؟**

### **مواصفات واجهة برمجة تطبيقات تصدير الجدول إلى تنسيق**

تُعرِّف <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات تصدير الجدول إلى تنسيق</a> واجهة برمجة متاحة عمومًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء مكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

### **استخدام SDKs لـ Aspose.Cells Cloud**

استخدام SDK هو أسرع طريقة للتطوير، حيث تُجرّدك من التفاصيل التقنية منخفضة المستوى، مما يسمح لك بتصدير جدول جدول بيانات إلى ملف بتنسيق مُحدّد باستخدام كود موجز. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب Aspose.Cells باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}