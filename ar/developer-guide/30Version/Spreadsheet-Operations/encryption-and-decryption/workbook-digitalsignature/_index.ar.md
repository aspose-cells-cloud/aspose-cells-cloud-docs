---
title: "إضافة توقيع رقمي إلى كتاب عمل Excel"
ArticleTitle: "إضافة توقيع رقمي إلى كتاب عمل Excel – واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktype: "توقيع رقمي"
type: docs
url: /ar/excel-digital-signature/
aliases:
  - /protect/digital-signature/
  - /workbook/digital-signature/
keywords: "Aspose.Cells Cloud، توقيع رقمي، كتاب عمل Excel، واجهة REST API، .pfx، JWT، API للتوقيع"
description: "تعرّف على كيفية إضافة توقيع رقمي إلى كتاب عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 4.0). يتضمن الرابط_endpoint_، المَعلمات، المصادقة، مخطط الاستجابة، معالجة الأخطاء، وأمثلة لواجهات برمجة التطبيقات (SDKs) بعدة لغات."
weight: 35
---

**المتطلبات المسبقة:**  
قبل استدعاء هذه النقطة النهائية (endpoint)، تأكّد من توفر ما يلي:

- رمز وصول JWT صالح تم الحصول عليه عبر مصادقة Aspose Cloud.  
- رفع كتاب العمل المستهدف إلى مساحة التخزين الخاصة بك على Aspose Cloud.  
- وجود ملف التوقيع الرقمي بصيغة `.pfx` أو `.p12` مع كلمة مرور هذا الملف.

تقوم هذه الواجهة البرمجية عبر REST بإضافة **توقيع رقمي** إلى كتاب عمل Excel.

## PostDigitalSignature API

```http
POST https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature
```

### **الأمان والمصادقة**

تُستخدم واجهات Aspose.Cells Cloud APIs أمانًا وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة قائمة على رمز JWT</a>.

### مَعلمات الطلب

| اسم المَعلمة            | النوع   | الموقع               | الوصف                                                  |
| ------------------------ | ------ | -------------------- | ------------------------------------------------------ |
| **name**                 | string | `<code>path</code>`  | اسم كتاب العمل.                                        |
| **digitalsignaturefile** | string | `<code>query</code>` | المسار إلى ملف التوقيع الرقمي (`.pfx` أو `.p12`).      |
| **password**             | string | `<code>query</code>` | كلمة المرور الخاصة بكتاب العمل، إن وُجدت.             |
| **folder**               | string | `<code>query</code>` | المجلد الذي يُخزّن فيه كتاب العمل.                    |
| **storageName**          | string | `<code>query</code>` | اسم خدمة التخزين المراد استخدامها.                    |

*ملاحظة: إذا احتوى اسم الملف على أحرف خاصة، فقم بترميزه باستخدام URL قبل إدراجه في سلسلة الاستعلام (query string).*

### معالجة الأخطاء

| حالة HTTP | المعنى                                                  |
| --------- | ------------------------------------------------------- |
| 200       | تم تطبيق التوقيع بنجاح.                                |
| 400       | طلب غير صالح – مَعلمات مفقودة أو غير صالحة.           |
| 401       | غير مُصرّح – رمز OAuth غير صالح أو منتهي الصلاحية.     |
| 403       | ممنوع – صلاحيات غير كافية أو تم رفض الوصول.            |
| 500       | خطأ داخلي في الخادم – فشل غير متوقع.                   |

### استجابات الأخطاء حسب حالة HTTPS

| حالة HTTP | الرمز               | الوصف                                                   |
| --------- | ------------------- | -------------------------------------------------------- |
| 400       | BadRequest          | مَعلمات مفقودة أو غير صالحة.                            |
| 401       | Unauthorized        | رمز وصول غير صالح أو مفقود.                             |
| 404       | NotFound            | كتاب العمل المحدد غير موجود في المجلد/مساحة التخزين المعطاة. |
| 500       | InternalServerError | خطأ غير متوقع في الخادم.                                |

## كيفية استخدام واجهة PostDigitalSignature مع واجهات برمجة التطبيقات (SDKs)

### مواصفات واجهة PostDigitalSignature API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Protection/PostDigitalSignature) واجهة برمجة تطبيقات قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL لاستدعاء خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي طلبًا موجّهًا إلى الواجهة:

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/digitalsignature?digitalsignaturefile=signature.pfx&password=YourPassword" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**مخطط الاستجابة**  
تعيد الواجهة كائن JSON يحتوي على الحقول التالية:

| الحقل         | النوع   | الوصف                                               |
| ------------- | ------- | ---------------------------------------------------- |
| `Code`        | int     | رمز حالة مشابه لحالة HTTP يُشير إلى النتيجة.         |
| `Status`      | string  | نص قصير يصف النتيجة (مثل `OK`).                    |
| `SignatureId` | string  | مُعرّف التوقيع الرقمي المُطبّق (اختياري).            |
| `Message`     | string  | معلومات إضافية أو تفاصيل الخطأ (اختياري).            |

### استخدام واجهات Aspose.Cells Cloud SDKs

استخدام واجهات برمجة التطبيقات (SDKs) يبسّط التكامل ويقلّل من الحاجة إلى كتابة كود متكرر. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطّلاع على القائمة الكاملة لواجهات برمجة التطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells باستخدام واجهات برمجة التطبيقات المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostDigitalSignature.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostDigitalSignature.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostDigitalSignature.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostDigitalSignature.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82a2de2e4189bc27ae92abf73c36b4df0" "Example_PostDigitalSignature.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostDigitalSignature.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostDigitalSignature.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostDigitalSignature.go" >}}

{{< /tab >}}

{{< /tabs >}}