---
title: "Aspose.Cells Cloud – تحويل ملف Excel إلى PDF وCSV وHTML وما ب ذلك (GET /cells/{name})"
second_title: "وثيقة"
linktitle: "تحويل ملف Excel"
type: docs
url: /get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, تحويل Excel, تحويل ملف Excel, PDF, CSV, HTML, ODS, JSON, تنسيقات الصور, تصدير جدول البيانات, API, REST"
description: "تعلم كيفية استرجاع ملف Excel بتنسيق مختلف (PDF وCSV وHTML وPNG وما إلى ذلك) باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن أمثلة لـ cURL وSDKات، ومصادقة، وتفاصيل الاستجابة."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – تحويل ملف Excel إلى PDF وCSV وHTML وما ب ذلك (GET /cells/{name})"
---

تقوم هذه الـ API باسترجاع ملف Excel بتنسيق مختلف.

## API GetWorkBook

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **مُعَيَّنات الاستعلام (Query Parameters)**

| اسم المُعَيَّن           | النوع   | الوصف                                                                                                                                                                      | القيمة الافتراضية |
| --------------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- |
| format                | string | تنسيق الملف الهدف (مثل: CSV وXLS وHTML وMHTML وODS وPDF وXML وTXT وTIFF وXLSB وXLSM وXLSX وXLTM وXLTX وXPS وPNG وJPG وGIF وEMF وBMP وMD وNumbers وWMF وSVG وما إلى ذلك).       | –                 |
| password              | string | كلمة المرور المطلوبة لفتح ملف Excel.                                                                                                                                       | –                 |
| isAutoFit             | bool   | ضبط عرض الصفوف والأعمدة تلقائيًا.                                                                                                                                           | false             |
| onlySaveTable         | bool   | عند تعيينها على **true**، يتم حفظ بيانات الجدول فقط. تقبل القيمتين `true` أو `false`.                                                                                         | false             |
| outPath               | string | المسار الذي سيتم حفظ النتيجة فيه. بالنسبة لملف واحد، تضمين اسم الملف وامتداده؛ بالنسبة لملفات متعددة، تحديد المجلد فقط.                                                      | –                 |
| outStorageName        | string | اسم مخزن الملفات الذي سيتم حفظ ملف الإخراج فيه.                                                                                                                            | –                 |
| checkExcelRestriction | bool   | التحقق من قيود Excel عند تعديل الخلايا أو الكائنات المرتبطة بها.                                                                                                             | false             |
| region                | string | إعدادات المنطقة المطبّقة على ملف Excel.                                                                                                                                     | –                 |
| pageWideFitOnPerSheet | bool   | ضبط عرض الصفحة ليناسب كل ورقة عمل عند التحويل إلى PDF.                                                                                                                       | false             |
| pageTallFitOnPerSheet | bool   | ضبط ارتفاع الصفحة ليناسب كل ورقة عمل عند التحويل إلى PDF.                                                                                                                     | false             |
| onePagePerSheet       | bool   | إنشاء صفحة PDF واحدة لكل ورقة عمل.                                                                                                                                           | false             |
| folder                | string | مسار المجلد الذي يحتوي على ملف Excel الأصلي.                                                                                                                                | –                 |
| storageName           | string | اسم مخزن الملفات الذي يوجد فيه الملف المصدر.                                                                                                                               | –                 |

### الاستجابة

**ناجح (200)**

- تُعيد الـ API كائن **[Workbook](/cells/workbook/)** يحتوي على معلومات هيكل ملف Excel عند تجاهل مُعَيَّن الاستعلام `format`.

- تُعيد الـ API الملف المحول بالتنسيق المطلوب عند تحديد نوع ملف في مُعَيَّن الاستعلام `format`.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(بيانات PDF ثنائية)
```

**رموز حالة HTTP**

| الرمز | المعنى                        | الوصف                                                         |
|------|-------------------------------|---------------------------------------------------------------|
| 200  | ناجح (OK)                     | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | طلب غير صالح (Bad Request)    | مُعَيَّنات مفقودة أو غير صالحة (مثل: تنسيق ملف غير مدعوم).   |
| 401  | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود.                                   |
| 413  | حمل البيانات كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح به.                  |
| 500  | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                   |

> **ملاحظات:**  
> - قد يستغرق تحويل ملفات Excel الكبيرة وقتًا أطول؛ يُوصى بزيادة مهلة الطلب.  
> - بعض التنسيقات (مثل `ODS`) غير مدعومة لبعض ميزات Excel مثل الماكرو.

## كيفية استخدام API GetWorkBook باستخدام SDKات

> **متطلبات مسبقة:**  
> - رمز وصول **JWT** صالح تم الحصول عليه عبر عملية مصادقة Aspose.Cells Cloud.  
> - يجب تخزين ملف Excel المصدر في مخزن Aspose المدعوم أو تقديمه مباشرةً في الطلب.  
> - تأكد من أن إصدار الـ API (`v3.0`) يطابق آخر إصدار صادر.

### مواصفات API GetWorkBook

تُعرّف <a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">مواصفة OpenAPI</a> واجهة برمجة تطبيقات عامة قابلة للاستخدام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

### مثال على الطلب

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي طلب GET صحيح مع رأس المصادقة المطلوب.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### استخدام SDKات Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة لتطوير البرمجيات. تُجرّدك SDKات من التفاصيل منخفضة المستوى لتركّز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطّلاع على قائمة كاملة بـ SDKات Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKات مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**انظر أيضًا**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">تحويل ملف Excel (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">حفظ باسم (GET)</a>

---

_آخر تحديث: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – تحويل ملف Excel إلى PDF وCSV وHTML وما ب ذلك (GET /cells/{name})",
  "description": "توثيق نقطة النهاية GET /cells/{name} في Aspose.Cells Cloud التي تحول ملفات Excel إلى تنسيقات مختلفة مثل PDF وCSV وHTML وما ب ذلك.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, تحويل Excel, PDF, CSV, HTML, API, REST, سحابة",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---