---
title: "تحويل ملف إكسل متقدم"
second_title: "مستند"
linktype: "تحويل متقدم"
type: docs
url: /advanced-convert-excel/
keywords: "Aspose.Cells, تحويل إكسل, واجهة برمجة تطبيقات السحابة, حزمة تطوير البرمجيات"
description: "تقدم واجهة Aspose.Cells Cloud REST API ميزات قوية لتحويل كتب عمل إكسل إلى مجموعة واسعة من التنسيقات، مع إمكانية ضبط إعدادات الصفحة، خيارات الحفظ، وإعدادات الطباعة. تتوفر حزم تطوير البرمجيات (SDKs) لأنظمة Android وC# وGo وJava وNode.js وPerl وPHP وPython وRuby وSwift، مما يمكّن من التكامل السلس عبر منصات متعددة."
weight: 50
ArticleTitle: "تحويل ملف إكسل متقدم – دليل واجهة Aspose.Cells Cloud API"
---

## واجهة برمجة تطبيقات سحابية متقدمة لتحويل إكسل

تتيح عملية التحويل المتقدمة (Advanced Convert) لك تحويل كتاب عمل إكسل إلى تنسيقات إخراج متنوعة (مثل PDF وHTML وCSV وما إلى ذلك)، مع منحك تحكمًا دقيقًا في إعدادات الصفحة، وخيارات الحفظ، وإعدادات الطباعة.

**المتطلبات الأساسية / المصادقة**  
لاستخدام هذه النقطة النهائية (Endpoint)، يجب عليك الحصول على رمز وصول (access token) من Aspose.Cells Cloud وإدراجه في رأس الطلب `Authorization` كرمز نوع Bearer.

**مرجع واجهة برمجة التطبيقات**  
- **الطريقة:** `PUT`  
- **النقطة النهائية (Endpoint):** `/cells/convert`  
- **المعاملات:**  
  - `format` (سلسلة نصية، مطلوبة) – تنسيق الإخراج المطلوب (مثل `pdf` أو `html`).  
  - `outPath` (سلسلة نصية، اختيارية) – المسار في التخزين السحابي الذي سيتم حفظ الملف المحول فيه.  
  - `options` (كائن، اختياري) – كائن JSON يحتوي على خيارات تحويل متقدمة مثل `pageSetup` و`saveOptions` و`printSettings`.  
- **مثال على جسم الطلب:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **الاستجابة:**  
  - `200 OK` – تم التحويل بنجاح؛ تحتوي الاستجابة على تدفق الملف المحول أو مرجع للملف المحفوظ.  
  - `400 Bad Request` – معاملات غير صالحة أو جسم طلب معطّل.  
  - `401 Unauthorized` – فشلت المصادقة أو نقص رمز الوصول.  
  - `500 Internal Server Error` – خطأ في الخادم أثناء عملية التحويل.  

**رموز حالة HTTP**

| الرمز | المعنى                      | الوصف                                               |
|------|-----------------------------|-----------------------------------------------------|
| 200  | OK                          | تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400  | Bad Request                 | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401  | Unauthorized                | رمز JWT غير صالح أو مفقود. |
| 413  | Payload Too Large           | حجم الملف المرفّق يتجاوز الحد المسموح. |
| 500  | Internal Server Error       | خطأ غير متوقع في الخادم. |

**ملاحظات**  
* بعض تنسيقات الإخراج لها قيود محددة (مثل أن تحويل HTML لا يحتفظ بالماكروز). راجع الوثائق الخاصة بكل تنسيق للحصول على التفاصيل.

### إمكانية تحميل ملفات جداول البيانات من مصادر بيانات متعددة

### ضبط إعدادات الصفحة وخيارات الحفظ

## عائلة حزم تطوير البرمجيات السحابية

يساعد استخدام حزمة تطوير البرمجيات (SDK) في تسريع عملية التطوير من خلال التعامل مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بحزم تطوير البرمجيات الخاصة بـ Aspose.Cells Cloud.

توضح الأمثلة التالية كيفية إجراء مكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام حزم تطوير البرمجيات المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud Advanced Convert",
  "description":"تحويل كتاب عمل إكسل إلى PDF/HTML/CSV مع خيارات متقدمة.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"تنسيق الإخراج المطلوب (pdf أو html أو csv أو إلخ)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>
---