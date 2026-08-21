---
title: "تصدير ورقة عمل – واجهة Aspose.Cells Cloud API الإصدار 4 (PDF وPNG وSVG وCSV)"
second_title: "مستند"
ArticleTitle: "كيفية تصدير ورقة عمل جدول بيانات عن بُعد إلى تنسيق آخر: دليل خطوة بخطوة"
linktype: "تصدير ورقة عمل"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, تصدير ورقة عمل, واجهة برمجة التطبيقات السحابية, PDF, PNG, CSV, تحويل Excel"
description: "قم بتحويل ورقة عمل مخزّنة في Aspose.Cells Cloud إلى تنسيق PDF أو PNG أو SVG أو CSV أو تنسيقات أخرى عبر طلب GET واحد. يشمل أمثلة كود بلغات C# وJava وPython وغيرها."
weight: 100
---

تصدير ورقة عمل من جدول بيانات/Excel مخزّن في السحابة إلى ملف بتنسيق آخر باستخدام واجهة Aspose.Cells Cloud Web API.

## **واجهة تصدير ورقة العمل كتنسيق**

### واجهة برمجة التطبيقات عبر الويب

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **معلمات الطلب**

| اسم المعلمة         | النوع   | المسار / سلسلة الاستعلام / جسم الطلب HTTP | الوصف                                                                                                                                               |
| :----------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path                       | (مطلوبة) اسم ملف المصنف المراد استرجاعه.                                                                                                           |
| **worksheet**      | String | Path                       | (مطلوبة) ورقة العمل المحددة المراد تحويلها.                                                                                                        |
| **format**         | String | Query                      | (مطلوبة) التنسيق المطلوب للملف الناتج (مثل `png` أو `pdf` أو `svg`).                                                                              |
| **folder**         | String | Query                      | (اختياري) مسار المجلد الذي يخزّن فيه المصنف. القيمة الافتراضية هي `null`.                                                                           |
| **storageName**    | String | Query                      | (اختياري) اسم مساحة التخزين السحابية المخصصة. استخدام مساحة التخزين الافتراضية عند حذفها.                                                          |
| **outPath**        | String | Query                      | (اختياري) مسار مجلد الإخراج. القيمة الافتراضية هي `null`.                                                                                          |
| **outStorageName** | String | Query                      | (اختياري) اسم مساحة تخزين الملف الناتج.                                                                                                            |
| **fontsLocation**  | String | Query                      | (اختياري) تحديد الخطوط المخصصة عند الحاجة.                                                                                                         |
| **region**         | String | Query                      | (اختياري) إعداد منطقة/لغة جدول البيانات (مثل `en-US` أو `fr-FR`). يؤثر على تنسيق الأرقام وتحليل التواريخ والسلوك المتعلق باللغة المحلية.            |
| **password**       | String | Query                      | (اختياري) كلمة المرور للوصول إلى ملف جدول البيانات.                                                                                                |

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

**كودات حالة HTTP**

| الكود | المعنى                    | الوصف                                                                |
| ---- | ------------------------- | --------------------------------------------------------------------- |
| 200  | ناجح                      | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.         |
| 400  | طلب غير صالح              | معلمات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم).                |
| 401  | غير مصدق                 | رمز JWT غير صحيح أو مفقود.                                           |
| 413  | حجم الحمولة كبير جدًا      | تجاوز حجم الملف المرفوع الحد المسموح به.                             |
| 500  | خطأ داخلي في الخادم        | خطأ غير متوقع في الخادم.                                              |

## **أين يجب استخدام واجهة تصدير ورقة العمل إلى تنسيق آخر؟**

- **ترحيل الأنظمة القديمة** – تحويل آلاف ملفات XLS القديمة إلى تنسيق XLSX لأنظمة حديثة.
- **توحيد التنسيقات للأرشفة** – جعل تنسيقات جداول البيانات المختلفة (XLS وXLSM وODS وCSV) موحدة لغرض الأرشفة.
- **التوافق مع حزم المكتب** – تحويل ملفات Excel إلى تنسيقات متوافقة مع LibreOffice أو Google Sheets أو Apple Numbers.
- **توحيد مصادر البيانات** – تحويل تنسيقات جداول البيانات المختلفة إلى CSV أو JSON لاستيرادها في قواعد البيانات.
- **النشر على الويب** – تحويل النماذج المالية إلى HTML لعرضها على الويب.

## **لماذا تستخدم واجهة تصدير ورقة العمل إلى تنسيق آخر؟**

- **دعم متعدد اللغات لواجهات برمجة التطبيقات (SDKs)** – توفر مكتبات عميل للغات برمجة متعددة، مما يسمح للمطورين باستدعاء الواجهة مباشرةً من بيئتهم المفضلة.
- **تحويل مباشر دون رفع مبدئي** – تتيح تحويل ورقة عمل مخزّنة في مساحة تخزين سحابية إلى التنسيق المطلوب دون الحاجة لتنزيل الملف وإعادة رفعه.
- **استخراج البيانات فقط** – تُعيد محتوى ورقة العمل بالتنسيق المختار دون الحفاظ على التنسيقات البصرية.

## **كيفية استخدام واجهة تصدير ورقة جدول البيانات كتنسيق باستخدام واجهات برمجة التطبيقات (SDKs)؟**

### مواصفات واجهة تصدير ورقة العمل كتنسيق

توفر [مواصفات واجهة تصدير ورقة العمل كتنسيق](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) واجهة برمجة مفتوحة للوصول إلى التفاعلات REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
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

### استخدام واجهات برمجة تطبيقات Aspose.Cells Cloud (SDKs)

استخدام واجهات برمجة التطبيقات (SDKs) هو أسرع طريقة للتطوير، لأنها تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بتصدير ورقة عمل جدول بيانات إلى ملف بتنسيق مطلوب بكود موجز.  
يرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بواجهات Aspose.Cells Cloud SDK.

توضح أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب Aspose.Cells باستخدام SDKs المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}