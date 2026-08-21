---
title: "تحويل Excel إلى TIFF"
second_title: "مستند"
linketitle: "تحويل Excel إلى TIFF"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/, /convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud، تحويل Excel إلى TIFF، واجهة برمجة التطبيقات REST، cURL، حزمة تطوير البرمجيات (SDK)، .NET، Java، Python، تصدير الصور"
description: "تعرّف على كيفية تحويل كتب عمل Excel إلى صور TIFF عالية الجودة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. أوامر cURL مفصّلة، أمثلة لحزم تطوير البرمجيات (SDK) (C#، Java، Python، إلخ)، خطوات المصادقة، ومعالجة الأخطاء."
weight: 90
---

تتيح لك نقاط النهاية **Convert** (تحويل)، و **SaveAs** (حفظ باسم)، و **Export** (تصدير) في Aspose.Cells Cloud تحويل كتاب عمل Excel إلى صورة TIFF.  
يمكنك استدعاء هذه نقاط النهاية مباشرة باستخدام **cURL** أو من خلال أحد حزم تطوير البرمجيات (SDKs) المدعومة.

## واجهة برمجة التطبيقات REST

| **واجهة برمجة التطبيقات** | **الطريقة** | **الغرض**                                                                                     | **رابط Swagger**                                                                            |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `/cells/convert`         | PUT        | يحوّل كتاب العمل المُزوَّد في جسم الطلب إلى التنسيق المحدّد (TIFF).                            | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`          | GET        | يصدّر كتاب العمل المسمّى إلى تنسيق آخر (TIFF) ويُعيد النتيجة في الاستجابة.                     | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs`   | POST       | يحفظ كتاب العمل بالتنسيق المختار (TIFF) ويحتفظ بالنتيجة في مساحة التخزين السحابية.            | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

يمكن الوصول إلى نقاط النهاية هذه علنًا واستدعاؤها مباشرة من متصفح ويب أو أي عميل HTTP.

### أمثلة باستخدام cURL

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64‑content>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **ملاحظة:**
>
> - يجب أن يحتوي جسم طلب **Convert** على الملف (أو مرجع إلى ملف مخزّن) وقيمة `SaveFormat` المرغوبة.
> - لا يتطلب طلب **Export** جسم طلب؛ يتم تحديد التنسيق عبر سلسلة الاستعلام (`format=tiff`).

## معالجة الأخطاء

| **رمز الحالة** | **المعنى**           | **السبب الشائع**                           |
| -------------- | -------------------- | ------------------------------------------ |
| 200            | نجاح                 | يتم إعادة صورة TIFF (دفق ثنائي).         |
| 400            | طلب غير صحيح         | معلمات مفقودة أو غير صحيحة صياغتها.       |
| 401            | غير مُصادَق          | رمز JWT غير صالح أو مفقود.                |
| 404            | غير موجود            | كتاب العمل المحدّد غير موجود.              |
| 500            | خطأ داخلي في الخادم  | ظرف غير متوقع من جانب الخادم.              |

عند حدوث خطأ، تُعيد واجهة برمجة التطبيقات حمولة JSON تحتوي على الحقول `Code` (الرمز)، و `Message` (الرسالة)، و`Description` (الوصف) اختياريًا.

## عائلة حزم تطوير البرمجيات (SDKs) السحابية

استخدام حزمة تطوير البرمجيات (SDK) هو أسرع طريقة لتطوير التطبيقات. فحزمة تطوير البرمجيات تُدير التفاصيل منخفضة المستوى، مما يتيح لك التركيز على مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات (SDKs) لـ Aspose.Cells Cloud.

تُظهر الأمثلة التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام حزم تطوير البرمجيات المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}