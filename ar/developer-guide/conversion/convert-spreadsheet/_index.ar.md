---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud الويبية - تحويل جدول البيانات إلى تنسيق آخر - أداة مجانية عبر الإنترنت"
second title: "وثيقة"
ArticleTitle: "كيفية تحويل جدول بيانات إلى تنسيق آخر: دليل خطوة بخطوة"
linktype: "تحويل جدول البيانات"
type: docs
url: /convert-spreadsheet/
keywords: "Aspose, Aspose.Cells, تحويل جدول البيانات, Excel إلى PDF, API لملفات Excel, تحويل الملفات عبر السحابة"
description: "قم بتحويل ملف جدول بيانات إلى تنسيق آخر باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud."
weight: 100
---

قم بتحويل ملف جدول بيانات/Excel محلي إلى تنسيق آخر باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud الويبية.

## **واجهة برمجة تطبيقات تحويل جدول البيانات**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الطلب:**

| اسم المعلمة | النوع | المسار/سلسلة الاستعلام/جسم HTTP | الوصف |
| :------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------- |
| Spreadsheet | ملف | FormData | رفع ملف جدول البيانات المراد تحويله. |
| format | نص | استعلام | (إلزامي) التنسيق الناتج المطلوب (مثل: "XLSX"، "PDF"، "CSV"). |
| outPath | نص | استعلام | (اختياري) مسار المجلد الذي سيتم حفظ المصنف المحول فيه. القيمة الافتراضية هي null. |
| outStorageName | نص | استعلام | تحديد اسم تخزين للملف الناتج. |
| fontsLocation | نص | استعلام | استخدام خطوط مخصصة لجدول البيانات. |
| region | نص | استعلام | تحديد إعداد منطقة جدول البيانات. |
| password | نص | استعلام | كلمة المرور لفتح ملف جدول البيانات إذا كان مشفرًا. |

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

**حالة النجاح**

- **200 OK** – تمّ التحويل بنجاح، وتحتوي حِمْل الاستجابة على تيار الملف المحول.
- يُظهر الرأس `Content-Type` نوع MIME لتنسيق الإخراج المطلوب (مثل: `application/pdf` لتنسيق PDF).

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK (تمّ بنجاح) | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request (طلب غير صالح) | معلمات مفقودة أو غير صالحة (مثل: نوع ملف غير مدعوم). |
| 401  | Unauthorized (غير مصرّح) | رمز JWT غير صالح أو مفقود. |
| 413  | Payload Too Large (حمولة كبيرة جدًا) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500  | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

## التنسيقات المدعومة

| **تنسيق الإخراج**                                                                                         | **الوصف**                                                                                                              |
| :----------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| <a href="https://docs.fileformat.com/spreadsheet/xls/" rel="noopener noreferrer">XLS</a>               | مصنف Excel 95/5.0 - 2003.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlsx/" rel="noopener noreferrer">XLSX</a>             | تنسيق ملف Excel SpreadsheetML المفتوح.                                                                               |
| <a href="https://docs.fileformat.com/spreadsheet/xlsb/" rel="noopener noreferrer">XLSB</a>             | مصنف Excel الثنائي.                                                                                                       |
| <a href="https://docs.fileformat.com/spreadsheet/xlsm/" rel="noopener noreferrer">XLSM</a>             | مصنف Excel المُمكّن للماكرو.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlt/" rel="noopener noreferrer">XLT</a>               | قالب Excel من 97 إلى 2003.                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xltx/" rel="noopener noreferrer">XLTX</a>             | قالب Excel.                                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/xltm/" rel="noopener noreferrer">XLTM</a>             | قالب Excel المُمكّن للماكرو.                                                                                                |
| <a href="https://docs.fileformat.com/spreadsheet/xlam/" rel="noopener noreferrer">XLAM</a>             | ملف إضافة Excel المُمكّن للماكرو، ويُستخدم لإضافة وظائف جديدة إلى Excel.                                                |
| <a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>               | ملف CSV (قيم مفصولة بفواصل).                                                                                            |
| <a href="https://docs.fileformat.com/spreadsheet/tsv/" rel="noopener noreferrer">TSV</a>               | ملف TSV (قيم مفصولة بمسافات.tab).                                                                                             |
| <a href="https://docs.fileformat.com/word-processing/txt/" rel="noopener noreferrer">TXT</a>           | ملف نصي عادي مفصول.                                                                                                   |
| <a href="https://docs.fileformat.com/web/html/" rel="noopener noreferrer">HTML</a>                     | تنسيق HTML.                                                                                                                 |
| <a href="https://docs.fileformat.com/web/mhtml/" rel="noopener noreferrer">MHTML</a>                   | ملف MHTML.                                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/ods/" rel="noopener noreferrer">ODS</a>               | ملف جدول بيانات OpenDocument (ODS).                                                                                              |
| SpreadsheetML                                                                                          | ملف Excel 2003 XML.                                                                                                         |
| <a href="https://docs.fileformat.com/spreadsheet/numbers/" rel="noopener noreferrer">Numbers</a>       | الملف تم إنشاؤه باستخدام تطبيق Apple "Numbers"، وهو جزء من حزمة iWork لأنظمة macOS وiOS.                |
| <a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>                     | تدوين كائن جافا سكريبت (JavaScript Object Notation).                                                                                                  |
| <a href="https://docs.fileformat.com/spreadsheet/dif/" rel="noopener noreferrer">DIF</a>               | تنسيق تبادل البيانات (Data Interchange Format).                                                                                                     |
| <a href="https://docs.fileformat.com/database/dbf/" rel="noopener noreferrer">DBF</a>                  | ملف الامتداد .dbf هو ملف قاعدة بيانات يُستخدم من قبل نظام إدارة قواعد بيانات dBASE.                              |
| <a href="https://docs.fileformat.com/pdf/" rel="noopener noreferrer">PDF</a>                           | تنسيق مستند Adobe Portable (Adobe Portable Document Format).                                                                                              |
| <a href="https://docs.fileformat.com/page-description-language/xps/" rel="noopener noreferrer">XPS</a> | تنسيق مواصفات ورقة XML (XML Paper Specification).                                                                                              |
| <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a> | تنسيق الرسومات المتجهة القابلة للتوسع (Scalable Vector Graphics).                                                                                             |
| <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>                   | تنسيق ملف الصور المُوسّم (Tagged Image File Format).                                                                                                    |
| <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>                     | تنسيق الرسومات الشبكية المحمولة (Portable Network Graphics).                                                                                            |
| <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>                     | تنسيق صورة نقطية (Bitmap).                                                                                                         |
| <a href="https://docs.fileformat.com/image/emf/" rel="noopener noreferrer">EMF</a>                     | تنسيق Metafile المُحسّن (Enhanced Metafile).                                                                                                    |
| <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>                   | JPEG هو نوع من صور الملفات المحفوظة باستخدام ضغط فاقد للبيانات.                                                        |
| <a href="https://docs.fileformat.com/image/gif/" rel="noopener noreferrer">GIF</a>                     | تنسيق تبادل الرسومات (Graphics Interchange Format).                                                                                                 |
| <a href="https://docs.fileformat.com/word-processing/md/" rel="noopener noreferrer">MARKDOWN</a>       | يمثل مستند Markdown.                                                                                              |
| <a href="https://docs.fileformat.com/spreadsheet/sxc/" rel="noopener noreferrer">SXC</a>               | تنسيق قائم على XML يُستخدم في OpenOffice وStarOffice.                                                                       |
| <a href="https://docs.fileformat.com/spreadsheet/fods/" rel="noopener noreferrer">FODS</a>             | هذا تنسيق Open Document محفوظ بصيغة XML مسطحة.                                                                          |
| <a href="https://docs.fileformat.com/word-processing/docx/" rel="noopener noreferrer">DOCX</a>         | تنسيق معروف لمستندات Microsoft Word، يجمع بين ملفات XML والثنائية.                                         |
| <a href="https://docs.fileformat.com/presentation/pptx/" rel="noopener noreferrer">PPTX</a>            | يعتمد تنسيق PPTX على تنسيق ملف العرض التقديمي المفتوح لـ PowerPoint من Microsoft.                                      |
| <a href="https://docs.fileformat.com/database/sql/" rel="noopener noreferrer">SqlScript</a>            | لغة الاستعلام المهيكلة (Structured Query Language).                                                                                                   |
| <a href="https://docs.fileformat.com/web/xhtml/" rel="noopener noreferrer">XHtml</a>                   | XHTML هو تنسيق ملف نصي يعتمد على علامات XML، ويستخدم إعادة صياغة لـ HTML 4.0.                                     |
| <a href="https://docs.fileformat.com/ebook/epub/" rel="noopener noreferrer">Epub</a>                   | الملفات ذات الامتداد .epub هي تنسيق للكتب الإلكترونية يوفّر معيارًا للنشر الرقمي للمؤلفين والمستخدمين. |
| <a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">Xml</a>                       | XML تعني لغة الترميز القابلة للتوسع (Extensible Markup Language)، وهي مشابهة لـ HTML لكنها تستخدم العلامات لتعريف الكائنات.                            |
| <a href="https://docs.fileformat.com/spreadsheet/ots/" rel="noopener noreferrer">Ots</a>               | ملف قالب جدول بيانات Open Document (OTS).                                                                                     |
| <a href="https://docs.fileformat.com/ebook/azw3/" rel="noopener noreferrer">AZW3</a>                   | AZW هو تنسيق ملف كتب إلكترونية طوّرته أمازون لأجهزة Kindle. AZW3، ويُعرف أيضًا باسم Kindle Format 8 (KF8).       |

## أين يجب استخدام واجهة برمجة تطبيقات تحويل جدول البيانات؟

- **ترحيل الأنظمة القديمة**: تحويل آلاف ملفات XLS القديمة إلى XLSX للاستخدام في الأنظمة الحديثة.
- **توحيد تنسيقات الأرشفة**: جعل تنسيقات جداول البيانات المختلفة (XLS، XLSM، ODS، CSV) موحّدة في تنسيق واحد للأرشفة.
- **التوافق مع حزم المكاتب**: تحويل ملفات Excel إلى تنسيقات متوافقة مع LibreOffice أو Google Sheets أو Apple Numbers.
- **توحيد مصادر البيانات**: تحويل جداول بيانات متنوعة إلى CSV أو JSON لاستهلاكها في قواعد البيانات.
- **النشر على الويب**: تحويل النماذج المالية إلى HTML لعرضها على الويب.

## لماذا يجب استخدام واجهة برمجة تطبيقات تحويل جدول البيانات؟

- **سهلة للمطورين**: توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، ما يتيح تطويرًا سريعًا، مع وثائق شاملة. مقارنةً بإنشاء حلول مخصصة لعرض الرسوم البيانية، فإنها تقلل بشكل كبير من جهد التطوير.
- **فعالة من حيث التكلفة**: يمكنك تحويل بيانات الجداول دون رفع المصنف مسبقًا، ما يوفر مساحة التخزين ويخفّض التكاليف.
- **دعم شامل للتنسيقات**: تحويل بين أكثر من 20 تنسيقًا لجدول البيانات.
- **الحفاظ على دقة البيانات والتنسيق الأصلي**.

## كيف تستخدم واجهة برمجة تطبيقات تحويل جدول البيانات باستخدام SDKs؟

تُظهر الأمثلة التالية كيفية استخدام واجهة برمجة تطبيقات تحويل جدول البيانات باستخدام مكتبات SDK مختلفة.

### مواصفات واجهة برمجة تطبيقات تحويل جدول البيانات

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheet" rel="noopener noreferrer">مواصفات واجهة برمجة تطبيقات تحويل جدول البيانات</a> تعرّف واجهة برمجة تطبيقات عامة قابلة للوصول، ما يسمح لك بإجراء تفاعلات REST مباشرة من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert?format=pdf \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="file.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات Aspose.Cells Cloud SDK

استخدام SDK هو أسرع طريقة للتطوير، إذ يخفّي التفاصيل من المستوى المنخفض، ويسمح لك بتحويل ملف جدول بيانات إلى تنسيق آخر عبر كود موجز. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorkbook.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorkbook.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorkbook.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorkbook.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorkbook.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorkbook.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorkbook.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorkbook.go" >}}
{{</tab>}}
{{< /tabs >}}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebAPI",
  "name": "Convert Spreadsheet",
  "description": "Convert a spreadsheet file to another format using Aspose.Cells Cloud.",
  "url": "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet",
  "documentation": "https://docs.aspose.cloud/cells/convert-spreadsheet/",
  "targetPlatform": "Web",
  "authenticationType": "OAuth2",
  "operation": [
    {
      "@type": "HttpOperation",
      "httpMethod": "PUT",
      "urlTemplate": "/cells/convert/spreadsheet",
      "description": "Convert a spreadsheet to the specified format."
    }
  ]
}
</script>