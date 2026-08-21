---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud الويبية - تصدير ورقة عمل إكسل عن بُعد إلى تنسيقات أخرى - أداة مجانية عبر الإنترنت"
second_title: "الوثيقة"
ArticleTitle: "كيف تُصَدِّر ورقة عمل جدول بيانات عن بُعد إلى تنسيقات أخرى: دليل خطوة بخطوة"
linktype: "تصدير جدول البيانات كتنسيق"
type: docs
url: /export-spreadsheet-as-format/
keywords: "Aspose.Cells، تحويل جداول البيانات، واجهة برمجة التطبيقات، تصدير، PDF، CSV، JSON، XLSX"
description: "حوّل كتب عمل إكسل المخزَّنة في خدمة Aspose Cloud إلى تنسيقات PDF أو XLSX أو CSV أو JSON أو HTML عبر نقطة نهاية REST واحدة. تعلّم بنية الطلب، المعاملات، وراجع أمثلة SDK بلغات C# وJava وPython وما إلى ذلك."
weight: 100
---

تصدير جدول بيانات سحابي (إكسل) إلى تنسيق ملف آخر.

## **واجهة برمجة تطبيقات تصدير جدول البيانات كتنسيق**

### واجهة برمجة التطبيقات الويبية

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معاملات الطلب:**

| اسم المعامل | النوع | المسار/سلسلة الاستعلام/جسم HTTP | الوصف |
| :---------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name | String | المسار | (إلزامي) اسم ملف كتاب العمل الذي سيتم استرجاعه. |
| format | String | استعلام | (إلزامي) التنسيق المطلوب للملف الناتج (مثل: "Xlsx"، "PDF"، "CSV"). |
| folder | String | استعلام | (اختياري) مسار المجلد الذي يُخزَّن فيه كتاب العمل. القيمة الافتراضية هي null. |
| storageName | String | استعلام | (اختياري) اسم التخزين عند استخدام تخزين سحابي مخصّص. استخدم التخزين الافتراضي إن حُذف. |
| outPath | String | استعلام | (اختياري) مسار المجلد الذي سيتم حفظ كتاب العمل فيه. القيمة الافتراضية هي null. |
| outStorageName | String | استعلام | (اختياري) اسم تخزين الملف الناتج. |
| fontsLocation | String | استعلام | (اختياري) موقع الخطوط المخصّصة. |
| region | String | استعلام | (اختياري) إعدادات إقليم/لغة جدول البيانات (مثل: `en-US`، `fr-FR`). يؤثر على تنسيق الأرقام، وتحليل التواريخ، والسلوك الخاص باللغة المحلية. |
| password | String | استعلام | (اختياري) كلمة المرور لفتح ملف جدول البيانات. |

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

تحتوي الاستجابة على كائن واحد يمثّل تيار الملف المحول.

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200 | ناجح (OK) | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401 | غير مُصادَق (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم. |

## أين يجب استخدام واجهة برمجة تطبيقات تصدير جدول البيانات كتنسيق آخر؟

- **ترحيل الأنظمة القديمة**: تحويل آلاف ملفات XLS القديمة إلى تنسيق XLSX لتناسب الأنظمة الحديثة.
- **توحيد التنسيقات للأرشفة**: جعل تنسيقات جداول البيانات المتنوعة (XLS، XLSM، ODS، CSV) موحدة إلى تنسيق واحد للأرشفة.
- **التوافق مع حزم المكاتب**: تحويل ملفات إكسل إلى تنسيقات متوافقة مع LibreOffice أو Google Sheets أو Apple Numbers.
- **توحيد مصادر البيانات**: تحويل تنسيقات جداول البيانات المتنوعة إلى CSV أو JSON لاستيعابها في قواعد البيانات.
- **النشر على الويب**: تحويل النماذج المالية إلى تنسيق HTML لعرضها على الويب.

## لماذا يجب استخدام واجهة برمجة تطبيقات تصدير جدول البيانات كتنسيق آخر؟

- **ملائمة للمطورين**: تقدّم Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، ما يُسهّل التطوير بسرعة، ويأتي مع وثائق شاملة. وبالمقارنة مع بناء حلول مخصّصة لعرض الرسوم البيانية، تقلّل هذه الخدمة بشكل كبير من جهد التطوير.
- **خفض تكاليف العمالة**: تقلّل الحاجة إلى تخصيص وظائف لأغراض دمج الوثائق.
- **الدفع حسب الاستخدام**: لا توجد استثمارات مبدئية؛ تدفع مقابل استدعاءات API الفعلية فقط.
- **لا يتطلب صيانة خوادم من جانبك**: لا حاجة لصيانة الخوادم أو تحديث البرامج أو التعامل مع مشاكل التوافق.
- **دعم شامل للتنسيقات**: يدعم التحويل بين أكثر من 20 تنسيق لجداول البيانات.
- **الحفاظ على دقة البيانات والتنسيق الأصلي**: تحفظ التخطيط والمعادلات والأنماط الأصلية أثناء التحويل.

## كيف تستخدم واجهة برمجة تطبيقات تصدير جدول البيانات كتنسيق مع مكتبات SDK؟

### مواصفات واجهة برمجة تطبيقات تصدير جدول البيانات كتنسيق

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات تصدير جدول البيانات كتنسيق</a> توفر واجهة برمجة مفتوحة للوصول واجهات REST بسلاسة.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells الويبية. يوضح المثال التالي كيفية إجراء استدعاءات لواجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
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

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة للتطوير، لأنها تُجرّدك من التفاصيل منخفضة المستوى، ما يسمح لك بتصدير جدول بيانات إلى ملف بصيغة معينة عبر كود موجز.  
قبل إجراء استدعاء لواجهة برمجة التطبيقات، احصل على رمز وصول OAuth 2.0 وأدرجْه في رأس `Authorization: Bearer <token>`.

يرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة لمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية التفاعل مع خدمات الويب الخاصة بـ Aspose.Cells عبر مكتبات SDK مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}