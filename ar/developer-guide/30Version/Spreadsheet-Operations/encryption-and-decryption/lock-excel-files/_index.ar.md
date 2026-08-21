---
title: "قفل ملفات Excel"
second_title: "مستند"
linktitle: "قفل ملفات Excel"
type: docs
url: /ar/lock-excel-files/
aliases: [  /ar/lock/without-storage/ , /ar/lock/ , /ar/lock/without-using-storage/ ]
keywords: "قفل, Excel, API, Aspose.Cells, Cloud, REST, Workbook, Spreadsheet, SDK"
description: "تعرّف على كيفية قفل كتب عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يشمل النهاية (Endpoint) عبر HTTPS، المصادقة، طلب cURL، مخطط الاستجابة، وأمثلة لرموز SDK بلغات C#، Java، Python، وغيرهما."
ArticleTitle: "قفل ملفات Excel – مستندات واجهة Aspose.Cells Cloud API"
weight: 70
---

**إصدار API:** v3.0 (الإصدار الحالي)

تقوم هذه **واجهة REST API** بقفل كتب عمل Excel.

## واجهة PostLock API

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**المتطلبات المسبقة** – يجب إرسال الطلب عبر بروتوكول **HTTPS**، ويتضمن رمز مميز (Bearer token) ساري المفعول من نوع OAuth 2.0 في رأس الطلب `Authorization`.

### معاملات الطلب

| اسم المعامل | النوع   | الموقع                   | الوصف                                      |
| ----------- | ------- | ------------------------ | ------------------------------------------ |
| file        | ملف     | بيانات النموذج (multipart body) | كتاب عمل Excel المراد رفعه وقفله.          |
| password    | نص (string) | سلسلة الاستعلام (query string) | كلمة المرور لكتاب العمل (اختيارية).         |

<a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> تعرّف واجهة برمجة تطبيقات متاحة عمومًا، وتتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يوضح المثال التالي كيفية **استدعاء** واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*يمكنك تنزيل كتاب عمل تجريبي — [Sample.xlsx](https://example.com/Sample.xlsx) — لاختبار الطلب.*

**ملاحظة:** تدعم الواجهة ملفات بحجم يصل إلى 100 ميغابايت؛ قد تؤدي الحمول الأكبر إلى استجابة برمز الخطأ 413 (Payload Too Large / حمل البيانات كبير جدًا).

### **تفاصيل الاستجابة**

| الحقل         | النوع            | الوصف                                              |
| ------------- | ---------------- | -------------------------------------------------- |
| Filename      | نص (string)       | اسم كتاب العمل المُقفل الذي تعيده الخدمة.          |
| FileSize      | عدد صحيح (integer) | حجم الملف المقفل بالبايت.                           |
| FileContent   | نص (Base64)      | كتاب العمل المقفل مشفرًا على هيئة سلسلة Base64.     |

للحصول على كتاب العمل المقفل، قم بفك تشفير القيمة `FileContent` من تنسيق Base64 واحفظه باستخدام الاسم المحدد في الحقل `Filename` ضمن الاستجابة.

### **معالجة الأخطاء**

– تُعيد الواجهة رموز حالة HTTP القياسية (مثل `400 Bad Request`، `401 Unauthorized`، `500 Internal Server Error`) مع كائن خطأ بصيغة JSON يحتوي على حقلين: `Code` و `Message`.

## عائلة SDK للحُوسبة السحابية

استخدام SDK يُعدّ أفضل طريقة لتسريع عملية التطوير؛ إذ تُجرّدك SDK من التفاصيل التقنية منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية إجراء استدعاءات لخدمات Aspose.Cells عبر الويب باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}